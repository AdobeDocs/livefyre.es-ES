---
description: Describe las opciones para agregar la autenticación de usuario a las aplicaciones de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.
title: Integración de identidad
exl-id: a3b849fc-0182-4fed-94b5-6d7199fc4e44
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Integración de identidad{#identity-integration}

Describe las opciones para agregar la autenticación de usuario a las aplicaciones de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.

## Integración de identidad {#t_about_identity_integration}

Describe las opciones para agregar la autenticación de usuario a las aplicaciones de Livefyre, incluida la captura de Janrain o su propio servicio de identidad.

Las aplicaciones de Livefyre incluyen funciones interactivas enriquecidas como publicar un comentario, escribir una revisión o indicar que gusta el contenido. Para que sus usuarios interactúen con las aplicaciones de Livefyre, deberá integrar Livefyre con un servicio de identidad mediante la autenticación de Livefyre.js.

Livefyre.js Auth proporciona autenticación centralizada para todas las aplicaciones de Livefyre en su sitio y le pone a cargo exactamente de cómo los usuarios deben iniciar sesión y registrarse. Agregue Auth globalmente a la plantilla de su sitio y utilícela en todas las páginas, o agréguela una vez por página, y cuando los usuarios hayan iniciado sesión en Livefyre JS Auth transmitirá automáticamente la información del usuario a todas las aplicaciones de la página.

Tanto si ha creado un servicio de identidad personalizado como si está utilizando un servicio de identidad de terceros como Janrain Capture, esta sección cubre todo lo que necesita saber para integrar.
