---
description: Aprenda a generar tokens de Livefyre con el lenguaje'C
seo-description: Aprenda a generar tokens de Livefyre con el lenguaje'C
seo-title: Creando tokens de Livefyre'C
solution: Experience Manager
title: Creando tokens de Livefyre'C
uuid: c 5 e 05625-8550-4 b 51-9211-134600 e 20 ec 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Creación de tokens de Livefyre C\ # {#creating-livefyre-tokens-c}

Descubra cómo generar tokens de Livefyre utilizando el idioma ``C#``.

Puede aprovechar documentación heredada y código de muestra para utilizar `C#.NET` métodos para crear tokens.

Para hacer referencia a las bibliotecas oficiales de Livefyre, utilice la biblioteca [Java](https://github.com/Livefyre/livefyre-java-utils) como punto de partida para `C#` los desarrolladores.

También puede considerar el uso de [la biblioteca Node. js](https://github.com/Livefyre/livefyre-nodejs-utils) desde la línea de comandos para generar tokens de referencia para usted mismo y familiarizarse con la estructura de método.

* [Ir al meta de la colección](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Ir a token de autenticación](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dependencias {#section_c15_fnh_xz}

* Necesitará el paquete [JWT nuget](https://www.nuget.org/packages/JWT) en el proyecto para generar los tokens.
* Los ejemplos de código de esta página utilizan [el paquete JSON](https://www.nuget.org/packages/newtonsoft.json/) de Newtonsoft.

## Collectionmeta Token {#section_dzt_4mh_xz}

Collectionmeta Token se pasa a Livefyre cuando incruste Comentarios en una página y proporciona al sistema los metadatos necesarios para la nueva colección. Además, creará un MD 5 `checksum` de estos datos, que Livefyre comprueba si los metadatos han cambiado. (p. ej., si se editó el título o la dirección URL del artículo).

Este token se firma con su `Site Key`, que su administrador de cuentas técnico le proporcionó en Livefyre.

Consulte también:

* Collectionmeta Token Documentos
* [Gist de ejemplo](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Cree un diccionario que contenga los metadatos de la colección. Solo vamos a agregar algunos de los campos necesarios en este paso, la ecuación queremos crear una suma de comprobación de este objeto ANTES DE agregar el artículo.

   ```
       // Site Key provided by Livefyre 
       string siteSecret = "ABCDE1234"; 
   
       var meta = new Dictionary<string, object>() { 
           {"title", "Kings win the Stanley Cup"}, 
           {"url", "https://www.website.com/kings-win-stanley-cup"}, 
           {"tags", "sports, hockey, stanley_cup"}, 
           {"type", "livecomments"} 
       };
   ```

   * **title** *requerido*: Título de la colección, normalmente el título del artículo. La longitud máxima es de 255 caracteres. No admite entidades HTML. Codifique caracteres especiales con UTF -8.
   * **url** *requerida*: URL canónica del artículo. Esto se utiliza en las funciones de uso compartido de comentarios y sincronización social, y en vínculos a su artículo desde el panel Administración. Si realiza pruebas localmente, tenga en cuenta que Livefyre no aceptará «localhost» como dominio.
   * **etiquetas** *opcionales*: Una lista de etiquetas separadas por coma que desea agregar a la colección en el tablero de Livefyre. Las etiquetas no pueden contener espacios. Utilice guiones bajos si desea que aparezca un espacio en el tablero Administración.
   * **type** *optional*:  A string indicating what type of collection to create. Los valores válidos son:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      Si no se especifica, se crea una colección livecomments de forma predeterminada.


1. JSON codifica este diccionario y genere una suma de comprobación md 5.

   ```
          var metaStr = JsonConvert.SerializeObject(meta); 
       byte[] hash; 
   
       using (var md5 = MD5.Create()) 
       { 
           hash = md5.ComputeHash(Encoding.UTF8.GetBytes(metaStr)); 
       } 
   
       StringBuilder sBuilder = new StringBuilder(); 
   
       // Loop through each byte of the hashed data  
       // and format each one as a hexadecimal string  
       for (int i = 0; i < hash.Length; i++) 
       { 
           sBuilder.Append(hash[i].ToString("x2")); 
       } 
   ```

1. Agregue **el artículo Artículo** al diccionario. La **suma de comprobación** no entra en collectionmeta token, pero debe enviarse como parámetro seaprate en el objeto convconfig js.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **Se** *requiere articleid*: Identificador único de su colección dentro del sitio de Livefyre. Normalmente, el único artículo de artículo utilizado en el CMS. (p. ej., su ID de anuncio de WordPress) Este valor nunca debe cambiar. Livefyre identifica colecciones únicas mediante la combinación de siteid y articleid.

1. Genere un testigo JWT firmado del diccionario, utilizando la clave del sitio proporcionada por Livefyre. Tenga en cuenta que debe especificar el algoritmo de hash correcto, ya que el paquete JWT no utiliza HS 256 de forma predeterminada.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## El testigo de autenticación de usuario {#section_g1d_43h_xz}

El autentificador de usuarios se utiliza para firmar un usuario a Livefyre. Cuando un usuario inicia sesión en el sitio, el sitio genera un testigo de autenticación de usuario que se pasa al widget de Livefyre en la página. (Para obtener más información sobre el proceso de autenticación, consulte Perfiles remotos).

Este token requiere el nombre de red (network. fyre. co) y se firma con la clave de red proporcionada por su administrador técnico de cuenta en Livefyre.

Consulte también:

* Documentos de autentificador de autenticación oficial
* [Gist de ejemplo](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. Cree un diccionario con la información necesaria.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **domain:** Nombre de la red (proporcionado por Livefyre). Por ejemplo mynetwork. fyre. co
   * **user_ id:** ID exclusivo de usuario para el usuario en el sistema de perfiles del sitio. Solo debe ser caracteres alfanuméricos (A-Z, a-z, 0-9). Si los sistemas de ID de usuario contienen caracteres no válidos, considere el envío de Livefyre a md 5 hash del ID de usuario, o bien una versión codificada de base 64. (Permita que el administrador de cuentas sepa si realiza esto).
   * **caduca:** La fecha (en la hora de Epoch) que caduca el token. Debe coincidir con la hora de inicio de sesión de los inicios de sesión en el sitio, de modo que el estado de inicio de sesión de Livefyre esté sincronizado con el estado de inicio de sesión del sitio.
   * **display_ name:** El nombre para mostrar del usuario en el sistema de perfiles, ya que debería mostrarse en el flujo de comentarios.

1. Genere un testigo JWT firmado del diccionario, utilizando la clave de red proporcionada por Livefyre. Tenga en cuenta que debe especificar el algoritmo de hash correcto, ya que el paquete JWT no utiliza HS 256 de forma predeterminada.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
