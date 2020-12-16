---
description: Puede utilizar la Identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión en Twitter para interactuar con las aplicaciones del sitio.
seo-description: Puede utilizar la Identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión en Twitter para interactuar con las aplicaciones del sitio.
seo-title: Crear una aplicación de Twitter para usar con la identidad de Livefyre
solution: Experience Manager
title: Crear una aplicación de Twitter para usar con la identidad de Livefyre
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Crear una aplicación de Twitter para usarla con la identidad de Livefyre{#create-a-twitter-app-for-use-with-livefyre-identity}

Puede utilizar la Identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión en Twitter para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión en Twitter, Livefyre requiere la siguiente información de la aplicación de Twitter:

* clave del cliente (clave de API)
* secreto de cliente (secreto de API)

Para crear una aplicación de Twitter para usar con la identidad de Livefyre:

1. Vaya a [https://apps.twitter.com/](https://apps.twitter.com/) e inicie sesión en su cuenta de Twitter para crear una aplicación nueva o seleccionar una existente para utilizarla con la identidad de Livefyre.
1. En la página Configuración de la aplicación:

   * Escriba **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (donde **{networkName}** es el nombre de red proporcionado por Livefyre. Por ejemplo:** [!UICONTROL labs]** en **[!UICONTROL `labs.fyre.co`]**.)
   * Anule la selección de **[!UICONTROL Enable Callback Locking]**.
   * Select **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. En la ficha **[!UICONTROL Permissions]**, seleccione **[!UICONTROL Access: Read only]**.

Una vez completada, la página Administración de aplicaciones > Claves y Tokenes de acceso de Twitter lista la Clave del cliente de la aplicación (clave de API) y el Secreto de cliente (secreto de API) para utilizarlos en la página Ajustes de integración de Studio.
