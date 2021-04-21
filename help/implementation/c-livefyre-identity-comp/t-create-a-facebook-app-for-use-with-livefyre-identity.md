---
description: Puede utilizar la identidad de Livefyre con Facebook para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones del sitio.
title: Crear una aplicación de Facebook para usarla con la identidad de Livefyre
exl-id: ec320865-6ea3-4f6f-a5f6-31f3d5cbdc93
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---

# Crear una aplicación de Facebook para usarla con la identidad de Livefyre{#create-a-facebook-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con Facebook para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones del sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de Facebook, Livefyre requiere la siguiente información de la aplicación de Facebook:

* ID de la aplicación
* Secreto de la aplicación

Para crear una aplicación de Facebook para usarla con la identidad de Livefyre:

1. Vaya a [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Inicie sesión en su cuenta de desarrollador de Facebook.
1. Haga clic en **[!UICONTROL Add New App]** o seleccione una aplicación existente para usarla con la identidad de Livefyre.
1. Haga clic en **[!UICONTROL Settings]** y luego en **[!UICONTROL Basic]**. Introduzca una dirección **[!UICONTROL Contact Email]**, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** y **[!UICONTROL Terms of Service URL]**.
1. Haga clic en el signo más ( **[!UICONTROL +]**) junto a **[!UICONTROL Products]**.
1. Haga clic en **[!UICONTROL Set Up]** en **[!UICONTROL Facebook Login]**.
1. Haga clic en **[!UICONTROL Settings]** y configure lo siguiente:

   * Establezca **[!UICONTROL Client OAuth Login]** en **[!UICONTROL Yes]**.
   * Establezca **[!UICONTROL Web OAuth Login]** en **[!UICONTROL Yes]**.
   * Establezca **[!UICONTROL Use Strict Mode for Redirect URIs]** en **[!UICONTROL Yes]**.
   * Establezca **[!UICONTROL Enforce HTTPS for Web OAuth Login]** en **[!UICONTROL Yes]**.
   * En **[!UICONTROL Valid OAuth redirect URLs]**, añada la URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (donde `{networkName}` es su nombre de red proporcionado por Livefyre).

1. En **[!UICONTROL App Review]**:

   * Hacer que la aplicación sea pública.
   * Asegúrese de que **[!UICONTROL Approved Items]** para **[!UICONTROL Login Permissions]** incluye `email`, `public_profile` y `user_friends`.

Cuando se complete, la página Tablero del desarrollador de Facebook enumerará su ID de aplicación y Secreto de aplicación para usarlos en la Configuración de integración de Studio.
