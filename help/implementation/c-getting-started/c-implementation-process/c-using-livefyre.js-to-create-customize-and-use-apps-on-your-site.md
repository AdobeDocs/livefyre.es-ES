---
seo-title: Incrustar una aplicación
solution: Experience Manager
title: Incrustar una aplicación
uuid: e 75 caf 0 e -04 ea -4 b 04-89 ed-fea 1183 ecf 63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Incrustar una aplicación{#embed-an-app}

Agregue aplicaciones de Livefyre a sus páginas web utilizando la estructura de código incrustado de Livefyre. js.

Esta documentación está destinada a una audiencia técnica. Para obtener [información no técnica sobre Aplicaciones](/help/using/c-about-apps/c-about-apps.md).

Esta sección describe la estructura de código que deberá incluir en la plantilla de página para incrustar aplicaciones de Livefyre en su sitio.

1. Cree un archivo.html con un marcador de posición de Livefyre.

   Cree un nuevo archivo.html en el editor de texto que elija. Cree un elemento de marcador de posición Livefyre `<div>` en el que se integrará la aplicación.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Incluya la biblioteca de Livefyre. js.

   A continuación, incluya la biblioteca JS de Livefyre. Coloque la siguiente referencia en un `<script>` elemento del `<head>` elemento. A continuación, abra la página en un navegador y utilice el inspector web del explorador para confirmar que se ha cargado Livefyre.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Construya la aplicación de Livefyre.

   Utilice `Livefyre.require` para construir aplicaciones principales y de SDK pasando los paquetes de Livefyre que planea utilizar.

   1. Compile una aplicación principal.

      Para generar una aplicación principal (comentarios, blog directo o chat), utilice la siguiente estructura:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Compile una aplicación SDK.

      Para compilar una aplicación SDK como Muro de medios o Fuente, utilice la siguiente estructura:

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

      Consulte [más información sobre aplicaciones específicas](/help/using/c-about-apps/c-about-apps.md). Se recomienda fijar la última versión importante del paquete (que se puede encontrar a través [de Livefyre. requerir](https://cdn.livefyre.com/packages.html)), para evitar integraciones dañadas inesperadas.

Siguiente: Agregue autenticación al sitio para permitir que los usuarios anuncien comentarios.
