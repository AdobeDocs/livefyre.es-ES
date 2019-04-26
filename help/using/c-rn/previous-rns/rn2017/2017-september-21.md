---
description: Notas de la versión de la versión del 21 de septiembre de 2017.
seo-description: Notas de la versión de la versión del 21 de septiembre de 2017.
seo-title: 21 de septiembre de 2017
title: 21 de septiembre de 2017
uuid: 1132 b 48 a-f 85 c -4 e 05-b 312-0093 db 9 ebc 8 f
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 21 de septiembre de 2017{#september}

Notas de la versión de la versión del 21 de septiembre de 2017.

## Versión de producción

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Mejora | Comentarios | Ahora los clientes pueden establecer la longitud máxima de Comentarios como parte de la configuración de red. |
| Error | Aplicación móvil | Este error corrige un problema en el modo en que las respuestas anidadas se procesaban en Mobile cuando estaban deshabilitadas. |
| Error | Mosaico | Se ha corregido un error de producción que hacía que Mosaic mostrara cuadros grises en IE 11 en UGC. |
| Mejora | Mosaico | Ahora los clientes pueden especificar el número de tarjetas que se mostrarán en la aplicación de visualización Mosaic. |
| Error | Rights Management | Se ha corregido un error que impedía que un usuario de Studio solicitara derechos en contenido de Instagram Carousel. |
| Error | Studio | Se han agregado mensajes de error más claros al crear sitios nuevos. |

## Versión de UAT

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Mejora | Aplicaciones | Ahora los clientes pueden crear una sola aplicación de Livefyre (Mosaico, Tira de película o Muro de medios) e incrustarla en varias páginas de productos, que filtran dinámicamente el UGC apropiado para cada página de producto (por ejemplo, UGC etiquetado para zapatos aparece en la página del producto zapatos). |
| Mejora | Tira de película | En la aplicación Tira de película hay una pancarta «Nueva» que marca el nuevo contenido de la aplicación para que los usuarios finales puedan identificar rápidamente el contenido nuevo. |
| Mejora | Identidad de Livefyre | Ahora los clientes pueden utilizar sus credenciales de Github para iniciar sesión en la identidad de Livefyre y participar en nuestras aplicaciones de comentarios. |
| Error | Rights Management | Se ha corregido un error que permitía insertar caracteres Unicode en mensajes de Rights Request para evitar la validación. |
| Mejora | Studio | Se ha actualizado el vínculo de la Ayuda de Livefyre en la barra de navegación superior. |
| Mejora | Comercio UGC | Ahora los clientes pueden cargar manualmente un catálogo de productos de Google a un estudio LF mediante una exportación de archivo JSON. Esto permite al cliente par UGC con productos de ese catálogo y visualizarlos en nuestras aplicaciones de comercio habilitadas. |
| Mejora | Comercio UGC | Los clientes pueden seleccionar qué carpetas de productos desean utilizar al filtrar su aplicación de comercio electrónico por ID de producto. Por ejemplo, quiero que mi nueva tira de película aparezca en las páginas de zapatos y zapatos para damas de mis damas, por lo que solo elegiré las carpetas de productos «Mis mallas para mujer» y «Bolsas de mujer». |
| Mejora | Comercio UGC | Los clientes de Livefyre ahora pueden filtrar el UGC publicado en sus aplicaciones solo si tienen derechos concedidos. Por ejemplo, un cliente puede depurar y publicar una selección de elementos, pero estos elementos solo se procesarán en la aplicación una vez que hayan sido concedidos por el autor. Esto es especialmente importante para los casos de uso del comercio electrónico, donde el UGC se utiliza con fines comerciales. |

