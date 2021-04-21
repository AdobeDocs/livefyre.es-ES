---
description: Notas de la versión de la versión del 23 de marzo de 2018.
title: 23 de marzo de 2018
exl-id: 85fd6f79-7fa8-425e-b4c7-2e1635d6ef17
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 7%

---

# 23 de marzo de 2018{#march}

Notas de la versión de la versión del 23 de marzo de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

Las siguientes funciones son nuevas en la versión de producción de esta versión:

* **Novedades en Producción:** Facebook creó una actualización de seguridad del inicio de sesión de Facebook que hará que el inicio de sesión de Facebook de un cliente no funcione correctamente. Para solucionar este problema, debe:

   1. Agregue la siguiente URL al campo **[!UICONTROL Valid OAuth redirect URIs]** en Configuración de OAuth de cliente. Sustituya `<networkname>` por su nombre de red correcto:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Cambie **[!UICONTROL Use Strict Mode for Redirect URI]** a **[!UICONTROL Yes]**.

* **Novedades en UAT:**  ahora puede elegir el umbral de confianza para las etiquetas inteligentes en los flujos. La configuración de la puntuación de precisión (0-100) para las etiquetas permite controlar la precisión de los recursos que se recuperan.

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | Muro de los medios | Se ha corregido un problema en el muro de medios en el cual no se podía hacer clic en las etiquetas cuando se agregaba una publicación de Instagram desde una regla de flujo. |
| Error, | ModQ | Se ha corregido un problema con ModQ que no se cargaba correctamente. |
| Error, | ModQ | Se ha corregido un problema por el cual la incrustación de audio provocaba que ModQ dejara de funcionar. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Mejora | Tira de película | Se han corregido algunos problemas para que la tira de película sea más accesible. |
| Mejora | Studio | Ahora puede iniciar sesión en Livefyre utilizando un inicio de sesión de IMS. |
