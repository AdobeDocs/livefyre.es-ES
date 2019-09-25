---
description: Para autenticar a un usuario con Livefyre mediante un flujo no activado por una aplicación de Livefyre, Livefyre recomienda implementar el método forEachAuthentication en el objeto AuthDelegate.
seo-description: Para autenticar a un usuario con Livefyre mediante un flujo no activado por una aplicación de Livefyre, Livefyre recomienda implementar el método forEachAuthentication en el objeto AuthDelegate.
seo-title: Implementación de SSO
solution: Experience Manager
title: Implementación de SSO
uuid: c96d456c-b1ac-40e0-8d18-224652b9697f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Implementación de SSO{#implementing-sso}

Para autenticar a un usuario con Livefyre mediante un flujo no activado por una aplicación de Livefyre, Livefyre recomienda implementar el método forEachAuthentication en el objeto AuthDelegate.

Esto se invocará cuando se pase el `authDelegate` a `auth.delegate`, y se pasará una función de autenticación que se puede pasar varias veces. Este método proporciona una inversión del control para los eventos de autenticación, de modo que `AuthDelegateobject` puede ser independiente sin requerir una referencia global a la autenticación.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre depende de tokens de usuario para coordinar la autenticación. Como resultado, su servicio de identidad debe devolver este token para autenticar a un usuario con Livefyre. Para obtener información sobre cómo crear un token de usuario de Livefyre, consulte Creación de un autentificador de usuario.

>[!NOTE]
>
>Después de iniciar sesión correctamente, auth creará una sesión para el usuario e intentará cargar la sesión de un usuario tras actualizar y volver a cargar la página. `auth.logout()` borrará esta sesión. Esto significa que no es necesario administrar la sesión de un usuario independientemente de la autorización.

