---
description: Puede agregar su dominio de vídeo a la lista de direcciones permitidas.
seo-description: Puede agregar su dominio de vídeo a la lista de direcciones permitidas.
seo-title: Userprivacyvideowhitelist
solution: Experience Manager
title: Userprivacyvideowhitelist
uuid: adfead 18-b 73 b -4 ac 4-97 a 0-d 39 f 528 b 7606
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacyvideowhitelist{#userprivacyvideowhitelist}

Si utiliza sus propios vídeos y reproductores personalizados como parte de los vídeos que se muestran en una aplicación de visualización de Livefyre, puede incluir su dominio de vídeo en la lista de direcciones permitidas. La lista blanca de su dominio de vídeo elimina la máscara de vídeo de los reproductores y vídeos personalizados.

>[!NOTE]
>
>Utilice rutas específicas para asegurarse de que solo los vídeos seguros están en la lista de direcciones permitidas. Si coloca una ruta amplia (por ejemplo, sampledomain.com), puede incluir vídeos no seguros.

* Agregue `userPrivacyVideoWhitelist` después `userPrivacyOptOut`. Puede agregar todos los indicadores de privacidad de Livefyre a la vez como parte de un objeto Livefyre.
* `userPrivacyVideoWhitelist` solo se aplica al contenido que no está incrustado en los medios sociales.

En el ejemplo siguiente, los vídeos que se muestran en Aplicaciones con `sampledomain.com/cdn/videos` la ruta están en la lista de direcciones permitidas:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
