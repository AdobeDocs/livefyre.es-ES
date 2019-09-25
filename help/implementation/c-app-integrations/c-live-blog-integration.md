---
description: Live Blog allows you to feature real-time updates and images from your site’s own editors when covering a live event.
seo-description: Live Blog le permite presentar actualizaciones en tiempo real e imágenes de los propios editores del sitio al cubrir un evento en directo.
seo-title: Blog en vivo
solution: Experience Manager
title: Blog en vivo
uuid: 5ca373f1-2008-45ab-9ec2-1e295af4e368
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Blog en vivo{#live-blog}

Live Blog le permite presentar actualizaciones en tiempo real e imágenes de los propios editores del sitio al cubrir un evento en directo.

## Blog en vivo {#topic_574DEE2125A94B85BFB5C3D2C57C337E}

Live Blog le permite presentar actualizaciones en tiempo real e imágenes de los propios editores del sitio al cubrir un evento en directo.

## de CRM {#c_live_blog_integration}

Live Blog allows you to feature real-time updates and images from your site’s own editors when covering a live event.

Para incrustar una aplicación de blog en directo, siga el procedimiento para incrustar una aplicación. Consulte [Incrustar una aplicación](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). El siguiente es un ejemplo de cómo se ve una aplicación de blog en directo incrustada.

### Ejemplo

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: "client-solutions.fyre.co" 
    }; 
    var convConfig = { 
      siteId: '347674', 
      articleId: '1', 
      el: 'livefyre', 
      collectionMeta: 'eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6IlRpdGxlIDEiLCJ1cmwiOiJodHRwOlwvXC9kZXYubGl2ZWZ5cmUuY29tIiwidGFncyI6InRhZzEsdGFnMiIsImNoZWNrc3VtIjoiY2Q0YTJjYWJkMTIxOTkyM2FjZGJhMjExOWY2NmYwNTUiLCJhcnRpY2xlSWQiOiIxIn0.Dq-ghi9KYmEPmagvCS1NPyYDRMGBujm735QaTRb7E7k', 
      checksum: '6e2e4faf7b95f896260fe695eafb34ba' 
    }; 
    
    Livefyre.require(['fyre.conv#3'], function(Conv) { 
        new Conv(networkConfig, [convConfig], function(blogWidget) {}); 
        auth.delegate({ 
          login: function (callback) { 
            callback(null,{livefyre:'<userauthtoken>'}); 
          }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

CollectionMeta es un objeto JSON codificado. En el ejemplo anterior, el objeto JSON adopta el siguiente formato antes de codificarse en JWT:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "liveblog",  
"title": "Title 1" 
}
```

## Objeto NetworkConfig {#c-networkconfig-object}

El `NetworkConfig` objeto es un objeto JSON que personaliza el sistema de autenticación para los usuarios de red.

El `NetworkConfig` objeto es un objeto JSON que contiene los siguientes parámetros:

| Parámetro | Tipo | Descripción |
|---|---|---|
| **authDelegate** | *objeto requerido* | Used to customize the authentication system for custom network users. |
| **network** | *required string   A Livefyre-provided network name.* For example: yourname.fyre.co.** |
| **attachmentDelegate** | *optional* object | Used to specify the types of media attachments visible in the App stream. For more information, see Restricting Media.[](../c-app-customizations/c-restrict-media.md#c_restrict_media) |
| **strings** | *optional object* | Se utiliza para personalizar cadenas de texto de los elementos HTML en cualquiera de las aplicaciones principales de Livefyre. For more information, see String Customizations.[](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md) |

## ConvConfig Object {#c-convconfig-object}

The  object is a JSON object used to specify the content that the Livefyre App renders on the page.`convConfig`

>[!NOTE]
>
>Los parámetros de `convConfig` objeto enumerados aquí no se aplican a la aplicación de críticas. Para obtener información sobre la integración de la aplicación de críticas mediante el `convConfig` objeto, consulte Integración de críticas.

El `ConvConfig` objeto contiene los siguientes parámetros obligatorios:

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| **articleId** | *cadena requerida* | Identifica exclusivamente una colección dentro del sitio. Normalmente, esto corresponde a una clave principal de base de datos o a un ID de anuncio dentro del CMS. For example: “post-42”. Límite de 255 caracteres.  Nota:  Si utiliza la URL del artículo como ID del artículo, asegúrese de que la cadena está codificada para MD5 o SHA-1. |
| **collectionMeta** | *cadena requerida* | JWT-encoded metadata about the Collection. Consulte CollectionMeta Object para obtener más información. |
| **el** | *cadena requerida* | ID de un elemento DOM al que se representará el flujo de contenido. |
| **siteId** | *cadena requerida* | ID proporcionada por Livefyre para el sitio web o la aplicación a la que pertenece la colección. Por ejemplo: "303617". |

>[!NOTE]
>
>El `app` parámetro no es necesario para una implementación de la aplicación Comentarios.

El `ConvConfig` objeto también puede contener los siguientes parámetros opcionales:

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| **actionButtons** | *matriz opcional* | An array of custom action buttons to add to a piece of content next to the  Share  and  Flag  buttons. Para obtener más información, consulte Adición de botones personalizados. |
| **animaciones** | *booleano opcional* | Define si las animaciones se ejecutarán dentro de la aplicación Livefyre. Establezca en false para desactivar las animaciones. El valor predeterminado es true. |
| **anónimoFlaggingEnabled** | Booleano | Define si los usuarios invitados tienen la opción de marcar el contenido. Default is true. |
| browserType | *optional String* | Defines the device for which display content should be generated. This will cause the CSS, and some functionality, to change to fit the input device type. Options are desktop, mobile, or tablet. (If left blank, will default to the Google Agent determination for the display format.) |
| **checksum** | *optional string (recommended)* | Identifica el estado actual de CollectionMeta. Si cambia este valor, Livefyre actualizará los datos del servidor con los nuevos valores de CollectionMeta. |
| **datetimeFormat** | *optional  string  object  function* | Specifies the datetime format of streamed content. Para obtener más información, consulte Personalización de marcas de fecha y hora. |
| disableAvatars | *booleano opcional* | Evita que los avatares se procesen en el flujo de la aplicación y, por tanto, reduce el número de elementos cargados en el explorador. El valor predeterminado es false. |
| disableIE8Shim | *booleano opcional* | Disables the default shiv used by Livefyre to polyfill Internet Explorer 8 so that HTML5 elements are supported. Livefyre utiliza el siguiente proyecto:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . El valor predeterminado es false.  Nota:  Si este valor es false, se debe usar un relleno poligonal de algún tipo antes de que se invoque el chat de Livefyre para la compatibilidad con Internet Explorer 8. |
| **disableThirdPartyAnalytics** | *booleano opcional* | Disables third party analytics systems (Quantserve and Google Analytics) that Livefyre may use for internal measurements. El valor predeterminado es false. |
| **editorCss** | *objeto opcional* | Se utiliza para personalizar el estilo del editor de comentarios. Puede aplicar estilo al color de fondo del campo del editor, así como al color, tamaño y familia de la fuente del texto que aparece dentro del editor.  Por ejemplo: {fondo: ‘#ccc’, color: ‘red’, fuente: ’30 px "Helvetica Neue", Helvetica, Arial, Ginebra, sans-serif"} |
| **initialNumVisible** | *integer opcional* | Le permite establecer el número predeterminado de comentarios visibles en la aplicación tras la carga. Puede ser un entero del 1 al 50. |
| **initialNumVisibleLegacy** | *integer opcional* | Le permite establecer el número predeterminado de elementos de contenido heredado visibles en la aplicación tras la carga. This may be an integer from 1 to 50. Si no se especifica este parámetro, el valor predeterminado es initialNumVisible.  Por ejemplo: Si la colección incluye 100 comentarios activos y 100 comentarios heredados, establezca initalNumVisible:10 e initialNumVisibleLegacy:5 para mostrar 10 comentarios activos (con el botón Mostrar más) + 5 comentarios de archivo (con el botón Mostrar más). |
| **maxVisible** | *integer opcional* | Define el número máximo de fragmentos visibles de contenido de nivel superior en la aplicación de chat. Si hay nuevos fragmentos de flujo de contenido en, el contenido de la parte inferior del flujo se eliminará de la página. Si se hace clic en el botón Mostrar más..., se ignora el parámetro y el usuario puede mostrar todo el contenido que desee. (Utilice este parámetro para controlar el número de elementos que aparecen en la página en flujos de alta velocidad). |
| **postToButtons** | *matriz opcional* | Se utiliza para configurar los proveedores que aparecen al incrustar la aplicación de blog en vivo. Las opciones disponibles son dos (Twitter), fb (Facebook) y li (LinkedIn). El valor predeterminado es [ tw, fb ]. |
| **readOnly** | *booleano opcional* | Desactiva toda la interactividad de la colección. Cuando el valor es true, los usuarios no pueden iniciar sesión en el flujo y no pueden anunciar, editar, responder o indicar "Me gusta" en el contenido. When true, users will be able to Flag and Share content. El valor predeterminado es false. |
| **stream** | *objeto opcional* | Contiene opciones para configurar el flujo de la aplicación. |
| stream.catchup | *integer opcional* | Especifica el número de segundos anteriores al momento actual en que se debe cargar el flujo. De forma predeterminada, Livefyre carga 50 fragmentos de contenido y, a continuación, carga todo el contenido enviado entre ellos y el momento actual. En casos de uso muy rápido, el contenido puede publicarse demasiado rápido para permitir que la aplicación se "ponga al día" en el presente. Utilice esta configuración para definir el número de segundos anteriores a ahora para el que se publicará contenido (después de la carga de contenido inicial). |
| **stream.delay** | *integer opcional* | Especifica el número de segundos entre solicitudes de flujo continuo. Utilice este parámetro para ayudar a controlar el flujo de contenido y retrasar la frecuencia con la que se actualiza el DOM.  Nota:  Si se define demasiado grande, el flujo puede quedar rezagado. |


>[!NOTE]
>
>Puede pasar uno o varios `convConfig` objetos durante la inicialización de la aplicación para mostrar varias aplicaciones en la misma página. Tenga en cuenta que las aplicaciones adicionales utilizan recursos del explorador y el rendimiento puede degradarse a medida que aumenta el número.

## CollectionMeta (objeto) {#c-collectionmeta-object}

El `CollectionMeta` objeto es un objeto JSON que especifica los metadatos que se almacenarán en la colección.

`CollectionMeta` siempre se codifica antes de pasarse a Livefyre para mayor seguridad. El valor codificado se pasa al `ConvConfig` objeto que se muestra arriba.

>[!NOTE]
>
>Debe agregar código del lado del servidor para codificar el objeto `CollectionMeta` JSON. Consulte Creación de tokens del lado del servidor para obtener más información.

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| **articleId** | *cadena requerida* | Un ID exclusivo para la colección. |
| **title** | *cadena requerida* | Título que desea aplicar a la colección. Esto suele corresponder al título de la página que muestra la aplicación.  Por ejemplo: "¡La integración es tan divertida!"  Nota:  La longitud máxima de caracteres del título es de 255 caracteres. El campo de título no admite entidades HTML. Codifique caracteres especiales con UTF-8. |
| **url** | *cadena requerida* | Dirección URL absoluta canónica que desea adjuntar a esta colección. Esta URL se utilizará para generar vínculos de regreso a la aplicación a partir de contenido compartido en Facebook y Twitter, notificaciones por correo electrónico y Livefyre Studio.  Nota:  Livefyre requiere el uso de un nombre de dominio completo; no es necesario el número de puerto o una llamada de retorno para resolver la configuración local. Si realiza pruebas localmente, asegúrese de utilizar un dominio de URL base válido. (Por ejemplo: `https://customer.com` es válido, mientras que `https://localhost:5995` no lo es). Una vez configurado el servidor web local para aceptar un nombre de dominio completo, no se necesitan rellamadas ni resoluciones y el desarrollo local puede continuar según lo esperado. |
| **type** | *cadena requerida* | Tipo de colección. Debe ser livechat . |

El `CollectionMeta` objeto también puede contener el siguiente parámetro opcional:

| Parámetro | Tipo | Descripción |
|---|---|---|
| **etiquetas** | *cadena opcional* | Una lista separada por comas de palabras clave o frases únicas. Buscar colecciones por etiquetas en Studio o con la API de búsqueda. **** Nota: Aunque las etiquetas agregadas a través de Studio pueden contener espacios, las etiquetas introducidas a través de la API no pueden. Utilice caracteres de subrayado para definir etiquetas que mostrarán espacios en la interfaz de usuario. (Por ejemplo: utilice Monday_Quarterback para mostrar Monday Quarterback en Studio). |

## Adición de un controlador de eventos {#concept_D835C710A7214F6D921571E0770B6BC5}

Para registrar controladores de eventos, utilice la llamada widget.on dentro de la función de llamada de retorno de la aplicación.

Por ejemplo:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

