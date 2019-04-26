---
description: Notas de la versión del 5 de octubre de 2017.
seo-description: Notas de la versión del 5 de octubre de 2017.
seo-title: 5 de octubre de 2017
title: 5 de octubre de 2017
uuid: 62 e 9 e 4 ee -1644-4 d 22-9589-2 e 208 a 68 aaeb
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 5 de octubre de 2017{#october}

Notas de la versión del 5 de octubre de 2017.

## Versión de producción

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Error | Identidad de Livefyre | Los clientes que usan la identidad de Livefyre para iniciar sesión experimentaban problemas al ver o actualizar sus avatares al publicar en aplicaciones de comentarios. Esto se ha solucionado ya, ya que las avatares ahora están visibles y disponibles para actualizar. |
| Error | Rights Management | Se ha corregido un error que mostraba los nombres de usuario largos en la ficha Rights Modal. |
| Mejora | Flujos | Se ha agregado la capacidad de visitar la tecla de tabulación en un campo de texto Flujos para completar un término de búsqueda. |

## Versión de UAT

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Mejora | Tira de película | Cuando un cliente implementa una aplicación de tira de película, el nuevo UGC transmitido por flujo continuo tendrá una etiqueta "nueva" junto a ella para identificarlos rápidamente. |
| Mejora | Tira de película | Tira de película es una aplicación de visualización completamente nueva, diseñada principalmente para exhibir UGC en escenarios de comercio electrónico, como páginas de productos o sitios web transaccionales. La tira de película alinea horizontalmente el UGC para que se muestre como carrete de cámara, una pieza en el momento. Los usuarios finales pueden navegar por la tira de película haciendo clic en las flechas laterales para desplazarse por el contenido disponible. |
| Mejora | Biblioteca | Los archivos cargados a la biblioteca por un cliente se conceden automáticamente. Ésta es una función útil cuando los usuarios han activado el filtro «Requerir derechos concedidos» en sus aplicaciones. |
| Mejora | Identidad de Livefyre | Ahora los clientes pueden utilizar sus credenciales de Github para iniciar sesión en la identidad de livefyre y participar en nuestras aplicaciones de comentarios. |
| Error | Rights Management | Se ha corregido un error que permitía insertar caracteres Unicode en mensajes de Rights Request para evitar la validación. |
| Mejora | SAFE | Se han añadido pequeñas mejoras a la detección de spam seguro. |
| Error | Servicio | Los usuarios sin correos electrónicos válidos tienen mensajes de correo electrónico creados para ellos. Se ha corregido un problema con los registros de producción en los que el sistema no enviaba correos electrónicos a estos usuarios. |
| Mejora | Studio | Se ha actualizado el vínculo de la Ayuda de Livefyre en la barra de navegación superior. |
| Mejora | Comercio UGC | Como cliente, ahora puedo crear una sola aplicación de Livefyre (Mosaico, tira de película o Muro de medios) e incrustarla en varias páginas de producto, filtrándola dinámicamente para cada página de producto (por ejemplo, UGC con zapatos para una página de producto Shoe). |
| Mejora | Comercio UGC | Ahora los clientes pueden cargar manualmente un catálogo de productos de Google en un estudio de Livefyre mediante una exportación de archivo JSON. Esto permite al cliente par UGC con productos de ese catálogo y visualizarlos en nuestras aplicaciones de comercio habilitadas. |
| Mejora | Comercio UGC | Los clientes pueden seleccionar qué carpetas de productos desean utilizar al filtrar su aplicación de comercio electrónico por ID de producto. Por ejemplo: deseo que mi nueva tira aparezca en las páginas de zapatos y zapatos para damas de mis damas, por lo que solo elegiré las carpetas de productos «Mis mallas para mujer» y «Bolsas de mujer». |
| Mejora | Comercio UGC | Los clientes de Livefyre ahora pueden filtrar el UGC publicado en sus aplicaciones solo si se han concedido derechos. Por ejemplo, un cliente puede depurar y publicar una selección de elementos, pero estos elementos solo se procesarán en la aplicación una vez que hayan sido concedidos por el autor. Esto es especialmente importante para los casos de uso de comercio electrónico, donde el UGC se utiliza con fines comerciales. |

