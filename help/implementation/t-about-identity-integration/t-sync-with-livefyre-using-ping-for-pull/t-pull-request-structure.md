---
description: Cree la estructura de solicitud de extracción para recibir y responder
  a las solicitudes de acceso a su sistema de identidad de usuario.
seo-description: Cree la estructura de solicitud de extracción para recibir y responder
  a las solicitudes de acceso a su sistema de identidad de usuario.
seo-title: Estructura de solicitud de extracción
solution: Experience Manager
title: Estructura de solicitud de extracción
uuid: bf 6 b 9 e 45-d 08 a -48 e 6-acc 6-e 4 fa 56428 d 25
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Estructura de solicitud de extracción{#pull-request-structure}

Cree la estructura de solicitud de extracción para recibir y responder a las solicitudes de acceso a su sistema de identidad de usuario.

Livefyre emite una solicitud de extracción a la URL de extremo.

Por ejemplo, si la URL de extremo de extracción es:

```
https://example.yoursite.com/some_path/?id={id}
```

La solicitud de salto de Livefyre a este punto final será:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

donde `lftoken` es un token web JSON firmado con la clave de red y **[!UICONTROL {userAuthToken}]** es el autentificador de usuario generado por Livefyre.

1. Se utiliza `lftoken` para validar que Livefyre envió las solicitudes al ping para obtener URL de extracción y no un agente malicioso.
1. Para todas las solicitudes entrantes:

   * Asegúrese de que la cadena `lftoken` de consulta está presente en la solicitud.
   * Utilice `validateLivefyreToken` el método de las bibliotecas de Livefyre para asegurarse de `lftoken` que se firma con su clave de red.

   * Si `lftoken` no está presente, o si falla la validación, no permita que el punto final responda con la información de perfil. En su lugar, responda con un código de estado 403 (prohibido) y sin cuerpo de respuesta.

1. `userAuthToken` la genera el `buildUserAuthToken` método Livefyre para el usuario, con el ID de usuario «sistema». Este usuario es el primer usuario creado para cada nueva red.
1. Para probar la página, utilice [el tester Ping para extraer](https://livefyre-p4p-wizard.herokuapp.com/home) para confirmar que todo funciona correctamente.
