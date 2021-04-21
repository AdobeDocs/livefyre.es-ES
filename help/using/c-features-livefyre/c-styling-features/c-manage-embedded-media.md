---
description: Defina las fuentes desde las que los usuarios pueden publicar los medios, y aquellas desde las que se prohibirán las publicaciones.
title: Administrar medios incrustados
exl-id: f0cc257b-cc82-47bc-9d42-6aef3e0fe8a7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Administrar medios incrustados{#manage-embedded-media}

Defina las fuentes desde las que los usuarios pueden publicar los medios, y aquellas desde las que se prohibirán las publicaciones.

De forma predeterminada, todos los archivos adjuntos de contenidos se pueden incrustar en los comentarios. Para obtener una lista completa de los proveedores admitidos, consulte embed.ly/providers.

Livefyre utiliza Embed.ly y los protocolos oEmbed estándar para incrustar medios en flujos de aplicaciones y pasará a través de todos los datos de medios proporcionados por su fuente.

Embed.ly pasará toda la información disponible, incluido el título, la descripción, la miniatura y el código incrustado del contenido para cualquier dirección URL proporcionada. La disponibilidad de estos artículos varía según el proveedor. Por ejemplo: Facebook no devuelve miniaturas de sus vídeos y solo pasa un vídeo incrustado. Al hacer clic en Reproducir se iniciará el vídeo (similar al formato de visualización de YouTube). Twitter solo pasa imágenes estáticas y no envía vídeos. Por lo tanto, es posible que los vídeos nativos de Twitter no se reproduzcan desde un flujo de Livefyre.

Puede evitar que ciertos archivos adjuntos se incrusten en los comentarios al incrustar el flujo de comentarios. También puede elegir ocultar todas las expansiones de Embed.ly en el nivel de red, sitio y conversación mediante Studio, mostrando solo los enlaces al medio, no los medios completamente incrustados.

Aplicaciones que usan esta función:

* [Tarjeta de características](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro de los medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
