---
description: Notas de la versión de la versión del 23 de marzo de 2018.
seo-description: Notas de la versión de la versión del 23 de marzo de 2018.
seo-title: 23 de marzo de 2018
solution: Experience Manager
title: 23 de marzo de 2018
uuid: b 69 b 8715-ace 4-48 e 0-8 f 54-ce 4 e 12170 ef 3
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 23 de marzo de 2018{#march}

Notas de la versión de la versión del 23 de marzo de 2018.

## Nuevas características {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* **Novedades de producción:** Facebook ha creado una actualización de seguridad para iniciar sesión en Facebook que ocasionará que el inicio de sesión de Facebook de un cliente no funcione correctamente. Para solucionar este problema, debe:

   1. Agregue la siguiente URL a **[!UICONTROL Valid OAuth redirect URIs]** field en la Configuración de oauth del cliente. Sustituya `<networkname>` por el nombre de red correcto:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Cambiar **[!UICONTROL Use Strict Mode for Redirect URI]** a **[!UICONTROL Yes]**.

* **Nuevo en UAT:** Ahora puede elegir el umbral de confianza para las etiquetas inteligentes en flujos. La configuración de la puntuación de precisión (0-100) para las etiquetas permite controlar la precisión de los recursos que se recuperan.

## Problemas {#section_ehw_ndt_wcb}

En esta versión se resolvieron los problemas de las tablas siguientes.

## Versión de producción

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Error | Muro de medios | Se ha corregido un problema en Wall Wall por el que las etiquetas no se podían hacer clic cuando se añadía un anuncio de Instagram desde una regla de flujo. |
| Error | Modq | Se ha corregido un problema por el que modq no se cargaba correctamente. |
| Error | Modq | Se ha corregido un problema que hacía que la incrustación de audio dejara de funcionar. |

## Versión de UAT

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Mejora | Tira de película | Se han corregido algunos problemas para hacer que Tira de película sea más accesible. |
| Mejora | Studio | Ahora puede iniciar sesión en Livefyre mediante un inicio de sesión IMS. |

