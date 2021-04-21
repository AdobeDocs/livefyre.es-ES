---
description: Cree la estructura de solicitud de extracción para recibir y responder a solicitudes de acceso a su sistema de identidad de usuario.
title: Estructura de solicitud de extracción
exl-id: 70203b23-9d7c-4a22-94ba-2a763e200972
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Estructura de solicitud de extracción{#pull-request-structure}

Cree la estructura de solicitud de extracción para recibir y responder a solicitudes de acceso a su sistema de identidad de usuario.

Livefyre envía una solicitud de extracción a la dirección URL del extremo.

Por ejemplo, si la URL del extremo de extracción es:

```
https://example.yoursite.com/some_path/?id={id}
```

la solicitud de extracción de Livefyre a este extremo será:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

donde `lftoken` es un token web JSON firmado con su clave de red y **[!UICONTROL {userAuthToken}]** es el token de autenticación de usuario generado por Livefyre.

1. Utilice `lftoken` para validar que las solicitudes a su Ping para URL de extracción fueron enviadas por Livefyre y no por un agente malicioso.
1. Para todas las solicitudes entrantes:

   * Asegúrese de que la cadena de consulta `lftoken` esté presente en la solicitud.
   * Utilice el método `validateLivefyreToken` de las bibliotecas de Livefyre para asegurarse de que `lftoken` se haya firmado con la clave de red.

   * Si `lftoken` no está presente o falla en la validación, no permita que el punto final responda con información de perfil. En su lugar, responda con un código de estado 403 (prohibido) y sin cuerpo de respuesta.

1. `userAuthToken` se genera mediante el  `buildUserAuthToken` método Livefyre para el usuario, con el id de usuario &quot;system&quot;. Este usuario es el primer usuario creado para cada nueva red.
