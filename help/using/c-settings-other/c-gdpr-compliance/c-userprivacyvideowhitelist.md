---
description: Puede incluir en la lista de permitidos su dominio de vídeo.
title: userPrivacyVideoWhitelist
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Si utiliza sus propios vídeos y reproductores personalizados como parte de los vídeos que se muestran en una aplicación de visualización de Livefyre, puede incluir en la lista de permitidos su dominio de vídeo. Al permitir que aparezca el dominio de vídeo, se elimina la máscara de vídeo de los reproductores y vídeos personalizados.

>[!NOTE]
>
>Utilice rutas específicas para asegurarse de que solo están permitidos los vídeos que son seguros. Si pone una ruta amplia (por ejemplo, samprometomain.com), puede incluir en la lista de permitidos vídeos no seguros.

* Agregue `userPrivacyVideoWhitelist` después de `userPrivacyOptOut`. Puede agregar todos los indicadores de privacidad de Livefyre a la vez como parte de un objeto Livefyre.
* `userPrivacyVideoWhitelist` solo se aplica al contenido que no está incrustado en los medios sociales.

En el siguiente ejemplo, los vídeos que se muestran en Aplicaciones con la ruta `sampledomain.com/cdn/videos` están permitidos:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
