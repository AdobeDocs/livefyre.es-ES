---
description: El objeto authdelegate implementa el comportamiento deseado para realizar
  acciones de autenticación y eventos, a fin de personalizar la integración con el
  sistema de autenticación existente del sitio.
seo-description: El objeto authdelegate implementa el comportamiento deseado para
  realizar acciones de autenticación y eventos, a fin de personalizar la integración
  con el sistema de autenticación existente del sitio.
seo-title: Objeto authdelegate
solution: Experience Manager
title: Objeto authdelegate
uuid: a 6 acc 4 ef-d 442-4782-9 bfa-bbe 494547 c 2 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Objeto authdelegate{#authdelegate-object}

El objeto authdelegate implementa el comportamiento deseado para realizar acciones de autenticación y eventos, a fin de personalizar la integración con el sistema de autenticación existente del sitio.

## Creación de un delegado de autenticación {#section_wmn_tv2_gz}

El paquete de autenticación debe proporcionarse con un delegado de autenticación para poder realizar una acción. Un delegado de autenticación es cualquier objeto JavaScript que implemente uno de los métodos de este tema.

## . login (finishlogin) {#section_mpk_lv2_gz}

Inicie sesión en un usuario válido e invoque la función finishlogin con un objeto Error si se produjo un error o las credenciales de Livefyre del usuario. Las implementaciones comunes de este método redireccionan al usuario a una página de inicio de sesión o abren una nueva ventana o modal.

Este ejemplo notifica automáticamente a un usuario de Livefyre con el autentificador de autenticación, token:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

El delegado de inicio de sesión más sencillo puede preguntar al usuario final de su token de Autenticación de Livefyre.

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

## . cerrar sesión (finishlogout) {#section_uqz_2v2_gz}

Cierre la sesión de un usuario e invoque la función finishlogout con un objeto Error si hubo un error o nulo para notificar que la sesión se ha cerrado correctamente.

Por ejemplo:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## . Viewprofile (usuario) {#section_kkv_dv2_gz}

Tome medidas para ver el perfil de un usuario.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## . Editprofile (usuario) {#section_bkx_pq2_gz}

Tome medidas para editar el perfil de un usuario.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Al implementar todos los métodos enumerados arriba, la autenticación se puede configurar con un delegado de autenticación personalizado. Una vez construido el delegado, se puede proporcionar para autenticarlo usando el método delegado.

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

