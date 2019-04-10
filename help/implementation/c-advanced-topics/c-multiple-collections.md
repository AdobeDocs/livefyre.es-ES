---
description: Exhibir varias colecciones en una sola página.
seo-description: Exhibir varias colecciones en una sola página.
seo-title: Varias colecciones
solution: Experience Manager
title: Varias colecciones
uuid: 9675 ffd 7-1 a 59-42 a 1-b 3 ba -40 af 1744 cfd 1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Varias colecciones {#multiple-collections}

Exhibir varias colecciones en una sola página.

Puede incluir varias colecciones en una sola página del sitio. Por ejemplo, para publicar un evento, puede tener un blog directo o un chat de chat durante el evento, con una aplicación separada en el lado de la página, mostrando Contenido depurado relacionado de alrededor de la Web social. O bien, puede incluir una aplicación de comentarios debajo de un artículo, con un chat al lado.

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
