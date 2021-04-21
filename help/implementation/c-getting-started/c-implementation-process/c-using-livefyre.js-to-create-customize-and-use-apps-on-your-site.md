---
title: Incrustar una aplicación
description: Incrustar una aplicación
exl-id: 12f75093-1b4d-4cf1-8593-dbd17ff33872
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Incrustar una aplicación{#embed-an-app}

Agregue aplicaciones de Livefyre a sus páginas web mediante la estructura de código incrustado de Livefyre.js .

Esta documentación está dirigida a una audiencia técnica. Para obtener [información no técnica sobre Apps](/help/using/c-about-apps/c-about-apps.md).

En esta sección se describe la estructura de código que debe incluir en la plantilla de página para incrustar aplicaciones de Livefyre en el sitio.

1. Cree un archivo .html con un marcador de posición de Livefyre.

   Cree un nuevo archivo .html en el editor de texto que desee. Cree un marcador de posición Livefyre `<div>` en el que la aplicación estará incrustada.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Incluya la biblioteca Livefyre.js .

   A continuación, incluya la biblioteca Livefyre JS. Coloque la siguiente referencia en un elemento `<script>` en el elemento `<head>` . A continuación, abra la página en un explorador y utilice el inspector web del explorador para confirmar que Livefyre se ha cargado.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Construya la aplicación Livefyre.

   Utilice `Livefyre.require` para construir aplicaciones principales y de SDK pasando los paquetes de Livefyre que planea utilizar.

   1. Crear una aplicación principal.

      Para crear una aplicación principal (comentarios, blogs en directo o chat), utilice la siguiente estructura:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Generar una aplicación SDK.

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

      Consulte [más información sobre aplicaciones específicas](/help/using/c-about-apps/c-about-apps.md). Se recomienda fijar a la última versión principal del paquete (que se puede encontrar en [Livefyre.requirements](https://cdn.livefyre.com/packages.html)) para evitar integraciones rotas inesperadas.

Siguiente: Agregue autenticación al sitio para permitir que los usuarios anuncien comentarios.
