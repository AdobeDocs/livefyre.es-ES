---
description: Notas de la versión de la versión del 15 de febrero de 2018.
title: 15 de febrero de 2018
exl-id: 7276de37-c8cd-4e85-bc92-90c272e5bf94
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 5%

---

# 15 de febrero de 2018{#february}

Notas de la versión de la versión del 15 de febrero de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* **Etiquetas inteligentes.**

   Livefyre utiliza la tecnología de reconocimiento de imágenes de Adobe Sensei para etiquetar automáticamente las imágenes guardadas en la biblioteca.
Con las etiquetas inteligentes, puede ahorrar una gran cantidad de tiempo buscando y moderando contenido. Con las etiquetas inteligentes, puede:

   * Buscar imágenes guardadas para contenido preciso basado en el contenido de la imagen, en lugar de solo texto
   * Recopilar contenido en flujos en función de términos de búsqueda precisos que analicen la imagen, en lugar de solo texto

   Para obtener más información sobre las etiquetas inteligentes, consulte [Etiquetas inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **Mensajes en el producto.** Ahora, cuando inicia sesión en Livefyre Studio, aparece una ventana de anuncios para mostrar actualizaciones sobre las nuevas funciones.
* **UGC para Carrusel.** Ahora puede utilizar todas las funciones de UGC Commerce en la aplicación Livefyre Carousel. Puede crear un botón de llamada a acción y conectar el catálogo de productos a la aplicación para crear una experiencia de ventas a partir de Carrusel.

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Problema | ModQ | Se ha corregido un problema por el cual los anuncios de Instagram marcados como aprobados o enviados a la papelera volvían a entrar en la cola. |
| Mejora | Rights Management | Se ha añadido una mejora para mostrar una advertencia al intentar utilizar cuentas de Instagram caducadas al realizar solicitudes de derechos. |
| Problema | Tendencias | Se ha corregido un problema por el que la aplicación de tendencias seguía permitiendo HTTP en ocasiones, en lugar de HTTPS. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Mejora | Aplicaciones | Se ha agregado la capacidad de eliminar aplicaciones de Livefyre. |
| Problema | Encuestas | Se han cambiado Encuestas para usar HTTPS exclusivamente. Anteriormente, se permitía el uso de Encuestas con HTTP. |
| Problema | UGC | Se ha corregido un problema por el cual UGC en una aplicación de visualización no filtraba por ID de producto como se esperaba. |
