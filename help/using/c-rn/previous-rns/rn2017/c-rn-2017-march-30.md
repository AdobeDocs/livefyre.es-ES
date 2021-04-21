---
description: Notas de la versión de la versión del 30 de marzo de 2017.
title: 30 de marzo de 2017
exl-id: 44c73ff9-8bc1-49c9-b720-aff425e5cd28
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 6%

---

# 30 de marzo de 2017{#march}

Notas de la versión de la versión del 30 de marzo de 2017.

## Versión de producción

| Tipo de incidencia | Componente | Nota de la versión |
|---|---|---|
| Error, | Búsqueda social | Se ha corregido un error que impedía que se publicaran los recursos guardados de YouTube en la Búsqueda social . |
| Mejora | Sincronización social | Twitter Social Sync obsoleto. |
| Mejora | Storify 2 | Se agregó una mejora para mostrar el mensaje &quot;No se encontraron resultados&quot; en la búsqueda por temas de Facebook cuando no se encontraron resultados. |
| Mejora | Transmisiones | Se han agregado reglas de resumen para reglas SEFE a la parte inferior de una página de flujo de Twitter. |
| Error, | Transmisiones | Se ha añadido una mejora para deshabilitar visiblemente la casilla &quot;Usuario verificado&quot; en las reglas de flujo de Twitter cuando se proporcionan autores excluidos. |
| Error, | Transmisiones | Se ha corregido un error para permitir el uso de palabras clave AND y un filtro de ubicación en una regla de Twitter. |
| Error, | Studio | Se ha corregido un error que impedía que la &quot;etiqueta de función&quot; se guardara correctamente cuando se aplicaba. |

## Versión de UAT

| Tipo de incidencia | Componente | Nota de la versión |
|---|---|---|
| Error, | Contenido de la aplicación | Se ha cambiado el comportamiento de &quot;Más información&quot; de modo que, si hay varios eventos de marca anónima en un contenido determinado, siempre se muestre el primer evento. |
| Error, | Biblioteca | Se ha corregido un error que provocaba que fallaran intermitentemente las búsquedas en la biblioteca con hashtags. |
| Error, | Mapas | Se ha corregido un error en Mapas que admitía un gran número de contenido en clústeres en dispositivos iOS. |
| Mejora | Mosaic | Se ha añadido la capacidad de configurar las aplicaciones de Mosaic para que hagan clic en cualquier lugar de una tarjeta de contenido y abran el modal por tipo de animación `none` en designer y `cardAnimation: 'off'`si se crean instancias a través del SDK. |
| Error, | Mosaic | Se ha corregido un error que permitía a los usuarios realizar cambios correctamente en las aplicaciones de Mosaic en Designer. |
| Mejora | Solicitud de derechos | Se ha agregado un nuevo estado de solicitud de derechos llamado &quot;Solicitud fallida&quot; para resaltar cuando los mensajes de solicitud de derechos no se pueden enviar. |
| Mejora | Configuración | Se ha agregado la capacidad para que los clientes creen reglas de moderación de correo no deseado en Configuración. |
| Mejora | Búsqueda social | Se ha corregido un error que impedía que las publicaciones de VK.com se mostraran a través de la URL Búsquedas sociales. |
| Mejora | Búsqueda social | Al buscar contenido de Instagram desde Studio, si la búsqueda se debe a un token de API de Instagram caducado, el mensaje de error ahora se indicará como tal. |
| Error, | Transmisiones | Se ha corregido un error que provocaba que un titular &quot;La aplicación no acepta contenido nuevo&quot; se mostrara falsamente sobre las páginas de reglas de flujo . |
| Mejora | Transmisiones | Se ha modificado el valor predeterminado de las reglas de flujo recién creadas para aplicar reglas SAFE cuando corresponda. |
| Mejora | Emisiones (anteriormente, Depurar reglas) | Se ha eliminado la opción &quot;Vinos&quot; únicamente de las reglas Flujo/Depuración de Twitter, ya que ahora los Vines se muestran como vídeos de Twitter. |
| Error, | Studio Shell | Se ha corregido un error para que Livefyre Studio se cargara si https:// se anteponía explícitamente a la dirección URL. |
