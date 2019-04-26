---
description: Utilice Bootstrap y la API de flujo con aplicaciones de Livefyre.
seo-description: Utilice Bootstrap y la API de flujo con aplicaciones de Livefyre.
seo-title: Implementación de aplicación
solution: Experience Manager
title: Implementación de aplicación
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# Implementación de aplicación {#appimplementation}

Caso de uso: Como cliente, quiero integrar Livefyre en mi CMS de terceros con el método Livefyre. js.

Existen tres formas de implementar Livefyre en un componente personalizado de AEM u otro CMS, como WordPress, Sitecore o demandware: Implementación de aplicación de Designer, API, implementación y integración de autenticación de terceros.

## Implementación de aplicación de Designer {#designerapp}

Qué: Forma más sencilla y rápida de integrar una aplicación de Livefyre. Puede diseñar, configurar y generar un código incrustado personalizado Javascript para integrar una aplicación Liveyfre en una página en minutos.

Cómo: [Crear, previsualizar, publicar e incrustar una aplicación de Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Ejemplo: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implementación de Livefyre. js {#livefyrejsimp}

Qué: [Livefyre. js](/help/implementation/c-livefyre.js.md) es la biblioteca principal que alimenta Aplicaciones y Auth en un sitio. Define el objeto global `window.Livefyre` y un único método público, Livefyre. requerir, que se puede utilizar para cargar otras bibliotecas de JavaScript de Livefyre que ayudan a incrustar aplicaciones de Livefyre e integración con plataformas de autenticación de usuario de terceros.

Cómo:

* [Crear una colección con collectionmeta Token](/help/implementation/t-create-a-collectionmeta-token.md)

* Integre aplicaciones en CMS de terceros mediante Integraciones de aplicación

Ejemplos:

* Aplicación de comentarios: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Revisar aplicación: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Muro de medios: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Para ver las personalizaciones avanzadas con el SDK, consulte SDK de streamhub.

## Implementación de API {#apiimplementation}

Para crear experiencias y visualizaciones de datos personalizadas, las aplicaciones de Livefyre se pueden crear desde cero, ya que consumen Livefyre y datos sociales mediante el uso de Bootstrap y la API de flujo.

## Integración de autenticación de terceros {#thirdpartyauth}

Para las aplicaciones de Livefyre que requieren autenticación, consulte [Integración](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) de identidad para plataformas de autenticación de terceros.

## Ejemplos de clientes {#customerexamples}

Los siguientes clientes implementaron Livefyre con Integraciones CMS de terceros:

* [Muro de medios de visita PGA](https://www.pgatour.com/social-hub.html)

* [Timeout](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
