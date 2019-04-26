---
description: Permita que los usuarios hagan clic en las colecciones desde un diseño
  de página único y URL.
seo-description: Permita que los usuarios hagan clic en las colecciones desde un diseño
  de página único y URL.
seo-title: Cambiar colección
solution: Experience Manager
title: Cambiar colección
uuid: 69 bafcc 7-c 55 e -47 d 6-bc 79-b 0 db 80 fdf 138
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Cambiar colección{#change-collection}

Permita que los usuarios hagan clic en las colecciones desde un diseño de página único y URL.

Use el delegado de cambio de colección para cambiar la colección mostrada en una página, sin cambiar la URL, mientras que una aplicación de Livefyre ya se ha cargado. Utilice esta función para mostrar galerías de vídeo o de vídeo u otras aplicaciones en las que la colección que se muestra debería cambiar después de una acción del usuario.

Por ejemplo, si hace clic en un vídeo o una foto en una galería, se cargará una colección específica para esa selección, mientras que la dirección URL de la página no cambiará.

Para cargar una de tres colecciones desde una página de recuento [de comentarios](/help/implementation/c-advanced-topics/t-display-comment-count.md) única:

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

