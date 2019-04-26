---
description: Adición de conversación directa a la página.
seo-description: Adición de conversación directa a la página.
seo-title: Chat
solution: Experience Manager
title: Chat
uuid: d 6761 a 69-efa 5-4 ad 3-abaf -1 ba 8 e 6 c 17 f 94 f
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Chat{#chat}

Adición de conversación directa a la página.

Chat permite a la audiencia participar en conversaciones en tiempo real alrededor de eventos en directo. El contenido se muestra como flujo continuo, lo que fomenta una rápida participación en el cuadro de diálogo desplegable.

Versión actual: Usos de chat `fyre.conv v3.0.0.`

## de CRM{#concept_0A99792A7E89403F95D082D52D600F17}

La incrustación de la aplicación de chat sigue el proceso de incrustación de una aplicación principal descrita en Introducción > [Incrustación de una aplicación](../c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md#using-livefyre-js-create-customize-apps).

Ejemplo:

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
        new Conv(networkConfig, [convConfig], function(chatWidget) {}); 
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

Como se indica en la sección [collectionmeta Token](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) , collectionmeta es un objeto JSON codificado. En el ejemplo anterior, el objeto JSON toma el siguiente formato antes de su codificación JWT:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "livechat",  
"title": "Title 1" 
}
```

## Objeto networkconfig {#c-networkconfig-object}

`NetworkConfig` El objeto es un objeto JSON que personaliza el sistema de autenticación para los usuarios de red.

`NetworkConfig` El objeto es un objeto JSON que contiene los parámetros siguientes:

| Parámetro | Tipo | Descripción |
|---|---|---|
| Authdelegate | *required* object | Se utiliza para personalizar el sistema de autenticación para los usuarios de red personalizados. |
| red | *required* string | Un nombre de red proporcionado por Livefyre. Por ejemplo: *yourname. fyre. co.* |
| Attachmentdelegate | Objeto | Se utiliza para especificar los tipos de archivos adjuntos de medios visibles en el flujo de la aplicación. Para obtener más información, consulte [Restricción de medios](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
| cadenas | *optional* object | Se utiliza para personalizar cadenas de texto de elementos HTML en cualquiera de las aplicaciones principales de Livefyre. Para obtener más información, consulte [Personalizaciones de cadenas](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Objeto convconfig {#c-convconfig-object}

`convConfig` El objeto es un objeto JSON utilizado para especificar el contenido que la aplicación de Livefyre procesa en la página.

>[!NOTE]
>
>Los parámetros `convConfig` de objeto que aparecen aquí no se aplican a la aplicación Reviews. Para obtener información sobre la integración de la aplicación Reviews con el `convConfig` objeto, consulte Análisis de la integración.

`ConvConfig` El objeto contiene los siguientes parámetros obligatorios:

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| Articleid | *required* string | Identifica exclusivamente una colección dentro del sitio. Normalmente, esto corresponde a una clave principal de base de datos o a ID de anuncio dentro del CMS. Por ejemplo: «post -42». Límite de 255 caracteres. Nota: Si utiliza la URL del artículo como artículo de artículo, asegúrese de que la cadena sea MD 5 o SHA -1 codificado. |
| Collectionmeta | *required* string | Metadatos codificados JWT sobre la colección. Consulte [collectionmeta Object](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) para obtener más información. |
| el | *required* string | El ID de un elemento DOM al que se procesará el flujo de contenido. |
| Siteid | *required* string | ID de Livefyre para el sitio Web o la aplicación a la que pertenece la colección. Por ejemplo: «303617». |

>[!NOTE]
>
>El `app` parámetro no es necesario para una implementación de aplicación de comentarios.

`ConvConfig` El objeto también puede contener los parámetros opcionales siguientes:

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| Actionbuttons | *optional* array | Matriz de botones de acción personalizados que se agregarán a un fragmento de contenido junto a los botones Compartir y Indicador. Para obtener más información, consulte Adición de botones personalizados. |
| animaciones | *optional* boolean | Define si las animaciones se ejecutarán dentro de la aplicación de Livefyre. Establezca en false para deshabilitar las animaciones. El valor predeterminado es true. |
| Anonymousflaggingenabled | *optional* boolean | Define si los usuarios invitados tienen la opción de marcar contenido. El valor predeterminado es true. |
| Browsertype | *optional* string | Define el dispositivo para el que se debe generar el contenido de visualización. Esto provocará que CSS, y algunas funcionalidades, cambien para adaptarse al tipo de dispositivo de entrada. Las opciones son escritorio, móvil o tableta. (Si se deja en blanco, se establecerá el valor predeterminado de la determinación Agent Agent para el formato de visualización). |
| checksum | *cadena recomendada* (recomendado) | Identifica el estado actual de collectionmeta. Si se cambia este valor, Livefyre actualizará los datos del servidor con los nuevos valores en collectionmeta. |
| Datetimeformat | *función de* objeto de cadena opcional | Especifica el formato de hora de envío del contenido transmitido. Para obtener más información, consulte Personalización de las marcas de fecha y hora. |
| Disableavatars | *optional* boolean | Evita que se procesen avatares en el flujo de la aplicación y, por lo tanto, reduce el número de elementos cargados en el navegador. El valor predeterminado es false. |
| disableIE8Shim | *optional* boolean | Desactiva el shiv predeterminado utilizado por Livefyre para polyfill Internet Explorer 8 para que se admitan elementos HTML 5. Livefyre usa el siguiente proyecto: [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv). El valor predeterminado es false. Nota: Si este valor es false, el polígono de cierta ordenación debe usarse antes de que se invoque el chat de Livefyre para la compatibilidad con Internet Explorer 8. |
| Disablethirdpartyanalytics | *optional* bboolean | Desactiva los sistemas de análisis de terceros (Quantserve y Google Analytics) que Livefyre puede utilizar para mediciones internas. El valor predeterminado es false. |
| Editorcss | *optional* object | Se utiliza para personalizar el estilo del editor de comentarios. Puede aplicar estilo al color de fondo del campo del editor como así también al color de fuente, el tamaño y la familia del texto que aparece dentro del editor. Por ejemplo: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| Initialnumvisible | *optional* integer | Permite establecer el número predeterminado de comentarios visibles en la aplicación después de cargar. Puede ser un número entero de 1 a 50. |
| Initialnumvisiblelegacy | *optional* integer | Permite establecer el número predeterminado de elementos de contenido heredados visibles en la aplicación después de cargar. Puede ser un número entero de 1 a 50. Si no se especifica este parámetro, el valor predeterminado es initialnumvisible. Por ejemplo: Si la colección incluye 100 comentarios activos y 100 comentarios preexistentes, establezca initalnumvisible: 10, e initialnumvisiblelegacy: 5, para mostrar 10 comentarios activos (con el botón Mostrar más) + 5 comentarios del archivado (con el botón Mostrar más). |
| Maxvisible | *optional* integer | Define el número máximo de partes visibles de contenido de nivel superior en la aplicación de chat. Si hay nuevas partes de flujo de contenido en, el contenido en la parte inferior del flujo se eliminará de la página. Si se hace clic en el botón Mostrar más…, se omite el parámetro y el usuario es gratuito para mostrar el contenido que desee. (Utilice este parámetro para controlar el número de elementos que aparecen en la página en flujos de velocidad alta). |
| Posttobuttons | *optional* array | Se utiliza para configurar qué proveedores aparecen al incrustar la aplicación de blog activo. Las opciones disponibles son tw (Twitter), fb (Facebook) y li (linkedin). Defaults to [ tw, fb ]. |
| Readonly | *optional* boolean | Desactiva toda la interactividad de la colección. Si el valor es true, los usuarios no podrán iniciar sesión en el flujo, ni publicar, editar, responder ni indicar que gusta el contenido. Si el valor es true, los usuarios podrán marcar y compartir contenido. El valor predeterminado es false. |
| flujo | *optional* object | Contiene opciones para configurar la transmisión de la aplicación. |
| stream. captura | *optional* integer | Especifica el número de segundos anteriores al momento actual que debería cargarse el flujo. De forma predeterminada, Livefyre carga 50 fragmentos de contenido y, a continuación, carga todo el contenido enviado entre ellos y el momento actual. En casos de uso muy rápidos, el contenido se puede publicar demasiado rápido para permitir que la aplicación se ponga en contacto con el presente. Utilice esta configuración para definir el número de segundos anteriores a ahora para el que se publicará el contenido (después de cargar el contenido inicial). |
| stream. delay | *optional* integer | Especifica el número de segundos entre solicitudes de flujo continuo. Utilice este parámetro para controlar el flujo de contenido y retrasar la frecuencia con que se actualiza el DOM. Nota: Si se establece demasiado grande, el flujo podría quedar atrás. |


>[!NOTE]
>
>Puede pasar uno o varios `convConfig` objetos durante la inicialización de la aplicación para mostrar varias aplicaciones en la misma página. Tenga en cuenta que las aplicaciones adicionales utilizan los recursos y el rendimiento del navegador a medida que aumenta el número.

## Collectionmeta Object {#c-collectionmeta-object}

`CollectionMeta` El objeto es un objeto JSON que especifica metadatos para almacenarlos dentro de la colección.

`CollectionMeta` siempre se codifica antes de pasarse a Livefyre por seguridad. El valor codificado se pasa al `ConvConfig` objeto que se muestra arriba.

>[!NOTE]
>
>Debe agregar código del lado del servidor para codificar el objeto `CollectionMeta` JSON. Consulte Creación de tokens del lado del servidor para obtener más información.

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| Articleid | *required* string | ID único de la colección. |
| title | *required* string | Título que desea aplicar a la colección. Esto suele corresponder al título de la página que muestra la aplicación. Por ejemplo: «La integración es tan divertida! »» Nota: La longitud máxima de caracteres para el título es de 255 caracteres. El campo de título no admite entidades HTML. Codifique caracteres especiales con UTF -8. |
| url | *required* string | Dirección URL canónica que desea adjuntar a esta colección. Esta URL se utilizará para generar vínculos de vuelta a la aplicación desde contenido compartido en Facebook y Twitter, notificaciones por correo electrónico y Livefyre Studio. Nota: Livefyre requiere el uso de un nombre de dominio completo; No es necesario el número de puerto o una rellamada para resolver la configuración local. Si realiza pruebas localmente, asegúrese de utilizar un dominio de URL base válido. (Por ejemplo: `https://customer.com` es válido, no `https://localhost:5995` es válido.) Una vez configurado el servidor web local para aceptar un nombre de dominio completo, no se necesitan rellamadas ni resoluciones, y el desarrollo local puede continuar según lo previsto. |
| type | *required* string | Tipo de colección. Debe estar en directo. |

`CollectionMeta` El objeto también puede contener el siguiente parámetro opcional:

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| tags | *optional* string | Lista separada por comas de frases o palabras clave únicas. Busque colecciones por etiquetas en Studio o con la API de búsqueda. Nota: Si bien las etiquetas agregadas a través de Studio pueden contener espacios, las etiquetas introducidas a través de la API no pueden. Utilice guiones bajos para definir etiquetas que muestren espacios en la interfaz de usuario. (Por ejemplo: Use Monday_ Quarterback para mostrar el Quarterback del lunes en Studio). |

## Adición de un controlador de eventos {#concept_E7C17EFB43F24F1A8572E60C69176C6D}

Para registrar controladores de eventos, utilice la llamada de utilidad. on dentro de la función de rellamada de la aplicación.

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

Para obtener más información, y para obtener una lista de eventos disponibles, consulte [Eventos de Javascript](../c-app-customizations/c-javascript-events.md#c_javascript_events).
