---
description: Permite a los usuarios personalizar la imagen que se muestra con su contenido.
seo-description: Permite a los usuarios personalizar la imagen que se muestra con su contenido.
seo-title: Avatares
title: Avatares
uuid: bf20f3bc-3dcc-4e16-a629-3380d1a7a3f2
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---


# Avatars{#avatars}

Permite a los usuarios personalizar la imagen que se muestra con su contenido.

Los avatares del usuario se muestran (de forma predeterminada) junto al contenido en todas las aplicaciones y se extraen del sistema de perfil de identidad utilizado en la implementación. Estos avatares varían en tamaño, según la aplicación en la que se muestran.

(Livefyre le permite desactivar los avatares si no desea mostrarlos en sus aplicaciones).

>[!NOTE]
>
>Los avatares se muestran en 25p x 25p para chat y 50p x 50p en la mayoría de las demás aplicaciones.

## Almacenamiento de avatar {#section_zbh_x1f_wy}

Los avatares se cargan asincrónicamente en Livefyre. Cuando un usuario inicia sesión por primera vez en la aplicación o cambia su archivo de imagen de avatar asociado, su imagen de perfil se agrega a una cola de tareas. (Un avatar predeterminado se muestra temporalmente mientras el del usuario se carga en la ubicación del almacenamiento de avatar de Livefyre).

## Gravatars {#section_mqh_p1f_wy}

Livefyre apoya el uso de Gravatars. Si un usuario no tiene un avatar personalizado como parte de su perfil de usuario, Livefyre buscará un Gravatar para ese usuario. Si no existe ningún Gravatar, se utilizará el avatar predeterminado.


Aplicaciones que utilizan esta función:

* [Carrusel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Conversación](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Tarjeta de función](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro de los medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Reseñas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

