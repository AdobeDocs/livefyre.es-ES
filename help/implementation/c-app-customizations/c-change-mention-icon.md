---
description: Cambie el icono mostrado para los usuarios de Livefyre en el menú desplegable @mention.
seo-description: Cambie el icono mostrado para los usuarios de Livefyre en el menú desplegable @mention.
seo-title: Cambiar el icono @mention
solution: Experience Manager
title: Cambiar el icono @mention
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 31%

---


# Cambiar `@mention` icono {#change-mention-icon}

Cambie el icono que se muestra para los usuarios de Livefyre en el menú desplegable `@mention`.

Cambie el icono Livefyre utilizado en el menú desplegable `@mention` por un icono de su elección, permitiéndole indicar a los miembros de su comunidad con su propio icono.

## Ejemplo

Para cambiar este icono, agregue la CSS siguiente a la hoja de estilo. Reemplace &lt;*su recurso*> url por la dirección URL de la imagen seleccionada para reemplazar el distintivo predeterminado de Livefyre.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
