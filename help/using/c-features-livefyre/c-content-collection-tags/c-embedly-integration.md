---
description: Use embed.ly para mostrar varios formatos multimedia directamente en
  la aplicación.
seo-description: Use embed.ly para mostrar varios formatos multimedia directamente
  en la aplicación.
seo-title: Integración con Embedly
solution: Experience Manager
title: Integración con Embedly
uuid: 1 f 27 e 32 c-c 2 c 3-4 f 7 c -93 de-c 9 c 7 bf 783 d 6 a
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Integración con Embedly{#embedly-integration}

Utilice `embed.ly` para mostrar varios formatos de medios directamente en la aplicación.

Para permitir mejor el contenido de medios incrustados desde una variedad de fuentes, incluso Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify y Tumblr, las aplicaciones de Livefyre utilizan Embtly como proveedor externo para la expansión de URL. Si un usuario o moderador incluye un vínculo admitido en una publicación, los medios incluidos en el vínculo se expandirán cuando se anuncien en la colección.

Esto proporciona aplicaciones de Livefyre con acceso a las más de 250 opciones de medios incrustados que admite Enfáticamente.

>[!NOTE]
>
>Livefyre expande solo un subconjunto de la lista de proveedores completa de Enbely. Las imágenes incrustadas se expanden en páginas HTTPS solo si el proveedor es Twitter, YouTube, Imgur, Enredur, Wikipedia o soundcloud. Póngase en contacto con su administrador de cuentas técnico para obtener más preguntas sobre la expansión o las fuentes de vínculos.

Esta página enumera algunos ejemplos de tipos de medios incorporados populares y sus patrones de URL aceptables. `Embed.ly` está agregando nuevas fuentes constantemente. Para obtener una lista completa de los proveedores, vaya `https://embed.ly/embed/features/providers`a.

>[!NOTE]
>
>El formato Encadenado requiere una longitud permanente completa. Los vínculos abreviados no funcionarán.

Solo se puede incrustar contenido públicamente visible. Si intenta incrustar un contenido que no sea público, el vínculo al contenido aparecerá en la publicación del blog y un icono de marcador de posición lo acompañará. Cuando se haga clic en él, el vínculo llevará al lector a un mensaje de error del servicio donde está alojado el contenido, como un mensaje de Facebook para una foto de solo amigos. Comuníquese con el administrador de cuentas si observa que los medios no se expanden según lo esperado.

## URL de muestra de muestra

| Tipo | Proveedor | URL |
|--- |--- |--- |
| Mapas | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Nota**: La dirección URL debe `http` comenzar con `https.` |
| Redes sociales | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Vídeo | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Fotos | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | Twitpic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Servicio de carga de contenido de Hootsuite) | `https://ow.ly/i/*` |
| Encuestas | Gopollgo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| Audio | Soundcloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Blogs | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Aplicaciones que utilizan esta función:

* [Carrusel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Tarjeta de función](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro de medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Encuestas](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Críticas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Tendencias](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Upload Button](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

