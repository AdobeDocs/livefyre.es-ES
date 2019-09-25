---
description: Notas de la versión de la versión del 23 de febrero de 2017.
seo-description: Notas de la versión de la versión del 23 de febrero de 2017.
seo-title: 23 de febrero de 2017
title: 23 de febrero de 2017
uuid: 9b08acf4-15e9-43b7-8abc-c0d720b156e6
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# February 23, 2017{#february}

Notas de la versión de la versión del 23 de febrero de 2017.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Mejora | Android SDK | Se ha reorganizado el SDK para Android para garantizar que los directorios de implementación de ejemplo y referencia se puedan identificar con mayor claridad por su ubicación. |
| Mejora | Android SDK | Se ha modificado el SDK para Android para que ahora admita una versión mínima del SDK de 14 (en comparación con 16). |
| Error, | Aplicaciones de conversación | Las aplicaciones de conversación mejoradas siempre se vinculan a perfiles de usuario, incluso sin una integración de autenticación completa. |
| Error, | Mosaico | Se ha corregido un error que ahora proporciona todas las imágenes de Twitter mediante HTTPS. |
| Mejora | Buscar y flujos | Se ha agregado la capacidad de buscar por lugares de Instagram (registro de entrada) en las reglas de búsqueda de Instagram y flujo de Instagram de la biblioteca. |
| Error, | Configuración | Se ha corregido un error que impedía guardar cuentas de Twitter Social. |
| Error, | Búsqueda social | Se ha corregido un error que impedía que la opción "Ocultar imágenes explícitas" funcionara correctamente. |
| Mejora | Storify 2 | Se ha mejorado Storify 2 para permitir que los vínculos permanentes abran un modal (anteriormente la aplicación se desplazaba a la ubicación de la publicación en la página). En el Diseñador de Storify 2, hemos agregado una configuración para alternar entre el comportamiento de vínculo permanente de desplazamiento y de desplazamiento. El comportamiento de vínculo permanente modal será el comportamiento predeterminado. |
| Mejora | Storify 2 | Se ha mejorado la integración de Google AMP de Storify 2 para producir un archivo CSS más pequeño. |
| Mejora | Flujos | Se ha corregido un error con las reglas de Facebook que hacía que el contenido se incluyera con metadatos incompletos. |
| Error, | Flujos | Se ha mejorado el contenido (imágenes y vídeos) de las reglas de flujo de correo electrónico para que esté disponible mediante HTTPS. |
| Error, | Flujos | Se ha agregado una etiqueta para el valor de radio móvil en los mapas en las reglas de flujo de Twitter. |
| Error, | Flujos | Se ha corregido un error con las reglas de flujo de página de Facebook y Facebook para extraer publicaciones con varios archivos adjuntos de medios correctamente. |
| Mejora | Flujos | Se ha agregado una nueva función que permite a los usuarios aplicar o deshabilitar reglas SAFE por regla de flujo. |
| Mejora | Studio | Se ha corregido un error que hacía que el contenido no se publicara o guardara correctamente si ya existía. |
| Error, | Studio | Se ha corregido un error que provocaba que varios &amp; se anexaran a la dirección URL al usar filtros en Studio. |
| Error, | Studio | Se ha corregido un error que impedía que determinadas casillas de verificación de los filtros de estudio se activaran sin marcar. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | Aplicaciones | Se ha corregido un error que mostraba el contenido en los modelos de medios con las proporciones de aspecto correctas. |
| Error, | Muro de los medios | Se ha corregido un error que hacía que Muros de medios no se representaran si se incluían caracteres externos específicos. |
| Error, | Buscar | Se ha corregido un error que hacía que las páginas se cargaran incorrectamente al paginar por los resultados de búsqueda con "Ocultación de imágenes explícitas" activada. |
| Mejora | Studio | Se ha aumentado el tiempo de sesión antes de caducar las sesiones de inicio de sesión del usuario de Studio. Una vez que caduque una sesión de Studio, se redirigirá al usuario para que vuelva a iniciar sesión. |
| Error, | Studio | Se ha corregido un error que a veces impedía a los usuarios guardar las credenciales de Instagram. |
| Error, | Studio | Se ha corregido un error que impedía que la "etiqueta de función" se guardara correctamente al aplicarla. |

