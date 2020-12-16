---
description: Cree el ping para que la página ping Livefyre cuando los usuarios actualicen su perfil.
seo-description: Cree el ping para que la página ping Livefyre cuando los usuarios actualicen su perfil.
seo-title: Construir el ping
solution: Experience Manager
title: Construir el ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Genere el ping{#build-the-ping}

Cree el ping para que la página ping Livefyre cuando los usuarios actualicen su perfil.

Cuando Livefyre recibe una notificación de actualización con las `networkName` y `user_id`, el sistema enviará una solicitud de extracción a la dirección URL de extracción de Ping.

>[!NOTE]
>
>403/No autorizado en respuesta a su ping indica un `lftoken` no válido anexado a la solicitud de ping. Asegúrese de que `lftoken` es para `user_id` con privilegios de propietario de red o para el usuario del sistema. Si utiliza bibliotecas de Livefyre, utilice el método `buildLivefyreToken` para generar un token de sistema válido para la solicitud.

1. Añada código a la página que llame a Livefyre cuando los usuarios actualicen su perfil. Construya la dirección URL de esta manera:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** El nombre de red proporcionado por Livefyre.
   * **[!UICONTROL user_id:]** ID del usuario.
   * **[!UICONTROL token:]** Distintivo válido del sistema.

1. Extraiga la estructura de la solicitud.
