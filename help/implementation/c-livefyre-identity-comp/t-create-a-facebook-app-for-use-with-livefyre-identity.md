---
description: Puede utilizar la Identidad de Livefyre con Facebook para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones de su sitio.
seo-description: Puede utilizar la Identidad de Livefyre con Facebook para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones de su sitio.
seo-title: Crear una aplicación de Facebook para usar con la identidad de Livefyre
solution: Experience Manager
title: Crear una aplicación de Facebook para usar con la identidad de Livefyre
uuid: a7f7be4e-8986-4e79-831a-0bb0ae55599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Crear una aplicación de Facebook para usar con la identidad de Livefyre{#create-a-facebook-app-for-use-with-livefyre-identity}

Puede utilizar la Identidad de Livefyre con Facebook para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones de su sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de Facebook, Livefyre requiere la siguiente información de la aplicación de Facebook:

* ID de la aplicación
* Secreto de la aplicación

Para crear una aplicación de Facebook para usar con la identidad de Livefyre:

1. Vaya a [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Inicie sesión en su cuenta de desarrollador de Facebook.
1. Haga clic **[!UICONTROL Add New App]** o seleccione una aplicación existente para utilizarla con la identidad de Livefyre.
1. Haga clic en **[!UICONTROL Settings]**, luego **[!UICONTROL Basic]**. Introduzca una **[!UICONTROL Contact Email]** dirección, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** y **[!UICONTROL Terms of Service URL]**.
1. Haga clic en el signo más ( **[!UICONTROL +]**) junto a **[!UICONTROL Products]**.
1. Haga clic en **[!UICONTROL Set Up]** debajo de **[!UICONTROL Facebook Login]**.
1. Haga clic **[!UICONTROL Settings]** y configure lo siguiente:

   * Set **[!UICONTROL Client OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Web OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Use Strict Mode for Redirect URIs]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Enforce HTTPS for Web OAuth Login]** to **[!UICONTROL Yes]**.
   * En **[!UICONTROL Valid OAuth redirect URLs]**, agregue la dirección URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (donde `{networkName}` es el nombre de red proporcionado por Livefyre).

1. Under **[!UICONTROL App Review]**:

   * Hacer pública la aplicación.
   * Asegúrese de que el **[!UICONTROL Approved Items]** para **[!UICONTROL Login Permissions]** incluye `email`, `public_profile`y `user_friends`.

Una vez completada, la página del panel del desarrollador de Facebook mostrará el ID de la aplicación y el secreto de la aplicación para utilizarlos en la configuración de integración de Studio.
