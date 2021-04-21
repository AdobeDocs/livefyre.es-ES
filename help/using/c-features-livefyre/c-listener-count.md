---
description: El recuento de oyentes es un contador que realiza el seguimiento del número de visitantes de un sitio para una aplicación en una página y muestra este número.
title: Recuento de oyentes
exl-id: a07e83c2-7465-42ec-9d24-821aac5ab74b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---

# Recuento de oyentes{#listener-count}

El recuento de oyentes es un contador que realiza el seguimiento del número de visitantes de un sitio para una aplicación en una página y muestra este número.

Recuento de oyentes es el número de visitantes del sitio que tienen un explorador abierto a la página en la que se crea una instancia de una aplicación. Esto le permite saber cuántos visitantes del sitio están en la página en un momento dado, de modo que pueda realizar un seguimiento mientras ven el flujo continuo o el contenido en directo en tiempo real.

El recuento de oyentes de Livefyre funciona de esta manera:

1. El sitio que contiene la aplicación envía un ping a un servidor de Livefyre cada 60 segundos.
1. El servidor de Livefyre responde con el número de visitantes del sitio en la página que muestra la aplicación (definido como el número de visitantes del sitio con un explorador abierto a esa página).
1. El número de visitantes del sitio en la página con la aplicación se muestra en la aplicación.

Aplicaciones que usan esta función:

* [Conversación](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reseñas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatares de escucha {#section_wcn_kxp_vz}

El recuento de oyentes muestra un máximo de 10 avatares y solo muestra avatares para las personas que han hecho clic **[!UICONTROL Follow]** en la conversación.

>[!NOTE]
>
>Debido a limitaciones de espacio, la interfaz móvil muestra solo el número de oyentes y un pequeño icono de &quot;personas&quot;.

El recuento de oyentes de Livefyre muestra el número de personas que participan activamente en la página en un momento determinado, además del número de personas que siguen la conversación. Si alguien está en la página y sigue la conversación, ese usuario no se contará dos veces. Por ejemplo, si un usuario está en una página y hace clic **[!UICONTROL Follow]**, el recuento de oyentes no aumentará; si ese usuario hace clic en **[!UICONTROL Unfollow]**, el recuento no disminuye.

Aplicaciones que usan esta función:

* [Conversación](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reseñas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)
