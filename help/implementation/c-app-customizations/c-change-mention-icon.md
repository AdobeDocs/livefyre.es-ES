---
description: Cambie el icono mostrado para los usuarios de Livefyre en el menú desplegable @mention.
title: Cambiar el icono @mention
exl-id: e078ef7f-7f16-4f5d-9152-95ae7fe7e4bd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 19%

---

# Cambiar `@mention` Icono {#change-mention-icon}

Cambie el icono mostrado para los usuarios de Livefyre en el menú desplegable `@mention`.

Cambie el icono de Livefyre utilizado en el menú desplegable `@mention` por un icono de su elección, lo que le permite indicar a los miembros de su comunidad con su propio icono.

## Ejemplo

Para cambiar este icono, agregue la CSS siguiente a la hoja de estilo. Reemplace la dirección url &lt;*del recurso*> por la URL de la imagen seleccionada para reemplazar el distintivo predeterminado de Livefyre.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
