---
description: Utilice las API de Livefyre para añadir funcionalidad de Google AMP a
  la página de Storify 2 para mantener el contenido interactivo y SEO.
seo-description: Utilice las API de Livefyre para añadir funcionalidad de Google AMP
  a la página de Storify 2 para mantener el contenido interactivo y SEO.
seo-title: Utilizar Google AMP con Storify 2
solution: Experience Manager
title: Utilizar Google AMP con Storify 2
uuid: 40 c 9 f 083-7284-43 ba-ae 27-53 b 1 ff 9 e 3954
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Utilizar Google AMP con Storify 2{#use-google-amp-with-storify}

Utilice las API de Livefyre para añadir funcionalidad de Google AMP a la página de Storify 2 para mantener el contenido interactivo y SEO.

Para utilizar Google AMP con Storify 2, debe crear una página para la aplicación Storify 2 con Google AMP.

La versión de AMP de la aplicación solicita actualizaciones desde la página original (utilice el parámetro **pollinterval** en la API **de amp-live-list** para establecer el intervalo para las solicitudes de actualización). Para asegurarse de que los visitantes de la página AMP obtienen el contenido más actualizado rápidamente, mantenga un TTL de baja caché en las páginas de Storify 2 AMP.

Los recursos que no son de imagen (por ejemplo, vídeos) incluidos como anuncios en una aplicación Storify 2 deben utilizar HTTPS como especifica la especificación AMP. Las URL de AMP que utilizan la red de entrega de contenido de Google Cloud (CDN) usan HTTPS.

Para utilizar Google AMP con Storify 2:

1. Cree una plantilla validada por AMP en el sitio.
1. Utilice una o varias de las siguientes API de Google AMP para personalizar su página de Google AMP:
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) para personalizar la visualización de Storify 2
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) para personalizar el intervalo de tiempo de las actualizaciones
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) para agregar un botón de uso compartido en redes sociales
1. Incluya el contenido de la siguiente página Storify 2 AMP en la CSS para la página Storify 2 dentro de la <style amp-custom> tag: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Incluya el contenido de la siguiente API de marcado Storify 2 AMP en la plantilla de Google AMP: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` donde {{APP_ ID}} es el ID de la aplicación para la aplicación Storify 2 en Livefyre Studio.
   1. El único parámetro de consulta es **pollinterval**, que es el intervalo en el que la aplicación buscará actualizaciones (configurada en milisegundos).
   1. La dirección URL incluye contenido de los anuncios más recientes (incluidos tweets, videos, etc.)
   1. La página del editor necesita obtener contenido de esta URL con la frecuencia con que desee actualizar la página de Google AMP.
