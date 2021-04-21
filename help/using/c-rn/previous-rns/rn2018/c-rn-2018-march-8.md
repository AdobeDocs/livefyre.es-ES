---
description: Notas de la versión de la versión del 8 de marzo de 2018.
title: 8 de marzo de 2018
exl-id: 46d4a425-17e0-48a2-a596-5cc7163f9edd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 5%

---

# 8 de marzo de 2018{#march}

Notas de la versión de la versión del 8 de marzo de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* **Eliminación de aplicaciones. **Se ha agregado la capacidad de eliminar aplicaciones en Studio para que los usuarios puedan administrar mejor la lista de aplicaciones. Al eliminar una aplicación, esta se elimina de la tabla, pero no del sitio. La aplicación seguirá recibiendo contenido de un flujo si está configurada para hacerlo.

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | Encuestas | Se han cambiado Encuestas para usar HTTPS exclusivamente. Anteriormente, se permitía el uso de Encuestas con HTTP. |
| Error, | Studio | Se ha corregido un problema que provocaba que la ventana modal que muestra los anuncios al iniciar sesión en Studio se mostrara demasiado grande en pantallas de baja resolución. |

## Versión de UAT

| Tipo de incidencia | Componente | Nota de la versión |
|--- |--- |--- |
| Mejora | Tira de película | Se han actualizado las siguientes funciones de accesibilidad para FilmStrip: <br><ul><li>Flechas izquierda/derecha corregidas de &lt;div> a &lt;button> </li><li>El elemento de la imagen de vista previa cambió de una etiqueta ARIA menos descriptiva de &quot;Abrir foto adjunta&quot; a una etiqueta que lee el nombre de la plataforma y el texto de la publicación.</li></ul> |
| Error, | Muro de los medios | Se ha corregido un problema en el muro de medios en el cual no se podía hacer clic en las etiquetas cuando se agregaba una publicación de Instagram desde una regla de flujo. |
| Mejora | Muro de los medios | Se ha mejorado la accesibilidad de Muro de medios de las siguientes maneras: <br><ul><li>Al abrir y cerrar los modales mediante comandos de teclado, ya no se volverá a desplazar el foco a la parte superior de la página. En su lugar, el enfoque permanece en el elemento centrado por última vez antes de la ventana emergente modal.</li><li>El botón Cargar más se puede activar con el tabulador y activar con la tecla Intro del teclado.</li></ul> |
| Error, | Rights Management | Se ha corregido un error por el que no se podía ver el modal de la solicitud de derechos después de conceder derechos para un recurso de Instagram. |
