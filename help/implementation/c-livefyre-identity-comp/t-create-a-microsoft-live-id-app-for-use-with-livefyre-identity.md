---
description: Puede utilizar la identidad de Livefyre con la identidad de Microsoft Live para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones de su sitio.
seo-description: Puede utilizar la identidad de Livefyre con la identidad de Microsoft Live para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones de su sitio.
seo-title: Crear una aplicación de identidad de Microsoft Live para utilizarla con la identidad de Livefyre
solution: Experience Manager
title: Crear una aplicación de identidad de Microsoft Live para utilizarla con la identidad de Livefyre
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Crear una aplicación de identidad de Microsoft Live para utilizarla con la identidad de Livefyre{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con la identidad de Microsoft Live para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones de su sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de Microsoft Live Identity, Livefyre requiere la siguiente información de identidad de Microsoft Live:

* ID del cliente (clave privada)
* Secreto del cliente (contraseña)

Para crear una aplicación de Microsoft Live Identity para utilizarla con Livefyre Identity:

1. Cree o inicie sesión en una cuenta de Microsoft Live en [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Cree una aplicación nueva o seleccione una existente para utilizarla con la identidad de Livefyre.
1. Haga clic en **[!UICONTROL Add Platform]**, luego seleccione Web como tipo de plataforma.
1. Asegúrese de que la **[!UICONTROL Allow Implicit Flow]** opción está marcada e introduzca la dirección URL de redireccionamiento, utilizando su nombre de red en lugar de {nombre de red}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Genere un nuevo par de clave/contraseña para obtener la clave privada.
1. En **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, cambie el **[!UICONTROL Enable Microsoft Live Login]** conmutador a **[!UICONTROL On]**.
1. Introduzca Microsoft Live Client ID y Microsoft Live Client Secret.
1. Haga clic en **[!UICONTROL Save Settings]**.

Cuando se complete, la página de detalles de la aplicación de Microsoft Live Identity mostrará el ID de cliente (clave de consumidor) y el Secreto de cliente (secreto de consumidor) de la aplicación para utilizarlos en la página Configuración de integración de Studio.
