---
description: Notas de la versión de la versión del 21 de septiembre de 2017.
seo-description: Notas de la versión de la versión del 21 de septiembre de 2017.
seo-title: 21 de septiembre de 2017
title: 21 de septiembre de 2017
uuid: 1132b48a-f85c-4e05-b312-0093db9ebc8f
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 6%

---


# 21 de septiembre de 2017{#september}

Notas de la versión de la versión del 21 de septiembre de 2017.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Mejora | Comentarios | Los clientes ahora pueden establecer la longitud máxima para Comentarios como parte de su configuración de red. |
| Error, | Aplicación móvil | Este error corrige un problema sobre cómo se procesaban las respuestas anidadas en Mobile cuando se deshabilitaban los avatares. |
| Error, | Mosaico | Se ha corregido un error de producción que hacía que Mosaic mostrara cajas grises en IE11 en UGC. |
| Mejora | Mosaico | Ahora los clientes pueden especificar el número de tarjetas que se mostrarán en la aplicación de visualización Mosaico. |
| Error, | Rights Management | Se ha corregido un error que impedía a un usuario de Studio solicitar derechos en el contenido de Instagram Carousel. |
| Error, | Studio | Se añadieron mensajes de error más claros al crear nuevos sitios. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Mejora | Aplicaciones | Ahora los clientes pueden crear una sola aplicación de Livefyre (Mosaic, Filmstris o Media Wall) e incrustarla en varias páginas de productos, que filtren de forma dinámica la UGC adecuada para cada página de producto (por ejemplo, en la página del producto zapatos se muestra la etiqueta UGC para zapatos). |
| Mejora | Tira de película | En la aplicación de tira de película hay una pancarta &quot;Nueva&quot; que marca el nuevo contenido en la aplicación para que los usuarios finales puedan identificar rápidamente el contenido nuevo. |
| Mejora | Identidad de Livefyre | Los clientes ahora pueden usar sus credenciales de Github para iniciar sesión en la identidad de Livefyre y participar en nuestras aplicaciones de comentarios. |
| Error, | Rights Management | Se ha corregido un error que permitía que la inserción de caracteres Unicode en los mensajes de solicitud de derechos evitara la validación. |
| Mejora | Studio | Se ha actualizado el vínculo Ayuda de Livefyre en la barra de navegación superior. |
| Mejora | Comercio UGC | Ahora los clientes pueden cargar manualmente un catálogo de productos de Google en un estudio LF mediante la exportación de archivos JSON. Esto permite al cliente emparejar UGC con productos de ese catálogo y visualizarlos en nuestras aplicaciones habilitadas para el comercio. |
| Mejora | Comercio UGC | Los clientes pueden seleccionar qué carpetas de productos desean utilizar al filtrar su aplicación de comercio electrónico por ID de producto. Por ejemplo, quiero que mi nueva tira de película aparezca en mis páginas de productos de zapatos para mujeres y bolsas para mujeres, por lo tanto seleccionaré sólo las carpetas de productos &quot;Colección de zapatos para mujeres&quot; y &quot;Bolsas para mujeres&quot;. |
| Mejora | Comercio UGC | Los clientes de Livefyre ahora pueden filtrar la UGC publicada en sus aplicaciones solo si tienen derechos garantizados. Por ejemplo, un cliente puede depurar y publicar una selección de elementos, pero dichos elementos solo se procesarán en la aplicación una vez que el autor les haya concedido derechos. Esto es particularmente importante en los casos de uso del comercio electrónico, en los que el UGC se utiliza con fines comerciales. |

