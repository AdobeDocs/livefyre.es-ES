---
description: Cambie el icono mostrado para los usuarios de Livefyre en el menú desplegable
  @mention.
seo-description: Cambie el icono mostrado para los usuarios de Livefyre en el menú
  desplegable @mention.
seo-title: Cambiar el icono @mention
solution: Experience Manager
title: Cambiar el icono @mention
uuid: a 395 f 4 ff-a 774-454 a -8 d 94-4 a 3371 d 8 cc 2 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Cambiar `@mention` icono {#change-mention-icon}

Cambie el icono mostrado para los usuarios de Livefyre en el menú `@mention` desplegable.

Cambie el icono de Livefyre utilizado en el menú `@mention` desplegable por un icono de su elección, permitiéndole indicar a los miembros de su comunidad su propio icono.

## Ejemplo

Para cambiar este icono, agregue la siguiente CSS a su hoja de estilo. Sustituya <*su recurso*> url por la URL de la imagen seleccionada para reemplazar la insignia predeterminada Livefyre.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
