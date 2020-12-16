---
description: Instale el paquete de autenticación para habilitar la autenticación de usuarios y que los usuarios puedan interactuar con sus aplicaciones.
seo-description: Instale el paquete de autenticación para habilitar la autenticación de usuarios y que los usuarios puedan interactuar con sus aplicaciones.
seo-title: Paquete de autenticación
solution: Experience Manager
title: Paquete de autenticación
uuid: 4eec30cf-66b6-408d-985d-3e23b8b70d01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---


# Paquete de autenticación{#authentication-package}

Instale el paquete de autenticación para habilitar la autenticación de usuarios y que los usuarios puedan interactuar con sus aplicaciones.

Las aplicaciones de Livefyre utilizan el paquete de autenticación global para asociar usuarios con acciones de la aplicación. El paquete de autenticación está disponible a través de `Livefyre.require`.

Para habilitar la autenticación en la página, primero agregue `Livefyre.js` al elemento `<head>` de la página Web o plantilla de sitio Web.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

El uso de Livefyre.required para habilitar auth es similar al uso de required para llamar a otros paquetes. El código de integración para requerir autenticación tiene este aspecto:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Métodos {#section_ojx_1lz_fz}

Una vez incluido como se indica arriba mediante `Livefyre.require`, el módulo Auth expone los siguientes métodos que puede utilizar para notificar a otras aplicaciones de la página sobre eventos relacionados con la autenticación.

| Método | Descripción |
|--- |--- |
| `.login(callback)` | Active el flujo de inicio de sesión tal como lo implementa AuthDelegate registrado. Normalmente, solo las aplicaciones habilitadas para la autenticación llamarán a esto y no a la página de host en sí. |
| `.logout(callback)` | Notifique a la autenticación que el usuario final ha cerrado la sesión por algún medio externo y que todas las aplicaciones de confianza deben borrar su estado de autenticación hasta el siguiente inicio de sesión. Esto borrará la sesión interna mantenida por Auth. |
| `.authenticate(credentials)` | Notifique a Auth que un usuario se ha autenticado por algún medio externo y que se ha adquirido un autentificador de Livefyre para el usuario final. Utilícelo si establece una cookie con el token de Livefyre o tiene un token para el usuario y desea iniciar sesión explícitamente al usuario. Por ejemplo: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delegar los detalles de implementación de la autenticación (por ejemplo, el flujo de autenticación personalizado) en un objeto que usted defina. La página de host debe llamar a esto para habilitar las funciones interactivas de las aplicaciones de Livefyre. |

