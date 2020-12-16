---
description: El objeto AuthDelegate implementa el comportamiento deseado para realizar acciones y eventos de autenticación, de modo que puede personalizar la integración con el sistema de autenticación existente del sitio.
seo-description: El objeto AuthDelegate implementa el comportamiento deseado para realizar acciones y eventos de autenticación, de modo que puede personalizar la integración con el sistema de autenticación existente del sitio.
seo-title: AuthDelegate (objeto)
solution: Experience Manager
title: AuthDelegate (objeto)
uuid: a6acc4ef-d442-4782-9bfa-bbe494547c2e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# AuthDelegate (objeto){#authdelegate-object}

El objeto AuthDelegate implementa el comportamiento deseado para realizar acciones y eventos de autenticación, de modo que puede personalizar la integración con el sistema de autenticación existente del sitio.

## Creación de un delegado de autenticación {#section_wmn_tv2_gz}

El paquete de autenticación debe proporcionarse con un delegado de autenticación para poder realizar una acción. Un delegado de autenticación es cualquier objeto JavaScript que implementa uno de los métodos de este tema.

## .login(FinishLogin) {#section_mpk_lv2_gz}

Inicie sesión en un usuario válido e invoque la función FinishLogin con un objeto Error si se produce un error o con las credenciales de Livefyre del usuario. Las implementaciones comunes de este método redirigen al usuario a una página de inicio de sesión o abren una nueva ventana o modal.

En este ejemplo se notifica automáticamente a la autenticación de un usuario de Livefyre con el token de autenticación, token:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

El delegado de inicio de sesión más sencillo puede solicitar al usuario final su autentificador de Livefyre.

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

## .logout(FinishLogout) {#section_uqz_2v2_gz}

Cierre la sesión de un usuario e invoque la función endLogout con un objeto Error si se produjo un error o nulo para notificar a la autenticación que el cierre de sesión se realizó correctamente.

Por ejemplo:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

Realice acciones para la vista del perfil de un usuario.

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

Al implementar todos los métodos enumerados anteriormente, la autenticación se puede configurar con un delegado de autenticación personalizado. Una vez construido un delegado, se puede proporcionar a auth mediante el método delegate.

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

