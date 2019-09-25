---
description: Puede incluir el dominio de vídeo en la lista blanca mediante .
seo-description: Puede incluir el dominio de vídeo en la lista blanca mediante .
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Si utiliza sus propios vídeos y reproductores personalizados como parte de los vídeos que se muestran en una aplicación de visualización de Livefyre, puede incluir su dominio de vídeo en la lista blanca. Al agregar una lista blanca al dominio de vídeo, se elimina la máscara de vídeo de los reproductores y vídeos personalizados.

>[!NOTE]
>
>Utilice rutas específicas para asegurarse de que solo se incluyen en la lista blanca los vídeos que son seguros. Si pone una ruta amplia (por ejemplo, samprometomain.com), puede incluir en la lista de permitidos los vídeos no seguros.

* Agregar `userPrivacyVideoWhitelist` después `userPrivacyOptOut`. Puede agregar todos los indicadores de privacidad de Livefyre a la vez como parte de un objeto de Livefyre.
* `userPrivacyVideoWhitelist` solo se aplica al contenido que no está incrustado en los medios sociales.

En el ejemplo siguiente, se incluyen en la lista blanca los vídeos que se muestran en Aplicaciones con la `sampledomain.com/cdn/videos` ruta:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
