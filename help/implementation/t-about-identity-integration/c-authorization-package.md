---
description: Instale el paquete de autenticación para habilitar la autenticación de usuarios para que los usuarios puedan interactuar con sus aplicaciones.
seo-description: Instale el paquete de autenticación para habilitar la autenticación de usuarios para que los usuarios puedan interactuar con sus aplicaciones.
seo-title: Paquete de autenticación
solution: Experience Manager
title: Paquete de autenticación
uuid: 4 eec 30 cf -66 b 6-408 d -985 d -3 e 23 b 8 b 70 d 01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Paquete de autenticación{#authentication-package}

Instale el paquete de autenticación para habilitar la autenticación de usuarios para que los usuarios puedan interactuar con sus aplicaciones.

Las aplicaciones de Livefyre utilizan el paquete de autenticación global para asociar usuarios con acciones de aplicación. El paquete de autenticación está disponible `Livefyre.require`.

Para habilitar la autenticación en la página, primero agregue `Livefyre.js` al `<head>` elemento de su página Web o plantilla de sitio Web.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

Utilizar Livefyre. requiere activar la autenticación es similar a utilizar para llamar a otros paquetes. El código de integración para requerir la autenticación tiene este aspecto:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Métodos {#section_ojx_1lz_fz}

Una vez que se incluye como arriba, `Livefyre.require`el módulo Auth expone los siguientes métodos que puede llamar para notificar a otras aplicaciones de la página acerca de los eventos relacionados con la autenticación.

| Método | Descripción |
|--- |--- |
| `.login(callback)` | Active el flujo de inicio de sesión tal como implementa authdelegate registrado. Normalmente, solo las aplicaciones habilitadas por autenticación se llamarán this, y no la propia página de host. |
| `.logout(callback)` | Notificar la autenticación que el usuario final ha cerrado por algunos medios externos y que todas las aplicaciones que confía deben borrar su estado de autenticación hasta el siguiente inicio de sesión. Esto borrará la sesión interna mantenida por Auth. |
| `.authenticate(credentials)` | Notifique a la autenticación que un usuario se ha autenticado por algunos medios externos y se ha adquirido un autentificador de autenticación de Livefyre para el usuario final. Utilice esta opción si establece una cookie con el token de Livefyre o si tiene un token para el usuario y desea registrar explícitamente al usuario. Por ejemplo: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delegar los detalles de implementación de la autenticación (por ejemplo, su flujo de autenticación personalizado) en un objeto que usted defina. La página host debe llamar a esto para habilitar las funciones interactivas de las aplicaciones de Livefyre. |

