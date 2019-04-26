---
description: Puede utilizar la identidad de Livefyre con Google para permitir que
  los usuarios utilicen sus inicios de sesión de Google para interactuar con Aplicaciones
  en el sitio.
seo-description: Puede utilizar la identidad de Livefyre con Google para permitir
  que los usuarios utilicen sus inicios de sesión de Google para interactuar con Aplicaciones
  en el sitio.
seo-title: Creación de un proyecto de Google para su uso con la identidad de Livefyre
solution: Experience Manager
title: Creación de un proyecto de Google para su uso con la identidad de Livefyre
uuid: b 0 a 6 bb 8 a-abea -4 f 5 c -92 ed -026 e 60183 e 1 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creación de un proyecto de Google para su uso con la identidad de Livefyre{#create-a-google-project-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con Google para permitir que los usuarios utilicen sus inicios de sesión de Google para interactuar con Aplicaciones en el sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de Google, Livefyre requiere la siguiente información de proyecto de Google:

* ID de cliente
* Secreto del cliente

Para crear un proyecto de Google para utilizarlo con la identidad de Livefyre:

1. Vaya a [https://console.cloud.google.com/project](https://console.cloud.google.com/project) e inicie sesión en su cuenta de Google para crear una nueva o seleccionar una existente para utilizarla con la identidad de Livefyre.
1. Desde el panel del proyecto para la aplicación, haga clic **[!UICONTROL Enable and Manage APIs]**en.
1. En la página Información general de API, en API de Social, haga clic en para habilitar la API de Google +.
1. Desde la página Credenciales de API, seleccione **[!UICONTROL Credentials > New credentials > OAuth]** ID de cliente. En **[!UICONTROL Create client ID]** la página que se abre:

   * Seleccionar tipo de aplicación: Aplicación web.
   * Introduzca un **[!UICONTROL Name]** para **[!UICONTROL Client ID]**.
   * Deje **[!UICONTROL Authorized JavaScript origins]** campo en blanco.
   * Introduzca **[!UICONTROL Authorized redirect URIs]**: `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/google_fyre` (donde **[!UICONTROL {networkName}]** es su nombre de red proporcionado por Livefyre). Por ejemplo: ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Haga clic para **[!UICONTROL Create]** guardar sus credenciales.

Cuando se complete, la página Administrador de API de Google > Credenciales mostrará el ID de cliente del proyecto y el secreto del cliente para su uso en la página Ajustes de integración de Studio.
