---
description: Defina las fuentes desde las cuales los usuarios pueden publicar los medios, y aquellas desde las que se prohibirán los anuncios de medios.
seo-description: Defina las fuentes desde las cuales los usuarios pueden publicar los medios, y aquellas desde las que se prohibirán los anuncios de medios.
seo-title: Administrar medios incrustados
title: Administrar medios incrustados
uuid: d8621be1-dcfb-429f-954e-b21fdcf02715
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Administrar medios incrustados{#manage-embedded-media}

Defina las fuentes desde las cuales los usuarios pueden publicar los medios, y aquellas desde las que se prohibirán los anuncios de medios.

De forma predeterminada, todos los archivos adjuntos de medios se pueden incrustar en los comentarios. Para obtener una lista completa de proveedores admitidos, consulte embed.ly/providers.

Livefyre utiliza los protocolos Embed.ly y oEmbed estándar para incrustar medios en los flujos de aplicaciones y pasará por todos los datos de medios proporcionados por su origen.

Embed.ly pasará toda la información disponible, incluido el título del medio, la descripción, la miniatura y el código incrustado de cualquier dirección URL proporcionada. La disponibilidad de estos elementos varía según el proveedor. Por ejemplo: Facebook no devuelve miniaturas de sus vídeos y solo pasa un vídeo incrustado. Al hacer clic en Reproducir se iniciará el vídeo (similar al formato de visualización de YouTube). Twitter solo pasa imágenes estáticas y no envía vídeos. Por lo tanto, es posible que los vídeos nativos de Twitter no se reproduzcan desde un flujo de Livefyre.

Puede evitar que ciertos archivos adjuntos se incrusten en comentarios al incrustar el flujo de comentarios. También puede elegir ocultar todas las expansiones de Embed.ly en el nivel de red, sitio y conversación mediante Studio, mostrando solo los vínculos a los medios, no los medios completamente incrustados.

Aplicaciones que utilizan esta función:

* [Tarjeta de función](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro de los medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)

