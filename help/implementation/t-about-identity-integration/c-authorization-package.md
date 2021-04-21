---
description: Instale el paquete de autenticación para habilitar la autenticación de usuarios y que los usuarios puedan interactuar con sus aplicaciones.
title: Paquete de autenticación
exl-id: 639032ee-ed7d-4cb0-83ba-f11d3dc607b6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# Paquete de autenticación{#authentication-package}

Instale el paquete de autenticación para habilitar la autenticación de usuarios y que los usuarios puedan interactuar con sus aplicaciones.

Las aplicaciones de Livefyre utilizan el paquete de autenticación global para asociar usuarios con acciones de aplicaciones. El paquete de autenticación está disponible a través de `Livefyre.require`.

Para habilitar la autenticación en la página, primero agregue `Livefyre.js` al elemento `<head>` de la página web o plantilla de sitio web.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

El uso de Livefyre.required para habilitar auth es similar a usar required para llamar a otros paquetes. El código de integración para requerir autenticación tiene este aspecto:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Métodos {#section_ojx_1lz_fz}

Una vez incluido como arriba utilizando `Livefyre.require`, el módulo Auth expone los siguientes métodos a los que puede llamar para notificar a otras aplicaciones de la página sobre eventos relacionados con la autenticación.

| Método | Descripción |
|--- |--- |
| `.login(callback)` | Déclencheur el flujo de inicio de sesión tal como lo implementa el AuthDelegate registrado. Por lo general, solo las aplicaciones habilitadas para la autenticación llamarán a esta página, y no a la propia página host. |
| `.logout(callback)` | Notifique a la autenticación que el usuario final ha cerrado la sesión por algún medio externo y que todas las aplicaciones de confianza deben borrar su estado de autenticación hasta el siguiente inicio de sesión. Esto borrará la sesión interna mantenida por Auth. |
| `.authenticate(credentials)` | Notifique a Auth que un usuario se ha autenticado por algún medio externo y se ha adquirido un token de autenticación de Livefyre para el usuario final. Utilícelo si establece una cookie con el token de Livefyre, o si tiene un token para el usuario y desea iniciar sesión explícitamente con el usuario. Por ejemplo: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delege los detalles de implementación de la autenticación (por ejemplo, el flujo de autenticación personalizado) en un objeto que defina. La página host debe llamar a esto para habilitar las funciones interactivas de las aplicaciones de Livefyre. |
