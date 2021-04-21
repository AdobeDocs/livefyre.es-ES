---
description: Cree aplicaciones de Livefyre desde cero para crear experiencias personalizadas y visualizaciones de datos.
title: Integración de Livefyre en un CMS
exl-id: 05d85792-de97-47b1-90cc-ad7e841754b5
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Implementar Livefyre con integración de terceros

Cree aplicaciones de Livefyre desde cero para crear experiencias personalizadas y visualizaciones de datos.

Puede crear una aplicación de Livefyre desde cero consumiendo Livefyre y datos sociales mediante el Bootstrap y la API de Stream.

Para las aplicaciones de Livefyre que requieren autenticación, consulte Integración de identidad para obtener información sobre plataformas de autenticación de terceros admitidas.

Para implementar aplicaciones de conversación (comentarios, chat, blog en directo, notas):

1. Realice la integración de aplicaciones.
a. Cree una colección utilizando el token CollectionMeta.
b. Integre las aplicaciones de Livefyre en sitios web mediante la estructura de código incrustado de Livefyre.js .

   * Para obtener más información sobre cómo utilizar la estructura de código incrustado de Livefyre.js, consulte [Incrustar una aplicación](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obtener información sobre cómo integrar la aplicación de comentarios, consulte [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md).

   * Para obtener información sobre cómo integrar la aplicación de chat, consulte [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Para obtener información sobre cómo integrar Live Blog App, consulte [Live Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Para obtener información sobre cómo integrar la aplicación Sidenotes, consulte [Notas](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Realice la integración de autenticación.
a. Cree tokens de autenticación de usuario para pasar y almacenar datos de usuario en Livefyre.
b. Integrar plataformas de autenticación y usuarios de terceros. Para obtener una lista de plataformas compatibles, consulte [Integración de identidad](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Realizar personalizaciones de aplicación. Opciones de personalización de aplicaciones para que coincidan con la marca y el estilo, y para agregar funcionalidad personalizada.

Para crear una aplicación de visualización (Mapa, Muro de medios, Tendencia, Carrusel, Tira de película, Storify, Tarjeta de función, Mosaic, Encuestas):

1. Realice la integración de aplicaciones.
a. Cree una colección utilizando el token CollectionMeta.
b. Integre las aplicaciones de Livefyre en sitios web mediante la estructura de código incrustado de Livefyre.js . Para obtener más información sobre cómo utilizar la estructura de código incrustado de Livefyre.js, consulte [Incrustar una aplicación](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obtener información sobre cómo integrar la aplicación de mapa, consulte [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Para obtener información sobre cómo integrar la aplicación de muro de comunicación, consulte [Muro de medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Para obtener información sobre cómo integrar la aplicación de tendencias, consulte [Tendencias](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Realice la integración de autenticación.
a. Cree tokens de autenticación de usuario para pasar y almacenar datos de usuario en Livefyre.
b. Integrar plataformas de autenticación y usuarios de terceros. Para obtener una lista de plataformas compatibles, consulte [Integración de identidad](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre no es compatible con las aplicaciones Carrusel, FilmStrip, Storify, Feature Card, Mosaic y Polls con Livefyre.js.

Integre estas aplicaciones mediante el proceso [Crear una aplicación](/help/using/c-about-apps/c-create-an-app.md).
