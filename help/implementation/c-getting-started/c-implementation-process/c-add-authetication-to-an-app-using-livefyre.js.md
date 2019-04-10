---
description: Utilice Livefyre. js para agregar autenticación en toda la página de
  sus aplicaciones de Livefyre.
seo-description: Utilice Livefyre. js para agregar autenticación en toda la página
  de sus aplicaciones de Livefyre.
seo-title: Agregar autenticación a una aplicación con Livefyre. js
solution: Experience Manager
title: Agregar autenticación a una aplicación con Livefyre. js
uuid: b 7 c 61 e 07-e 341-45 d 7-9112-c 50155 e 38 f 1 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Agregar autenticación a una aplicación con Livefyre. js{#add-authetication-to-an-app-using-livefyre-js}

Utilice Livefyre. js para agregar autenticación en toda la página de sus aplicaciones de Livefyre.

`Livefyre.js Aut`h es un paquete JavaScript desarrollado por Livefyre que permite que todas las aplicaciones del sitio web compartan una única integración de autenticación. Auth permite definir cómo deben registrarse los usuarios, iniciar sesión y cerrar sesión delegando estos flujos en un objeto authdelegate que usted defina.

## Paso 1: Habilitar la autenticación para una página {#section_pgp_jtt_bbb}

Utilice `Livefyre.js` para habilitar la autenticación para una página a fin de permitir que los usuarios inicien sesión e interactúen con Aplicaciones usando el sistema de autenticación existente.

1. Para habilitar la autenticación en una página, agregue `Livefyre.js` al elemento *< head >* de su página web o plantilla de sitio web.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Se utiliza `Livefyre.require` para habilitar la autenticación. El uso `Livefyre.require` es parecido a utilizar para llamar a otros paquetes. El código de integración para requerir la autenticación tiene este aspecto:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Paso 2: Registro de un authdelegate {#section_oqm_15t_bbb}

Para habilitar la autenticación, cree un `AuthDelegate` y páselo a `Livefyre.js` Autenticación.

Un `AuthDelegate` es un objeto que se define que determina cómo los usuarios iniciarán sesión, cierran sesión y verán perfiles.

1. Cree `AuthDelegate`un. La manera de construir una `AuthDelegate` depende del proveedor de identidad. Consulte Integración de identidad para obtener instrucciones más detalladas.

1. Pase `AuthDelegate` a `Livefyre.js` Autenticación. El mismo usuario `AuthDelegate` registra el mismo usuario en cada vez que un usuario activó el método de inicio de sesión delegado desde una aplicación:

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

Sincronice la información de perfil de usuario entre Livefyre y el proveedor de identidad.

Debe sincronizar su información de perfil de usuario entre Livefyre y su proveedor de identidad. Para obtener más información, consulte [Integración de JPS Capture](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
