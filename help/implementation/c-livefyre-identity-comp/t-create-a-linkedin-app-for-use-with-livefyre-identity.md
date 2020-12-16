---
description: Puede utilizar la identidad de Livefyre con LinkedIn para permitir que los usuarios utilicen sus inicios de sesión de LinkedIn para interactuar con las aplicaciones de su sitio.
seo-description: Puede utilizar la identidad de Livefyre con LinkedIn para permitir que los usuarios utilicen sus inicios de sesión de LinkedIn para interactuar con las aplicaciones de su sitio.
seo-title: Crear una aplicación de LinkedIn para usarla con la identidad de Livefyre
solution: Experience Manager
title: Crear una aplicación de LinkedIn para usarla con la identidad de Livefyre
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Crear una aplicación de LinkedIn para usarla con la identidad de Livefyre{#create-a-linkedin-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con LinkedIn para permitir que los usuarios utilicen sus inicios de sesión de LinkedIn para interactuar con las aplicaciones de su sitio.

Para habilitar el inicio de sesión de LinkedIn, Livefyre requiere la siguiente información de la aplicación de LinkedIn:

* clave del cliente (clave de API)
* secreto de cliente (secreto de API)

Para crear una aplicación de LinkedIn para utilizarla con la identidad de Livefyre:

1. Vaya a https://www.linkedin.com/secure/developer e inicie sesión en su cuenta de LinkedIn para crear una aplicación nueva o seleccione una existente para utilizarla con la identidad de Livefyre.
1. Haga clic **[!UICONTROL Create Application]**.
1. Complete el formulario para crear la aplicación.
1. En **[!UICONTROL Default Application Permissions]**, habilite los permisos de la aplicación **[!UICONTROL r_basicprofile]** y **[!UICONTROL r_emailaddress]**.
1. Escriba **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** como `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Guarde la aplicación.
1. En **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, cambie la **[!UICONTROL Enable LinkedIn Login]** a **[!UICONTROL On]**.
1. Introduzca el ID de cliente de LinkedIn y el secreto de cliente de LinkedIn.
1. Haga clic **[!UICONTROL Save Settings]**.

Una vez completada, la página de detalles de la aplicación de LinkedIn lista la clave de API (Clave del cliente) y el secreto de API (Secreto de cliente) de la aplicación para utilizarlos en la página Ajustes de integración de Studio.
