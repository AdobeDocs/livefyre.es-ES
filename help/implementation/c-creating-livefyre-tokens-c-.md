---
description: Aprenda a generar tokens de Livefyre utilizando el lenguaje "C#".
title: Creación de tokens de Livefyre `C#`
exl-id: 6360c325-0c3f-4ecb-90f7-951ef4e6f410
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 2%

---

# Creación de tokens de Livefyre C\# {#creating-livefyre-tokens-c}

Descubra cómo generar tokens de Livefyre utilizando el idioma ``C#``.

Puede aprovechar la documentación heredada y el código de muestra para utilizar `C#.NET` para escribir métodos para crear tokens.

Para hacer referencia a las bibliotecas oficiales de Livefyre, utilice la [Biblioteca Java](https://github.com/Livefyre/livefyre-java-utils) como punto de partida para los desarrolladores de `C#`.

También puede considerar la posibilidad de utilizar la [Biblioteca de Node.js](https://github.com/Livefyre/livefyre-nodejs-utils) desde la línea de comandos para generar tokens de referencia por su cuenta y para familiarizarse con la estructura del método.

* [Saltar al Meta Token de la colección](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Saltar al token de autenticación](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dependencias {#section_c15_fnh_xz}

* Necesitará el [JWT nuget package](https://www.nuget.org/packages/JWT) en su proyecto para generar los tokens.
* Los ejemplos de código de esta página utilizan el paquete [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/).

## CollectionMeta Token {#section_dzt_4mh_xz}

El CollectionMeta Token se pasa a Livefyre cuando incrusta Comentarios en una página y proporciona a nuestro sistema los metadatos necesarios para su nueva colección. Además, creará un MD5 `checksum` de estos datos, que Livefyre comprobará para ver si los metadatos han cambiado. (por ejemplo, si se ha editado el título o la dirección URL del artículo).

Este token está firmado con su `Site Key`, que le proporcionó el administrador de cuentas técnico de Livefyre.

Consulte también:

* Documentos oficiales de CollectionMeta Token
* [Ejemplo de Gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Cree un diccionario que contenga los metadatos de la colección. Solo vamos a añadir algunos de los campos necesarios en este paso, porque queremos crear una suma de comprobación de este objeto ANTES de añadir el articleId.

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

   * **** *titlerrequired*: Título de la colección, normalmente el título del artículo. La longitud máxima es de 255 caracteres. No admite entidades html. Codifique caracteres especiales utilizando UTF-8.
   * **** *urlrequired*: La URL canónica de su artículo. Lo utilizan las funciones de uso compartido de comentarios y sincronización social, y los vínculos al artículo desde el panel de administración. Si realiza pruebas localmente, tenga en cuenta que Livefyre no aceptará &quot;localhost&quot; como dominio.
   * **** *etiquetas opcionales*: Una lista separada por comas de las etiquetas que desee agregar a la colección en el panel de Livefyre. Las etiquetas no pueden contener espacios. Utilice guiones bajos si desea que aparezca un espacio en el panel de administración.
   * **** *tipo opcional*: Cadena que indica qué tipo de colección se va a crear. Los valores válidos son:

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

1. Agregue el **articleId** al diccionario. La **suma de comprobación** no va al token collectionMeta, pero debe enviarse como parámetro independiente en el objeto js convConfig.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **** *articleIdrequired*: Un identificador único para su colección dentro de su sitio de Livefyre. Normalmente, el único articleId utilizado en su CMS. (p. ej. su ID de publicación de WordPress) Este valor nunca debe cambiar. Livefyre identifica colecciones únicas mediante la combinación de siteId y articleId.

1. Genere un token JWT firmado del diccionario, utilizando la clave de sitio proporcionada por Livefyre. Tenga en cuenta que debe especificar el algoritmo hash correcto, ya que el paquete JWT no utiliza HS256 de forma predeterminada.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## El token de autenticación de usuario {#section_g1d_43h_xz}

El token de autenticación de usuario se utiliza para firmar a un usuario en Livefyre. Cuando un usuario inicia sesión en el sitio, el sitio genera un token de autenticación de usuario que se pasa al widget Livefyre en la página. (Para obtener más información sobre el proceso de autenticación, consulte Perfiles remotos).

Este token requiere su nombre de red (network.fyre.co) y está firmado con su clave de red que le proporciona su administrador técnico de cuentas en Livefyre.

Consulte también:

* Documentos oficiales de autenticador de autenticación
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

   * **dominio:** El nombre de su red (proporcionado por Livefyre). Por ejemplo, mynetwork.fyre.co
   * **user_id:** ID de usuario único para el usuario en el sistema de perfiles de su sitio. Solo debe tener caracteres alfanuméricos (A-Z, a-z, 0-9). Si los ID de usuario de su sistema contienen caracteres no válidos, considere enviar a Livefyre un hash md5 del id de usuario o una versión codificada base64 de él. (Informe a su administrador de cuentas si lo hace).
   * **caduca:** la fecha (en hora de Epoch) en la que caduca el token. Esto debe coincidir con el tiempo de sesión de los inicios de sesión del sitio, de modo que el estado de inicio de sesión de Livefyre se mantenga sincronizado con el estado de inicio de sesión del sitio.
   * **display_name:** el nombre para mostrar del usuario en el sistema de perfiles, tal como debe aparecer en el flujo de comentarios.

1. Genere un token JWT firmado del diccionario, utilizando la clave de red que le proporciona Livefyre. Tenga en cuenta que debe especificar el algoritmo hash correcto, ya que el paquete JWT no utiliza HS256 de forma predeterminada.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
