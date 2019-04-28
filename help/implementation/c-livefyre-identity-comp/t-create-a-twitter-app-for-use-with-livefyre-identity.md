---
description: Puede utilizar la identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión de Twitter para interactuar con aplicaciones en el sitio.
seo-description: Puede utilizar la identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión de Twitter para interactuar con aplicaciones en el sitio.
seo-title: Crear una aplicación de Twitter para usarla con la identidad de Livefyre
solution: Experience Manager
title: Crear una aplicación de Twitter para usarla con la identidad de Livefyre
uuid: 841 cce 7 c -618 d -4154-85 a 3-1 de 96 d 04 bb 69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Crear una aplicación de Twitter para usarla con la identidad de Livefyre{#create-a-twitter-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con Twitter para permitir que los usuarios utilicen sus inicios de sesión de Twitter para interactuar con aplicaciones en el sitio.

Para habilitar el inicio de sesión en Twitter, Livefyre requiere la siguiente información de la aplicación de Twitter:

* Clave del consumidor (Clave de API)
* Secreto del consumidor (Secreto de API)

Para crear una aplicación de Twitter para utilizarla con la identidad de Livefyre:

1. Vaya a [https://apps.twitter.com/](https://apps.twitter.com/)e inicie sesión en su cuenta de Twitter para crear una nueva o seleccionar una existente para utilizarla con la identidad de Livefyre.
1. Desde la página Configuración de la aplicación:

   * Introduzca **[!UICONTROL Callback URL:]**`https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (donde **{networkname}** es su nombre de red proporcionado por Livefyre? Por ejemplo: ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Deselect **[!UICONTROL Enable Callback Locking]**.
   * Seleccione **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. En la **[!UICONTROL Permissions]** ficha, seleccione **[!UICONTROL Access: Read only]**.

Cuando se complete, la página Administración de aplicaciones de Twitter &gt; Claves y Autentificadores de acceso mostrará la clave de consumidores (clave de API) y el secreto del consumidor de la aplicación para su uso en la página Ajustes de integración de Studio.
