---
description: Cambie el icono mostrado para los usuarios de Livefyre en el menú desplegable @mention.
seo-description: Cambie el icono mostrado para los usuarios de Livefyre en el menú desplegable @mention.
seo-title: Cambiar el icono @mention
solution: Experience Manager
title: Cambiar el icono @mention
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# Cambiar `@mention` icono {#change-mention-icon}

Change the icon displayed for Livefyre users in the `@mention` pulldown menu.

Cambie el icono Livefyre utilizado en el menú `@mention` desplegable por un icono de su elección, lo que le permite indicar a los miembros de su comunidad con su propio icono.

## Ejemplo

Para cambiar este icono, agregue la CSS siguiente a la hoja de estilo. Reemplazar la dirección URL de &lt;*su recurso*&gt; por la dirección URL de la imagen seleccionada para reemplazar la marca de Livefyre predeterminada.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
