---
description: Cree el ping para que su página pings Livefyre cuando los usuarios actualicen su perfil.
title: Construya el ping
exl-id: 626c200b-eaff-483f-b1eb-7d8993fe5e7c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Generar el Ping{#build-the-ping}

Cree el ping para que su página pings Livefyre cuando los usuarios actualicen su perfil.

Cuando Livefyre recibe una notificación de actualización con `networkName` y `user_id`, el sistema enviará una solicitud de extracción a su Ping para obtener la URL de extracción.

>[!NOTE]
>
>403/No autorizado en respuesta a su Ping indica un `lftoken` no válido anexado a la solicitud Ping. Asegúrese de que `lftoken` es para un `user_id` con privilegios de propietario de red o para el usuario del sistema. Si utiliza bibliotecas de Livefyre, utilice el método `buildLivefyreToken` para generar un token de sistema válido para la solicitud.

1. Agregue código a la página que pings Livefyre cuando los usuarios actualicen su perfil. Construya la URL de esta manera:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Su Livefyre ha proporcionado el nombre de red.
   * **[!UICONTROL user_id:]** El ID de su usuario.
   * **[!UICONTROL token:]** Token válido del sistema.

1. Extraiga la estructura de la solicitud.
