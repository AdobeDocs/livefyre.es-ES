---
description: Puede utilizar la identidad de Livefyre con la identidad de Microsoft Live para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones del sitio.
title: Crear una aplicación de identidad de Microsoft Live para usarla con la identidad de Livefyre
exl-id: 7702c956-ecb5-424a-9866-d6f73d4d4bc9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Crear una aplicación de identidad de Microsoft Live para usarla con la identidad de Livefyre{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con la identidad de Microsoft Live para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones del sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de Microsoft Live Identity, Livefyre requiere la siguiente información de Microsoft Live Identity:

* ID del cliente (clave privada)
* Secreto del cliente (contraseña)

Para crear una aplicación de identidad de Microsoft Live para usarla con la identidad de Livefyre:

1. Cree o inicie sesión en una cuenta de Microsoft Live en [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Cree una aplicación nueva o seleccione una existente para usarla con la identidad de Livefyre.
1. Haga clic en **[!UICONTROL Add Platform]** y, a continuación, seleccione Web como tipo de plataforma.
1. Asegúrese de que la opción **[!UICONTROL Allow Implicit Flow]** esté marcada e introduzca la dirección URL de redireccionamiento, utilizando su nombre de red en lugar de {network-name}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Genere un nuevo par de contraseña/clave para obtener la clave privada.
1. En **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, cambie el **[!UICONTROL Enable Microsoft Live Login]** a **[!UICONTROL On]**.
1. Introduzca el Microsoft Live Client ID y Microsoft Live Client Secret.
1. Haga clic **[!UICONTROL Save Settings]**.

Cuando se complete, la página de detalles de la aplicación de Microsoft Live Identity enumerará el ID de cliente (clave de consumidor) y el Secreto de cliente (secreto de consumidor) de la aplicación para utilizarlos en la página Configuración de integración de Studio.
