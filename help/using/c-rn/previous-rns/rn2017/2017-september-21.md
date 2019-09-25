---
description: Release Notes for the September 21, 2017 release.
seo-description: Notas de la versión de la versión del 21 de septiembre de 2017.
seo-title: 21 de septiembre de 2017
title: 21 de septiembre de 2017
uuid: 1132b48a-f85c-4e05-b312-0093db9ebc8f
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# September 21, 2017{#september}

Release Notes for the September 21, 2017 release.

## Production Release

| **Tipo de incidencia** | **Componente** | **Release Note** |
|---|---|---|
| Mejora | Comentarios | Customers can now set the maximum length for Comments as part of their network configuration. |
| Error, | Aplicación móvil | This bug corrects an issue on how nested replies rendered in Mobile when avatars were disabled. |
| Error, | Mosaic | Se ha corregido un error de producción que hacía que Mosaic mostrara cajas grises en IE11 en UGC. |
| Mejora | Mosaic | Customers can now specify the number of cards to be displayed in the Mosaic visualization app. |
| Error, | Rights Management | Fixed a bug preventing a Studio user from requesting rights on Instagram Carousel content. |
| Error, | Studio | Se agregaron mensajes de error más claros al crear nuevos sitios. |

## UAT Release

| **Tipo de incidencia** | **Componente** | **Release Note** |
|---|---|---|
| Mejora | Aplicaciones | Customers can now create a single Livefyre app (Mosaic, Filmstrip or Media Wall) and embed it in multiple product pages, that dynamically filter the appropriate UGC for each product page (for example, UGC tagged for shoes displays on the shoe product page). |
| Mejora | Filmstrip | In the Filmstrip App there is a "New" banner that flags new content in the App so that end-users can quickly identify fresh content. |
| Mejora | Livefyre Identity | Los clientes ahora pueden usar sus credenciales de Github para iniciar sesión en la identidad de Livefyre y participar en nuestras aplicaciones de comentarios. |
| Error, | Rights Management | Fixed a bug that allowed insertion of unicode characters in Rights Request messages to bypass validation. |
| Mejora | Studio | Updated the Livefyre Help link in the top navigation bar. |
| Mejora | Comercio UGC | Ahora los clientes pueden cargar manualmente un catálogo de productos de Google en un estudio LF mediante la exportación de archivos JSON. This enables the customer to pair UGC with products from that catalogue and visualize them in our commerce enabled apps. |
| Mejora | Comercio UGC | Customers can select which product folders they want to use when filtering their e-commerce app by product ID. For example, I want my new Filmstrip to appear in my women's shoes and women bags product pages, therefore I will select only the "Women's shoes collection" and "Women's bags" product folders. |
| Mejora | Comercio UGC | Los clientes de Livefyre ahora pueden filtrar la UGC publicada en sus aplicaciones solo si tienen derechos garantizados. Por ejemplo, un cliente puede depurar y publicar una selección de elementos, pero dichos elementos solo se procesarán en la aplicación una vez que el autor les haya concedido derechos. Esto es particularmente importante en los casos de uso del comercio electrónico, en los que el UGC se utiliza con fines comerciales. |

