---
description: Cree aplicaciones de Livefyre desde cero para crear experiencias personalizadas y visualizaciones de datos.
seo-description: Cree aplicaciones de Livefyre desde cero para crear experiencias personalizadas y visualizaciones de datos.
seo-title: Integración de Livefyre con integración de terceros
solution: Experience Manager
title: Integrar Livefyre en un CMS
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 2436c389cbe14c7d64dd8c0392a3e0f031468836
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Implementar Livefyre con integración de terceros

Cree aplicaciones de Livefyre desde cero para crear experiencias personalizadas y visualizaciones de datos.

Puede crear una aplicación de Livefyre desde cero consumiendo datos sociales y de Livefyre mediante el Bootstrap y la API de flujo.

Para las aplicaciones de Livefyre que requieren autenticación, consulte Integración de identidad para obtener información sobre plataformas de autenticación de terceros admitidas.

Para implementar las aplicaciones de conversación (comentarios, chat, blog en vivo, notas de identidad):

1. Realice la integración de aplicaciones.
a. Cree una colección con el token CollectionMeta.
b. Integre las aplicaciones de Livefyre en sitios mediante la estructura de código incrustado de Livefyre.js.

   * Para obtener más información sobre cómo utilizar la estructura de código incrustado de Livefyre.js, consulte [Incrustar una aplicación](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obtener información sobre cómo integrar la aplicación Comentarios, consulte [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md).

   * Para obtener información sobre cómo integrar la aplicación de chat, consulte [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Para obtener información sobre cómo integrar la aplicación de blogs en vivo, consulte [Live Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Para obtener información sobre cómo integrar la aplicación Sidenotes, consulte [Notas](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)de identidad.

1. Realice la integración de autenticación.
a. Cree tokens de autenticación de usuario para pasar y almacenar datos de usuario en Livefyre.
b. Integrar plataformas de autenticación y usuarios de terceros. Para obtener una lista de las plataformas admitidas, consulte Integración [de identidades](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Realizar personalizaciones de la aplicación. Opciones de personalización de la aplicación para coincidir con la marca y el estilo y agregar funcionalidad personalizada.

Para crear una aplicación de visualización (Mapa, Muro de los medios, Tendencias, Carrusel, Tira de película, Storify, Tarjeta de función, Mosaico, Encuestas):

1. Realice la integración de aplicaciones.
a. Cree una colección con el token CollectionMeta.
b. Integre las aplicaciones de Livefyre en sitios mediante la estructura de código incrustado de Livefyre.js. Para obtener más información sobre cómo utilizar la estructura de código incrustado de Livefyre.js, consulte [Incrustar una aplicación](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obtener información sobre cómo integrar la aplicación de mapa, consulte [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Para obtener información sobre cómo integrar la aplicación Media Wall, consulte [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Para obtener información sobre cómo integrar la aplicación de tendencias, consulte [Tendencias](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Realice la integración de autenticación.
a. Cree tokens de autenticación de usuario para pasar y almacenar datos de usuario en Livefyre.
b. Integrar plataformas de autenticación y usuarios de terceros. Para obtener una lista de las plataformas admitidas, consulte Integración [de identidades](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre no es compatible con Carrusel, Tira de película, Storify, Tarjeta de función, Mosaico y Aplicaciones de encuestas mediante Livefyre.js.

Integre estas aplicaciones mediante el proceso [Crear una aplicación](/help/using/c-about-apps/c-create-an-app.md) .