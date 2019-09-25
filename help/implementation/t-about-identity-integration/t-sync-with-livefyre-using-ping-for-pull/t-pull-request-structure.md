---
description: Cree la estructura de solicitud de extracción para recibir y responder a las solicitudes de acceso al sistema de identidad de usuario.
seo-description: Cree la estructura de solicitud de extracción para recibir y responder a las solicitudes de acceso al sistema de identidad de usuario.
seo-title: Estructura de solicitud de extracción
solution: Experience Manager
title: Estructura de solicitud de extracción
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

---


# Estructura de solicitud de extracción{#pull-request-structure}

Cree la estructura de solicitud de extracción para recibir y responder a las solicitudes de acceso al sistema de identidad de usuario.

Livefyre envía una solicitud de extracción a la dirección URL del extremo.

Por ejemplo, si la dirección URL del extremo de extracción es:

```
https://example.yoursite.com/some_path/?id={id}
```

la solicitud de extracción de Livefyre a este extremo será:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

donde `lftoken` es un token web JSON firmado con la clave de red y **[!UICONTROL {userAuthToken}]** es el autentificador del usuario generado por Livefyre.

1. Utilice `lftoken` para validar que las solicitudes a la URL de extracción de Ping las envió Livefyre y no un agente malicioso.
1. Para todas las solicitudes entrantes:

   * Asegúrese de que la cadena de `lftoken` consulta está presente en la solicitud.
   * Utilice el `validateLivefyreToken` método de las bibliotecas de Livefyre para asegurarse de que `lftoken` se ha firmado con la clave de red.

   * Si no `lftoken` está presente o no se supera la validación, no permita que el punto final responda con la información del perfil. En su lugar, responda con un código de estado 403 (prohibido) y sin cuerpo de respuesta.

1. `userAuthToken` se genera mediante el `buildUserAuthToken` método Livefyre para el usuario, con el identificador de usuario "system". Este usuario es el primer usuario creado para cada nueva red.
