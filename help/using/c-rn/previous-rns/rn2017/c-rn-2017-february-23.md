---
description: Notas de la versión de la versión del 23 de febrero de 2017.
title: 23 de febrero de 2017
exl-id: 3a5708a1-4be6-447f-ae6e-8f5a37171ed7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 7%

---

# 23 de febrero de 2017{#february}

Notas de la versión de la versión del 23 de febrero de 2017.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Mejora | Android SDK | Se ha reorganizado el SDK para Android para garantizar que los directorios de implementación de ejemplo y referencia se puedan identificar con mayor claridad por su ubicación. |
| Mejora | SDK para Android | El SDK para Android se ha modificado para que ahora admita una versión mínima del SDK de 14 (frente a la versión 16). |
| Error, | Aplicaciones de conversación | Aplicaciones de conversación mejoradas para vincular siempre a perfiles de usuario, incluso sin una integración de autenticación completa. |
| Error, | Mosaic | Se ha corregido un error que ahora proporciona todas las imágenes de Twitter a través de HTTPS. |
| Mejora | Búsqueda y flujos | Se ha agregado la capacidad de buscar por Instagram Places (registros) en las reglas de búsqueda de Instagram de biblioteca y de flujo de Instagram. |
| Error, | Configuración | Se ha corregido un error que impedía guardar cuentas de Twitter Social. |
| Error, | Búsqueda social | Se ha corregido un error que impedía que la opción &quot;Ocultar imágenes explícitas&quot; funcionara correctamente. |
| Mejora | Storify 2 | Se ha mejorado Storify 2 para permitir que los vínculos permanentes abran un modal (anteriormente, la aplicación se desplazaba a la ubicación de la publicación en la página). En el Diseñador de Storify 2, se ha añadido una configuración para alternar entre el comportamiento del vínculo permanente de desplazamiento y modal. El comportamiento del vínculo permanente modal será el comportamiento predeterminado. |
| Mejora | Storify 2 | Se ha mejorado la integración de Google AMP de Storify 2 para producir un archivo CSS más pequeño. |
| Mejora | Transmisiones | Se ha corregido un error en las reglas de Facebook que hacía que el contenido se incluyera con metadatos incompletos. |
| Error, | Transmisiones | Se ha mejorado el contenido (imágenes y vídeos) de las reglas de flujo de correo electrónico para que esté disponible mediante HTTPS. |
| Error, | Transmisiones | Se ha añadido una etiqueta para el valor de radio móvil en los mapas de las reglas de flujo de Twitter. |
| Error, | Transmisiones | Se ha corregido un error con las reglas de flujo de página de Facebook y Facebook para extraer publicaciones con varios archivos adjuntos de medios correctamente. |
| Mejora | Transmisiones | Se ha agregado una nueva función para permitir a los usuarios elegir aplicar o deshabilitar reglas SAFE por regla de flujo. |
| Mejora | Studio | Se ha corregido un error que hacía que el contenido no se publicara o guardara correctamente si ya existía. |
| Error, | Studio | Se ha corregido un error que impedía que se adjuntaran varios y a la dirección URL al usar filtros en Studio. |
| Error, | Studio | Se ha corregido un error que impedía que ciertas casillas de verificación de los filtros de estudio no estuvieran seleccionadas. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | Aplicaciones | Se ha corregido un error para mostrar contenido en modelos de medios con las proporciones de aspecto correctas. |
| Error, | Muro de los medios | Se ha corregido un error que hacía que Muros de medios no se procesaran si se incluían caracteres externos específicos. |
| Error, | Buscar | Se ha corregido un error que hacía que las páginas se cargaran incorrectamente al paginar los resultados de búsqueda con &quot;Concebir imágenes explícitas&quot; habilitado. |
| Mejora | Studio | Se ha aumentado el tiempo de sesión antes de caducar las sesiones de inicio de sesión del usuario de Studio . Una vez que caduque una sesión de Studio, se redirigirá al usuario para que vuelva a iniciar sesión. |
| Error, | Studio | Se ha corregido un error que a veces impedía que los usuarios guardaran las credenciales de Instagram. |
| Error, | Studio | Se ha corregido un error que impedía que la &quot;etiqueta de función&quot; se guardara correctamente cuando se aplicaba. |
