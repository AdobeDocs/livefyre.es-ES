---
description: Notas de la versión de la versión del 8 de marzo de 2018.
seo-description: Notas de la versión de la versión del 8 de marzo de 2018.
seo-title: 8 de marzo de 2018
solution: Experience Manager
title: 8 de marzo de 2018
uuid: 4ed67147-0837-4d5e-8e99-532a4278bcce
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# March 8, 2018{#march}

Notas de la versión de la versión del 8 de marzo de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* **Eliminación de aplicaciones. **Se ha agregado la capacidad de eliminar aplicaciones en Studio para que los usuarios puedan administrar mejor la lista de aplicaciones. Al eliminar una aplicación, ésta se elimina de la tabla, pero no del sitio. La aplicación seguirá recibiendo contenido de un flujo si está configurada para hacerlo.

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | Encuestas | Se han cambiado las encuestas para usar HTTPS exclusivamente. Anteriormente, aún se permitía el uso de encuestas con HTTP. |
| Error, | Studio | Se ha corregido un problema que provocaba que la ventana modal que muestra anuncios al iniciar sesión en Studio se mostrara demasiado grande en pantallas de baja resolución. |

## Versión de UAT

| Tipo de incidencia | Componente | Nota de versión |
|--- |--- |--- |
| Mejora | Tira de película | Se han actualizado las siguientes funciones de accesibilidad para la tira de película: <br><ul><li>Flechas izquierda/derecha corregidas de &lt;div&gt; a &lt;button&gt; </li><li>La vista previa del elemento de imagen ha cambiado de una etiqueta ARIA menos descriptiva de "Abrir foto adjunta" a una etiqueta que lee el nombre de la plataforma y el texto de la publicación.</li></ul> |
| Error, | Muro de los medios | Se corrigió un problema en el Muro de medios en el cual no se podía hacer clic en las etiquetas cuando se agregaba una publicación de Instagram desde una regla de flujo. |
| Mejora | Muro de los medios | Se ha mejorado la accesibilidad de Media Wall de las siguientes maneras: <br><ul><li>Al abrir y cerrar los modales mediante comandos de teclado ya no se volverá a desplazar el enfoque a la parte superior de la página. El enfoque permanece en el último elemento seleccionado antes de la ventana emergente modal.</li><li>El botón Cargar más se puede activar con la tecla Intro del teclado.</li></ul> |
| Error, | Rights Management | Se corrigió un error en el cual no se podía ver el modo de solicitud de derechos después de otorgar derechos para un recurso de Instagram. |

