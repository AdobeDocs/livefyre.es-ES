---
description: Notas de la versión de la versión del 26 de abril de 2018.
seo-description: Notas de la versión de la versión del 26 de abril de 2018.
seo-title: 26 de abril de 2018
solution: Experience Manager
title: 26 de abril de 2018
uuid: a84ebe5c-40d5-43b5-a300-3e041ab22046
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# April 26, 2018{#april}

Notas de la versión de la versión del 26 de abril de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* Se ha agregado una nueva función que permite a los clientes configurar un número específico de columnas para un muro multimedia. El número de columnas que elija fuerza el Muro de medios a ese número de columnas, independientemente del tamaño. De lo contrario, el número de columnas de Muro de medios predeterminado es "auto", donde las columnas se ajustan a un número que optimiza Muro de medios para el tamaño de pantalla.
* En Media Wall Designer ahora hay un conmutador que permite desactivar la animación automática de Media Wall que se produce cuando se carga una página con un Media Wall.
* Ahora puede elegir el umbral de confianza para las etiquetas inteligentes en los flujos. La definición de la puntuación de precisión (0-100) para las etiquetas permite controlar la precisión de los recursos que se están recuperando.
* Se agregaron recomendaciones de moderación. Livefyre ahora explora cada publicación al comentar aplicaciones y predice si la descartará o no en base a datos históricos y aprendizaje automático. Estas recomendaciones aparecen en ModQ.
   * Los usuarios pueden desactivar las recomendaciones de moderación, lo que permite a los usuarios filtrar ModQ por el contenido que Livefyre piensa que va a eliminar.
   * Se ha agregado la capacidad de filtrar ModQ por la etiqueta de recomendación de moderación, Papelera.

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | Rights Management | Se corrigió un problema en el cual las solicitudes de derechos no funcionaban para Recursos después de buscarlas en una búsqueda social. |
| Mejora | Flujos | Se ha actualizado el mecanismo de flujo que permite que el contenido se transmita desde Facebook para cumplir con un cambio de back-end creado por Facebook. |
| Error, | Comercio UGC | Se corrigió un problema en el cual el botón "Tienda" de llamada a acción no se mostraba en una aplicación de tira de película o mosaico o en un modal de productos al pasar el ratón sobre una tarjeta con un producto cuando el botón de llamada a acción está activado. |
| Mejora | Comercio UGC | Se corrigió un problema en el cual el indicador de comercio UGC se establecía en "desactivado" de forma predeterminada, en lugar de en "activado". |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | Biblioteca/Búsqueda | Se ha corregido un problema que impedía que los vídeos se cargaran correctamente. |
| Mejora | Studio | Se ha agregado la capacidad de ver palabras sugeridas al escribir nombres de etiquetas. |

