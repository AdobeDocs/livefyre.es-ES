---
description: Elimine los componentes estándar de la aplicación Livefyre de su aplicación.
title: Ocultar elementos de aplicación
exl-id: f8bbed2c-d009-41b8-927d-8d6ac4a63571
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# Ocultar elementos de aplicación{#hide-app-elements}

Elimine los componentes estándar de la aplicación Livefyre de su aplicación.

Utilice CSS para ocultar los elementos predeterminados de la aplicación Livefyre de su página, lo que le permite personalizar la experiencia del usuario para adaptarla a sus necesidades.

Para ocultar elementos de la aplicación, simplemente configure display en none.

Ejemplos:

```
/* Hide the 'reply' button */ 
.fyre-comment-reply { 
    display: none !important; 
} 
  
/* Hide all user avatars */ 
.fyre-comment-user .fyre-mention-item-avatar .fyre-listener-avatars .fyre-avatar fyre-user-avatar-25 { 
    display: none !important; 
} 
.fyre-comment-head .fyre-comment-body .fyre-comment-footer .fyre-comment-divider { 
    margin-left: 0; 
} 
  
/* Hide 'Edit Profile' link */ 
.fyre-edit-profile-link { 
    display: none !important; 
} 
  
/* Hide 'Logout' link */ 
.fyre-logout-link { 
    display: none; 
} 
  
/* Hide 'Comment Notifier' */ 
.fyre-notifier-message { 
    display:none; 
}
```
