---
description: Críticas ofrece una amplia gama de personalizaciones que le permiten
  crear una aplicación de revisión que coincida con sus necesidades y con la marca.
seo-description: Críticas ofrece una amplia gama de personalizaciones que le permiten
  crear una aplicación de revisión que coincida con sus necesidades y con la marca.
seo-title: Creación de una aplicación de revisiones
solution: Experience Manager
title: Creación de una aplicación de revisiones
uuid: 6 caeafe 7-c 04 e -484 e-b 02 f -98 dc 6 d 9 b 3184
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Creación de una aplicación de revisiones{#creating-a-reviews-app}

Críticas ofrece una amplia gama de personalizaciones que le permiten crear una aplicación de revisión que coincida con sus necesidades y con la marca.

Use la aplicación de revisiones personalizada en su sitio como aplicación JS. No puede crear una aplicación de revisiones en Livefyre Studio. Para crear una aplicación de revisiones en el sitio, consulte [Análisis de la integración](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Clasificaciones {#section_hs5_c4h_21b}

Las clasificaciones son el valor numérico que los usuarios asignan a la revisión. Todas las revisiones deben incluir una clasificación, que se muestra como sistema de 5 estrellas de forma predeterminada. (Mientras que las clasificaciones se muestran como 0,5 - 5 en la aplicación, Livefyre almacena una proporción de X/100 en el back-backend, de modo que 1 estrella es 20/100 y 2 estrellas es 40/100. Esta proporción se muestra al ver las revisiones en Studio.)

La escala de clasificación de 0,5 a 5 puede configurarse hasta una clasificación de 100, con clasificaciones medias también disponibles.

Para obtener más información, consulte el campo maxrating para el objeto convconfig Reviews.

## Estilo de icono de clasificación {#section_cqn_c4h_21b}

Los iconos de clasificación pueden personalizarse para adaptarse a su marca y estilo.

Para obtener más información, consulte **[!UICONTROL Configure Star Ratings]** en Revisiones personalizadas.

## Clasificar dimensiones {#section_cnx_snh_21b}

Las dimensiones de clasificación son las categorías sobre las que los revisores clasifican su producto o servicio. Ejemplos de dimensiones de clasificación son «rendimiento», «diseño», «costo», «en general» o cualquier otra categoría que elija.

El valor predeterminado es mostrar una dimensión de clasificación «global», pero puede definir e implementar varias dimensiones de clasificación, como se muestra en el ejemplo siguiente.

Para obtener más información, consulte el campo ratingdimensions en Revisar metadatos de recopilación.

## Revisar campos de texto {#section_xcm_4nh_21b}

También puede incluir campos de texto adicionales en el producto o la experiencia que se está revisando. (Por ejemplo, los campos de texto pueden incluir Pros y Contras, o bien No echar un vistazo). El número, el título y el texto predeterminado del campo se pueden personalizar. Los usuarios deberán completar todos los campos de texto, así como también el título, el cuerpo y la clasificación para publicar su revisión. No es posible incluir campos de texto opcionales.

Para obtener más información, consulte el campo ratingdimensions para ver los metadatos de la colección.

## Revisar resumen {#section_ysz_lnh_21b}

De forma predeterminada, se muestra una sección de resumen en la parte superior de la aplicación de revisiones. Esta sección incluye una visualización de la Clasificación de usuarios promedio y el Desglose de clasificación para la Colección de revisiones, mostrando sólo números enteros. Esta sección es de solo lectura y se puede ocultar si lo desea.

Para obtener más información, consulte el campo ratingresumyenabled para el objeto convconfig reviews.

## Filtro de profanidad y correo no deseado {#section_hcm_jnh_21b}

El texto de Título y cuerpo de una revisión pasa a través de nuestro filtro de filtro no deseado y filtro de profanidad en cuanto se publica la revisión.

## Personalización de texto {#section_tjf_hnh_21b}

Las cadenas de texto, incluidas las sugerencias y las etiquetas, pueden personalizarse para el idioma o para ajustarse a su marca.

## Responder a una revisión {#section_yng_fnh_21b}

Los usuarios pueden responder a su propia versión o a la de otros revisores en cada colección de revisiones. Solo los usuarios que inician sesión pueden publicar una respuesta en una revisión.

La opción para que los usuarios respondan a una Revisión está activada en Studio. Los propietarios pueden cambiar esta configuración para el nivel de red, sitio o colección. Los moderadores pueden habilitar esta configuración únicamente para sus colecciones.

## Socialsync y Curate {#section_llh_2nh_21b}

Como las revisiones están diseñadas para agregar un valor numérico para cada parte del contenido enviado, socialsync y Depure no son compatibles con las Revisiones.

## API de revisiones {#section_xrh_wmh_21b}

Las API de revisiones están disponibles para permitirle mostrar la clasificación promedio de usuarios y la información de desglose de clasificación, y el usuario revisa las actividades de otras secciones del sitio.

[Clasificaciones y críticas](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** El extremo de API de Bootstrap permite que los motores de búsqueda lean su revisión como Google para que el contenido y las palabras clave puedan mejorar la optimización de los motores de búsqueda.

* **[!UICONTROL Average User Ratings]** La API Media de clasificaciones de usuario recupera la clasificación de usuario promedio para una o varias colecciones de críticas, lo que permite crear una visualización de esta información en una página de índice o agregar a una página de índice de búsqueda.

* **[!UICONTROL Ratings Breakdown]** La API de desglose de clasificaciones recupera un desglose de todas las clasificaciones de una colección de revisiones específica y permite crear una visualización que muestra la cantidad de revisiones asociadas con cada clasificación de estrella.

* **[!UICONTROL User Reviews]** La API de críticas de usuarios recupera las revisiones más recientes de un usuario específico. Esta actividad se puede utilizar para mostrar las revisiones de un usuario en su página de perfil público.
