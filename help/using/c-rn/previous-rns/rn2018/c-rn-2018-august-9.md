---
description: Notas de la versión del 9 de agosto de 2018.
seo-description: Notas de la versión del 9 de agosto de 2018.
seo-title: 9 de agosto de 2018
solution: Experience Manager
title: 9 de agosto de 2018
uuid: c 59 ae 5 ec -9 d 26-41 c 4-9 a 98-cb 95 c 89 ee 26 a
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 9 de agosto de 2018{#august}

Notas de la versión del 9 de agosto de 2018.

## Nuevas características {#section_syx_mdt_wcb}

**Etiquetas inteligentes de vídeo:** Ahora los usuarios pueden ver etiquetas inteligentes para vídeos de menos de 50 MB.

## Problemas {#section_ehw_ndt_wcb}

En esta versión se resolvieron los problemas de las tablas siguientes.

## Versión de producción

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Error | Contenido de la aplicación | Se ha corregido un problema que impedía a los administradores y administradores de contenido editar contenido en Contenido de la aplicación. |
| Mejora | Aplicaciones | Las redes sociales han realizado cambios de privacidad que significan que las menciones sociales ya no serán compatibles con Facebook o Twitter. |
| Mejora | Aplicaciones | Las redes sociales han realizado cambios de privacidad. La función «Publicar en» que publica automáticamente contenido a redes sociales (Facebook, linkedin, Twitter) se ha eliminado. |
| Mejora | RGPD | Se ha eliminado el modo de detalles de la página Detalles de la solicitud en Configuración > Privacidad. Para obtener acceso al modo de detalles, agregue /dbg al final de la URL. |
| Error | Integración: AEM | Se ha corregido un problema que hacía que, al arrastrar y soltar aplicaciones de Livefyre en AEM, apareciera varias aplicaciones. |
| Error | Biblioteca | Se ha corregido un problema por el que un recurso no se guardaba correctamente en la biblioteca. |
| Error | Identidad de Livefyre | Se ha corregido un problema con la identidad LF que provocaba errores 403 al iniciar sesión. |
| Error | Búsqueda social | Se corrigió un problema en el cual los usuarios no podían buscar publicaciones públicas de Facebook usando la opción URL en la búsqueda social. |
| Mejora | Sincronización social | Las redes sociales han realizado cambios de privacidad que significa que la sincronización social ya no será compatible con Facebook. |
| Mejora | Flujos | Ahora, al eliminar una aplicación, se eliminan todos los flujos asociados con la aplicación. |
| Mejora | Studio | Ahora los clientes pueden emitir eventos de Livefyre a Adobe Analytics individualmente en lugar de en lotes. |
| Mejora | Studio | Las ventanas modales que se muestran en aplicaciones de conversación para redes sociales ahora serán ventanas modales de la red social en lugar de Adobe Experience Manager Livefyre u otras ventanas modal con marca. |

## Versión de UAT

Los problemas de las tablas siguientes se resolvieron en la versión de la versión UAT.

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Error | RGPD | Se corrigió un problema en el cual los mensajes de exclusión no se mostraban en algunos vídeos de Instagram. |
| Error | Biblioteca | Se ha corregido un problema que hacía que una tarjeta con derechos concedidos mostrara manualmente el estado incorrecto de la solicitud de derechos. |
| Error | Biblioteca | Se ha corregido un problema que impedía guardar un recurso en una carpeta. |
| Error | Biblioteca/Búsqueda | Se ha restaurado la capacidad de buscar URL desde Instagram en la búsqueda social. |
| Error | Modq | Se ha corregido un problema por el que el menú Más información de modq no se mostraba donde se esperaba. |
| Error | Rights Management | Se ha corregido un problema por el que la ordenación en modq debería estar en una posición fija cuando se desplazaba por la página. |
| Error | Flujos | Se ha corregido un problema con la visualización de flujos en el entorno de ensayo. |
| Mejora | Flujos | Se ha añadido un elemento Seguro para trabajar (SFW) y No seguro para el trabajo (NSFW) a Flujos. |
| Mejora | Studio | Se ha añadido la funcionalidad de etiquetas inteligentes al contenido cargado en la biblioteca de Livefyre Studio a través de filestack (funcionalidad de carga en Todos los recursos). |

