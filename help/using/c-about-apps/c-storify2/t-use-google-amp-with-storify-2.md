---
description: Utilice las API de Livefyre para añadir la funcionalidad de Google AMP a la página de Storify 2 a fin de mantener el contenido interactivo y compatible con SEO.
seo-description: Utilice las API de Livefyre para añadir la funcionalidad de Google AMP a la página de Storify 2 a fin de mantener el contenido interactivo y compatible con SEO.
seo-title: Usar Google AMP con Storify 2
solution: Experience Manager
title: Usar Google AMP con Storify 2
uuid: 40c9f083-7284-43ba-ae27-53b1ff9e3954
translation-type: tm+mt
source-git-commit: 65d931e5bd04964db44f8e3a0e000ecec2652893
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# Usar Google AMP con Storify 2{#use-google-amp-with-storify}

Utilice las API de Livefyre para añadir la funcionalidad de Google AMP a la página de Storify 2 a fin de mantener el contenido interactivo y compatible con SEO.

Para utilizar Google AMP con Storify 2, debe crear una página para la aplicación Storify 2 con el marcado AMP de Google.

La versión AMP de la aplicación solicita actualizaciones desde la página original (utilice el parámetro **pollInterval** en la API **amp-live-lista** para establecer el intervalo de las solicitudes de actualización). Para garantizar que los visitantes de la página de AMP obtengan el contenido más actualizado rápidamente, mantenga un TTL de caché baja en las páginas de Storify 2 AMP.

Los recursos que no son de imagen (por ejemplo, vídeos) incluidos como anuncios en una aplicación de Storify 2 deben utilizar HTTPS según lo especificado en la especificación de AMP. Las direcciones URL de AMP que utilizan la red de Envío de contenido de Google Cloud (CDN) utilizan HTTPS.

Para usar Google AMP con Storify 2:

1. Cree una plantilla validada por AMP en su sitio.
1. Utilice una o más de las siguientes API de AMP de Google para personalizar su página de AMP de Google:
   1. [amp-](https://www.ampproject.org/docs/reference/components/amp-iframe) iframeto para personalizar la pantalla Storify 2
   1. [amp-live-](https://www.ampproject.org/docs/reference/components/amp-live-list) list para personalizar el intervalo de tiempo para las actualizaciones
   1. [amp-social-](https://www.ampproject.org/docs/reference/components/amp-social-share) sharpara agregar un botón de uso compartido en redes sociales
1. Incluya el contenido de la siguiente página de AMP de Storify 2 en la CSS de la página de Storify 2 dentro de la etiqueta `<style amp-custom>`: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Incluya el contenido de la siguiente API de marcado de Storify 2 AMP en la plantilla de Google AMP: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` donde {{APP_ID}} es el ID de la aplicación de Storify 2 en Livefyre Studio.
   1. El único parámetro de consulta es **pollInterval**, que es el intervalo en el que la aplicación buscará actualizaciones (establecido en milisegundos).
   1. La dirección URL incluye contenido de los anuncios más recientes (incluidos tweets, vídeos, etc.)
   1. La página del editor necesita obtener contenido de esta dirección URL con la frecuencia que desee que se actualice la página AMP de Google.
