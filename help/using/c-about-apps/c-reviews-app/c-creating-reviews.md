---
description: Reviews ofrece una amplia gama de personalizaciones, lo que le permite crear una aplicación de revisión que se adapte a sus necesidades y a su marca.
seo-description: Reviews ofrece una amplia gama de personalizaciones, lo que le permite crear una aplicación de revisión que se adapte a sus necesidades y a su marca.
seo-title: Creación de una aplicación de críticas
solution: Experience Manager
title: Creación de una aplicación de críticas
uuid: 6caeafe7-c04e-484e-b02f-98dc6d9b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creación de una aplicación de críticas{#creating-a-reviews-app}

Reviews ofrece una amplia gama de personalizaciones, lo que le permite crear una aplicación de revisión que se adapte a sus necesidades y a su marca.

Utilice la aplicación de revisiones incrustándola en el sitio como una aplicación JS. No puede crear una aplicación de críticas en Livefyre Studio. Para crear una aplicación de críticas en el sitio, consulte Integración de [críticas](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Clasificaciones {#section_hs5_c4h_21b}

Las clasificaciones son el valor numérico que los usuarios asignan a la revisión. Cada revisión debe incluir una clasificación, que se muestra como un sistema de 5 estrellas de forma predeterminada. (Mientras que las clasificaciones se muestran entre 0,5 y 5 en la aplicación, Livefyre almacena una proporción de X/100 en el servidor, de modo que 1 estrella es 20/100 y 2 estrellas es 40/100. Esta proporción se muestra al ver las revisiones en Studio).

La escala de clasificación de 0,5 a 5 puede configurarse hasta una clasificación de 100, con medias clasificaciones disponibles.

Para obtener más información, consulte el campo maxRating del objeto convConfig de revisiones.

## Estilo de icono de clasificación {#section_cqn_c4h_21b}

Los iconos de clasificación pueden personalizarse para adaptarse a su marca y estilo.

Para obtener más información, consulte **[!UICONTROL Configure Star Ratings]** en Personalización de revisiones.

## Clasificación de dimensiones {#section_cnx_snh_21b}

Las dimensiones de clasificación son las categorías en las que los revisores califican su producto o servicio. Algunos ejemplos de dimensiones de clasificación son "rendimiento", "diseño", "costo", "total" o cualquier otra categoría que elija.

El valor predeterminado es mostrar una dimensión de clasificación "general", aunque puede definir e implementar varias dimensiones de clasificación, como se muestra en el ejemplo siguiente.

Para obtener más información, consulte el campo ratingDimensions en Revisar metadatos de la colección.

## Revisar campos de texto {#section_xcm_4nh_21b}

También puede incluir campos de texto adicionales en el producto o experiencia que se está revisando. (Por ejemplo, los campos de texto pueden incluir Ventajas y Contras o No perder). Se pueden personalizar el número, el título y el texto predeterminado del campo. Los usuarios deberán completar todos los campos de texto, así como el título, cuerpo y clasificación de la revisión, para publicar su revisión. No es posible incluir campos de texto opcionales.

Para obtener más información, consulte el campo ratingDimensions para revisar los metadatos de la colección.

## Resumen de revisión {#section_ysz_lnh_21b}

De forma predeterminada, se muestra una sección de resumen en la parte superior de la aplicación de revisiones. Esta sección incluye una visualización de la Clasificación promedio de usuarios y el Desglose de clasificación de la colección de críticas, mostrando sólo números enteros. Esta sección es de solo lectura y puede ocultarse si lo desea.

Para obtener más información, consulte el campo ratingSummaryEnabled del objeto convConfig de revisiones.

## Filtro de correo no deseado y lenguaje obsceno {#section_hcm_jnh_21b}

El texto del Título y el Cuerpo de una Revisión se pasa a través de nuestro Filtro de correo no deseado y Filtro de lenguaje natural en cuanto se publica la Revisión.

## Personalización del texto {#section_tjf_hnh_21b}

Las cadenas de texto, incluidas la información sobre herramientas y las etiquetas, pueden personalizarse para el idioma o para adaptarse a la marca.

## Respuesta a una revisión {#section_yng_fnh_21b}

Los usuarios pueden responder a su propia o a la de otra persona en cada colección de críticas. Solo los usuarios que iniciaron sesión pueden publicar una respuesta a una revisión.

La opción para que los usuarios respondan a una revisión está activada en Studio. Los propietarios pueden cambiar esta configuración para el nivel de red, sitio o colección. Los moderadores pueden habilitar esta configuración solo para sus colecciones.

## SocialSync y Depurar {#section_llh_2nh_21b}

Dado que las críticas están diseñadas para agregar un valor numérico a cada parte del contenido enviado, SocialSync y Depurar no son compatibles con las críticas.

## API de revisiones {#section_xrh_wmh_21b}

Las API de revisiones están disponibles para permitirle mostrar la clasificación promedio del usuario y la información de desglose de clasificación, y el usuario revisa la actividad en otras secciones del sitio.

[Clasificaciones y críticas](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** El extremo de la API de Bootstrap permite que los motores de búsqueda como Google lean la revisión para que el contenido y las palabras clave mejoren la optimización del motor de búsqueda.

* **[!UICONTROL Average User Ratings]** La API de clasificación de usuarios promedio recupera la clasificación de usuario promedio para una o varias colecciones de críticas, lo que permite crear una visualización de esta información en una página de índice o agregarla a una página de índice de búsqueda.

* **[!UICONTROL Ratings Breakdown]** La API de desglose de clasificaciones recupera un desglose de todas las clasificaciones de una colección de críticas específica y permite crear una visualización que muestra el número de revisiones asociadas a cada clasificación por estrellas.

* **[!UICONTROL User Reviews]** La API de reseñas de usuario recupera las revisiones más recientes de un usuario específico. Esta actividad se puede utilizar para mostrar las revisiones de un usuario en su página de perfil público.
