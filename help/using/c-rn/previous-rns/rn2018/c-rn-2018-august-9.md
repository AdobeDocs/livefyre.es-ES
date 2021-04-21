---
description: Notas de la versión de la versión del 9 de agosto de 2018.
title: 9 de agosto de 2018
exl-id: 7b2fb562-33bf-4c34-ab83-5fc34f5d1f4f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 8%

---

# 9 de agosto de 2018{#august}

Notas de la versión de la versión del 9 de agosto de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

**Etiquetas inteligentes de vídeo:** ahora los usuarios pueden ver etiquetas inteligentes para vídeos de menos de 50 MB.

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | Contenido de la aplicación | Se ha corregido un problema que impedía que los administradores y los administradores de contenido editaran contenido en Contenido de aplicación. |
| Mejora | Aplicaciones | Las redes sociales han realizado cambios en la privacidad que significan que las menciones sociales ya no serán compatibles con Facebook ni Twitter. |
| Mejora | Aplicaciones | Las redes sociales han realizado cambios en la privacidad. Se ha eliminado la función &quot;Publicar en&quot; que publica automáticamente contenido en redes sociales (Facebook, LinkedIn, Twitter). |
| Mejora | RGPD | Se ha eliminado el modo de alternancia para detalles de la página de detalles de la solicitud en Configuración > Privacidad. Se puede acceder a la opción de alternancia del modo Detalles añadiendo /dbg al final de la dirección URL. |
| Error, | Integración: AEM | Se ha corregido un problema por el cual al arrastrar y soltar aplicaciones de Livefyre en AEM aparecía crear varias aplicaciones. |
| Error, | Biblioteca | Se ha corregido un problema en el cual un recurso no se guardaba correctamente en la biblioteca. |
| Error, | Identidad de Livefyre | Se ha corregido un problema con la identidad de LF que provocaba errores 403 al iniciar sesión. |
| Error, | Búsqueda social | Se ha corregido un problema en el cual los usuarios no podían buscar anuncios públicos de Facebook usando la opción URL en Búsqueda social. |
| Mejora | Sincronización social | Las redes sociales han realizado cambios en la privacidad que significan que la sincronización social ya no será compatible con Facebook. |
| Mejora | Transmisiones | Ahora, al eliminar una aplicación, se eliminan todos los flujos asociados a ella. |
| Mejora | Studio | Los clientes ahora tienen la capacidad de emitir eventos de Livefyre a Adobe Analytics individualmente, en lugar de hacerlo en lotes. |
| Mejora | Studio | Las ventanas modales que se muestran en las aplicaciones de conversación para redes sociales ahora serán ventanas modales de la red social en lugar de Adobe Experience Manager Livefyre u otras ventanas modales con marca. |

## Versión de UAT

Los problemas de las tablas siguientes se resolvieron en la versión de UAT.

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | RGPD | Se ha corregido un problema por el cual los mensajes de exclusión no se mostraban en algunos vídeos de Instagram. |
| Error, | Biblioteca | Se ha corregido un problema por el cual una tarjeta con derechos otorgados mostraba manualmente el estado de solicitud de derechos incorrecto. |
| Error, | Biblioteca | Se ha corregido un problema que impedía guardar un recurso en una carpeta. |
| Error, | Biblioteca/Buscar | Se ha restaurado la capacidad de buscar direcciones URL desde Instagram en la búsqueda social. |
| Error, | ModQ | Se ha corregido un problema por el cual el menú Más información en ModQ no se mostraba donde se esperaba. |
| Error, | Rights Management | Se ha corregido un problema en el cual la ordenación en ModQ debería estar en una posición fija cuando la página se está desplazando. |
| Error, | Transmisiones | Se ha corregido un problema con la visualización de emisiones en el entorno de ensayo. |
| Mejora | Transmisiones | Se ha añadido la opción Seguridad para el trabajo (SFW) y No seguro para el trabajo (NSFW) a las emisiones. |
| Mejora | Studio | Se ha agregado la funcionalidad de etiquetas inteligentes al contenido cargado en la biblioteca Livefyre Studio Library a través de FileStack (funcionalidad de carga en Todos los recursos). |
