---
description: Use Livefyre.js para agregar autenticación de toda la página para sus aplicaciones de Livefyre.
seo-description: Use Livefyre.js para agregar autenticación de toda la página para sus aplicaciones de Livefyre.
seo-title: Añadir autenticación en una aplicación mediante Livefyre.js
solution: Experience Manager
title: Añadir autenticación en una aplicación mediante Livefyre.js
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# Añadir la autenticación en una aplicación mediante Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Use Livefyre.js para agregar autenticación de toda la página para sus aplicaciones de Livefyre.

`Livefyre.js Aut`h es un paquete JavaScript desarrollado por Livefyre que permite que todas las aplicaciones de su sitio web compartan una única integración de autenticación. La autenticación le permite definir cómo deben registrarse los usuarios, iniciar sesión y cerrar sesión delegando estos flujos en un objeto AuthDelegate que defina.

## Paso 1: Habilitar la autenticación para una página {#section_pgp_jtt_bbb}

Utilice `Livefyre.js` para habilitar la autenticación de una página a fin de permitir que los usuarios inicien sesión e interactúen con las aplicaciones mediante el sistema de autenticación existente.

1. Para habilitar la autenticación en una página, agregue `Livefyre.js` al elemento *&lt;head>* de la página Web o plantilla de sitio Web.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Utilice `Livefyre.require` para habilitar la autenticación. El uso de `Livefyre.require` es similar al de requerir llamar a otros paquetes. El código de integración para requerir autenticación tiene este aspecto:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Paso 2: Registrar un AuthDelegate {#section_oqm_15t_bbb}

Para habilitar la autenticación, cree una `AuthDelegate` y pásela a `Livefyre.js` Autenticación.

Un `AuthDelegate` es un objeto que usted define que determina cómo los usuarios iniciarán sesión, cerrarán sesión y vistas de perfiles.

1. Cree un `AuthDelegate`. La forma en que construya un `AuthDelegate` depende de su proveedor de identidad. Consulte Integración de identidades para obtener instrucciones más detalladas.

1. Pase la `AuthDelegate` a la autenticación `Livefyre.js`. El `AuthDelegate` más sencillo registra al mismo usuario cada vez que un usuario activa el método de inicio de sesión delegado desde una aplicación:

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

Sincronice la información de perfil del usuario entre Livefyre y su proveedor de identidad.

Debe sincronizar la información de perfil de usuario entre Livefyre y su proveedor de identidad. Para obtener más información, consulte [Integración de captura de Janrain](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
