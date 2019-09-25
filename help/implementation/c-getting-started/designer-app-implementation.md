---
description: Utilice Bootstrap y Stream API con Livefyre Apps.
seo-description: Utilice Bootstrap y Stream API con Livefyre Apps.
seo-title: Implementación de aplicaciones
solution: Experience Manager
title: Implementación de aplicaciones
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# Implementación de aplicaciones {#appimplementation}

Caso de uso: Como cliente, quiero integrar Livefyre en mi CMS de terceros mediante el método Livefyre.js.

Existen tres formas de implementar Livefyre en un componente personalizado de AEM u otro CMS como WordPress, Sitecore o DemandWare: Implementación de aplicaciones de Designer, API, implementación e integración de autenticación de terceros.

## Implementación de la aplicación de Designer {#designerapp}

Qué: La forma más sencilla y rápida de integrar una aplicación de Livefyre. Puede diseñar, configurar y generar un código incrustado de JavaScript personalizado para integrar una aplicación LiveCycle en una página en cuestión de minutos.

Cómo: [Crear, previsualizar, publicar e incrustar una aplicación de Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Ejemplo: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implementación de Livefyre.js {#livefyrejsimp}

Qué: [Livefyre.js](/help/implementation/c-livefyre.js.md) es la biblioteca principal que activa las aplicaciones y la autenticación en un sitio. Define el `window.Livefyre` objeto global y un único método público, Livefyre.required, que puede utilizarse para cargar otras bibliotecas JavaScript de Livefyre que ayudan a incrustar aplicaciones de Livefyre e integrarse con plataformas de autenticación de usuarios de terceros.

Cómo:

* [Creación de una colección con el token CollectionMeta](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrar aplicaciones en CMS de terceros mediante integraciones de aplicaciones

Ejemplos:

* Aplicación de comentarios: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Aplicación de críticas: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Muro de los medios: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Para obtener personalizaciones avanzadas con el SDK, consulte SDK de StreamHub.

## Implementación de API {#apiimplementation}

Para crear experiencias y visualizaciones de datos personalizadas, las aplicaciones de Livefyre se pueden crear desde cero consumiendo datos sociales y de Livefyre mediante la API de Bootstrap y Stream.

## Integración de autenticación de terceros {#thirdpartyauth}

Para las aplicaciones de Livefyre que requieren autenticación, consulte Integración [de identidad](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) para plataformas de autenticación de terceros.

## Ejemplos de clientes {#customerexamples}

Los siguientes clientes implementaron Livefyre con integraciones de CMS de terceros:

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [Tiempo de espera](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
