---
description: Use la API de Bootstrap y flujo con aplicaciones de Livefyre.
title: Implementación de aplicaciones
uuid: null
exl-id: f1edef86-491d-4f8e-8ce5-f6e019d057ec
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Implementación de aplicación {#appimplementation}

Caso de uso: Como cliente, quiero integrar Livefyre en mi CMS de terceros utilizando el método Livefyre.js.

Hay tres maneras de implementar Livefyre en un componente de AEM personalizado u otro de CMS como WordPress, SiteServer o DemandWare: Implementación de aplicaciones de Designer, API, implementación e integración de autenticación de terceros.

## Implementación de aplicación de Designer {#designerapp}

Qué: La forma más sencilla y rápida de integrar una aplicación Livefyre. Puede diseñar, configurar y generar un código incrustado personalizado de Javascript para integrar una aplicación Live en una página en cuestión de minutos.

Cómo: [Crear, previsualizar, publicar e incrustar una aplicación de Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Ejemplo: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implementación de Livefyre.js {#livefyrejsimp}

Qué: [Livefyre.js](/help/implementation/c-livefyre.js.md) es la biblioteca principal que alimenta las aplicaciones y la autenticación en un sitio. Define el objeto `window.Livefyre` global y un único método público, Livefyre.required, que puede utilizarse para cargar otras bibliotecas JavaScript de Livefyre que ayudan a incrustar aplicaciones de Livefyre e integrar con plataformas de autenticación de usuarios de terceros.

Cómo:

* [Creación de una colección mediante el token CollectionMeta](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrar aplicaciones en CMS de terceros mediante integraciones de aplicaciones

Ejemplos:

* Aplicación de comentarios: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Aplicación de reseñas: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Muro de medios: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Para personalizaciones avanzadas con el SDK, consulte SDK de StreamHub.

## Implementación de API {#apiimplementation}

Para crear experiencias personalizadas y visualizaciones de datos, las aplicaciones de Livefyre se pueden crear desde cero consumiendo datos sociales y de Livefyre mediante el Bootstrap y la API de Stream.

## Integración de autenticación de terceros {#thirdpartyauth}

Para las aplicaciones de Livefyre que requieren autenticación, consulte [Integración de identidad](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) para plataformas de autenticación de terceros.

## Ejemplos de clientes {#customerexamples}

Los siguientes clientes implementaron Livefyre con integraciones de CMS de terceros:

* [Pared de medios Tour PGA](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
