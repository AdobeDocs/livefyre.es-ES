---
description: Use embed.ly para mostrar varios formatos multimedia directamente en la aplicación.
title: Integración con Embedly
exl-id: 859fe306-367e-4207-b9f7-c730ba0cd24d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 11%

---

# Integración con Embedly {#embedly-integration}

Utilice `embed.ly` para mostrar varios formatos multimedia directamente en la aplicación.

Para habilitar mejor el contenido de medios incrustados de una variedad de fuentes, incluidos Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify y Tumblr, las aplicaciones de Livefyre utilizan Embedly como proveedor de terceros para la expansión de URL. Si un usuario o moderador incluye un vínculo admitido en una publicación, los medios incluidos en el vínculo se ampliarán cuando se publiquen en la colección.

Esto proporciona a las aplicaciones Livefyre acceso a las más de 250 opciones de medios incrustados diferentes que admite Embedly.

>[!NOTE]
>
>Livefyre sólo expande un subconjunto de la lista completa de proveedores de Embedly. Las imágenes incrustadas se expandirán en páginas HTTPS solo si el proveedor es Twitter, YouTube, Imgur, Vine, Wikipedia o SoundCloud. Póngase en contacto con su administrador técnico de cuentas para cualquier otra pregunta sobre la expansión o las fuentes de los vínculos.

Esta página enumera ejemplos de algunos tipos de medios incrustados populares y sus patrones de URL aceptables. `Embed.ly` agrega continuamente nuevas fuentes. Para obtener una lista completa de proveedores, vaya a `https://embed.ly/embed/features/providers`.

>[!NOTE]
>
>El formato Embedly requiere un vínculo permanente completo. Los vínculos abreviados no funcionarán.

Solo se puede incrustar contenido visible públicamente. Si intenta incrustar un fragmento de contenido que no sea público, el vínculo al contenido aparecerá en la publicación del blog y lo acompañará un icono de marcador de posición. Cuando se hace clic, el vínculo lleva al lector a un mensaje de error del servicio en el que está alojado el contenido, como un mensaje de Facebook para una foto solo de amigos. Póngase en contacto con su administrador de cuentas si observa que los medios no se expanden según lo esperado.

## Ejemplo de URL con Embedly

| Tipo | Proveedor | Direcciones URL |
|--- |--- |--- |
| Mapas | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Nota**: La dirección URL debe comenzar por  `http` y no  `https.` |
| Redes sociales | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Vídeo | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Fotos | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Servicio de carga de contenido de Hootsuite) | `https://ow.ly/i/*` |
| Encuestas | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| Audio | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Blogs | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Aplicaciones que usan esta función:

* [Carrusel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Conversación](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Tarjeta de características](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro de los medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Encuestas](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Reseñas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Notas](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Tendencias](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Upload Button](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
