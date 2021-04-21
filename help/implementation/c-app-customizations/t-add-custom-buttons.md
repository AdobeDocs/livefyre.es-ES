---
description: Agregue acciones personalizadas a sus aplicaciones de Livefyre.
title: Agregar botones personalizados
exl-id: a62d8605-59c2-4214-af26-805c1989aca1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# Agregar botones personalizados{#add-custom-buttons}

Agregue acciones personalizadas a sus aplicaciones de Livefyre.

Livefyre permite agregar botones personalizados junto a los botones de acción existentes (como **[!UICONTROL Share]** y **[!UICONTROL Flag]**) en un fragmento de contenido.

Utilice el argumento mobile para definir si el botón se mostrará en los dispositivos móviles.

Por ejemplo, para agregar un botón de acción personalizado a la interfaz del dispositivo móvil:

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

1. Pase un argumento adicional en el objeto ConvConfig denominado actionButton, que contenga una matriz de objetos que describa cada botón que desee añadir.
1. Defina una clave para el texto que se mostrará en cada botón.
1. Agregue una llamada de retorno que se invoque en un evento de clic para cada botón.

La rellamada se invoca con un objeto con dos claves: `authorId` y `contentId`.
