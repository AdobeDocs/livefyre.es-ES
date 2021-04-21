---
description: Para autenticar a un usuario con Livefyre a través de un flujo que no se active mediante una aplicación Livefyre, Livefyre recomienda implementar el método foreachAuthentication en el objeto AuthDelegate .
title: Implementación de SSO
exl-id: 9af75b8a-9d2a-446e-8cce-2de8645038f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Implementación de SSO{#implementing-sso}

Para autenticar a un usuario con Livefyre a través de un flujo que no se active mediante una aplicación Livefyre, Livefyre recomienda implementar el método foreachAuthentication en el objeto AuthDelegate .

Esto se invocará cuando el `authDelegate` se pase a `auth.delegate` y se pasará una función de autenticación que se puede pasar varias veces. Este método proporciona una inversión del control para los eventos de autenticación, de modo que su `AuthDelegateobject` puede ser independiente sin requerir una referencia global a auth.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre depende de tokens de usuario para coordinar la autenticación. Como resultado, el servicio de identidad debe devolver este token para autenticar a un usuario con Livefyre. Para obtener información sobre cómo crear un token de usuario de Livefyre, consulte Creación de un token de autenticación de usuario.

>[!NOTE]
>
>Después de un inicio de sesión correcto, auth creará una sesión para el usuario e intentará cargar una sesión del usuario tras actualizar y volver a cargar la página. `auth.logout()` borrará esta sesión. Esto significa que no es necesario administrar la sesión de un usuario independientemente de la autorización.
