---
description: Describe las opciones para agregar la autenticación de usuario a las aplicaciones de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.
seo-description: Describe las opciones para agregar la autenticación de usuario a las aplicaciones de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.
seo-title: Integración de identidades
solution: Experience Manager
title: Integración de identidades
uuid: 079dc9c7-656a-49d0-920d-9e5a421a319c
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Integración de identidades{#identity-integration}

Describe las opciones para agregar la autenticación de usuario a las aplicaciones de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.

## Integración de identidades {#t_about_identity_integration}

Describe las opciones para agregar la autenticación de usuario a las aplicaciones de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.

Las aplicaciones de Livefyre incluyen funciones interactivas enriquecidas como publicar un comentario, escribir una reseña o indicar que gusta el contenido. Para que los usuarios interactúen con las aplicaciones de Livefyre, deberá integrar Livefyre con un servicio de identidad mediante la autenticación de Livefyre.js.

Livefyre.js Auth proporciona una autenticación centralizada de todas las aplicaciones de Livefyre en el sitio y le pone a cargo de la manera exacta en que los usuarios deben iniciar sesión y registrarse. Agregue Auth de forma global a la plantilla del sitio y utilícela en todas las páginas, o agréguela una vez por página, y cuando los usuarios hayan iniciado sesión en Livefyre JS Auth, la información del usuario se retransmitirá automáticamente a todas las aplicaciones de la página.

Ya sea que haya creado un servicio de identidad personalizado o que esté utilizando un servicio de identidad de terceros como Janrain Capture, esta sección cubre todo lo que necesita saber para integrarlo.
