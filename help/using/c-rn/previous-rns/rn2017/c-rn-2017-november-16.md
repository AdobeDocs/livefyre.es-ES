---
description: Notas de la versión de la versión del 16 de noviembre de 2017.
title: 16 de noviembre de 2017
exl-id: 167b8c7d-f2fb-4735-9681-d349646ec3eb
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 8%

---

# 16 de noviembre de 2017{#november}

Notas de la versión de la versión del 16 de noviembre de 2017.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | AEM, biblioteca | Se ha corregido un error sin que se devolvieran resultados al utilizar la búsqueda de etiqueta y clasificación en la biblioteca. |
| Error, | Aplicaciones | Se ha corregido un problema en el cual la etiqueta de características no se mostraba en una aplicación de tarjeta única. |
| Error, | Carrusel | Se ha corregido un problema por el que Carrusel no aparecía en Designer. |
| Error, | Comentarios | Se han corregido recuentos de comentarios inexactos en las aplicaciones de comentarios. |
| Mejora | Tarjeta de características | La aplicación de tarjetas de características tiene todas las funcionalidades comerciales activadas. |
| Mejora | Tira de película | Hemos añadido opciones de cambio de tamaño para la tira de película para que el usuario pueda tener más control sobre el aspecto de las imágenes en la aplicación. |
| Error, | Subprocesos en caliente | Se han corregido los mensajes de error de los subprocesos activos para que sean más seguros. |
| Mejora | Biblioteca | Los clientes pueden eliminar las etiquetas inteligentes aplicadas por nuestro sistema de IA. Una vez eliminadas, no verán esas etiquetas en los resultados de búsqueda. |
| Error, | Biblioteca | Se ha corregido un problema por el cual una imagen no se mostraba correctamente después de agregarla a la biblioteca desde una búsqueda social. |
| Error, | Biblioteca | Se ha corregido un problema que hacía que la creación de carpetas fuera lenta. |
| Error, | Biblioteca | Los usuarios ahora pueden publicar archivos .mov en colecciones. |
| Error, | Biblioteca | Las imágenes con caracteres especiales en el título no se cargarían en la biblioteca, pero ahora se ha corregido. |
| Mejora | Biblioteca | Hemos actualizado nuestro algoritmo de clasificación de &quot;relevancia&quot; cuando un usuario busca etiquetas inteligentes, por lo que cuando un usuario alterna la clasificación de &quot;relevancia&quot; en la búsqueda de bibliotecas, se aplica el nuevo algoritmo de clasificación. Este nuevo algoritmo de clasificación tiene en cuenta las puntuaciones de precisión de etiquetas inteligentes, el número de estrellas asignadas por usuario y la edad del documento. El objetivo es hacer que la experiencia de búsqueda de etiquetas sea más precisa para el usuario. |
| Mejora | Biblioteca | Cuando un cliente guarda un recurso en la biblioteca, Livefyre emplea la tecnología de aprendizaje automático de Adobe Sensei para agregar etiquetas que describan lo que se encuentra en la imagen del recurso automáticamente. Esto permite al usuario buscar esas etiquetas en el sistema. |
| Mejora | Biblioteca | Cuando un cliente guarda un recurso basado en imágenes en la biblioteca, Livefyre lo etiquetará automáticamente mediante la tecnología de IA de Adobe, extrayendo funciones, categorías y propiedades estéticas del sistema. Esto permite al usuario buscar en la biblioteca según el contenido de las imágenes, no solo el texto. |
| Error, | Identidad de Livefyre | Los avatares no se cargaban correctamente para la implementación de Microsoft de la identidad LF, esto se ha solucionado. |
| Error, | ModQ | Se ha corregido un problema por el cual las versiones de premoderación y ModQ no mostraban todo el contenido correctamente. |
| Mejora | Configuración | Los clientes ahora pueden visitar nuestra política de privacidad y las condiciones de servicio del Adobe en un pie de página en Configuración. |
| Mejora | Transmisiones | Se ha corregido un error en la premoderación de las reglas de flujo basadas en correo electrónico. |
| Mejora | Transmisiones | Se ha agregado la capacidad de filtrar el contenido de la emisión por idioma. |
| Mejora | Usuarios | Se ha agregado la capacidad de usar archivos .png para avatares del usuario. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | Administrador de aplicaciones | Se ha corregido un problema con la búsqueda de etiquetas de aplicación en el Administrador de aplicaciones. |
| Error, | Biblioteca | Se ha corregido un problema que impedía añadir estrellas para varios fragmentos de contenido a la vez en la biblioteca de recursos. |
| Error, | Studio | Se ha corregido un problema que impedía que algunos usuarios iniciaran sesión en Livefyre. |
