---
description: Puede utilizar la identidad de Livefyre con linkedin para permitir que
  los usuarios utilicen los inicios de sesión de linkedin con el fin de interactuar
  con las aplicaciones del sitio.
seo-description: Puede utilizar la identidad de Livefyre con linkedin para permitir
  que los usuarios utilicen los inicios de sesión de linkedin con el fin de interactuar
  con las aplicaciones del sitio.
seo-title: Creación de una aplicación de linkedin para su uso con la identidad de
  Livefyre
solution: Experience Manager
title: Creación de una aplicación de linkedin para su uso con la identidad de Livefyre
uuid: c 5112 f 24-a 4 e 0-4526-afe 8-b 8 f 27 a 3 b 2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creación de una aplicación de linkedin para su uso con la identidad de Livefyre{#create-a-linkedin-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con linkedin para permitir que los usuarios utilicen los inicios de sesión de linkedin con el fin de interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión de linkedin, Livefyre requiere la siguiente información de la aplicación linkedin:

* Clave del consumidor (Clave de API)
* Secreto del consumidor (Secreto de API)

Para crear una aplicación de linkedin para utilizarla con la identidad de Livefyre:

1. Vaya a https://www.linkedin.com/secure/developer e inicie sesión en su cuenta de linkedin para crear una nueva o seleccionar una existente para utilizarla con la identidad de Livefyre.
1. Haga clic **[!UICONTROL Create Application]**en.
1. Complete el formulario para crear la aplicación.
1. En **[!UICONTROL Default Application Permissions]**, habilite los permisos **[!UICONTROL r_basicprofile]** y **[!UICONTROL r_emailaddress]** la aplicación.
1. Escriba como **[!UICONTROL OAuth 2.0 Authorized Redirect URL]**`https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Guarde la aplicación.
1. En **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, cambie **[!UICONTROL Enable LinkedIn Login]** a **[!UICONTROL On]**.
1. Introduzca el ID de cliente de linkedin y el secreto del cliente de linkedin.
1. Haga clic **[!UICONTROL Save Settings]**en.

Una vez completada, la página de detalles de la aplicación de linkedin enumera la clave de API (clave del consumidor) y la clave secreta de API (Secreto del consumidor) de la aplicación para su uso en la página Ajustes de integración de Studio.
