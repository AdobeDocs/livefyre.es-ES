---
description: Puede iniciar sesión a través de la consola durante la integración y la prueba para depurar la autorización.
seo-description: Puede iniciar sesión a través de la consola durante la integración y la prueba para depurar la autorización.
seo-title: Delegado de autenticación de depuración
solution: Experience Manager
title: Delegado de autenticación de depuración
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Delegado de autenticación de depuración{#debugging-auth-delegate}

Puede iniciar sesión a través de la consola durante la integración y la prueba para depurar la autorización.

Inicie sesión en la consola con el siguiente `auth.authenticate` (token) y pase un token de usuario de Livefyre para autenticar a los usuarios de la página.

También puede modificar el ejemplo que se muestra arriba y agregar el siguiente fragmento en línea en su JavaScript para iniciar sesión rápidamente en Livefyre (requiere una referencia a auth).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

