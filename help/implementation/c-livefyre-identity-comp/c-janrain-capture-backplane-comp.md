---
description: Los clientes que utilizan Janrain Capture y Backplane pueden utilizar Livefyre Auth para el inicio de sesión único (SSO), lo que permite a los usuarios interactuar inmediatamente con sus aplicaciones de Livefyre cuando inician sesión en el sitio.
title: Captura de Janrain/Retroplano
exl-id: c7e6cfef-7570-4f9c-9d2c-79f890ee5c49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 1%

---

# Captura/plano posterior de Janrain{#janrain-capture-backplane}

Los clientes que utilizan Janrain Capture y Backplane pueden utilizar Livefyre Auth para el inicio de sesión único (SSO), lo que permite a los usuarios interactuar inmediatamente con sus aplicaciones de Livefyre cuando inician sesión en el sitio.

Para beneficiarse de esta integración integrada de Captura/Retroplano, debe realizar cambios de configuración tanto en la aplicación de Captura como en la integración de Livefyre.js.

>[!NOTE]
>
>Omita esta sección si no utiliza Janrain Capture.

Para obtener más información, consulte [Documentación del plano posterior de Janrain](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Configure la captura.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Opcional) [Agregue los valores predeterminados de Livefyre a su aplicación de captura](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Genere el objeto AuthDelegate .](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Sincronizar con Livefyre con Ping para extracción.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Paso 1: Configurar captura {#section_r2f_kxt_bbb}

Livefyre necesita ciertas credenciales de su aplicación de captura de Janrain.

1. Configure la aplicación de captura de Janrain.
1. Recopile la siguiente información para Livefyre:

   * Acceso a la instancia de captura de Janrain.
   * Acceda a su tablero de Janrain Engage.
   * La configuración y las credenciales de captura.
   * Sus credenciales de participación.
   * Su URL de identidad.

>[!NOTE]
>
>Livefyre recibe datos directamente desde el CNAME; por lo tanto, esta URL de identidad no puede ser un registro CNAMEd (un CNAME de URL de vanidad) que se resuelva en el CNAME real de la captura de Janrain.

## Paso 2: (Opcional) Añada los valores predeterminados de Livefyre a la aplicación de captura {#section_z2s_txt_bbb}

Agregue los valores predeterminados de Livefyre a los usuarios almacenados en la aplicación de captura para permitirles enviar notificaciones por correo electrónico a los usuarios o permitirles seguir automáticamente las conversaciones en las que los usuarios comentan.

1. Complete [Paso 1: Configure la captura](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Agregue los siguientes campos predeterminados de Livefyre. Todos los campos son opcionales.

| Parámetro | Tipo | Descripción |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | Cadena | Notifique al usuario cuando alguien comenta sobre un artículo que esté siguiendo. Puede ser inmediata, a menudo o nunca. |
| **[!UICONTROL livefyre_likes]** | Cadena | Notifique al usuario cuando le guste una de sus publicaciones. Puede ser inmediata, a menudo o nunca. |
| **[!UICONTROL livefyre_replies]** | Cadena | Notifique al usuario cuando alguien responda a una de sus publicaciones. Puede ser inmediata, a menudo o nunca. |
| **[!UICONTROL livefyre_moderator_comments]** | Cadena | Notifique al moderador cuando alguien comente sobre una conversación que está moderando. Puede ser inmediata, a menudo o nunca. |
| **[!UICONTROL livefyre_moderator_flags]** | Cadena | Notifique al moderador cuando alguien marca una publicación en una conversación que está moderando. Puede ser inmediata, a menudo o nunca. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Booleano | Haga que el usuario siga automáticamente una conversación cuando salga de una publicación. Puede ser verdadero o falso. |

## Paso 3: Generar el objeto AuthDelegate para la integración con Janrain {#section_asv_vyt_bbb}

Livefyre.required proporciona un plugin que permite a auth escuchar el bus Janrain Backplane.

### Inicio de sesión {#login}

Cuando se emite un mensaje de identidad/inicio de sesión en el canal del plano posterior, se llamará a auth.authentication() con el token de autenticación de Livefyre del usuario. Aún debe implementar un AuthDelegate.

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
>El objeto window.Backplane debe definirse en la página antes de llamar a auth.plugin con el complemento Retroplano de Livefyre. Para asegurarse de que el objeto Plano posterior está disponible, llame al código de creación de instancias de Livefyre desde una llamada de retorno onReady . Consulte con su contacto de Janrain para determinar cuándo otras aplicaciones pueden utilizar el objeto de plano posterior.



>[!NOTE]
>
>El delegado de autenticación variará según la instancia de Janrain.

A continuación se muestran algunos ejemplos de cómo un delegado de autenticación puede buscar una integración de captura de Janrain.

* `errback`: La llamada de retorno transferida al método de inicio de sesión del delegado de autenticación
* `janrain`: La referencia a la variable de captura de Janrain.
* `window.Backplane`: Referencia al objeto Plano posterior.

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

### Cerrar sesión {#logout}

* `finishLogout`: La rellamada se pasó al método de inicio de sesión del delegado de autenticación.

* `window.Backplane`: Referencia al objeto Plano posterior.

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

### Editar perfil {#editprofile}

Esto puede vincular cualquier parte del sitio que desee que visiten los usuarios para ver su propia página de perfil. Este ejemplo simplemente imprime el objeto de autor transferido.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

### Ver perfil {#viewprofile}

Al igual que Editar perfil, esto debe vincular a una página de usuario que sea diferente a la del usuario que ha iniciado sesión en ese momento. Esto se puede implementar como sea necesario. En este ejemplo, simplemente se registra el parámetro de autor en la consola.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## Paso 4: Sincronizar con Livefyre con Ping para extracción para integración con Janrain {#section_ilv_bzt_bbb}

Mantener los Perfiles remotos de Livefyre sincronizados con su sistema de administración de usuarios de Capture implica una serie de pasos denominados Ping for Pull. Este proceso requiere que obtenga un token de acceso válido de Janrain y que pase dicho token a un punto final especificado en el paso 3, a continuación.

1. Obtenga un código de acceso de Janrain.

   Para obtener el código de acceso, proporcione las credenciales necesarias, especifique user_type como &quot;user&quot; y uuid como el uuid del usuario actual que desea actualizar. Para obtener más información, consulte [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Comercie el código de acceso para un token de acceso. Proporcione las credenciales necesarias, el código de acceso recibido desde el paso 1 y especifique el elemento grant_type como &quot;authorization_code&quot;.

   Para obtener más información, consulte [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Pulse el punto final &quot;Ping to Pull Capture&quot; de Livefyre.

   Dirección URL del extremo: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] donde ***{networkName}*** es el nombre de red que le proporciona Livefyre, y jrtoken es el token recibido de Janrain en el paso 2.

   Una vez que llegue a este punto final, recibirá una respuesta de 202 y Livefyre comenzará un proceso asíncrono.

## Cómo funciona todo {#concept_mty_f31_2cb}

Para beneficiarse de esta integración integrada de Captura/Retroplano, debe realizar algunos cambios de configuración tanto en la aplicación de Captura como en la integración de Livefyre.js.

Janrain envía mensajes de inicio/cierre de sesión correctos a través del bus Backplane, en el que la aplicación Livefyre, cuando está configurada correctamente, escucha. Estos mensajes contienen toda la información necesaria para mostrar a los usuarios de la aplicación con la sesión iniciada o finalizada. Los desarrolladores pueden ver los mensajes de bus Backplane inspeccionando la pestaña Red (Network) en la consola para desarrolladores del navegador.

## Ejemplo de código de inicio de sesión {#section_ftt_tvp_mz}

Solicitud:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

Respuesta:

```
Backplane.response([{ 
  "id": "2014-05-06T22:51:55.406Z-eZp1HB1F7B", 
  "channel_name": "{CHANNEL_NAME}", 
  "message": { 
    "source": "https://{CUSTOMER_DOMAIN}", 
    "type": "identity/login", 
    "sticky": true, 
    "payload": { 
      "context": "https://{CUSTOMER_DOMAIN}", 
      "identities": { 
        "startIndex": 0, 
        "itemsPerPage": 1, 
        "totalResults": 1, 
        "entry": { 
          "id": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
          "displayName": "{USER_DISPLAY_NAME}", 
          "accounts": [ 
            { 
              "username": "{USER_DISPLAY_NAME}", 
              "identityUrl": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
              "photos": [ 
                { 
                  "id": 48570146, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "other" 
                }, 
                { 
                  "id": 48570147, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "original" 
                }, 
                { 
                  "id": 48570148, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "large" 
                }, 
                { 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "avatar" 
                } 
              ] 
            }, 
            { 
              "identityUrl": "{USER_PROFILE_LINK}" 
            } 
          ] 
        } 
      } 
    } 
  } 
} 
]);
```

Respuesta vacía:

```
Backplane.response([]);
```

## Ejemplo de código de cierre de sesión {#section_t52_svp_mz}

Solicitud:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

Respuesta:

```
Backplane.finishInit("{CHANNEL}");
```

Si estos mensajes no aparecen en las solicitudes de red, Livefyre no tendrá en cuenta los intentos de inicio/cierre de sesión y, por lo tanto, Livefyre no podrá integrar al usuario en la aplicación.
