---
description: Notas de la versión de la versión del 16 de noviembre de 2017.
seo-description: Notas de la versión de la versión del 16 de noviembre de 2017.
seo-title: 16 de noviembre de 2017
solution: Experience Manager
title: 16 de noviembre de 2017
uuid: e7d09640-d2c1-4d23-8fa6-ecc90d0b2daa
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# November 16, 2017{#november}

Notas de la versión de la versión del 16 de noviembre de 2017.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | AEM, Biblioteca | Se ha corregido un error que no devolvía ningún resultado al utilizar la búsqueda de etiquetas y clasificación en la biblioteca. |
| Error, | Aplicaciones | Se corrigió un problema en el cual la etiqueta de función no se mostraba en una aplicación de una sola tarjeta. |
| Error, | Carrusel | Se corrigió un problema en el cual Carrusel no aparecía en Designer. |
| Error, | Comentarios | Se corrigieron los recuentos de comentarios inexactos en las aplicaciones de comentarios. |
| Mejora | Tarjeta de función | La aplicación de la tarjeta de características tiene todas las funcionalidades comerciales activadas. |
| Mejora | Tira de película | Hemos añadido opciones de tamaño para la tira de película para que el usuario pueda tener más control sobre el aspecto de las imágenes en la aplicación. |
| Error, | Subprocesos en caliente | Se corrigieron los mensajes de error de los subprocesos interactivos para hacerlos más seguros. |
| Mejora | Biblioteca | Los clientes pueden eliminar las etiquetas inteligentes aplicadas por nuestro sistema de AI. Una vez eliminadas, no verán esas etiquetas en los resultados de búsqueda. |
| Error, | Biblioteca | Se corrigió un problema en el cual una imagen no se mostraba correctamente después de agregarla a la biblioteca desde una búsqueda social. |
| Error, | Biblioteca | Se ha corregido un problema que hacía que la creación de carpetas fuera lenta. |
| Error, | Biblioteca | Los usuarios ahora pueden publicar archivos .mov en colecciones. |
| Error, | Biblioteca | Las imágenes con caracteres especiales en el título no se cargarían en la biblioteca, ya se ha corregido. |
| Mejora | Biblioteca | Hemos actualizado nuestro algoritmo de clasificación de "relevancia" cuando un usuario busca etiquetas inteligentes, de modo que cuando un usuario activa la clasificación de "relevancia" en la búsqueda de biblioteca, se aplica el nuevo algoritmo de clasificación. Este nuevo algoritmo de clasificación tiene en cuenta las puntuaciones de precisión de etiquetas inteligentes, el número de estrellas asignadas por usuario y la edad del documento. El objetivo es que la experiencia de búsqueda de etiquetas sea más precisa para el usuario. |
| Mejora | Biblioteca | Cuando un cliente guarda un recurso en la biblioteca, Livefyre emplea la tecnología de aprendizaje automático Adobe Sensei para añadir etiquetas que describan lo que se encuentra en la imagen del recurso automáticamente. Esto permite al usuario buscar esas etiquetas en el sistema. |
| Mejora | Biblioteca | Cuando un cliente guarda un recurso basado en imágenes en la biblioteca, Livefyre lo etiquetará automáticamente mediante la tecnología Adobe AI, extrayendo funciones, categorías y propiedades estéticas del sistema. Esto permite al usuario buscar en la biblioteca por lo que hay dentro de las imágenes, no sólo por el texto. |
| Error, | Identidad de Livefyre | Los avatares no se cargaban correctamente para la implementación de Microsoft de la identidad LF, esto se ha corregido. |
| Error, | ModQ | Se corrigió un problema en el cual la premoderación de flujos y ModQ no mostraban todo el contenido correctamente. |
| Mejora | Configuración | Los clientes ahora pueden visitar nuestra política de privacidad y las condiciones de servicio de Adobe en un pie de página en Configuración. |
| Mejora | Flujos | Se ha corregido un error en la moderación previa de reglas de flujo basadas en correo electrónico. |
| Mejora | Flujos | Se ha agregado la capacidad de filtrar el contenido del flujo por idioma. |
| Mejora | Usuarios | Se ha agregado la capacidad de usar archivos .png para avatares del usuario. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | Administrador de aplicaciones | Se ha corregido un problema con la búsqueda de etiquetas de aplicación en App Manager. |
| Error, | Biblioteca | Se ha corregido un problema que impedía añadir estrellas para varios fragmentos de contenido a la vez en la biblioteca de recursos. |
| Error, | Studio | Se ha corregido un problema que impedía que algunos usuarios iniciaran sesión en Livefyre. |

