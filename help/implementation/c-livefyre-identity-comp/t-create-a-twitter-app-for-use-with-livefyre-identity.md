---
description: Puede utilizar la Identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión en Twitter para interactuar con las aplicaciones del sitio.
seo-description: Puede utilizar la Identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión en Twitter para interactuar con las aplicaciones del sitio.
seo-title: Crear una aplicación de Twitter para usar con la identidad de Livefyre
solution: Experience Manager
title: Crear una aplicación de Twitter para usar con la identidad de Livefyre
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Crear una aplicación de Twitter para usar con la identidad de Livefyre{#create-a-twitter-app-for-use-with-livefyre-identity}

Puede utilizar la Identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión en Twitter para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión en Twitter, Livefyre requiere la siguiente información de la aplicación de Twitter:

* Clave de consumidor (clave de API)
* Secreto del consumidor (secreto de API)

Para crear una aplicación de Twitter para usar con la identidad de Livefyre:

1. Vaya a [https://apps.twitter.com/](https://apps.twitter.com/)e inicie sesión en su cuenta de Twitter para crear una aplicación nueva o seleccionar una existente para utilizarla con la identidad de Livefyre.
1. En la página Configuración de la aplicación:

   * Introduzca **[!UICONTROL Callback URL:]** (donde `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` {networkName} **** es el nombre de red proporcionado por Livefyre). For example:** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Anule la selección **[!UICONTROL Enable Callback Locking]**.
   * Select **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. En la **[!UICONTROL Permissions]** ficha, seleccione **[!UICONTROL Access: Read only]**.

Una vez completada, la página Administración de aplicaciones de Twitter &gt; Claves y tokens de acceso mostrará la clave de consumo (clave de API) y el secreto de consumidor (secreto de API) de la aplicación para utilizarlos en la página Configuración de integración de Studio.
