---
description: Notas de la versión de la versión del 1 de noviembre de 2018.
seo-description: Notas de la versión de la versión del 1 de noviembre de 2018.
seo-title: 1 de noviembre de 2018
solution: Experience Manager
title: 1 de noviembre de 2018
uuid: ed1a3bf1-b3f1-4746-8462-07283723ba62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 1 de noviembre de 2018{#november}

Notas de la versión de la versión del 1 de noviembre de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

En la versión de producción de esta versión se lanzaron las siguientes nuevas funciones:

* Etiquetas inteligentes de vídeo

   Aproveche la tecnología de visión informática más avanzada, con tecnología Adobe Sensei, para etiquetar automáticamente el contenido de vídeo al guardarlo en la biblioteca. Las etiquetas inteligentes le ayudan a administrar UGC de forma más eficaz, pero también a crear reglas de depuración (flujos) muy precisas que recopilan contenido en función de lo que hay en el vídeo, no solo del texto, lo que le ahorra un esfuerzo considerable al moderar el contenido no deseado.

   Detalles de la función:

   * Las etiquetas inteligentes se agregan automáticamente a los vídeos obtenidos a partir de búsquedas sociales, flujos y archivos de vídeo cargados en la biblioteca. Ver etiquetas en los detalles de recursos de un vídeo individual
   * Etiqueta vídeos en formato .MP4, .MOV y AVI
   * Etiqueta vídeos de hasta 60 segundos o 50 MB
   * Se aplican dos categorías de etiquetas inteligentes a los vídeos: características (animales, objetos, lugares, etc.) y acciones (correr, caminar, cantar, etc.)
   For more information see [Smart Tags](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Límite de la tasa de Instagram

   Instagram ha cambiado el número de solicitudes que cualquier empresa que utilice la API de Instagram, incluida Livefyre, puede realizar de 5.000 solicitudes por hora por token a 200 solicitudes por hora por token. Esto se conoce como limitación de *velocidad*. Para obtener más información, consulte Límite de velocidad de [Instagram](/help/using/c-streams/c-instagram-rate-limiting.md).

* Archivos de audio de la biblioteca

   Ahora puede realizar las siguientes funciones en archivos de audio desde el panel Biblioteca:

   * Buscar
   * Vista previa
   * Importar
   * Filtrar por archivos de audio
   * Arrastrar y soltar archivos en el diseñador

## Problemas {#section_ehw_ndt_wcb}

No se resolvieron nuevos problemas en la versión de producción de esta versión. Consulte [la sección anterior](#c_rn/section_syx_mdt_wcb).

## Versión de UAT {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

Los problemas de las tablas siguientes se resolvieron en la versión UAT de esta versión.

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Mejora | RGPD | Se eliminarán todos los datos atribuidos a clientes anteriores dentro de Analytics. |
| Error, | Biblioteca | Se corrigió un problema en el cual un vídeo cargado en la biblioteca y visualizado posteriormente con los detalles del recurso no se mostraba correctamente. |
| Error, | Mosaico | Se corrigió un problema en el cual un mosaico mostraba la última parte de contenido de un carrusel de Instagram como una miniatura, en lugar de una tarjeta. |
| Error, | Búsqueda social | Se corrigió un problema en el cual la búsqueda social en Instagram no funcionaba según lo esperado. |

