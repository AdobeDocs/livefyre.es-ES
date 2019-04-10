---
description: Puede utilizar la identidad de Livefyre con Facebook para permitir a
  los usuarios utilizar sus inicios de sesión de Facebook para interactuar con Aplicaciones
  en el sitio.
seo-description: Puede utilizar la identidad de Livefyre con Facebook para permitir
  a los usuarios utilizar sus inicios de sesión de Facebook para interactuar con Aplicaciones
  en el sitio.
seo-title: Crear una aplicación de Facebook para su uso con la identidad de Livefyre
solution: Experience Manager
title: Crear una aplicación de Facebook para su uso con la identidad de Livefyre
uuid: a 7 f 7 be 4 e -8986-4 e 79-831 a -0 bb 0 ae 555599
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Crear una aplicación de Facebook para su uso con la identidad de Livefyre{#create-a-facebook-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con Facebook para permitir a los usuarios utilizar sus inicios de sesión de Facebook para interactuar con Aplicaciones en el sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de Facebook, Livefyre requiere la siguiente información de aplicación de Facebook:

* ID de la aplicación
* Secreto de aplicación

Para crear una aplicación de Facebook para utilizarla con la identidad de Livefyre:

1. Vaya a [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Inicie sesión en su cuenta de desarrollador de Facebook.
1. Haga clic **[!UICONTROL Add New App]** o seleccione una aplicación existente para usarla con la identidad de Livefyre.
1. Haga clic **[!UICONTROL Settings]**en y **[!UICONTROL Basic]**luego. Introduzca **[!UICONTROL Contact Email]** una dirección **[!UICONTROL Display Name]****[!UICONTROL Privacy Policy URL]**, y **[!UICONTROL Terms of Service URL]**.
1. Haga clic en el signo más ( **[!UICONTROL +]**) al lado **[!UICONTROL Products]**de.
1. Click on **[!UICONTROL Set Up]** under **[!UICONTROL Facebook Login]**.
1. Haga clic y **[!UICONTROL Settings]** configure lo siguiente:

   * Establecida **[!UICONTROL Client OAuth Login]** en **[!UICONTROL Yes]**.
   * Establecida **[!UICONTROL Web OAuth Login]** en **[!UICONTROL Yes]**.
   * Establecida **[!UICONTROL Use Strict Mode for Redirect URIs]** en **[!UICONTROL Yes]**.
   * Establecida **[!UICONTROL Enforce HTTPS for Web OAuth Login]** en **[!UICONTROL Yes]**.
   * En **[!UICONTROL Valid OAuth redirect URLs]**, agregue la URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (donde `{networkName}` es su nombre de red proporcionado por Livefyre).

1. En **[!UICONTROL App Review]**:

   * Haga pública la aplicación.
   * Asegúrese de **[!UICONTROL Approved Items]****[!UICONTROL Login Permissions]** que la inclusión `email`, `public_profile`y `user_friends`.

Cuando se complete, la página del panel del desarrollador de Facebook mostrará el ID de la aplicación y el secreto de aplicación para su uso en los ajustes de integración de Studio.
