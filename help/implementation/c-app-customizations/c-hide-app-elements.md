---
description: Elimine los componentes estándar de la aplicación Livefyre.
seo-description: Elimine los componentes estándar de la aplicación Livefyre.
seo-title: Ocultar elementos de la aplicación
solution: Experience Manager
title: Ocultar elementos de la aplicación
uuid: ea090b6e-99f5-4bd7-aa9e-d39a4dff1543
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Ocultar elementos de la aplicación{#hide-app-elements}

Elimine los componentes estándar de la aplicación Livefyre.

Utilice CSS para ocultar los elementos predeterminados de la aplicación Livefyre de la página, lo que le permite personalizar la experiencia del usuario para adaptarla a sus necesidades.

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

