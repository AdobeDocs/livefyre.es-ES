---
description: Reviews ofrece una amplia gama de personalizaciones, lo que le permite crear una aplicación de revisión que se adapte a sus necesidades y a su marca.
title: Creación de una aplicación de reseñas
exl-id: 14f074d2-922c-4997-8d7d-f2c92f069e07
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# Creación de una aplicación de reseñas{#creating-a-reviews-app}

Reviews ofrece una amplia gama de personalizaciones, lo que le permite crear una aplicación de revisión que se adapte a sus necesidades y a su marca.

Utilice la aplicación de revisiones incrustándola en el sitio como aplicación JS. No puede crear una aplicación de reseñas en Livefyre Studio. Para crear una aplicación de revisiones en el sitio, consulte [Integración de revisiones](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Clasificaciones {#section_hs5_c4h_21b}

Las clasificaciones son el valor numérico que los usuarios asignan a la revisión. Cada revisión debe incluir una clasificación, que se muestra como un sistema de 5 estrellas de forma predeterminada. (Mientras que las clasificaciones se muestran como de 0,5 a 5 en la aplicación, Livefyre almacena una proporción de X/100 en el servidor, de modo que 1 estrella es de 20/100 y 2 estrellas es de 40/100. Esta proporción se muestra al ver las revisiones en Studio).

La escala de clasificación de 0,5 a 5 puede configurarse hasta una clasificación de 100, con medias clasificaciones disponibles.

Para obtener más información, consulte el campo maxRating del objeto convConfig de revisiones.

## Icono de clasificación Estilo {#section_cqn_c4h_21b}

Los iconos de clasificación pueden personalizarse para adaptarse a su marca y estilo.

Para obtener más información, consulte **[!UICONTROL Configure Star Ratings]** en Personalización de revisiones.

## Dimension de clasificación {#section_cnx_snh_21b}

Las dimensiones de clasificación son las categorías sobre las que los revisores clasifican su producto o servicio. Algunos ejemplos de dimensiones de clasificación son &quot;rendimiento&quot;, &quot;diseño&quot;, &quot;coste&quot;, &quot;total&quot; o cualquier otra categoría que elija.

El valor predeterminado es mostrar una dimensión de clasificación &quot;general&quot;, aunque puede definir e implementar varias dimensiones de clasificación, como se muestra en el ejemplo siguiente.

Para obtener más información, consulte el campo ratingDimensions en Revisar metadatos de colección.

## Revisar campos de texto {#section_xcm_4nh_21b}

También puede incluir campos de texto adicionales sobre el producto o experiencia que se está revisando. (Por ejemplo, los campos de texto pueden incluir Ventajas e inconvenientes, o No perder). Se pueden personalizar el número, el título y el texto predeterminado del campo. Los usuarios deberán completar todos los campos de texto, así como el título, cuerpo y clasificación de la revisión, para publicar su revisión. No es posible incluir campos de texto opcionales.

Para obtener más información, consulte el campo ratingDimensions para Revisar metadatos de colección.

## Revisar resumen {#section_ysz_lnh_21b}

De forma predeterminada, se muestra una sección de resumen en la parte superior de la aplicación de revisiones. Esta sección incluye una visualización de la clasificación promedio del usuario y el desglose de clasificación de la colección de revisiones, mostrando solo números enteros. Esta sección es de solo lectura y se puede ocultar si lo desea.

Para obtener más información, consulte el campo ratingSummaryEnabled para el objeto convConfig de revisiones.

## Filtro de correo no deseado y lenguaje {#section_hcm_jnh_21b}

El texto del Título y el Cuerpo de una Revisión se pasa a través de nuestro Filtro de correo no deseado y Filtro de profanidad en cuanto se publica la Revisión.

## Personalización de texto {#section_tjf_hnh_21b}

Las cadenas de texto, incluidas las descripciones emergentes y las etiquetas, pueden personalizarse para el idioma o para ajustarse a la marca.

## Responder a una revisión {#section_yng_fnh_21b}

Los usuarios pueden responder a la revisión propia o de otro tipo en cada colección de reseñas. Solo los usuarios que hayan iniciado sesión pueden publicar una respuesta a una revisión.

La opción para que los usuarios respondan a una revisión está habilitada en Studio. Los propietarios pueden alternar esta configuración para el nivel de red, sitio o colección. Los moderadores pueden habilitar esta configuración solo para sus colecciones.

## SocialSync y Depurar {#section_llh_2nh_21b}

Como Reviews está diseñado para agregar un valor numérico a cada parte del contenido enviado, SocialSync y Depurar no son compatibles con las revisiones.

## Revisa las API {#section_xrh_wmh_21b}

Las API de revisiones están disponibles para permitirle mostrar la clasificación promedio de los usuarios y la información de desglose de clasificación, así como la actividad de los usuarios en otras secciones de su sitio.

[Clasificaciones y revisiones](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** El extremo de la API de Bootstrap permite que motores de búsqueda como Google lean la revisión para que el contenido y las palabras clave mejoren la optimización de los motores de búsqueda.

* **[!UICONTROL Average User Ratings]** La API de clasificación de usuarios promedio recupera la clasificación de usuario promedio para una o más colecciones de reseñas, lo que le permite crear una visualización de esta información en una página de índice o agregarla a una página de índice de búsqueda.

* **[!UICONTROL Ratings Breakdown]** La API de desglose de clasificaciones recupera un desglose de todas las clasificaciones de una colección de reseñas específica y le permite crear una visualización que muestra el número de revisiones asociadas a cada clasificación por estrellas.

* **[!UICONTROL User Reviews]** La API de reseñas de usuario recupera las revisiones más recientes de un usuario específico. Esta actividad se puede utilizar para mostrar las revisiones de un usuario en su página de perfil público.
