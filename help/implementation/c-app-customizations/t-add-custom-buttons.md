---
description: Agregue acciones personalizadas a sus aplicaciones de Livefyre.
seo-description: Agregue acciones personalizadas a sus aplicaciones de Livefyre.
seo-title: Agregar botones personalizados
solution: Experience Manager
title: Agregar botones personalizados
uuid: 27 d 24 c 21-d 83 f -49 df -9 b 3 f -15 d 7 abbd 2 bd 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Agregar botones personalizados{#add-custom-buttons}

Agregue acciones personalizadas a sus aplicaciones de Livefyre.

Livefyre permite agregar botones personalizados junto a los botones de acción existentes (como **[!UICONTROL Share]**y **[!UICONTROL Flag]**) en un fragmento de contenido.

Utilice el argumento móvil para definir si el botón se mostrará en dispositivos móviles.

Por ejemplo, para agregar un botón de acción personalizado para la interfaz de dispositivo móvil:

```
var convConfig = {...}; // Should have siteId, articleId, etc. 
convConfig.actionButtons = [ 
   { 
      mobile: true,  
      // (optional) sets whether the button will appear on mobile devices 
      key: 'Do Something', 
      callback: function(contentInfo) { 
         console.log('Author of content is ' + contentInfo.authorId); 
         console.log('id of content is ' + contentInfo.contentId); 
      } 
   }, 
    ... 
]; 
  
fyre.conv.load(networkConfig, [convConfig]);
```

1. Pase un argumento adicional en el objeto convconfig denominado actionbuttons, que contiene una matriz de objetos que describe cada botón que desee agregar.
1. Defina una clave para que el texto se muestre en cada botón.
1. Agregue una llamada de retorno que se invoque en un suceso click para cada botón.

La rellamada se invoca con un objeto con dos claves: `authorId` y `contentId`.
