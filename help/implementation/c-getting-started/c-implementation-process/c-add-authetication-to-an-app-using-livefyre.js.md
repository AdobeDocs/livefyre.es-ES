---
description: Use Livefyre.js para agregar autenticación de toda la página para sus aplicaciones de Livefyre.
seo-description: Use Livefyre.js para agregar autenticación de toda la página para sus aplicaciones de Livefyre.
seo-title: Agregar autenticación a una aplicación mediante Livefyre.js
solution: Experience Manager
title: Agregar autenticación a una aplicación mediante Livefyre.js
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# Agregar autenticación a una aplicación mediante Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Use Livefyre.js para agregar autenticación de toda la página para sus aplicaciones de Livefyre.

`Livefyre.js Aut`h es un paquete JavaScript desarrollado por Livefyre que permite que todas las aplicaciones de su sitio web compartan una única integración de autenticación. La autenticación le permite definir cómo deben registrarse los usuarios, iniciar sesión y cerrar sesión delegando estos flujos en un objeto AuthDelegate que defina.

## Paso 1: Habilitar la autenticación para una página {#section_pgp_jtt_bbb}

Utilícelo `Livefyre.js` para habilitar la autenticación en una página y permitir que los usuarios inicien sesión e interactúen con las aplicaciones mediante el sistema de autenticación existente.

1. Para habilitar la autenticación en una página, agregue `Livefyre.js` al elemento *&lt;head&gt;* de la página web o plantilla de sitio web.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Se utiliza `Livefyre.require` para habilitar la autenticación. El uso `Livefyre.require` es similar a utilizar la función requerir para llamar a otros paquetes. El código de integración para requerir autenticación tiene este aspecto:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Paso 2: Registrar un delegado automático {#section_oqm_15t_bbb}

Para habilitar la autenticación, cree un `AuthDelegate` y pase a `Livefyre.js` Authentication.

Un `AuthDelegate` es un objeto que define que determina cómo iniciarán sesión los usuarios, cerrarán la sesión y verán los perfiles.

1. Cree un `AuthDelegate`. La forma en que construye un `AuthDelegate` depende del proveedor de identidad. Consulte Integración de identidades para obtener instrucciones más detalladas.

1. Pasa el `AuthDelegate` a `Livefyre.js` Autenticación. El usuario más sencillo `AuthDelegate` registra al mismo usuario cada vez que un usuario activa el método de inicio de sesión delegado desde una aplicación:

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## Paso 3: Sincronizar datos de usuario {#section_u4m_j5t_bbb}

Sincronice la información de perfil de usuario entre Livefyre y su proveedor de identidad.

Debe sincronizar la información de perfil de usuario entre Livefyre y su proveedor de identidad. Para obtener más información, consulte Integración [de captura de](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)Janrain.
