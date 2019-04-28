---
description: Los clientes que utilizan Janrain Capture y Backplane pueden utilizar la autenticación de Livefyre para el inicio de sesión único (SSO), lo que permite a los usuarios interactuar inmediatamente con las aplicaciones de Livefyre cuando inicien sesión en el sitio.
seo-description: Los clientes que utilizan Janrain Capture y Backplane pueden utilizar la autenticación de Livefyre para el inicio de sesión único (SSO), lo que permite a los usuarios interactuar inmediatamente con las aplicaciones de Livefyre cuando inicien sesión en el sitio.
seo-title: Janrain Capture/Backplane
solution: Experience Manager
title: Janrain Capture/Backplane
uuid: 776 e 9626-db 04-4 c 34-adfe -681 a 71 b 552 c 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain Capture/Backplane{#janrain-capture-backplane}

Los clientes que utilizan Janrain Capture y Backplane pueden utilizar la autenticación de Livefyre para el inicio de sesión único (SSO), lo que permite a los usuarios interactuar inmediatamente con las aplicaciones de Livefyre cuando inicien sesión en el sitio.

Para beneficiarse de esta integración integrada entre Captura y Plano, debe realizar cambios de configuración tanto en la aplicación Capture como en la integración de Livefyre. js.

>[!NOTE]
>
>Omita esta sección si no utiliza Janrain Capture.

Para obtener más información, consulte [la documentación de Backplane de Jrome](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Configure Captura.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Opcional) [Agregue valores predeterminados de Livefyre a la aplicación de captura](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Cree el objeto authdelegate.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Sincronice con Livefyre con Ping para la Extracción.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Paso 1: Configurar captura {#section_r2f_kxt_bbb}

Livefyre necesita ciertas credenciales a partir de su aplicación de Janrain Capture.

1. Configure la aplicación de Captación de Janrain.
1. Recopile la siguiente información para Livefyre:

   * Acceso a su instancia de Janrain Capture.
   * Acceso al tablero de Janrain Engage.
   * Ajustes y credenciales de captura.
   * Sus credenciales de participación.
   * Su URL de identidad.

>[!NOTE]
>
>Livefyre recibe datos directamente desde CNAME; Por lo tanto, esta URL de identidad no puede ser un registro CNAME (un CNAME de URL de vanidad) que responde al CNAME real de Janrain Capture.

## Paso 2: (Opcional) Agregue valores predeterminados de Livefyre a la aplicación de captura {#section_z2s_txt_bbb}

Agregue el valor predeterminado de Livefyre a los usuarios almacenados en su aplicación de captura para permitirle enviar notificaciones por correo electrónico de los usuarios o permitirles seguir automáticamente conversaciones sobre las que los usuarios hacen comentarios.

1. Complete [el paso 1: Configure Captura](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Agregue los campos predeterminados de Livefyre siguientes. Todos los campos son opcionales.

| Parámetro | Tipo | Descripción |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | Cadena | Notificar al usuario cuando alguien comenta en un artículo que está siguiendo. Puede ser inmediatamente, a menudo, o nunca. |
| **[!UICONTROL livefyre_likes]** | Cadena | Notificar al usuario cuando alguien le gusta uno de sus anuncios. Puede ser inmediatamente, a menudo, o nunca. |
| **[!UICONTROL livefyre_replies]** | Cadena | Notificar al usuario cuando alguien responde a uno de sus anuncios. Puede ser inmediatamente, con frecuencia o nunca. |
| **[!UICONTROL livefyre_moderator_comments]** | Cadena | Notificar al moderador cuando alguien comenta en una conversación que están moderando. Puede ser inmediatamente, a menudo, o nunca. |
| **[!UICONTROL livefyre_moderator_flags]** | Cadena | Notificar al moderador cuando alguien marca una publicación en una conversación que estén moderando. Puede ser inmediatamente, a menudo, o nunca. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Booleano | Haga que el usuario siga automáticamente una conversación cuando abandone un anuncio. Puede ser verdadero o falso. |

## Paso 3: Compilación del objeto authdelegate para la integración de Janrain {#section_asv_vyt_bbb}

Livefyre. require proporciona un complemento que permite escuchar el bus de Janrain Backplane.

### Inicio de sesión {#login}

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



>[!NOTE]
>
>Su delegado de autenticación variará según la instancia de Janrain.

A continuación se muestran algunos ejemplos de cómo un delegado de autenticación puede buscar una integración de Jrome Capture.

* `errback`: La rellamada pasada al método de inicio de sesión de su delegado de autenticación.
* `janrain`: Referencia a la variable de captura de Janrain.
* `window.Backplane`: Referencia al objeto Backflight.

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

* `finishLogout`: La rellamada pasada al método de inicio de sesión de su delegado de autenticación.

* `window.Backplane`: Referencia al objeto Backflight.

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

### Ver perfil {#viewprofile}

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

## Paso 4: Sincronizar con Livefyre con Ping para la obtención de integración de Janrain {#section_ilv_bzt_bbb}

Mantener sincronizados los perfiles remotos de Livefyre con el sistema de administración de usuarios Capture implica una serie de pasos referidos como Ping para Extract. Este proceso requiere que obtenga un token de acceso válido de Janrain y luego pase dicho token a un extremo especificado en el paso 3.

1. Obtenga un código de acceso de Janrain.

   Para obtener el código de acceso, proporcione las credenciales necesarias, especifique el usuario_ type como «usuario» y uuid como el uuid del usuario actual para actualizar. Para obtener más información, consulte [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Comercialice el código de acceso para un autentificador de acceso. Proporcione las credenciales necesarias, el código de acceso recibido del paso 1 y especifique el valor grant_ type como «permission_ code».

   Para obtener más información, consulte [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Presione el punto final «Ping to Pull Capture» de Livefyre.

   URL de extremo: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] donde ***{networkname}*** es el nombre de red proporcionado por Livefyre, y jrtoken es el testigo recibido de Janrain en el paso 2.

   Una vez que haya alcanzado este extremo, recibirá una respuesta 202 y Livefyre inicia un proceso asíncrono.

## Cómo funciona todo {#concept_mty_f31_2cb}

Para beneficiarse de esta integración integrada entre Captura y Plano, debe realizar algunos cambios de configuración tanto en la aplicación Capture como en la integración de Livefyre. js.

Janrain envía mensajes de inicio de sesión y cierre de sesión correctos a través del bus Backplane, en los que la aplicación de Livefyre, cuando se configura correctamente, escucha. Estos mensajes contienen toda la información necesaria para mostrar a los usuarios de la aplicación una sesión iniciada o cerrada. Los desarrolladores pueden ver mensajes de bus de Backplane inspeccionando la ficha Red en la consola de desarrollador del explorador.

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

Si estos mensajes no aparecen en las solicitudes de red, Livefyre no reconocerá los intentos de inicio de sesión o cierre de sesión y, por tanto, Livefyre no podrá integrar el usuario en la aplicación.
