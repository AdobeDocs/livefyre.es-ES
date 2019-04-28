---
description: Notas de la versión de la versión del 26 de abril de 2018.
seo-description: Notas de la versión de la versión del 26 de abril de 2018.
seo-title: 26 de abril de 2018
solution: Experience Manager
title: 26 de abril de 2018
uuid: a 84 ebe 5 c -40 d 5-43 b 5-a 300-3 e 041 ab 22046
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 26 de abril de 2018{#april}

Notas de la versión de la versión del 26 de abril de 2018.

## Nuevas características {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* Se ha agregado una nueva función que permite a los clientes configurar un número específico de columnas para un muro de medios. El número de columnas que elija forzará el Muro de medios a ese número de columnas, independientemente del tamaño. De lo contrario, el número de columnas de Muro de medios toma como valor predeterminado &quot;auto&quot;, donde las columnas se ajustan a un número que optimiza el Muro de medios para el tamaño de pantalla.
* En el Muro de medios, ahora hay un conmutador que le permite desactivar la animación automática de muro de medios que se produce cuando se carga una página con un muro de medios.
* Ahora puede elegir el umbral de confianza para las etiquetas inteligentes en flujos. La configuración de la puntuación de precisión (0-100) para las etiquetas permite controlar la precisión de los recursos que se recuperan.
* Se agregaron recomendaciones de moderación. Livefyre ahora examina todas las publicaciones de las aplicaciones de comentarios y predice si la liberará o no basándose en datos históricos y aprendizaje automático. Estas recomendaciones aparecen en modq.
   * Los usuarios pueden desactivar las recomendaciones de moderación, que permiten a los usuarios filtrar modq por el contenido que Livefyre considera que va a vaciar.
   * Se ha agregado la capacidad de filtrar modq por la etiqueta de recomendación de moderación, Papelera.

## Problemas {#section_ehw_ndt_wcb}

En esta versión se resolvieron los problemas de las tablas siguientes.

## Versión de producción

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Error | Rights Management | Se corrigió un problema en el cual las solicitudes de derechos no funcionaban para Recursos después de buscarlas en una Búsqueda social. |
| Mejora | Flujos | Se ha actualizado el mecanismo de flujo continuo que permite que el contenido fluya de Facebook para cumplir con un cambio de back-end creado por Facebook. |
| Error | Comercio UGC | Se ha corregido un problema por el que el botón &quot;Shop&quot; de llamada a acción no se mostraba en una aplicación de mosaico o tira de película ni en un modal de productos al pasar el ratón por encima de una tarjeta con un producto cuando el botón de llamada a acción estaba habilitado. |
| Mejora | Comercio UGC | Se ha corregido un problema por el cual el indicador de Comercio UGC se establecía en &quot;off&quot; de forma predeterminada, en lugar de &quot;activado&quot;. |

## Versión de UAT

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Error | Biblioteca/Búsqueda | Se ha corregido un problema por el que los vídeos no se cargaban correctamente. |
| Mejora | Studio | Se ha agregado la capacidad de ver palabras sugeridas al escribir en nombres de etiquetas. |

