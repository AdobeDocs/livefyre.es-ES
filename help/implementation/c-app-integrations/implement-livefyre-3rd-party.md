---
description: Cree aplicaciones de Livefyre desde cero para crear experiencias personalizadas
  y visualizaciones de datos.
seo-description: Cree aplicaciones de Livefyre desde cero para crear experiencias
  personalizadas y visualizaciones de datos.
seo-title: Integrar Livefyre con integración de terceros
solution: Experience Manager
title: Integrar Livefyre en un CMS
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Implementar Livefyre con integración de terceros

Cree aplicaciones de Livefyre desde cero para crear experiencias personalizadas y visualizaciones de datos.

Puede crear una aplicación de Livefyre desde cero, consumiendo Livefyre y datos sociales utilizando Bootstrap y la API de flujo.

Para las aplicaciones de Livefyre que requieren autenticación, consulte Integración de identidad para obtener información sobre las plataformas de autenticación de terceros admitidas.

Para implementar aplicaciones de conversación (comentarios, chat, blog directo, Sidenotes):

1. Realizar la integración de aplicaciones.
a. Crear una colección con collectionmeta Token.
b. Integre aplicaciones de Livefyre en sitios utilizando la estructura de código incrustado de Livefyre. js.

   * Para obtener más información sobre cómo utilizar la estructura de código incrustado de Livefyre. js, consulte [Incrustar una aplicación](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obtener información sobre cómo integrar la aplicación de comentarios, consulte [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md).

   * Para obtener información sobre cómo integrar la aplicación de chat, consulte [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Para obtener información sobre cómo integrar la aplicación de blog en directo, consulte [Live Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Para obtener información sobre cómo integrar la aplicación Sidenotes, consulte [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Realizar la integración de autenticación.
a. Crear tokens de autenticación de usuario para transmitir y almacenar datos de usuario en Livefyre.
b. Integrar plataformas de autenticación y usuario de terceros. Para obtener una lista de plataformas admitidas, consulte [Integración de identidad](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Realizar personalizaciones de aplicaciones. Opciones de personalización de aplicaciones para hacer coincidir su marca y estilo y agregar funcionalidad personalizada.

Para crear una aplicación de visualización (Mapa, Muro de medios, Tendencias, Carrusel, Tira de película, Storify, Tarjeta de funciones, Mosaico, Encuestas):

1. Realizar la integración de aplicaciones.
a. Crear una colección con collectionmeta Token.
b. Integre aplicaciones de Livefyre en sitios utilizando la estructura de código incrustado de Livefyre. js. Para obtener más información sobre cómo utilizar la estructura de código incrustado de Livefyre. js, consulte [Incrustar una aplicación](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obtener información sobre cómo integrar la aplicación de mapa, consulte [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Para obtener información sobre cómo integrar la aplicación de muro de medios, consulte [Muro de medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Para obtener información sobre cómo integrar la aplicación Tendencias, consulte [Tendencias](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Realizar la integración de autenticación.
a. Crear tokens de autenticación de usuario para pasar y almacenar datos de usuario en Livefyre.
b. Integrar plataformas de autenticación y usuario de terceros. Para obtener una lista de plataformas admitidas, consulte [Integración de identidad](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre no admite Carrusel, Tira de película, Storify, Tarjeta de funciones, Mosaico y Encuestas con Livefyre. js.
Integre estas aplicaciones con [el](/help/using/c-about-apps/c-create-an-app.md) proceso Crear una aplicación.