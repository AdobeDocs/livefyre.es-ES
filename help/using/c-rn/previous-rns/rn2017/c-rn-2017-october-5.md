---
description: Notas de la versión de la versión del 5 de octubre de 2017.
title: 5 de octubre de 2017
exl-id: 6e39a86e-82dd-47ff-ad68-2b483f8b1921
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 4%

---

# 5 de octubre de 2017{#october}

Notas de la versión de la versión del 5 de octubre de 2017.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | Identidad de Livefyre | Los clientes que usaban la identidad de Livefyre para iniciar sesión experimentaban problemas al ver o actualizar sus avatares al publicar para comentar aplicaciones. Esto se ha corregido ahora, ya que los avatares ahora son visibles y están disponibles para su actualización. |
| Error, | Rights Management | Se ha corregido un error que mostraba nombres de usuario largos en la ficha Modelo de derechos . |
| Mejora | Transmisiones | Se ha agregado la capacidad de pulsar la tecla de tabulación en un campo de texto Emisiones para completar un término de búsqueda. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Mejora | Tira de película | Cuando un cliente implementa una aplicación de tiras de película, el UGC recién transmitido tendrá una etiqueta &quot;nueva&quot; junto a él para identificarlos rápidamente. |
| Mejora | Tira de película | FilmStrip es una aplicación de visualización completamente nueva, diseñada principalmente para mostrar UGC en escenarios de comercio electrónico, como páginas de productos o sitios web transaccionales. La tira de película alinea horizontalmente el UGC para que se muestre como un carrete de cámara, una pieza a la vez. Los usuarios finales pueden navegar por Tira de película haciendo clic en las flechas laterales para desplazarse por el contenido disponible. |
| Mejora | Biblioteca | Los archivos cargados en la biblioteca por un cliente se concederán automáticamente. Esta función es útil cuando los usuarios han activado el filtro &quot;se requieren derechos concedidos&quot; en sus aplicaciones. |
| Mejora | Identidad de Livefyre | Los clientes ahora pueden usar sus credenciales de Github para iniciar sesión en la identidad de LIvefyre y participar en nuestras aplicaciones de comentarios. |
| Error, | Rights Management | Se ha corregido un error que permitía que la inserción de caracteres Unicode en mensajes de solicitud de derechos evitara la validación. |
| Mejora | SEGURO | Se han añadido mejoras menores a la detección de correo no deseado SAFE. |
| Error, | Servicio | Los usuarios sin correos electrónicos válidos tienen correos electrónicos creados para ellos. Se ha corregido un problema con los registros de producción en el cual el sistema no enviaba correos electrónicos a estos usuarios. |
| Mejora | Studio | Se ha actualizado el vínculo Ayuda de Livefyre en la barra de navegación superior. |
| Mejora | Comercio UGC | Como cliente, ahora puedo crear una sola aplicación de Livefyre (Mosaic, FilmStrip o Media Wall) e incrustarla en varias páginas de producto, que filtra dinámicamente el UGC apropiado para cada página de producto (por ejemplo, UGC con zapatos para una página de producto de zapato). |
| Mejora | Comercio UGC | Los clientes ahora pueden cargar manualmente un catálogo de productos de Google en Livefyre Studio mediante una exportación de archivos JSON. Esto permite al cliente emparejar UGC con productos de ese catálogo y visualizarlos en nuestras aplicaciones habilitadas para el comercio. |
| Mejora | Comercio UGC | Los clientes pueden seleccionar qué carpetas de productos desean utilizar al filtrar su aplicación de comercio electrónico por ID de producto. Por ejemplo, quiero que mi nueva tira de película aparezca en mis páginas de productos de zapatos para mujeres y bolsas para mujeres, por lo que seleccionaré solamente las carpetas de productos &quot;Colección de zapatos para mujeres&quot; y &quot;Bolsas para mujeres&quot;. |
| Mejora | Comercio UGC | Los clientes de Livefyre ahora pueden filtrar el UGC publicado en sus aplicaciones solo si han obtenido derechos. Por ejemplo, un cliente puede depurar y publicar una selección de elementos, pero estos solo se procesarán en la aplicación una vez que el autor les haya concedido los derechos. Esto es especialmente importante en los casos de uso del comercio electrónico, en los que el UGC se utiliza con fines comerciales. |
