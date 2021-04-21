---
description: Permita a los usuarios hacer clic en Colecciones desde un único diseño de página y dirección URL.
title: Cambiar colección
exl-id: 5cfae2c6-e328-4d2c-b08b-709be94e4c54
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Cambiar colección{#change-collection}

Permita a los usuarios hacer clic en Colecciones desde un único diseño de página y dirección URL.

Utilice Cambiar Delegado de Recopilación para cambiar la Colección que se muestra en una página, sin cambiar la URL, mientras que una Aplicación Livefyre ya está cargada. Utilice esta función para mostrar galerías de fotos o vídeos, u otras aplicaciones en las que la colección mostrada debería cambiar después de una acción del usuario.

Por ejemplo, al hacer clic en un vídeo o una foto de una galería, se cargará una colección específica de esa selección, mientras que la dirección URL de la página no cambiará.

Para cargar una de las tres colecciones desde una sola página [recuento de comentarios](/help/implementation/c-advanced-topics/t-display-comment-count.md):

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
