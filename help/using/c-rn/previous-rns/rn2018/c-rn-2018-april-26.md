---
description: Notas de la versión de la versión del 26 de abril de 2018.
title: 26 de abril de 2018
exl-id: af0ee64d-d60c-4b21-a628-08848313781c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 4%

---

# 26 de abril de 2018{#april}

Notas de la versión de la versión del 26 de abril de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* Se ha agregado una nueva función que permite a los clientes configurar un número específico de columnas para un muro de medios. El número de columnas que elija forzará el muro de medios a ese número de columnas, independientemente de su tamaño. De lo contrario, el número de columnas de Muro de medios toma como valor predeterminado &quot;auto&quot;, donde las columnas se ajustan a un número que optimiza el Muro de medios para el tamaño de la pantalla.
* En el Diseñador de muro de medios ahora hay un conmutador que le permite desactivar la animación automática de muro de medios que se produce cuando se carga una página con un muro de medios.
* Ahora puede elegir el umbral de confianza para las etiquetas inteligentes en los flujos. La configuración de la puntuación de precisión (0-100) para las etiquetas permite controlar la precisión de los recursos que se recuperan.
* Se agregaron recomendaciones de moderación. Ahora Livefyre analiza cada publicación comentando aplicaciones y predice si la va a enviar a la papelera o no en función de los datos históricos y del aprendizaje automático. Estas recomendaciones aparecen en ModQ.
   * Los usuarios pueden desactivar las recomendaciones de moderación, lo que permite a los usuarios filtrar ModQ por el contenido que Livefyre piensa que va a enviar a la basura.
   * Se ha agregado la capacidad de filtrar ModQ por medio de la etiqueta de recomendación de moderación, Papelera.

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | Rights Management | Se ha corregido un problema en el cual las solicitudes de derechos no funcionaban para los recursos después de encontrarlos en una búsqueda social. |
| Mejora | Transmisiones | Se ha actualizado el mecanismo de flujo continuo que permite que el contenido se transmita desde Facebook para cumplir con un cambio back-end creado por Facebook. |
| Error, | Comercio UGC | Se ha corregido un problema en el cual el botón &quot;Comprar&quot; de CTA no se mostraba en una aplicación de Mosaic o FilmStrip o en un modal de productos al pasar el ratón por encima de una tarjeta con un producto cuando el botón CTA está habilitado. |
| Mejora | Comercio UGC | Se ha corregido un problema por el que el indicador de comercio UGC se establecía en &quot;desactivado&quot; de forma predeterminada, en lugar de en &quot;activado&quot;. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | Biblioteca/Buscar | Se ha corregido un problema por el que los vídeos no se cargaban correctamente. |
| Mejora | Studio | Se ha agregado la capacidad de ver palabras sugeridas al escribir nombres de etiquetas. |
