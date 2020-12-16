---
description: Notas de la versión de la versión del 30 de marzo de 2017.
seo-description: Notas de la versión de la versión del 30 de marzo de 2017.
seo-title: 30 de marzo de 2017
title: 30 de marzo de 2017
uuid: 2adf04a9-6c52-4fa1-a0c9-b2d3886305e9
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 7%

---


# 30 de marzo de 2017{#march}

Notas de la versión de la versión del 30 de marzo de 2017.

## Versión de producción

| Tipo de incidencia | Componente | Nota de la versión |
|---|---|---|
| Error, | Búsqueda social | Se ha corregido un error que impedía que se publicaran los recursos guardados de YouTube en la búsqueda social. |
| Mejora | Sincronización social | Sincronización social de Twitter obsoleta. |
| Mejora | Storify 2 | Se añadió una mejora para mostrar el mensaje &quot;No se encontraron resultados&quot; en la búsqueda por temas de Facebook cuando no se encontraron resultados. |
| Mejora | Flujos | Reglas de resumen añadidas para reglas SAFE en la parte inferior de una página de flujo de Twitter. |
| Error, | Flujos | Se ha añadido una mejora para deshabilitar de forma visible la casilla &quot;Usuario verificado&quot; en las reglas de flujo de Twitter cuando se proporcionan autores excluidos. |
| Error, | Flujos | Se ha corregido un error que permitía el uso de palabras clave ANDing y un filtro de ubicación en una regla de Twitter. |
| Error, | Studio | Se ha corregido un error que impedía que la &quot;etiqueta de función&quot; se guardara correctamente al aplicarla. |

## Versión de UAT

| Tipo de incidencia | Componente | Nota de la versión |
|---|---|---|
| Error, | Contenido de la aplicación | Se ha cambiado el comportamiento de &quot;Más información&quot; de modo que, si hay varios eventos de marca anónima en un determinado contenido, siempre se muestra el evento más antiguo. |
| Error, | Biblioteca | Se ha corregido un error que provocaba que las búsquedas de biblioteca con hashtags fallaran de forma intermitente. |
| Error, | Mapas | Se ha corregido un error en los mapas para admitir un gran número de contenido en clústeres en dispositivos iOS. |
| Mejora | Mosaico | Se ha añadido la capacidad de configurar aplicaciones de mosaico para que hagan clic en cualquier lugar de una tarjeta de contenido para abrir el modal por tipo de animación `none` en designer y `cardAnimation: 'off'`si se crea una instancia a través del SDK. |
| Error, | Mosaico | Se ha corregido un error que permitía a los usuarios realizar cambios correctamente en las aplicaciones de mosaico en Designer. |
| Mejora | Solicitud de derechos | Se ha añadido un nuevo estado de solicitud de derechos denominado &quot;Error de solicitud&quot; para resaltar cuándo no se pueden enviar los mensajes de solicitud de derechos. |
| Mejora | Configuración | Se añadió la capacidad de los clientes para crear reglas de moderación de correo no deseado en Configuración. |
| Mejora | Búsqueda social | Se ha corregido un error que impedía que las publicaciones de VK.com se mostraran a través de las búsquedas sociales de URL. |
| Mejora | Búsqueda social | Al buscar contenido de Instagram desde Studio, si la búsqueda se debe a un testigo de la API de Instagram caducado, el mensaje de error se indicará como tal. |
| Error, | Flujos | Se ha corregido un error que provocaba que se mostrara falsamente una pancarta &quot;La aplicación no acepta contenido nuevo&quot; en la parte superior de las páginas de reglas de flujo. |
| Mejora | Flujos | Se ha modificado el valor predeterminado de las reglas de flujo recién creadas para aplicar reglas SAFE cuando corresponda. |
| Mejora | Flujos (anteriormente, Reglas de depuración) | Se ha eliminado la opción &quot;Viñetas&quot; únicamente de las reglas de flujo/depuración de Twitter, ya que las vides ahora se muestran como vídeos de Twitter. |
| Error, | Studio Shell | Se ha corregido un error por el que Livefyre Studio se cargaba si https:// se añadía explícitamente a la URL. |

