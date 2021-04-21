---
description: Notas de la versión de la versión del 1 de noviembre de 2018.
title: 1 de noviembre de 2018
exl-id: b12b6a56-f14f-4447-9fde-25cb3acf6665
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 4%

---

# 1 de noviembre de 2018{#november}

Notas de la versión de la versión del 1 de noviembre de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

En la versión de producción de esta versión se lanzaron las siguientes funciones nuevas:

* Etiquetas inteligentes de vídeo

   Aproveche la tecnología de visión informática más avanzada, con tecnología de Adobe Sensei, para etiquetar automáticamente el contenido de vídeo cuando lo guarde en la biblioteca. Las etiquetas inteligentes le ayudan a administrar el UGC de forma más eficaz, pero también a crear reglas de depuración (transmisiones) superprecisas que recopilen contenido en función de lo que hay en el vídeo, no solo el texto, lo que le ahorra un esfuerzo significativo para moderar el contenido no deseado.

   Detalles de las funciones:

   * Las etiquetas inteligentes se añaden automáticamente a los vídeos procedentes de búsquedas sociales, flujos y archivos de vídeo cargados en la biblioteca. Ver etiquetas en los detalles de recursos de un vídeo individual
   * Etiqueta vídeos en los formatos .MP4, .MOV y AVI
   * Etiqueta vídeos de hasta 60 segundos o 50 MB
   * Se aplican dos categorías de etiquetas inteligentes a los vídeos: características (animales, objetos, lugares, etc.) y acciones (correr, caminar, cantar, etc.)

   Para obtener más información, consulte [Etiquetas inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Limitación de la tasa de instagram

   Instagram ha cambiado el número de solicitudes que cualquier empresa que utilice la API de Instagram, incluido Livefyre, puede realizar de 5000 solicitudes por hora por token a 200 solicitudes por hora por token. Esto se conoce como *limitación de velocidad*. Para obtener más información, consulte [Límite de velocidad de Instagram](/help/using/c-streams/c-instagram-rate-limiting.md).

* Archivos de audio de la biblioteca

   Ahora puede realizar las siguientes funciones en archivos de audio desde el panel de biblioteca:

   * Buscar
   * Vista previa
   * Importar
   * Filtrar por archivos de audio
   * Arrastrar y soltar archivos en el diseñador

## Problemas {#section_ehw_ndt_wcb}

No se han resuelto nuevos problemas en la versión de producción de esta versión. Consulte la [sección anterior](#c_rn/section_syx_mdt_wcb).

## Versión UAT {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

Los problemas de las tablas siguientes se resolvieron en la versión UAT de esta versión.

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Mejora | RGPD | Se eliminarán todos los datos atribuidos a clientes anteriores dentro de Analytics. |
| Error, | Biblioteca | Se ha corregido un problema por el cual un vídeo cargado en la biblioteca y luego visualizado en detalle de recursos no se mostraba correctamente. |
| Error, | Mosaic | Se ha corregido un problema por el cual un mosaico mostraba la última parte de contenido de un carrusel de Instagram como una miniatura, en lugar de una tarjeta. |
| Error, | Búsqueda social | Se ha corregido un problema por el cual la búsqueda social de Instagram no funcionaba como se esperaba. |
