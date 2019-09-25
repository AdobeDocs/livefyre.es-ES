---
description: Agregue acciones personalizadas a sus aplicaciones de Livefyre.
seo-description: Agregue acciones personalizadas a sus aplicaciones de Livefyre.
seo-title: Agregar botones personalizados
solution: Experience Manager
title: Agregar botones personalizados
uuid: 27d24c21-d83f-49df-9b3f-15d7abbd2bd7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Agregar botones personalizados{#add-custom-buttons}

Agregue acciones personalizadas a sus aplicaciones de Livefyre.

Livefyre permite agregar botones personalizados junto a los botones de acción existentes (como **[!UICONTROL Share]** y **[!UICONTROL Flag]**) en un fragmento de contenido.

Utilice el argumento mobile para definir si el botón se mostrará en los dispositivos móviles.

Por ejemplo, para agregar un botón de acción personalizado para la interfaz del dispositivo móvil:

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

1. Pase un argumento adicional en el objeto ConvConfig denominado actionButtons, que contiene una matriz de objetos que describen cada botón que desee agregar.
1. Defina una tecla para que se muestre el texto de cada botón.
1. Agregue una llamada de retorno que se invocará en un evento de clic para cada botón.

La llamada de retorno se invoca con un objeto con dos claves: `authorId` y `contentId`.
