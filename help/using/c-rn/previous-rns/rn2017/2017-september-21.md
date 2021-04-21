---
description: Notas de la versión de la versión del 21 de septiembre de 2017.
title: 21 de septiembre de 2017
exl-id: 6d01710e-dab4-4065-85c5-b00f45d8d4fd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 6%

---

# 21 de septiembre de 2017{#september}

Notas de la versión de la versión del 21 de septiembre de 2017.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Mejora | Comentarios | Los clientes ahora pueden establecer la longitud máxima para los comentarios como parte de su configuración de red. |
| Error, | Aplicación móvil | Este error corrige un problema sobre cómo se representaban las respuestas anidadas en Mobile cuando se deshabilitaban los avatares. |
| Error, | Mosaic | Se ha corregido un error de producción que hacía que Mosaic mostrara cajas grises en IE11 en UGC. |
| Mejora | Mosaic | Los clientes ahora pueden especificar el número de tarjetas que se mostrarán en la aplicación de visualización de Mosaic. |
| Error, | Rights Management | Se ha corregido un error que impedía que un usuario de Studio solicitara derechos en el contenido de Instagram Carousel. |
| Error, | Studio | Se han añadido mensajes de error más claros al crear nuevos sitios. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Mejora | Aplicaciones | Los clientes ahora pueden crear una sola aplicación de Livefyre (Mosaic, FilmStrip o Media Wall) e incrustarla en varias páginas de productos, que filtren dinámicamente el UGC apropiado para cada página de producto (por ejemplo, el UGC etiquetado para zapatos se muestra en la página de producto de zapatos). |
| Mejora | Tira de película | En la aplicación de tira de película hay un banner &quot;Nuevo&quot; que marca contenido nuevo en la aplicación para que los usuarios finales puedan identificar rápidamente contenido nuevo. |
| Mejora | Identidad de Livefyre | Los clientes ahora pueden usar sus credenciales de Github para iniciar sesión en la identidad de Livefyre y participar en nuestras aplicaciones de comentarios. |
| Error, | Rights Management | Se ha corregido un error que permitía que la inserción de caracteres Unicode en mensajes de solicitud de derechos evitara la validación. |
| Mejora | Studio | Se ha actualizado el vínculo Ayuda de Livefyre en la barra de navegación superior. |
| Mejora | Comercio UGC | Los clientes ahora pueden cargar manualmente un catálogo de productos de Google en el estudio LF mediante una exportación de archivos JSON. Esto permite al cliente emparejar UGC con productos de ese catálogo y visualizarlos en nuestras aplicaciones habilitadas para el comercio. |
| Mejora | Comercio UGC | Los clientes pueden seleccionar qué carpetas de productos desean utilizar al filtrar su aplicación de comercio electrónico por ID de producto. Por ejemplo, quiero que mi nueva tira de película aparezca en las páginas de productos de mis zapatos de mujer y bolsas de mujer, por lo que seleccionaré solamente las carpetas de productos &quot;Colección de zapatos de mujer&quot; y &quot;Bolsas de mujer&quot;. |
| Mejora | Comercio UGC | Los clientes de Livefyre ahora pueden filtrar el UGC publicado en sus aplicaciones solo si tienen derechos concedidos. Por ejemplo, un cliente puede depurar y publicar una selección de elementos, pero estos solo se procesarán en la aplicación una vez que el autor les haya otorgado derechos. Esto es especialmente importante en los casos de uso del comercio electrónico, en los que el UGC se utiliza con fines comerciales. |
