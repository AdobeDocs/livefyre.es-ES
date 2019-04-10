---
description: Notas de la versión de la versión del 8 de marzo de 2018.
seo-description: Notas de la versión de la versión del 8 de marzo de 2018.
seo-title: 8 de marzo de 2018
solution: Experience Manager
title: 8 de marzo de 2018
uuid: 4 ed 67147-0837-4 d 5 e -8 e 99-532 a 4278 bcce
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 8 de marzo de 2018{#march}

Notas de la versión de la versión del 8 de marzo de 2018.

## Nuevas características {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* ** Eliminación de aplicaciones. ** Se ha agregado la capacidad de eliminar aplicaciones en Studio para que los usuarios puedan gestionar mejor la lista de aplicaciones. Al eliminar una aplicación, esta se elimina de la tabla, pero no se elimina de su sitio. La aplicación seguirá recibiendo contenido de un flujo si está configurado para hacerlo.

## Problemas {#section_ehw_ndt_wcb}

En esta versión se resolvieron los problemas de las tablas siguientes.

## Versión de producción

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Error | Encuestas | Se han cambiado las encuestas para utilizar exclusivamente HTTPS. Anteriormente, las encuestas todavía podían utilizarse con HTTP. |
| Error | Studio | Se ha corregido un problema que provocaba que la ventana modal mostrase anuncios al iniciar sesión en Studio para mostrarse demasiado grande en pantallas de baja resolución. |

## Versión de UAT

| Tipo de problema | Componente | Versión de la versión |
|--- |--- |--- |
| Mejora | Tira de película | Se han actualizado las siguientes funciones de accesibilidad para Tira de película: <br><ul><li>Flechas izquierda/derecha corregidas desde < div > a < botón > </li><li>La vista previa del elemento de imagen cambió de una etiqueta ARIA menos descriptiva, "Abrir foto adjunta", a una etiqueta que lee el nombre de la plataforma y el texto de la publicación.</li></ul> |
| Error | Muro de medios | Se ha corregido un problema en Wall Wall por el que las etiquetas no se podían hacer clic cuando se añadía un anuncio de Instagram desde una regla de flujo. |
| Mejora | Muro de medios | Se mejoró la accesibilidad del muro de medios de las siguientes maneras: <br><ul><li>Los modales de apertura y cierre a través de los comandos de teclado ya no cambiarán de enfoque en la parte superior de la página. El enfoque se mantiene en el último elemento centrado antes de la ventana emergente modal.</li><li>El botón Cargar más se puede tabular y activar con la tecla Intro del teclado.</li></ul> |
| Error | Rights Management | Se corrigió un error en el cual no se podía ver el modal de solicitud de derechos después de otorgar derechos para un recurso de Instagram. |

