---
seo-title: Incrustar una aplicación
solution: Experience Manager
title: Incrustar una aplicación
uuid: e75caf0e-04ea-4b04-89ed-fea1183ecf63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Incrustar una aplicación{#embed-an-app}

Agregue aplicaciones de Livefyre a sus páginas web mediante la estructura de código incrustado de Livefyre.js.

Esta documentación está dirigida a un público técnico. Para obtener información [no técnica sobre las aplicaciones](/help/using/c-about-apps/c-about-apps.md).

Esta sección describe la estructura de código que deberá incluir en la plantilla de página para incrustar las aplicaciones de Livefyre en el sitio.

1. Cree un archivo .html con un marcador de posición de Livefyre.

   Cree un nuevo archivo .html en el editor de texto que desee. Cree un `<div>` elemento Livefyre de marcador de posición en el que se incruste la aplicación.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Incluya la biblioteca Livefyre.js.

   A continuación, incluya la biblioteca Livefyre JS. Coloque la siguiente referencia en un `<script>` elemento del `<head>` elemento. A continuación, abra la página en un navegador y utilice el inspector web del navegador para confirmar que Livefyre está cargado.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Construya la aplicación Livefyre.

   Utilícelo `Livefyre.require` para crear aplicaciones principales y de SDK pasando los paquetes de Livefyre que va a utilizar.

   1. Cree una aplicación principal.

      Para crear una aplicación principal (Comentarios, Blog en directo o Chat), utilice la siguiente estructura:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Creación de una aplicación de SDK.

      Para crear una aplicación de SDK como Media Wall o Feed, utilice la siguiente estructura:

      ```
             Livefyre.require(['app#{version_number}'], 
         function (App, SDK) { 
            var app = new App({ 
            el: document.getElementById('app'), 
         }); 
         var collection = new SDK.Collection({ 
            network: "`labs.fyre.co`", 
            environment: "livefyre.com", 
            siteId: "315833", 
            articleId: 'livefyre-tweets' 
         }); 
         collection.pipe(feed); 
      }); 
      ```

      Consulte [más información sobre aplicaciones](/help/using/c-about-apps/c-about-apps.md)específicas. Se recomienda fijar a la última versión principal del paquete (que se puede encontrar en [Livefyre.required](https://cdn.livefyre.com/packages.html)) para evitar integraciones inesperadas dañadas.

Siguiente: Agregue autenticación a su sitio para permitir que los usuarios publiquen comentarios.
