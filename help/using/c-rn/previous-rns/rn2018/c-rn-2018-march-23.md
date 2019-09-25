---
description: Notas de la versión de la versión del 23 de marzo de 2018.
seo-description: Notas de la versión de la versión del 23 de marzo de 2018.
seo-title: 23 de marzo de 2018
solution: Experience Manager
title: 23 de marzo de 2018
uuid: b69b8715-ace4-48e0-8f54-ce4e12170ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# March 23, 2018{#march}

Notas de la versión de la versión del 23 de marzo de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* **** Nuevo en producción: Facebook creó una actualización de seguridad para el inicio de sesión en Facebook que causará que el inicio de sesión en Facebook de un cliente no funcione correctamente. Para solucionar este problema, debe:

   1. Agregue la siguiente URL al campo **[!UICONTROL Valid OAuth redirect URIs]** en Configuración de OAuth de cliente. Reemplazar `<networkname>` por el nombre de red correcto:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Cambie **[!UICONTROL Use Strict Mode for Redirect URI]** a **[!UICONTROL Yes]**.

* **** Novedades en UAT:Ahora puede elegir el umbral de confianza para las etiquetas inteligentes en los flujos. La definición de la puntuación de precisión (0-100) para las etiquetas permite controlar la precisión de los recursos que se están recuperando.

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | Muro de los medios | Se corrigió un problema en el Muro de medios en el cual no se podía hacer clic en las etiquetas cuando se agregaba una publicación de Instagram desde una regla de flujo. |
| Error, | ModQ | Se ha corregido un problema con ModQ que no se cargaba correctamente. |
| Error, | ModQ | Se ha corregido un problema que provocaba que ModQ dejara de funcionar al incrustar audio. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Mejora | Tira de película | Se han corregido algunos problemas para que la tira de película sea más accesible. |
| Mejora | Studio | Ahora puede iniciar sesión en Livefyre mediante un inicio de sesión en IMS. |

