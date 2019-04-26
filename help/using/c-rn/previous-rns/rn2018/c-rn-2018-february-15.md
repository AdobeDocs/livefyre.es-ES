---
description: Notas de la versión de la versión del 15 de febrero de 2018.
seo-description: Notas de la versión de la versión del 15 de febrero de 2018.
seo-title: 15 de febrero de 2018
solution: Experience Manager
title: 15 de febrero de 2018
uuid: ee 46 f 088-9 fb 7-49 e 2-a 42 c-e 0 d 4 b 2 f 24 a 32
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 15 de febrero de 2018{#february}

Notas de la versión de la versión del 15 de febrero de 2018.

## Nuevas características {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* **Etiquetas inteligentes.**

   Livefyre utiliza la tecnología de reconocimiento de imágenes de Adobe Sensei para etiquetar imágenes automáticamente que guarde en la biblioteca.
Con Etiquetas inteligentes puede ahorrar una considerable cantidad de tiempo y moderar contenido. Con Etiquetas inteligentes puede:

   * Buscar imágenes guardadas para un contenido preciso según el contenido de la imagen, en lugar de solo texto
   * Recopile contenido en flujos basados en términos de búsqueda precisos que analicen la imagen, en lugar de solo texto
   Para obtener más información sobre Etiquetas inteligentes, consulte [Etiquetas inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **Mensajes internos del producto.** Ahora, al iniciar sesión en Livefyre Studio, aparece una ventana de anuncios para mostrar las actualizaciones sobre las nuevas funciones.
* **UGC para Carrusel.** Ahora puede utilizar todas las funciones de Comercio UGC en la aplicación de carrusel de Livefyre. Puede crear un botón de llamada a acción y conectar el catálogo de productos a la aplicación para crear una experiencia de ventas desde Carrusel.

## Problemas {#section_ehw_ndt_wcb}

En esta versión se resolvieron los problemas de las tablas siguientes.

## Versión de producción

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Problema | Modq | Se corrigió un problema en el cual las publicaciones de Instagram marcadas como aprobadas o eliminadas volvían a entrar en la cola. |
| Mejora | Rights Management | Se agregó una mejora para mostrar una advertencia al intentar utilizar cuentas caducadas de Instagram al hacer solicitudes de derechos. |
| Problema | Tendencias | Se ha corregido un problema con la aplicación de tendencias que todavía permitía HTTP en lugar de HTTPS. |

## Versión de UAT

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Mejora | Aplicaciones | Se ha agregado la capacidad de eliminar aplicaciones de Livefyre. |
| Problema | Encuestas | Se han cambiado las encuestas para utilizar exclusivamente HTTPS. Anteriormente, las encuestas todavía podían utilizarse con HTTP. |
| Problema | UGC | Se corrigió un problema en el que UGC en una aplicación de visualización no se filtraba por ID de producto según lo esperado. |

