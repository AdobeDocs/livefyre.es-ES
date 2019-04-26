---
description: Genere el ping para que sus pings de página sean Livefyre cuando los
  usuarios actualicen su perfil.
seo-description: Genere el ping para que sus pings de página sean Livefyre cuando
  los usuarios actualicen su perfil.
seo-title: Generar el ping
solution: Experience Manager
title: Generar el ping
uuid: cb 8 cc 043-9 ea 5-407 c-b 70 f -3 f 1 e 37 accdae
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Generar el ping{#build-the-ping}

Genere el ping para que sus pings de página sean Livefyre cuando los usuarios actualicen su perfil.

Cuando Livefyre reciba una notificación de actualización con y `networkName``user_id`, el sistema enviará una solicitud Pull al ping para obtener URL de extracción.

>[!NOTE]
>
>403/No autorizado en respuesta al ping indica un anexo no válido `lftoken` a la solicitud Ping. Asegúrese de `lftoken` que sea para los privilegios `user_id` de propietario de red o para el usuario del sistema. Si utiliza bibliotecas de Livefyre, utilice `buildLivefyreToken` el método para generar un token de sistema válido para la solicitud.

1. Agregue código a la página que pings Livefyre cuando los usuarios actualicen su perfil. Cree la URL de esta manera:

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** Su Livefyre ha proporcionado el nombre de la red.
* **[!UICONTROL user_id:]** El ID del usuario.
* **[!UICONTROL token:]** Token válido del sistema.

1. Extraiga la estructura de la solicitud.
