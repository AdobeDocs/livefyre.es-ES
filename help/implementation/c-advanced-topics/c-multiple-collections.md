---
description: Muestra varias colecciones en una sola página.
seo-description: Muestra varias colecciones en una sola página.
seo-title: Varias colecciones
solution: Experience Manager
title: Varias colecciones
uuid: 9675ffd7-1a59-42a1-b3ba-40af1744cfd1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Varias colecciones {#multiple-collections}

Muestra varias colecciones en una sola página.

Puede incluir varias colecciones en una sola página del sitio. Por ejemplo, para publicar un evento, es posible que tenga un blog en directo o una conversación por chat durante el evento, con una aplicación independiente en la parte lateral de la página, que muestre el contenido depurado relacionado de la web social. O bien, puede incluir una aplicación de comentarios debajo de un artículo, con un chat a un lado.

Para obtener varias conversaciones en una página, agregue una o más configuraciones en una matriz y pase la matriz a la llamada de carga. Por ejemplo.

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```
