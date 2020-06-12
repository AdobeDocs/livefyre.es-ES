---
description: Puede permitir la lista del dominio de vídeo.
seo-description: Puede permitir la lista del dominio de vídeo.
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Si utiliza sus propios vídeos y reproductores personalizados como parte de los vídeos que se muestran en una aplicación de visualización de Livefyre, puede permitir la lista del dominio de vídeo. Al permitir que se muestre el dominio de vídeo, se elimina la máscara de vídeo de los vídeos y reproductores personalizados.

>[!NOTE]
>
>Utilice rutas específicas para asegurarse de que solo los vídeos seguros están permitidos. Si pone una ruta amplia (por ejemplo, samprometomain.com), puede permitir la lista de videos no seguros.

* Añadir `userPrivacyVideoWhitelist` después `userPrivacyOptOut`. Puede agregar todos los indicadores de privacidad de Livefyre a la vez como parte de un objeto de Livefyre.
* `userPrivacyVideoWhitelist` solo se aplica al contenido que no está incrustado en los medios sociales.

En el siguiente ejemplo, se permiten los vídeos que se muestran en Aplicaciones con la `sampledomain.com/cdn/videos` ruta:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
