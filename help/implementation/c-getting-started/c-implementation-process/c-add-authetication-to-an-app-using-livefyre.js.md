---
description: Use Livefyre.js para agregar autenticación de toda la página para sus aplicaciones de Livefyre.
title: Agregar autenticación a una aplicación mediante Livefyre.js
exl-id: 6246a2bc-e7ff-4f86-a63a-36261c71d460
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Agregar autenticación a una aplicación mediante Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Use Livefyre.js para agregar autenticación de toda la página para sus aplicaciones de Livefyre.

`Livefyre.js Aut`h es un paquete JavaScript desarrollado por Livefyre que permite que todas las aplicaciones de su sitio web compartan una sola integración de autenticación. La autenticación permite definir cómo deben registrarse, iniciar sesión y cerrar sesión los usuarios delegando estos flujos en un objeto AuthDelegate que usted defina.

## Paso 1: Habilitar la autenticación para una página {#section_pgp_jtt_bbb}

Utilice `Livefyre.js` para habilitar la autenticación de una página y permitir a los usuarios iniciar sesión e interactuar con las aplicaciones mediante el sistema de autenticación existente.

1. Para habilitar la autenticación en una página, agregue `Livefyre.js` al elemento *&lt;head>* de la página web o la plantilla del sitio web.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Utilice `Livefyre.require` para habilitar la autenticación. El uso de `Livefyre.require` es similar a usar la requiere para llamar a otros paquetes. El código de integración para requerir autenticación tiene este aspecto:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Paso 2: Registrar un AuthDelegate {#section_oqm_15t_bbb}

Para habilitar la autenticación, cree un `AuthDelegate` y páselo a la autenticación `Livefyre.js`.

Un `AuthDelegate` es un objeto que define y que determina cómo los usuarios iniciarán sesión, cerrarán la sesión y verán los perfiles.

1. Cree un `AuthDelegate`. La forma de construir un `AuthDelegate` depende de su proveedor de identidad. Consulte Integración de identidad para obtener instrucciones más detalladas.

1. Pase la `AuthDelegate` a la autenticación `Livefyre.js`. El `AuthDelegate` más sencillo inicia sesión del mismo usuario cada vez que un usuario activa el método de inicio de sesión delegado desde una aplicación:

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

Debe sincronizar la información de perfil de usuario entre Livefyre y su proveedor de identidad. Para obtener más información, consulte [Integración de captura de Janrain](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
