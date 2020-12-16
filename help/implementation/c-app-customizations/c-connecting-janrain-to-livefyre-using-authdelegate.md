---
description: Livefyre.required proporciona un complemento que permite a la autenticación escuchar el bus Janrain Backplane.
seo-description: Livefyre.required proporciona un complemento que permite a la autenticación escuchar el bus Janrain Backplane.
seo-title: Conexión de Janrain a Livefyre mediante AuthDelegate
title: Conexión de Janrain a Livefyre mediante AuthDelegate
uuid: 9d56e3f4-960a-4108-aab5-2795b0e71c88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 1%

---


# Conexión de Janrain a Livefyre mediante AuthDelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre.required proporciona un complemento que permite a la autenticación escuchar el bus Janrain Backplane.

Cuando se retransmite un mensaje de inicio de sesión o identidad en el canal Backplane, se le llamará auth.authentication() con el autentificador Livefyre del usuario. Aún debe implementar un AuthDelegate.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>El objeto window.Backplane debe definirse en la página antes de llamar a auth.plugin con el complemento Livefyre Backplane. Para asegurarse de que el objeto Plano posterior está disponible, llame al código de creación de instancias de Livefyre desde una llamada de retorno onReady. Consulte con el contacto de Janrain para determinar cuándo otras aplicaciones pueden utilizar el objeto de plano posterior.

A continuación se muestran algunos ejemplos de cómo un delegado de autenticación puede buscar una integración de captura de Janrain.

>[!NOTE]
>
>El delegado de autenticación variará según la instancia de Janrain.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* La llamada de retorno pasada al método de inicio de sesión del delegado de autenticación
* La referencia a la variable de captura de Janrain.
* :: Referencia al objeto Plano posterior.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

Cerrar sesión

* **endLogout:** la devolución de llamada pasada al método de inicio de sesión del delegado de autenticación.

* **window.Backplane:** Una referencia al objeto de plano posterior.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

Editar perfil

Esto puede vincularse a cualquier parte del sitio que desee que visiten los usuarios para vista de su propia página de perfil. Este ejemplo simplemente imprime el objeto de autor que se ha pasado.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

Perfil de vista

Al igual que Editar Perfil, esto debe vincularse a una página de usuario distinta de la del usuario que ha iniciado sesión en ese momento. Esto se puede implementar según lo que considere necesario. Este ejemplo simplemente registra el parámetro author en la consola.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

