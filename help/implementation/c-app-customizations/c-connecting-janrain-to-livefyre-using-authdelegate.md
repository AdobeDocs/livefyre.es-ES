---
description: Livefyre. require proporciona un complemento que permite escuchar el
  bus de Janrain Backplane.
seo-description: Livefyre. require proporciona un complemento que permite escuchar
  el bus de Janrain Backplane.
seo-title: Conexión de Janrain a Livefyre mediante authdelegate
title: Conexión de Janrain a Livefyre mediante authdelegate
uuid: 9 d 56 e 3 f 4-960 a -4108-aab 5-2795 b 0 e 71 c 88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Conexión de Janrain a Livefyre mediante authdelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre. require proporciona un complemento que permite escuchar el bus de Janrain Backplane.

Cuando se retransmite un mensaje de identidad o inicio de sesión en el canal Backplane, se llamará a auth. authenticate () con el testigo de autenticación de Livefyre de usuario. Todavía debe implementar un authdelegate.

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
>El objeto window. Backplane debe definirse en la página antes de llamar a auth. plugin con el complemento de Livefyre Backplane. Para asegurarse de que el objeto Backflight está disponible, llame al código de instanciación de Livefyre desde una rellamada onready. Consulte el contacto de Janrain para determinar cuándo otras aplicaciones pueden utilizar el objeto Backflight.

A continuación se muestran algunos ejemplos de cómo un delegado de autenticación puede buscar una integración de Jrome Capture.

>[!NOTE]
>
>Su delegado de autenticación variará según la instancia de Janrain.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* La rellamada pasada al método de inicio de sesión de su delegado de autenticación.
* Referencia a la variable de captura de Janrain.
* : Referencia al objeto Backflight.

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

* **Finishcerrar:** La rellamada pasada al método de inicio de sesión de su delegado de autenticación.

* **window. Backplane:** Referencia al objeto Backflight.

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

Esto puede vincular a cualquier parte del sitio que desee que visiten los usuarios para ver su propia página de perfil. Este ejemplo simplemente imprime el objeto de autor pasado.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

Ver perfil

Al igual que Editar perfil, debe vincular a la página de un usuario diferente del usuario que ha iniciado sesión. Esto puede implementarse si se considera adecuado. Este ejemplo simplemente registra el parámetro del autor en la consola.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

