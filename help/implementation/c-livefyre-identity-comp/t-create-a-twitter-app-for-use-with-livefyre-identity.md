---
description: Puede utilizar la identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión de Twitter para interactuar con las aplicaciones del sitio.
title: Crear una aplicación de Twitter para usarla con la identidad de Livefyre
exl-id: 4f2b919f-fe5d-49a3-8432-04ffb3d68ce4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Crear una aplicación de Twitter para usarla con la identidad de Livefyre{#create-a-twitter-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión de Twitter para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión en Twitter, Livefyre requiere la siguiente información de la aplicación de Twitter:

* Clave de consumidor (clave de API)
* Secreto del consumidor (secreto de API)

Para crear una aplicación de Twitter para usarla con la identidad de Livefyre:

1. Vaya a [https://apps.twitter.com/](https://apps.twitter.com/) e inicie sesión en su cuenta de Twitter para crear una aplicación nueva o seleccionar una existente para usarla con la identidad de Livefyre.
1. En la página Configuración de la aplicación:

   * Introduzca **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (donde **{networkName}** es su nombre de red proporcionado por Livefyre. Por ejemplo:** [!UICONTROL labs]** en **[!UICONTROL `labs.fyre.co`]**).
   * Anule la selección de **[!UICONTROL Enable Callback Locking]**.
   * Select **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. En la pestaña **[!UICONTROL Permissions]**, seleccione **[!UICONTROL Access: Read only]**.

Cuando se complete, la página Administración de aplicaciones de Twitter > Claves y token de acceso enumerará la clave de consumidor (clave de API) y el secreto de consumidor (secreto de API) de la aplicación para utilizarlos en la página Configuración de integración de Studio.
