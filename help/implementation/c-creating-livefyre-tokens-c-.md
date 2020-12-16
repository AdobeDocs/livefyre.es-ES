---
description: Aprenda a generar tokens de Livefyre utilizando el lenguaje "C#".
seo-description: Aprenda a generar tokens de Livefyre utilizando el lenguaje "C#".
seo-title: Creación de tokens de Livefyre "C#"
solution: Experience Manager
title: Creación de tokens de Livefyre "C#"
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 2%

---


# Creación de tokens de Livefyre C\# {#creating-livefyre-tokens-c}

Descubra cómo generar tokens de Livefyre utilizando el idioma ``C#``.

Puede aprovechar la documentación heredada y el código de muestra para utilizar `C#.NET` para escribir métodos para crear tokens.

Para hacer referencia a las bibliotecas oficiales de Livefyre, utilice la [Biblioteca de Java](https://github.com/Livefyre/livefyre-java-utils) como punto de partida para los programadores de `C#`.

También puede considerar la posibilidad de utilizar la [biblioteca Node.js](https://github.com/Livefyre/livefyre-nodejs-utils) desde la línea de comandos para generar tokens de referencia por sí mismo y familiarizarse con la estructura de métodos.

* [Ir a token de metadatos de colección](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Saltar al autentificador](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dependencias {#section_c15_fnh_xz}

* Necesitará el [paquete de nuget JWT](https://www.nuget.org/packages/JWT) en su proyecto para generar los tokens.
* Los ejemplos de código de esta página utilizan el paquete [JSON](https://www.nuget.org/packages/newtonsoft.json/) de Newtonsoft.

## Token de CollectionMeta {#section_dzt_4mh_xz}

El token de CollectionMeta se pasa a Livefyre cuando se incrustan Comentarios en una página y proporciona al sistema los metadatos necesarios para la nueva colección. Además, creará un MD5 `checksum` de estos datos, que Livefyre comprueba para ver si los metadatos han cambiado. (p. ej., si se editó el título o la dirección URL del artículo).

Este token se firma con su `Site Key`, que le proporcionó el administrador de cuentas técnico de Livefyre.

Consulte también:

* Documentos oficiales de token de CollectionMeta
* [Ejemplo de Gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Cree un diccionario que contenga los metadatos de la colección. Solo vamos a agregar algunos de los campos necesarios en este paso, porque queremos crear una suma de comprobación de este objeto ANTES de agregar el articleId.

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

   * **** *titulerrequerido*: Título de la colección, normalmente el título del artículo. La longitud máxima es de 255 caracteres. No admite entidades HTML. Codifique caracteres especiales con UTF-8.
   * **** *urlrequired*: Dirección URL canónica del artículo. Esto lo utilizan las funciones de uso compartido de comentarios y sincronización social, así como los vínculos a su artículo desde el panel de administración. Si realiza pruebas localmente, tenga en cuenta que Livefyre no aceptará ‘localhost’ como dominio.
   * **** *tagsopcionales*: Una lista separada por comas de las etiquetas que desee agregar a la colección en el panel Livefyre. Las etiquetas no pueden contener espacios. Utilice caracteres de subrayado si desea que aparezca un espacio en el panel de administración.
   * **** *typeopcional*: Una cadena que indica qué tipo de colección se va a crear. Los valores válidos son:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`

      Si no se especifica, se crea una colección LiveComments de forma predeterminada.


1. JSON codifica este diccionario y genera una suma de comprobación md5.

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

1. Añada el **articleId** al diccionario. La **suma de comprobación** no entra en el token collectionMeta, pero debe enviarse como un parámetro independiente en el objeto js convConfig.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **** *articleIdrequired*: Un identificador único para su colección dentro de su sitio de Livefyre. Normalmente, el único articleId utilizado en el CMS. (p. ej. su ID de anuncio de WordPress) Este valor nunca debe cambiar. Livefyre identifica colecciones únicas mediante la combinación de siteId y articleId.

1. Genere un token de JWT firmado del diccionario, utilizando la clave del sitio proporcionada por Livefyre. Tenga en cuenta que debe especificar el algoritmo hash correcto, ya que el paquete JWT no utiliza HS256 de forma predeterminada.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## El autentificador del usuario {#section_g1d_43h_xz}

El autentificador de autenticación de usuario se utiliza para firmar a un usuario en Livefyre. Cuando un usuario inicia sesión en el sitio, el sitio genera un autentificador de autenticación de usuario que se pasa al widget Livefyre de la página. (Para obtener más información sobre el proceso de autenticación, consulte Perfiles remotos).

Este token requiere su nombre de red (network.fyre.co) y está firmado con su clave de red, que le proporciona el administrador técnico de cuentas de Livefyre.

Consulte también:

* Documentos oficiales del autentificador de autenticación
* [Ejemplo de Gist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. Cree un diccionario que contenga la información necesaria.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **dominio:** El nombre de la red (proporcionado por Livefyre). por ejemplo mynetwork.fyre.co
   * **user_id:** ID de usuario único para el usuario en el sistema de perfil del sitio. Sólo deben ser caracteres alfanuméricos (A-Z, a-z, 0-9). Si los ID de usuario de su sistema contienen caracteres no válidos, considere enviar a Livefyre un hash md5 del ID de usuario o una versión codificada base64 del mismo. (Indique al administrador de su cuenta si lo hace).
   * **expires:** la fecha (en hora de Epoch) en la que caduca el token. Esto debe coincidir con el tiempo de sesión de los inicios de sesión en el sitio, de modo que el estado de inicio de sesión de Livefyre se mantenga en sincronización con el estado de inicio de sesión del sitio.
   * **display_name:** El nombre para mostrar del usuario en el sistema de perfil, tal como debería mostrarse en el flujo de comentarios.

1. Genere un token de JWT firmado del diccionario mediante la clave de red proporcionada por Livefyre. Tenga en cuenta que debe especificar el algoritmo hash correcto, ya que el paquete JWT no utiliza HS256 de forma predeterminada.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
