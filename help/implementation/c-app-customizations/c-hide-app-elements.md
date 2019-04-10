---
description: Elimine los componentes estándar de la aplicación Livefyre de su aplicación.
seo-description: Elimine los componentes estándar de la aplicación Livefyre de su
  aplicación.
seo-title: Ocultar elementos de aplicación
solution: Experience Manager
title: Ocultar elementos de aplicación
uuid: ea 090 b 6 e -99 f 5-4 bd 7-aa 9 e-d 39 a 4 dff 1543
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Ocultar elementos de aplicación{#hide-app-elements}

Elimine los componentes estándar de la aplicación Livefyre de su aplicación.

Utilice CSS para ocultar elementos predeterminados de la aplicación Livefyre de su página, lo que le permite personalizar la experiencia del usuario para adaptarla a sus necesidades.

Para ocultar elementos de la aplicación, simplemente establezca la pantalla en ninguno.

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

