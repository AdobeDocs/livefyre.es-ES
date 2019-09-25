---
description: Cree el ping para que la página ping Livefyre cuando los usuarios actualicen su perfil.
seo-description: Cree el ping para que la página ping Livefyre cuando los usuarios actualicen su perfil.
seo-title: Construir el ping
solution: Experience Manager
title: Construir el ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Construir el ping{#build-the-ping}

Cree el ping para que la página ping Livefyre cuando los usuarios actualicen su perfil.

Cuando Livefyre reciba una notificación de actualización con el `networkName` y `user_id`, el sistema enviará una solicitud de extracción a su Ping para URL de extracción.

>[!NOTE]
>
>403/No autorizado en respuesta a su ping indica que se ha agregado un valor no válido `lftoken` a la solicitud de ping. Asegúrese de que `lftoken` es para un usuario `user_id` con privilegios de propietario de red o del sistema. Si utiliza bibliotecas de Livefyre, utilice el `buildLivefyreToken` método para generar un token de sistema válido para la solicitud.

1. Agregue código a la página que ping Livefyre cuando los usuarios actualicen su perfil. Construya la dirección URL de esta manera:

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** El nombre de red proporcionado por Livefyre.
* **[!UICONTROL user_id:]** ID del usuario.
* **[!UICONTROL token:]** Distintivo válido del sistema.

1. Extraiga la estructura de la solicitud.
