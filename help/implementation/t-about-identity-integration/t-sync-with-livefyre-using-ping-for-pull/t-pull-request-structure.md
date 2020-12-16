---
description: Cree la estructura de solicitud de extracción para recibir y responder a las solicitudes de acceso al sistema de identidad de usuario.
seo-description: Cree la estructura de solicitud de extracción para recibir y responder a las solicitudes de acceso al sistema de identidad de usuario.
seo-title: Estructura de solicitud de extracción
solution: Experience Manager
title: Estructura de solicitud de extracción
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

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

donde `lftoken` es un testigo Web JSON firmado con su clave de red y **[!UICONTROL {userAuthToken}]** es el autentificador del usuario generado por Livefyre.

1. Utilice `lftoken` para validar que las solicitudes de URL de extracción a su Ping fueron enviadas por Livefyre y no por un agente malicioso.
1. Para todas las solicitudes entrantes:

   * Asegúrese de que la cadena de consulta `lftoken` está presente en la solicitud.
   * Utilice el método `validateLivefyreToken` de las bibliotecas de Livefyre para asegurarse de que `lftoken` se haya firmado con la clave de red.

   * Si `lftoken` no está presente o falla en la validación, no permita que el punto final responda con información de perfil. En su lugar, responda con un código de estado 403 (prohibido) y sin cuerpo de respuesta.

1. `userAuthToken` se genera mediante el  `buildUserAuthToken` método Livefyre para el usuario, con el identificador de usuario &quot;system&quot;. Este usuario es el primer usuario creado para cada nueva red.
