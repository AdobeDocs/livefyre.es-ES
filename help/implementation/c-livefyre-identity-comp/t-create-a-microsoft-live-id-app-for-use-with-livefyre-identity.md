---
description: Puede utilizar la identidad de Livefyre con Identidad de Microsoft Live para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con Aplicaciones en el sitio.
seo-description: Puede utilizar la identidad de Livefyre con Identidad de Microsoft Live para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con Aplicaciones en el sitio.
seo-title: Creación de una aplicación de identidad de Microsoft Live para su uso con la identidad de Livefyre
solution: Experience Manager
title: Creación de una aplicación de identidad de Microsoft Live para su uso con la identidad de Livefyre
uuid: 0 c 13 e 1 bc -817 f -43 ed -85 d 5-09 c 9 e 95 b 6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creación de una aplicación de identidad de Microsoft Live para su uso con la identidad de Livefyre{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con Identidad de Microsoft Live para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con Aplicaciones en el sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de identidad de Microsoft Live, Livefyre requiere la siguiente información de identidad de Microsoft Live:

* ID de cliente (clave privada)
* Secreto del cliente (Contraseña)

Para crear una aplicación de identidad de Microsoft Live para utilizarla con la identidad de Livefyre:

1. Cree o inicie sesión en una cuenta de Microsoft Live en [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Cree una nueva o seleccione una existente para utilizarla con la identidad de Livefyre.
1. Haga clic en **[!UICONTROL Add Platform]** y seleccione Web como tipo de plataforma.
1. Asegúrese de que la **[!UICONTROL Allow Implicit Flow]** opción está marcada e introduzca la URL de redireccionamiento utilizando el nombre de red en lugar de {nombre de red}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Genere un par de contraseña/clave nuevo para obtener la clave privada.
1. En **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, cambie **[!UICONTROL Enable Microsoft Live Login]** a **[!UICONTROL On]**.
1. Introduzca el ID de cliente de Microsoft Live y el secreto del cliente de Microsoft Live.
1. Haga clic **[!UICONTROL Save Settings]** en.

Cuando se complete, la página de detalles de la aplicación de Microsoft Live Identity mostrará el ID de cliente de la aplicación (Clave del consumidor) y el Secreto del cliente (Secreto del cliente) para su uso en la página Ajustes de integración de Studio.
