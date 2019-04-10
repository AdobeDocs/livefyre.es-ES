---
description: Permita que los usuarios personalicen la imagen que se muestra con su
  contenido.
seo-description: Permita que los usuarios personalicen la imagen que se muestra con
  su contenido.
seo-title: Avatars
title: Avatars
uuid: bf 20 f 3 bc -3 dcc -4 e 16-a 629-3380 d 1 a 7 a 3 f 2
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Avatars{#avatars}

Permita que los usuarios personalicen la imagen que se muestra con su contenido.

Los avatares del usuario se muestran (de forma predeterminada) al lado del contenido de todas las aplicaciones y se extraen del sistema de perfiles de identidad utilizado en la implementación. Estas avatares varían según la aplicación en la que se muestran.

(Livefyre le permite deshabilitar Avatares si no desea mostrarlos en sus aplicaciones).

>[!NOTE]
>
>Las avatares se muestran a 25 p x 25 p para la conversación y 50 p x 50 p en la mayoría de las otras aplicaciones.

## Almacenamiento de avatar {#section_zbh_x1f_wy}

Las avatares se cargan asincrónicamente en Livefyre. Cuando un usuario inicia sesión por primera vez en la aplicación o cambia su archivo de imagen avatar asociado, su imagen de perfil se agrega a una cola de tareas. (Un avatar predeterminado se muestra temporalmente mientras el usuario se carga en la ubicación de almacenamiento de avatar de Livefyre).

## Gravatars {#section_mqh_p1f_wy}

Livefyre admite el uso de Gravatars. Si un usuario no tiene un avatar personalizado como parte de su perfil de usuario, Livefyre buscará un gravatar para ese usuario. Si no existe ningún gravatar, se utilizará el avatar predeterminado.

Si se han incorporado Comentarios mediante el complemento Livefyre WordPress, el Gravatar del usuario se utilizará si se cumplen las siguientes condiciones:

* Gravatar se activó en el panel de administración de WordPress y
* el usuario tiene una cuenta de Gravatar y
* no se proporciona un avatar personalizado.

Para obtener más información, consulte la documentación de Truatar de WordPress.



Aplicaciones que utilizan esta función:

* [Carrusel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Tarjeta de función](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro de medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Críticas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

