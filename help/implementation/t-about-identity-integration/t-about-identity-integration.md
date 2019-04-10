---
description: Describe las opciones para agregar autenticación de usuario a aplicaciones
  de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.
seo-description: Describe las opciones para agregar autenticación de usuario a aplicaciones
  de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.
seo-title: Integración de identidad
solution: Experience Manager
title: Integración de identidad
uuid: 079 dc 9 c 7-656 a -49 d 0-920 d -9 e 5 a 421 a 319 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Integración de identidad{#identity-integration}

Describe las opciones para agregar autenticación de usuario a aplicaciones de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.

## Integración de identidad {#t_about_identity_integration}

Describe las opciones para agregar autenticación de usuario a aplicaciones de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.

Las aplicaciones de Livefyre incluyen funciones interactivas enriquecidas como publicar un comentario, escribir una revisión o indicar que gusta contenido. Para que los usuarios interactúen con las aplicaciones de Livefyre, deberá integrar Livefyre con un servicio de identidad con Auth de Livefyre. js.

La autenticación de Livefyre. js proporciona autenticación centralizada para todas las aplicaciones de Livefyre en el sitio y le pone a cargo de cómo los usuarios deben iniciar sesión y registrarse. Agregue la autenticación de forma global a la plantilla del sitio y utilícela en todas las páginas, o añádalo una vez por página, y cuando los usuarios hayan firmado en Livefyre JS Auth, retransmitan automáticamente la información del usuario a todas las aplicaciones de la página.

Tanto si ha creado un servicio de identidad personalizado como si utiliza un servicio de identidad de terceros como Janrain Capture, esta sección cubre todo lo que necesita saber para integrar.
