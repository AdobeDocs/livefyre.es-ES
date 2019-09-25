---
description: El recuento de oyentes es un contador que rastrea el número de visitantes de un sitio para una aplicación en una página y muestra este número.
seo-description: El recuento de oyentes es un contador que rastrea el número de visitantes de un sitio para una aplicación en una página y muestra este número.
seo-title: Recuento de escucha
solution: Experience Manager
title: Recuento de escucha
uuid: fdd7cfe4-ae69-4d31-baa2-8978368fc3e8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Recuento de escucha{#listener-count}

El recuento de oyentes es un contador que rastrea el número de visitantes de un sitio para una aplicación en una página y muestra este número.

Recuento de oyentes es el número de visitantes del sitio que tienen un explorador abierto a la página en la que se crea una instancia de una aplicación. Esto le permite saber cuántos visitantes del sitio están en la página en un momento dado, de modo que puede rastrearlos mientras ven el flujo o el contenido en directo en tiempo real.

El recuento de oyentes de Livefyre funciona así:

1. El sitio que contiene la aplicación envía un ping al servidor de Livefyre cada 60 segundos.
1. El servidor de Livefyre responde con el número de visitantes del sitio en la página que muestra la aplicación (definida como el número de visitantes del sitio con un explorador abierto a esa página).
1. El número de visitantes del sitio en la página con la aplicación se muestra en la aplicación.

Aplicaciones que utilizan esta función:

* [Conversación](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reseñas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatares de escucha {#section_wcn_kxp_vz}

El recuento de oyentes muestra un máximo de 10 avatares y solo muestra avatares para las personas que han hecho clic **[!UICONTROL Follow]** en la conversación.

>[!NOTE]
>
>Debido a limitaciones de espacio, la interfaz móvil muestra únicamente el número de oyentes y un pequeño icono de "personas".

El recuento de oyentes de Livefyre muestra el número de personas activas en la página en un momento determinado, además del número de personas que siguen la conversación. Si alguien está en la página y sigue la conversación, ese usuario no se contará dos veces. Por ejemplo, si un usuario está en una página y hace clic en ella **[!UICONTROL Follow]**, el recuento de oyentes no aumentará; si ese usuario hace clic **[!UICONTROL Unfollow]**, el recuento no disminuirá.

Aplicaciones que utilizan esta función:

* [Conversación](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reseñas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)

