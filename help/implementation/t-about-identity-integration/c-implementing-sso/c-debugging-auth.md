---
description: Puede registrar a un usuario a través de la consola durante la integración
  y pruebas para depurar la autorización.
seo-description: Puede registrar a un usuario a través de la consola durante la integración
  y pruebas para depurar la autorización.
seo-title: Delegado de autenticación de depuración
solution: Experience Manager
title: Delegado de autenticación de depuración
uuid: fb 0 c 7396-190 e -4 dc 9-bf 26-23 dde 9 efd 45 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Delegado de autenticación de depuración{#debugging-auth-delegate}

Puede registrar a un usuario a través de la consola durante la integración y pruebas para depurar la autorización.

Inicie sesión en la consola mediante la consola siguiente `auth.authenticate` (token) y pase un testigo de usuario de Livefyre para autenticar a los usuarios de la página.

También puede modificar el ejemplo que se muestra arriba y agregar el siguiente fragmento en línea en JavaScript para registrar rápidamente un usuario en Livefyre (requiere una referencia a la autenticación).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

