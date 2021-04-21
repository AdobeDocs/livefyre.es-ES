---
description: El objeto AuthDelegate implementa el comportamiento deseado para realizar acciones y eventos de autenticación de modo que pueda personalizar la integración con el sistema de autenticación existente en el sitio.
title: Objeto AuthDelegate
exl-id: 7c669138-627e-476e-a177-c71346f730df
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# AuthDelegate (objeto){#authdelegate-object}

El objeto AuthDelegate implementa el comportamiento deseado para realizar acciones y eventos de autenticación de modo que pueda personalizar la integración con el sistema de autenticación existente en el sitio.

## Creación de un delegado de autenticación {#section_wmn_tv2_gz}

El paquete de autenticación debe proporcionarse con un delegado de autenticación para poder realizar una acción. Un delegado de autenticación es cualquier objeto JavaScript que implementa uno de los métodos de este tema.

## .login(finishLogin) {#section_mpk_lv2_gz}

Inicie sesión en un usuario válido e invoque la función finishLogin con un objeto Error si se ha producido un error o con las credenciales de Livefyre del usuario. Las implementaciones comunes de este método redirigen al usuario a una página de inicio de sesión o abren una nueva ventana o modal.

En este ejemplo se notifica automáticamente a la autenticación de un usuario de Livefyre con el token de autenticación, token:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

El delegado de inicio de sesión más sencillo puede preguntar al usuario final su token de autenticación de Livefyre.

```
authDelegate.login = function contrivedLogin(finishLogin) { 
  var lfToken = prompt("Please type your Livefyre Token");  
  if (lfToken.length === 0) { 
   return finishLogin(new Error("User failed to type their lftoken")); 
  }  
 finishLogin(null, { 
   livefyre: lfToken 
 }); 
};
```

## .logout(finishLogout) {#section_uqz_2v2_gz}

Cierre la sesión de un usuario e invoque la función finishLogout con un objeto Error si se ha producido un error o nulo para notificar a la autenticación que el cierre de sesión se ha realizado correctamente.

Por ejemplo:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

Realice una acción para ver el perfil de un usuario.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(user) {#section_bkx_pq2_gz}

Realice acciones para editar el perfil de un usuario.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Al implementar todos los métodos enumerados anteriormente, la autenticación se puede configurar con un delegado de autenticación personalizado. Una vez construido un delegado, se puede proporcionar a auth mediante el método delegado.

```
var authDelegate = { 
 login: function(cb) { 
  ... 
  cb(null); 
 }, 
 ... 
} 
  
auth.delegate(authDelegate);
```
