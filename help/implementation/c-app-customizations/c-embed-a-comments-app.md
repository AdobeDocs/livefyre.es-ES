---
description: La incrustación de la aplicación de comentarios sigue el proceso para
  incrustar una aplicación principal.
seo-description: La incrustación de la aplicación de comentarios sigue el proceso
  para incrustar una aplicación principal.
seo-title: Incrustar una aplicación de comentarios
solution: Experience Manager
title: Incrustar una aplicación de comentarios
uuid: e 4982 ad 3-cab 1-4805-a 55 c -594 cca 3 b 7203
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Incrustar una aplicación de comentarios{#embed-a-comments-app}

La incrustación de la aplicación de comentarios sigue el proceso para incrustar una aplicación principal.

Incrustar la aplicación de comentarios sigue el proceso para incrustar una aplicación principal descrita en [Incrustar una aplicación](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

## Ejemplo

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

Como se indica en la sección Compilar collectionmeta, collectionmeta es un objeto JSON codificado. En el ejemplo anterior, el objeto JSON toma el siguiente formato antes de codificar JWT:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

