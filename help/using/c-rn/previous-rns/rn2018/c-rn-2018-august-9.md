---
description: Notas de la versión de la versión del 9 de agosto de 2018.
seo-description: Notas de la versión de la versión del 9 de agosto de 2018.
seo-title: 9 de agosto de 2018
solution: Experience Manager
title: 9 de agosto de 2018
uuid: c59ae5ec-9d26-41c4-9a98-cb95c89ee26a
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 9 de agosto de 2018{#august}

Notas de la versión de la versión del 9 de agosto de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

**** Etiquetas inteligentes de vídeo: Ahora los usuarios pueden ver etiquetas inteligentes para vídeos con menos de 50 MB.

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | Contenido de la aplicación | Se ha corregido un problema que impedía a los administradores y administradores de contenido editar contenido en Contenido de la aplicación. |
| Mejora | Aplicaciones | Las redes sociales han realizado cambios en la privacidad que significan que las menciones sociales ya no serán compatibles con Facebook o Twitter. |
| Mejora | Aplicaciones | Las redes sociales han realizado cambios en la privacidad. Se ha eliminado la función "Publicar en" que publica automáticamente contenido en las redes sociales (Facebook, LinkedIn, Twitter). |
| Mejora | RGPD | Se ha eliminado el modo de alternancia de detalles de la página de detalles de la solicitud en Configuración &gt; Privacidad. Se puede acceder a la opción de alternancia del modo Detalles agregando /dbg al final de la dirección URL. |
| Error, | Integración: AEM | Se ha corregido un problema que hacía que, al arrastrar y soltar aplicaciones de Livefyre en AEM, pareciera que se creaban varias aplicaciones. |
| Error, | Biblioteca | Se corrigió un problema en el cual un recurso no se guardaba correctamente en la biblioteca. |
| Error, | Identidad de Livefyre | Se ha corregido un problema con la identidad LF que provocaba errores 403 al iniciar sesión. |
| Error, | Búsqueda social | Se corrigió un problema en el cual los usuarios no podían buscar publicaciones públicas de Facebook mediante la opción URL en la búsqueda social. |
| Mejora | Sincronización social | Las redes sociales han realizado cambios en la privacidad que significan que Facebook ya no admitirá la sincronización social. |
| Mejora | Flujos | Ahora, cuando elimina una aplicación, elimina todos los flujos asociados a ella. |
| Mejora | Studio | Ahora los clientes pueden emitir eventos de Livefyre a Adobe Analytics de forma individual, en lugar de hacerlo por lotes. |
| Mejora | Studio | Las ventanas de modo que se muestran en la conversación Las aplicaciones para redes sociales serán ahora ventanas modales de la red social en lugar de Adobe Experience Manager Livefyre u otras ventanas modales con marca. |

## Versión de UAT

Los problemas de las tablas siguientes se resolvieron en la versión de UAT.

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | RGPD | Se corrigió un problema en el cual los mensajes de exclusión no se mostraban en algunos vídeos de Instagram. |
| Error, | Biblioteca | Se corrigió un problema en el cual una tarjeta con derechos concedidos mostraba manualmente el estado de solicitud de derechos incorrecto. |
| Error, | Biblioteca | Se ha corregido un problema que impedía guardar un recurso en una carpeta. |
| Error, | Biblioteca/Búsqueda | Se ha restaurado la capacidad de buscar direcciones URL desde Instagram en la búsqueda social. |
| Error, | ModQ | Se corrigió un problema en el cual Más menú de información en ModQ no se mostraba donde se esperaba. |
| Error, | Rights Management | Se corrigió un problema en el cual la ordenación en ModQ debería estar en una posición fija cuando la página se está desplazando. |
| Error, | Flujos | Se ha corregido un problema con la visualización de flujos en el entorno de ensayo. |
| Mejora | Flujos | Se ha agregado la opción Seguro para el trabajo (SFW) y No seguro para el trabajo (NSFW) a Flujos. |
| Mejora | Studio | Se ha agregado la funcionalidad de etiquetas inteligentes al contenido cargado en la biblioteca de Livefyre Studio mediante FileStack (funcionalidad de carga en todos los recursos). |

