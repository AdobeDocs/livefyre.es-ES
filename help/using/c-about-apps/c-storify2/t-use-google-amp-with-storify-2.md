---
description: Utilice las API de Livefyre para añadir la funcionalidad de AMP de Google a la página de Storify 2 para mantener el contenido interactivo y compatible con SEO.
title: Usar Google AMP con Storify 2
exl-id: 2fee8655-ac9f-484e-a042-9b7ac7151fcc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Usar Google AMP con Storify 2{#use-google-amp-with-storify}

Utilice las API de Livefyre para añadir la funcionalidad de AMP de Google a la página de Storify 2 para mantener el contenido interactivo y compatible con SEO.

Para utilizar Google AMP con Storify 2, debe crear una página para la aplicación Storify 2 con marcado AMP de Google.

La versión AMP de la aplicación solicita actualizaciones desde la página original (utilice el parámetro **pollInterval** en la API **amp-live-list** para establecer el intervalo para las solicitudes de actualización). Para garantizar que los visitantes de su página de AMP obtengan rápidamente el contenido más actualizado, mantenga un TTL de baja caché en sus páginas de AMP de Storify 2.

Los recursos que no sean imágenes (por ejemplo, vídeos) incluidos como anuncios en una aplicación de Storify 2 deben utilizar HTTPS según lo especificado en la especificación de AMP. Las direcciones URL de AMP que utilizan la red de distribución de contenido (CDN) de Google Cloud utilizan HTTPS.

Para usar Google AMP con Storify 2:

1. Cree una plantilla validada por AMP en su sitio.
1. Utilice una o más de las siguientes API de AMP de Google para personalizar su página de AMP de Google:
   1. [amp-](https://www.ampproject.org/docs/reference/components/amp-iframe) iframe para personalizar la pantalla de Storify 2
   1. [amp-live-](https://www.ampproject.org/docs/reference/components/amp-live-list) list para personalizar el intervalo de tiempo para las actualizaciones
   1. [amp-social-](https://www.ampproject.org/docs/reference/components/amp-social-share) share para agregar un botón de uso compartido en redes sociales
1. Incluya el contenido de la siguiente página de AMP de Storify 2 en el CSS para la página de Storify 2 dentro de la etiqueta `<style amp-custom>` : [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Incluya el contenido de la siguiente API de marcado AMP de Storify 2 en la plantilla AMP de Google: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` donde {{APP_ID}} es el ID de la aplicación Storify 2 de Livefyre Studio.
   1. El único parámetro de consulta es **pollInterval**, que es el intervalo en el que la aplicación buscará actualizaciones (establecido en milisegundos).
   1. La dirección URL incluye contenido de los anuncios más recientes (incluidos tweets, vídeos, etc.)
   1. La página del editor necesita obtener contenido de esta dirección URL tan a menudo como desee que se actualice la página de AMP de Google.
