---
description: Habilite los comentarios activos en la página.
seo-description: Habilite los comentarios activos en la página.
seo-title: Comentarios
solution: Experience Manager
title: Comentarios
uuid: decad9b0-2074-4748-bd77-914008817bfa
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 3%

---


# Comentarios{#comments}

Habilite los comentarios activos en la página. Los comentarios le permiten reemplazar su sistema de comentarios predeterminado por conversaciones en tiempo real en su página.

## de CRM {#concept_4093E8BAA96A464BA74D263DA031C0B0}

Incrustar la aplicación de comentarios sigue el proceso de incrustación de una aplicación principal descrito en Introducción > Incrustación de una aplicación.

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
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
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

Como se indica en la sección Building CollectionMeta, CollectionMeta es un objeto JSON codificado. En el ejemplo anterior, el objeto JSON toma el siguiente formato antes de codificarse en JWT:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

## Objeto NetworkConfig {#c-networkconfig-object}

El objeto `NetworkConfig` es un objeto JSON que personaliza el sistema de autenticación para los usuarios de red.
El objeto `NetworkConfig` es un objeto JSON que contiene los siguientes parámetros:

| Parámetro | Tipo | Descripción |
|---|---|---|
| **authDelegate** | **  requiredobject | Se utiliza para personalizar el sistema de autenticación para usuarios de red personalizados. |
| **network** | Cadena *requerida* | Un nombre de red proporcionado por Livefyre. Por ejemplo: *nombre.fyre.co.* |
| **attachmentDelegate** | ** optionalobject | Se utiliza para especificar los tipos de archivos adjuntos de medios visibles en el flujo de la aplicación. Para obtener más información, consulte [Restricción de medios](/help/implementation/c-app-customizations/c-restrict-media.md#c_restrict_media). |
| **cadenas** | ** optionalobject | Se utiliza para personalizar cadenas de texto de los elementos HTML en cualquiera de las aplicaciones principales de Livefyre. Para obtener más información, consulte [Personalizaciones de cadena](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## ConvConfig (objeto) {#c-convconfig-object}

El objeto `convConfig` es un objeto JSON utilizado para especificar el contenido que la aplicación Livefyre representa en la página.

>[!NOTE]
>
>Los parámetros de objeto `convConfig` enumerados aquí no se aplican a la aplicación de críticas. Para obtener información sobre la integración de la aplicación de críticas mediante el objeto `convConfig`, consulte Integración de revisiones.

El objeto `ConvConfig` contiene los siguientes parámetros obligatorios:

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| **articleId** | ** required string | Identifica exclusivamente una colección dentro del sitio. Normalmente, esto corresponde a una clave principal de base de datos o a un ID de anuncio dentro del CMS. Por ejemplo: &quot;post-42&quot;. Límite de 255 caracteres.  Nota:  Si utiliza la URL del artículo como ID del artículo, asegúrese de que la cadena está codificada para MD5 o SHA-1. |
| **authPageReload** | **  optionalboolean | Se aplica a la aplicación Comentarios: Permite controlar si el comentario de un usuario se almacena localmente durante el proceso de autenticación. Si el valor es true, si un usuario introduce un comentario y luego inicia sesión en la aplicación, el comentario se almacenará localmente y se volverá a introducir en el campo de contenido después de iniciar sesión y actualizar la página. Si el valor es false, el contenido introducido se borrará durante el proceso de inicio de sesión y se deberá volver a escribir. |
| **collectionMeta** | ** required string | Metadatos con codificación JWT sobre la colección. Consulte [CollectionMeta](#c_collectionmeta_object) Objeto para obtener más información. |
| **el** | ** required string | ID de un elemento DOM al que se representará el flujo de contenido. |
| **siteId** | ** required string | El ID proporcionado por Livefyre para el sitio web o la aplicación a la que pertenece la colección. Por ejemplo: &quot;303617&quot;. |

>[!NOTE]
>
>El parámetro `app` no es necesario para una implementación de la aplicación Comentarios.

El objeto `ConvConfig` también puede contener los siguientes parámetros opcionales:

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| **actionButtons** | *matriz* opcional | Matriz de botones de acción personalizados para agregar a un fragmento de contenido junto a los botones Compartir y Marcar. Para obtener más información, consulte Añadir botones personalizados. |
| **animaciones** | ** optionalboolean | Define si las animaciones se ejecutarán dentro de la aplicación Livefyre. Establezca en false para desactivar las animaciones. El valor predeterminado es true. |
| **anónimoFlaggingEnabled** | ** optionalboolean | Define si los usuarios invitados tienen la opción de marcar el contenido. El valor predeterminado es true. |
| **browserType** | *cadena* opcional | Define el dispositivo para el que se debe generar contenido de visualización. Esto hará que el CSS, y algunas funciones, cambien para adaptarse al tipo de dispositivo de entrada. Las opciones son escritorio, móvil o tablet. (Si se deja en blanco, se pasará de forma predeterminada a la determinación del agente de Google para el formato de visualización). |
| **checksum** | ** recommendationsString | Identifica el estado actual de CollectionMeta. Si cambia este valor, Livefyre actualizará los datos del servidor con los nuevos valores de CollectionMeta. |
| **datetimeFormat** | *función*  opcional de objeto de cadena | Especifica el formato de fecha y hora del contenido transmitido. Para obtener más información, consulte Personalización de marcas de fecha y hora. |
| **disableAvatars** | ** optionalboolean | Evita que los avatares se procesen en el flujo de la aplicación y, por tanto, reduce el número de elementos cargados en el explorador. El valor predeterminado es false. |
| **disableIE8Shim** | ** optionalboolean | Deshabilita el gráfico predeterminado utilizado por Livefyre para rellenar Internet Explorer 8 de forma que se admitan los elementos HTML5. Livefyre utiliza el siguiente proyecto:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv). El valor predeterminado es false.  Nota:  Si este valor es false, se debe usar un relleno poligonal de algún tipo antes de que se invoque el chat de Livefyre para la compatibilidad con Internet Explorer 8. |
| **disableThirdPartyAnalytics** | ** optionalboolean | Deshabilita los sistemas de análisis de terceros (Quantserve y Google Analytics) que Livefyre puede utilizar para las mediciones internas. El valor predeterminado es false. |
| **editorCss** | ** optionalobject | Se utiliza para personalizar el estilo del editor de comentarios. Puede aplicar estilo al color de fondo del campo del editor, así como al color, tamaño y familia de la fuente del texto que aparece dentro del editor.  Por ejemplo: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| **initialNumVisible** | ** optionalinteger | Le permite establecer el número predeterminado de comentarios visibles en la aplicación tras la carga. Puede ser un entero del 1 al 50. |
| **initialNumVisibleLegacy** | ** optionalinteger | Le permite establecer el número predeterminado de elementos de contenido heredado visibles en la aplicación tras la carga. Puede ser un entero del 1 al 50. Si no se especifica este parámetro, el valor predeterminado es initialNumVisible.  Por ejemplo: Si la colección incluye 100 comentarios activos y 100 comentarios heredados, establezca initalNumVisible:10 e initialNumVisibleLegacy:5 para mostrar 10 comentarios activos (con el botón Mostrar más) + 5 comentarios de archivo (con el botón Mostrar más). |
| **maxVisible** | ** optionalinteger | Define el número máximo de fragmentos visibles de contenido de nivel superior en la aplicación de chat. Si hay nuevos fragmentos de flujo de contenido en, el contenido de la parte inferior del flujo se eliminará de la página. Si se hace clic en el botón Mostrar más..., se ignora el parámetro y el usuario puede mostrar todo el contenido que desee. (Utilice este parámetro para controlar el número de elementos que aparecen en la página en flujos de alta velocidad). |
| **postToButtons** | *matriz* opcional | Se utiliza para configurar los proveedores que aparecen al incrustar la aplicación de blog en vivo. Las opciones disponibles son dos (Twitter), fb (Facebook) y li (LinkedIn). El valor predeterminado es [ tw, fb ]. |
| **readOnly** | ** optionalboolean | Desactiva toda la interactividad de la colección. Cuando el valor es true, los usuarios no pueden iniciar sesión en el flujo y no pueden anunciar, editar, responder o indicar &quot;Me gusta&quot; en el contenido. Cuando sea true, los usuarios podrán marcar y compartir contenido. El valor predeterminado es false. |
| **stream** | ** optionalobject | Contiene opciones para configurar el flujo de la aplicación. |
| **stream.catchup** | ** optionalinteger | Especifica el número de segundos anteriores al momento actual en que se debe cargar el flujo. De forma predeterminada, Livefyre carga 50 fragmentos de contenido y, a continuación, carga todo el contenido enviado entre ellos y el momento actual. En casos de uso muy rápido, el contenido puede publicarse demasiado rápido para permitir que la aplicación se &quot;ponga al día&quot; en el presente. Utilice esta configuración para definir el número de segundos anteriores a ahora para el que se publicará contenido (después de la carga de contenido inicial). |
| **stream.delay** | ** optionalinteger | Especifica el número de segundos entre solicitudes de flujo continuo. Utilice este parámetro para ayudar a controlar el flujo de contenido y retrasar la frecuencia con la que se actualiza el DOM.  Nota:  Si se define demasiado grande, el flujo puede quedar rezagado. |


>[!NOTE]
>
>Puede pasar uno o varios objetos `convConfig` durante la inicialización de la aplicación para mostrar varias aplicaciones en la misma página. Tenga en cuenta que las aplicaciones adicionales utilizan recursos del explorador y el rendimiento puede degradarse a medida que aumenta el número.

## CollectionMeta Object {#c-collectionmeta-object}

El objeto `CollectionMeta` es un objeto JSON que especifica los metadatos que se almacenarán en la colección.

`CollectionMeta` siempre se codifica antes de pasarse a Livefyre para mayor seguridad. El valor codificado se pasa al objeto `ConvConfig` que se muestra arriba.

>[!NOTE]
>
>Debe agregar código del lado del servidor para codificar el objeto `CollectionMeta` JSON. Consulte Creación de tokens del lado del servidor para obtener más información.

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| **articleId** | ** required string | Un ID exclusivo para la colección. |
| **title** | ** required string | Título que desea aplicar a la colección. Esto suele corresponder al título de la página que muestra la aplicación.  Por ejemplo: &quot;¡La integración es tan divertida!&quot; <br>**Nota:**  La longitud máxima de caracteres del título es de 255 caracteres. El campo de título no admite entidades HTML. Codifique caracteres especiales con UTF-8. |
| **url** | ** required string | Dirección URL absoluta canónica que desea adjuntar a esta colección. Esta URL se utilizará para generar vínculos de regreso a la aplicación a partir de contenido compartido en Facebook y Twitter, notificaciones por correo electrónico y Livefyre Studio.  <br>**** NotaLivefyre requiere el uso de un nombre de dominio completo; no es necesario el número de puerto o una llamada de retorno para resolver la configuración local. Si realiza pruebas localmente, asegúrese de utilizar un dominio de URL base válido. <br>Por ejemplo:  `https://customer.com` es válido, mientras que no  `https://localhost:5995` lo es. Una vez configurado el servidor web local para aceptar un nombre de dominio completo, no se necesitan rellamadas ni resoluciones y el desarrollo local puede continuar según lo esperado. |
| **type** | ** required string | Tipo de colección. Debe ser `livechat`. |

El objeto `CollectionMeta` también puede contener el siguiente parámetro opcional:

| Parámetro | Tipo | Descripción |
|---|---|---|
| **etiquetas** | *cadena* opcional | Lista separada por comas de palabras clave o frases únicas. Buscar colecciones por etiquetas en Studio o con la API de búsqueda. <br> **Nota:** Aunque las etiquetas agregadas a través de Studio pueden contener espacios, las etiquetas introducidas a través de la API no pueden. Utilice caracteres de subrayado para definir etiquetas que mostrarán espacios en la interfaz de usuario. (Por ejemplo: utilice `Monday_Quarterback` para mostrar Monday Quarterback en Studio). |

## Añadir un controlador de Evento {#concept_06D8B811C98B4CC6B38C6340EBA176E5}

Para registrar controladores de evento, utilice la llamada widget.on dentro de la función de llamada de retorno de la aplicación.

### Por ejemplo

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```
