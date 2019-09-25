---
description: Notas de la versión de la versión del 15 de febrero de 2018.
seo-description: Notas de la versión de la versión del 15 de febrero de 2018.
seo-title: 15 de febrero de 2018
solution: Experience Manager
title: 15 de febrero de 2018
uuid: ee46f088-9fb7-49e2-a42c-e0d4b2f24a32
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# February 15, 2018{#february}

Notas de la versión de la versión del 15 de febrero de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* **Etiquetas inteligentes.**

   Livefyre utiliza la tecnología de reconocimiento de imágenes de Adobe Sensei para etiquetar automáticamente las imágenes guardadas en la biblioteca.
Con las etiquetas inteligentes puede ahorrar una cantidad considerable de tiempo en la búsqueda y moderación del contenido. Con las etiquetas inteligentes, puede:

   * Buscar imágenes guardadas para contenido preciso basado en el contenido de la imagen, en lugar de solo texto
   * Recopilar contenido en flujos en función de términos de búsqueda precisos que analicen la imagen, en lugar de solo texto
   Para obtener más información sobre las etiquetas inteligentes, consulte Etiquetas [inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **Mensajes en el producto.** Ahora, cuando inicia sesión en Livefyre Studio, aparece una ventana de anuncios para mostrar las actualizaciones sobre las nuevas funciones.
* **UGC para Carrusel.** Ahora puede usar todas las funciones de comercio UGC en la aplicación de carrusel de Livefyre. Puede crear un botón de llamada a acción y conectar el catálogo de productos a la aplicación para crear una experiencia de ventas a partir de Carrusel.

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Problema | ModQ | Se corrigió un problema en el cual las publicaciones de Instagram marcadas como aprobadas o desechadas volvían a entrar en la cola. |
| Mejora | Rights Management | Se agregó una mejora para mostrar una advertencia al intentar usar cuentas de Instagram caducadas al realizar solicitudes de derechos. |
| Problema | Tendencias | Se ha corregido un problema por el que la aplicación de tendencias aún permitía HTTP en ocasiones, en lugar de HTTPS. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Mejora | Aplicaciones | Se ha agregado la capacidad de eliminar aplicaciones de Livefyre. |
| Problema | Encuestas | Se han cambiado las encuestas para usar HTTPS exclusivamente. Anteriormente, aún se permitía el uso de encuestas con HTTP. |
| Problema | UGC | Se corrigió un problema en el cual UGC en una aplicación de visualización no filtraba por ID de producto como se esperaba. |

