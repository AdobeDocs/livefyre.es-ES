---
description: Notas de la versión del 1 de noviembre de 2018.
seo-description: Notas de la versión del 1 de noviembre de 2018.
seo-title: 1 de noviembre de 2018
solution: Experience Manager
title: 1 de noviembre de 2018
uuid: ed 1 a 3 bf 1-b 3 f 1-4746-8462-07283723 ba 62
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 1 de noviembre de 2018{#november}

Notas de la versión del 1 de noviembre de 2018.

## Nuevas características {#section_syx_mdt_wcb}

Se han publicado las siguientes funciones nuevas en la versión de producción de esta versión:

* Etiquetas inteligentes de vídeo

   Aproveche el estado de la tecnología de percepción del equipo de arte, con tecnología de Adobe Sensei, para etiquetar automáticamente contenido de vídeo al guardarlo en la biblioteca. Las etiquetas inteligentes le ayudan a administrar UGC de forma más eficaz pero también crean reglas de depuración super precisas (flujos) que recopilan contenido en función de lo que hay en el vídeo, no solo del texto, lo que ahorra un esfuerzo importante moderando contenido no deseado.

   Detalles de la función:

   * Las etiquetas inteligentes se añaden automáticamente a los vídeos obtenidos de la búsqueda social, flujos y archivos de vídeo cargados en la biblioteca. Ver etiquetas en los detalles del recurso para un vídeo individual
   * Vídeos de etiquetas en formatos. MP 4. MOV y AVI
   * Vídeos de etiquetas de hasta 60 segundos o 50 MB
   * Se aplican dos categorías de etiquetas inteligentes a los vídeos: características (animals, objetos, lugares, etc.) y acciones (running, walk, singing, etc.)
   Para obtener más información, consulte [Etiquetas inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Límite de tasa de Instagram

   Instagram ha cambiado el número de solicitudes que cualquier empresa que utilice la API de Instagram, incluido Livefyre, puede crear desde 5.000 solicitudes por hora por testigo a 200 solicitudes una hora por testigo. Esto se conoce como limitación *de tasa*. Para obtener más información, consulte [Limitación de tasa de Instagram](/help/using/c-streams/c-instagram-rate-limiting.md).

* Archivos de audio de la biblioteca

   Ahora puede realizar las siguientes funciones en archivos de audio desde el panel Biblioteca:

   * Buscar
   * Vista preliminar
   * Importar
   * Filtrar por archivos de audio
   * Arrastrar y soltar archivos en el diseñador

## Problemas {#section_ehw_ndt_wcb}

No se han resuelto nuevos problemas en la versión de producción de esta versión. Consulte [la sección anterior](#c_rn/section_syx_mdt_wcb).

## Versión de UAT {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

Los problemas de las tablas siguientes se resolvieron en la versión UAT de esta versión.

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Mejora | RGPD | Se eliminarán todos los datos atribuidos a clientes anteriores dentro de Analytics. |
| Error | Biblioteca | Se ha corregido un problema por el que un vídeo cargado a la biblioteca y luego visto en detalle de recurso no se mostraba correctamente. |
| Error | Mosaico | Se ha corregido un problema por el que un mosaico mostraba la última parte de contenido de un carrusel de Instagram como miniatura, en lugar de una tarjeta. |
| Error | Búsqueda social | Se corrigió un problema en el cual la búsqueda social de Instagram no funcionaba según lo esperado. |

