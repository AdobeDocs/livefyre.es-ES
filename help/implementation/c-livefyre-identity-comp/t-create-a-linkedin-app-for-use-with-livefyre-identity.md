---
description: Puede utilizar la identidad de Livefyre con LinkedIn para permitir que los usuarios utilicen sus inicios de sesión de LinkedIn para interactuar con las aplicaciones del sitio.
title: Crear una aplicación de LinkedIn para usarla con la identidad de Livefyre
exl-id: e77eca6a-1698-414e-994e-1189f780ada1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# Crear una aplicación de LinkedIn para usarla con la identidad de Livefyre{#create-a-linkedin-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con LinkedIn para permitir que los usuarios utilicen sus inicios de sesión de LinkedIn para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión en LinkedIn, Livefyre requiere la siguiente información de la aplicación de LinkedIn:

* Clave de consumidor (clave de API)
* Secreto del consumidor (secreto de API)

Para crear una aplicación de LinkedIn para usarla con la identidad de Livefyre:

1. Vaya a https://www.linkedin.com/secure/developer e inicie sesión en su cuenta de LinkedIn para crear una aplicación nueva o seleccionar una existente para usarla con la identidad de Livefyre.
1. Haga clic **[!UICONTROL Create Application]**.
1. Complete el formulario para crear la aplicación.
1. En **[!UICONTROL Default Application Permissions]**, habilite los permisos de las aplicaciones **[!UICONTROL r_basicprofile]** y **[!UICONTROL r_emailaddress]**.
1. Introduzca **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** como `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Guarde la aplicación.
1. En **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, cambie el **[!UICONTROL Enable LinkedIn Login]** a **[!UICONTROL On]**.
1. Introduzca el ID de cliente de LinkedIn y el Secreto de cliente de LinkedIn.
1. Haga clic **[!UICONTROL Save Settings]**.

Cuando se complete, la página de detalles de la aplicación de LinkedIn enumerará la clave de API de la aplicación (clave de consumidor) y el secreto de API (secreto de consumidor) que se utilizarán en la página Configuración de integración de Studio.
