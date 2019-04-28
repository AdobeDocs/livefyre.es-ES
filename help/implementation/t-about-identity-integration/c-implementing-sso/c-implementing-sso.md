---
description: Para autenticar a un usuario con Livefyre a través de un flujo no activado por una aplicación de Livefyre, Livefyre recomienda implementar el método foreachauthentication en el objeto authdelegate.
seo-description: Para autenticar a un usuario con Livefyre a través de un flujo no activado por una aplicación de Livefyre, Livefyre recomienda implementar el método foreachauthentication en el objeto authdelegate.
seo-title: Implementación de SSO
solution: Experience Manager
title: Implementación de SSO
uuid: c 96 d 456 c-b 1 ac -40 e 0-8 d 18-224652 b 9697 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Implementación de SSO{#implementing-sso}

Para autenticar a un usuario con Livefyre a través de un flujo no activado por una aplicación de Livefyre, Livefyre recomienda implementar el método foreachauthentication en el objeto authdelegate.

Se invocará cuando se pase el `authDelegate` valor `auth.delegate`y se pasará una función de autenticación que se puede pasar varias veces. Este método proporciona una inversión de control para los eventos de autenticación para que pueda `AuthDelegateobject` ser independiente sin requerir una referencia global a la autenticación.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre depende de tokens de usuario para coordinar la autenticación. Como resultado, el servicio de identidad debe devolver este token para autenticar a un usuario con Livefyre. Para aprender cómo crear un token de usuario de Livefyre, consulte Creación de un token de autenticación de usuario.

>[!NOTE]
>
>Después de iniciar sesión correctamente, la autenticación creará una sesión para el usuario e intentará cargar la sesión de un usuario al actualizar y recargar la página. `auth.logout()` borrará esta sesión. Esto significa que no es necesario gestionar la sesión de un usuario independientemente de la autorización.

