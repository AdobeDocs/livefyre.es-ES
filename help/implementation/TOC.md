---
product: livefyre
audience: end-user
user-guide-title: Guía de implementación de Livefyre
translation-type: tm+mt
source-git-commit: 3664bc1c51d2b372c358385127a1ca9c2f0cfef8
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 4%

---


# Guía de implementación de Livefyre {#implementation}

+ [Guía de implementación de Livefyre](home.md)
+ Introducción {#getting-started}
   + [Introducción a la integración de Livefyre](c-getting-started/c-getting-started.md)
   + Proceso de implementación {#implementation-process}
      + [Proceso de implementación](c-getting-started/c-implementation-process/c-implementation-process.md)
      + [Tipos de integración de aplicaciones](c-getting-started/c-implementation-process/c-app-integration-types.md)
      + [Implementación de la aplicación](c-getting-started/designer-app-implementation.md)
      + [Implementar Livefyre con integración de terceros](c-app-integrations/implement-livefyre-3rd-party.md)
      + [Arquitectura](c-getting-started/c-implementation-process/c-architecture.md)
      + [Incrustar una aplicación](c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)
      + [Añadir autenticación en una aplicación mediante Livefyre.js](c-getting-started/c-implementation-process/c-add-authetication-to-an-app-using-livefyre.js.md)
      + [Generar tokens del lado del servidor](c-getting-started/c-implementation-process/c-build-server-side-tokens.md)
      + [CollectionMeta Token](c-getting-started/c-implementation-process/c-collectionmeta-tokent.md)
      + [Autentificador de usuario](c-getting-started/c-implementation-process/c-user-auth-token.md)
      + [Creación de una colección con el token CollectionMeta](t-create-a-collectionmeta-token.md)
      + [Creación de una suma de comprobación](c-creating-a-checksum.md)
+ Integración de identidades {#identity-integration}
   + [Integración de identidades](t-about-identity-integration/t-about-identity-integration.md)
   + [Paquete de autenticación](t-about-identity-integration/c-authorization-package.md)
   + [AuthDelegate (objeto)](t-about-identity-integration/c-building-an-auth-delegate.md)
   + [Registro de permisos de usuario en sistemas externos (opcional)](t-about-identity-integration/c-posting-user-permissions-to-external-systems.md)
   + Implementar SSO {#implementing-sso}
      + [Implementación de SSO](t-about-identity-integration/c-implementing-sso/c-implementing-sso.md)
      + [Delegado de autenticación de depuración](t-about-identity-integration/c-implementing-sso/c-debugging-auth.md)
   + Sincronizar con Livefyre {#sync-ping-for-pull}
      + [Sincronizar con Livefyre usando Ping para extracción](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)
      + [Generar el extremo de extracción](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-pull-endpoint.md)
      + [Registro del extremo con Studio](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-register-the-endpoint-with-studio.md)
      + [Construir el ping](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-ping.md)
      + [Estructura de solicitud de extracción](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-pull-request-structure.md)
      + [Generar el ping para la respuesta de extracción](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-build-the-ping-for-pull-response.md)
+ Identidad de Livefyre {#livefyre-identity}
   + [Identidad de Livefyre](c-livefyre-identity-comp/c-livefyre-identity-comp.md)
   + [Habilitar la identidad de Livefyre](c-livefyre-identity-comp/t-enable-livefyre-identity.md)
   + Usar aplicaciones sociales con identidad de Livefyre {#use-social-apps-with-livefyre-identity}
      + [Crear aplicaciones sociales](c-livefyre-identity-comp/t-create-your-social-apps.md)
      + [Crear una aplicación de Facebook para usar con la identidad de Livefyre](c-livefyre-identity-comp/t-create-a-facebook-app-for-use-with-livefyre-identity.md)
      + [Crear una aplicación de Twitter para usar con la identidad de Livefyre](c-livefyre-identity-comp/t-create-a-twitter-app-for-use-with-livefyre-identity.md)
      + [Crear un Yahoo! Aplicación para usar con la identidad de Livefyre](c-livefyre-identity-comp/t-create-a-yahoo-app-for-use-with-livefyre-identity.md)
      + [Crear una aplicación de identidad de Microsoft Live para utilizarla con la identidad de Livefyre](c-livefyre-identity-comp/t-create-a-microsoft-live-id-app-for-use-with-livefyre-identity.md)
      + [Crear una aplicación de LinkedIn para usarla con la identidad de Livefyre](c-livefyre-identity-comp/t-create-a-linkedin-app-for-use-with-livefyre-identity.md)
      + [Creación de una aplicación de identidad de GitHub para su uso con la identidad de Livefyre](c-livefyre-identity-comp/c-create-a-github-identity.md)
      + [Uso de Studio para conectar las aplicaciones sociales a la implementación de Livefyre](c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)
   + [Añadir Livefyre.js a la página](c-livefyre-identity-comp/t-add-livefyre.js-to-the-page.md)
   + [Inicializar la identidad de Livefyre](c-livefyre-identity-comp/t-initialize-livefyre-identity.md)
   + [Correos electrónicos para la identidad de Livefyre](c-livefyre-identity-comp/c-emails-for-livefyre-identity.md)
   + [Captura de Janrain/plano posterior](c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)
   + Instalación {#installation}
      + [Instalación de bibliotecas](c-installing-libraries/c-installing-libraries.md)
      + [Clases y métodos](c-installing-libraries/c-methods-livefyre.md)
      + [Métodos de red](c-installing-libraries/c-network-methods.md)
      + [setSSL Network (método)](c-installing-libraries/r-setssl-method.md)
      + [buildLivefyreToken Network (método)](c-installing-libraries/r-buildlivefyretoken-method.md)
      + [buildUserAuthToken (método de red)](c-installing-libraries/r-builduserauthtoken-method.md)
      + [validateLivefyreToken Network (método)](c-installing-libraries/c-validatelivefyretoken-network-method.md)
      + [setUserSyncUrl (método de red)](c-installing-libraries/r-setusersyncurl-method.md)
      + [syncUser Network (método)](c-installing-libraries/r-syncuser-method.md)
      + [getUrn Network (método)](c-installing-libraries/r-geturn-method.md)
      + [getUrnForUser (método de red)](c-installing-libraries/r-geturnforuser-method.md)
      + [getNetworkName (método de red)](c-installing-libraries/r-getnetworkname-method.md)
      + [getSite Network (método)](c-installing-libraries/r-getsite-method.md)
      + [Métodos de clase de red](c-installing-libraries/c-network-class-methods.md)
      + [Métodos de clase de colección](c-installing-libraries/c-collection-methods.md)
      + [createOrUpdate (método de recopilación)](c-installing-libraries/r-createorupdate-collection-method.md)
      + [buildCollectionMetaToken (método de recopilación)](c-installing-libraries/r-buildcollectionmetatoken-collection-method.md)
      + [buildChecksum (método de recopilación)](c-installing-libraries/r-buildchecksum-collection-method.md)
      + [getCollectionContent (método de recopilación)](c-installing-libraries/t-getcollectioncontent-collection-method.md)
      + [getUrn (método de recopilación)](c-installing-libraries/r-geturn-collection-method.md)
      + [Métodos de clase de sitio](c-installing-libraries/c-site-methods.md)
      + [buildBlogCollection (método del sitio)](c-installing-libraries/r-buildblogcollection-site-method.md)
      + [buildChatCollection (método de sitio)](c-installing-libraries/r-buildchatcollection-site-method.md)
      + [buildCommentsCollection (método de sitio)](c-installing-libraries/r-buildcommentscollection-site-method.md)
      + [buildCountingCollection (método de sitio)](c-installing-libraries/r-buildcountingcollection-site-method.md)
      + [buildRatingsCollection (método de sitio)](c-installing-libraries/r-buildratingscollection-site-method.md)
      + [buildReviewsCollection (método de sitio)](c-installing-libraries/r-buildreviewscollection-site-method.md)
      + [buildSitenotesCollection (método de sitio)](c-installing-libraries/r-buildsitenotescollection-site-method.md)
      + [buildCollection (método de sitio)](c-installing-libraries/r-buildcollection-site-method.md)
      + [getUrn Site (método)](c-installing-libraries/r-geturn-site-method.md)
      + [Ejemplos](c-installing-libraries/c-libraries-examples.md)
   + SDK para móvil {#mobile-sdks}
      + [SDK para móvil](c-mobile-sdks/c-mobile-sdks.md)
      + [Livefyre iOS SDK](c-mobile-sdks/c-livefyre-ios-sdk.md)
      + [Android SDK](c-mobile-sdks/c-android-sdk.md)
+ [Livefyre.js](c-livefyre.js.md)
+ [Creación de tokens de Livefyre C#](c-creating-livefyre-tokens-c-.md)
+ Integraciones de aplicaciones {#app-integrations}
   + [Conversación](c-app-integrations/c-app-integratios-chat.md)
   + Comentarios {#comments}
      + [Comentarios](c-app-integrations/c-comments-integration/c-comments-integration.md)
   + [Blog en vivo](c-app-integrations/c-live-blog-integration.md)
   + [Reseñas](c-app-integrations/c-reviews-integration.md)
   + Notas de identidad {#sidenotes}
      + [Integración de Sidenotes](c-app-integrations/c-sidenotes-integration/r-sidenotes-integration.md)
      + [Añadir notas a una página](c-app-integrations/c-sidenotes-integration/r-adding-sidenotes-to-a-page.md)
      + [Eventos de la aplicación Sidenotes](c-app-integrations/c-sidenotes-integration/r-app-events.md)
      + [Muestra las opciones de configuración](c-app-integrations/c-sidenotes-integration/r-configuration-options.md)
      + [Identifica estilos personalizados](c-app-integrations/c-sidenotes-integration/r-custom-styles.md)
      + [Identifica cadenas personalizadas](c-app-integrations/c-sidenotes-integration/r-custom-strings.md)
      + [Implementación de Sidenotes](c-app-integrations/c-sidenotes-integration/r-sidenotes-implementation.md)
      + [updateAnchors (método)](c-app-integrations/c-sidenotes-integration/update-anchors-method.md)
   + [Mapa](c-app-integrations/c-map-integration.md)
   + [Muro de los medios](c-app-integrations/c-media-wall-integration.md)
   + [Tendencias](c-app-integrations/c-trending-integration.md)
+ Personalizaciones de la aplicación {#app-customizations}
   + [Personalizaciones de la aplicación](c-app-customizations/c-app-customizations.md)
   + [Cambiar opciones de visualización](c-app-customizations/c-change-display-options.md)
   + [Clases CSS](c-app-customizations/c-css-classes.md)
   + [Storify CSS Clases](c-app-customizations/c-storify-css-classes.md)
   + [Conjuntos de traducción](c-app-customizations/c-translation-sets.md)
   + [Mover el logotipo de Livefyre](c-app-customizations/c-move-the-livefyre-logo.md)
   + [Restringir medios](c-app-customizations/c-restrict-media.md)
   + [Ocultar elementos de la aplicación](c-app-customizations/c-hide-app-elements.md)
   + [Cambiar el icono @mention](c-app-customizations/c-change-mention-icon.md)
   + [Resaltar contenido](c-app-customizations/c-highlight-content.md)
   + [Personalización de la marca de fecha y hora](c-app-customizations/c-date-time-stamp.md)
   + Contenido de la función {#feature-content}
      + [Contenido de las funciones](c-app-customizations/t-feature-content.md)
      + [Activar contenido de presentación en Studio](c-app-customizations/t-enable-featuring-content-in-studio.md)
      + [Seleccione el contenido para la función desde una aplicación](c-app-customizations/t-select-content-to-feature.md)
      + [Seleccione el contenido para la función de estudio](c-app-customizations/t-select-content-to-feature-from-studio.md)
      + [Utilizar CSS para aplicar estilo al contenido destacado](c-app-customizations/c-use-css-to-style-featured-content.md)
      + [API de funciones](c-app-customizations/c-feature-apis.md)
   + [Conexión de Janrain a Livefyre mediante AuthDelegate](c-app-customizations/c-connecting-janrain-to-livefyre-using-authdelegate.md)
   + [Contenido destacado agregado mediante las API destacadas](c-app-customizations/c-aggregated-featured-content-using-the-featured-apis.md)
   + Contenido de estilo {#style-content}
      + [Estilo del contenido del grupo de usuarios](c-app-customizations/c-style-user-group-content.md)
      + [Añadir usuarios a grupos](c-app-customizations/c-adding-users-to-groups.md)
   + Aplicar estilos personalizados {#apply-custom-styles}
      + [Aplicación de estilos personalizados](c-app-customizations/c-applying-custom-styles-.md)
      + [Añadir botones personalizados](c-app-customizations/t-add-custom-buttons.md)
   + Eventos Javascript {#javascript-events}
      + [Definiciones y ejemplos de Eventos JavaScript](c-app-customizations/c-javascript-events.md)
      + [Eventos Javascript para aplicaciones de visualización](c-app-customizations/c-javascript-events-for-visualization-apps.md)
      + [Eventos Javascript para Media Wall](c-app-customizations/c-javascript-events-media-wall.md)
      + [Eventos de JavaScript para aplicaciones de conversación](c-app-customizations/c-javascript-events-for-conversation-apps.md)
   + [Incrustar una aplicación de comentarios](c-app-customizations/c-embed-a-comments-app.md)
   + [Seguimiento de referencia](c-app-customizations/c-referral-tracking.md)
   + [Compatibilidad con dispositivos y navegadores](c-app-customizations/c-device-and-browser-support.md)
   + [Requisitos de visualización de Twitter](c-app-customizations/c-twitter-display-requirements.md)
+ [Directiva de prueba de esfuerzo](c-stress-test-policy.md)
+ Analytics {#analytics}
   + [Analytics](livefyre-analytics/livefyre-analytics.md)
   + [Uso de Livefyre con Adobe Analytics y el Administrador dinámico de etiquetas (DTM)](livefyre-analytics/c-use-livefyre-with-adobe-analytics.md)
   + [Uso de Livefyre con otras herramientas de Analytics](livefyre-analytics/c-livefyre-analytics.md)
   + [Eventos de análisis de Livefyre](livefyre-analytics/c-livefyre-analytics-events.md)
+ [Integración de Livefyre con AEM](c-livefyre-aem-integration.md)
+ Temas avanzados {#advanced-topics}
   + [Mostrar recuento de comentarios](c-advanced-topics/t-display-comment-count.md)
   + [Activación del uso compartido en redes sociales](c-advanced-topics/c-enabling-social-sharing.md)
   + [Flujo de actividad](c-advanced-topics/c-activity-stream.md)
   + [HTML Bootstrap](c-advanced-topics/c-bootstrap-html.md)
   + [Cambiar colección](c-advanced-topics/c-change-collection.md)
   + [Varias colecciones](c-advanced-topics/c-multiple-collections.md)
   + [Cambiar tipos de aplicaciones principales](c-advanced-topics/c-switch-core-app-types.md)
   + [Contador social](c-advanced-topics/c-social-counter.md)
   + [Uso de la API de arranque y flujo con las aplicaciones de Livefyre](c-advanced-topics/bootstrap-stream-api.md)
