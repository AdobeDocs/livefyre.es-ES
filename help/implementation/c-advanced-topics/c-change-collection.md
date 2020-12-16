---
description: Permite a los usuarios hacer clic en Colecciones desde una única dirección URL y un diseño de página.
seo-description: Permite a los usuarios hacer clic en Colecciones desde una única dirección URL y un diseño de página.
seo-title: Cambiar colección
solution: Experience Manager
title: Cambiar colección
uuid: 81c8a554-375f-4659-9e25-5b3618824633
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Cambiar colección {#change-collection}

Permite a los usuarios hacer clic en Colecciones desde una única dirección URL y un diseño de página.

Utilice el Delegado de la colección de cambios para cambiar la colección que se muestra en una página, sin cambiar la URL, mientras que una aplicación de Livefyre ya está cargada. Utilice esta función para mostrar las galerías de fotos o vídeos, u otras aplicaciones en las que la colección mostrada debería cambiar tras una acción del usuario.

Por ejemplo, al hacer clic en un vídeo o una fotografía de una galería se cargará una colección específica de esa selección, mientras que la dirección URL de la página no cambiará.

Para [cargar una de las tres colecciones desde una sola página](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count):

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
