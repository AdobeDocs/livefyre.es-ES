---
description: Para habilitar un inicio de sesión social, utilice Studio para agregar las credenciales de sus aplicaciones sociales a su integración de Livefyre y personalice el modo de inicio de sesión.
title: Uso de Studio para conectar las aplicaciones sociales a la implementación de Livefyre
exl-id: 2ccb9737-8c59-4c1d-93d3-61f913b3cdd6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 1%

---

# Uso de Studio para conectar sus aplicaciones sociales a su implementación de Livefyre{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Para habilitar un inicio de sesión social, utilice Studio para agregar las credenciales de sus aplicaciones sociales a su integración de Livefyre y personalice el modo de inicio de sesión.

## Personalización del modo de inicio de sesión {#section_v4c_hv2_3z}

El modo de inicio de sesión le permite personalizar la información que verán los usuarios al iniciar sesión en sus aplicaciones. Puede personalizar la ventana modal.

* **Logotipo:** cargue un logotipo para utilizarlo en los modelos de inicio de sesión.
* **Familia de fuentes:** seleccione una fuente para que coincida con su marca.
* **Color de marca:** introduzca un color hexadecimal que se utilizará para texto específico dentro del modal.
* **URL de términos y condiciones:** introduzca la dirección URL de la página Términos y condiciones de la empresa. Este campo es necesario para su uso con la identidad de Livefyre.

## Traducción de la identidad de Livefyre {#section_xxt_z52_3z}

Puede crear y modificar conjuntos de traducción para cadenas de texto en la identidad de Livefyre.

Consulte Conjuntos de traducción para obtener más información sobre el uso de conjuntos de traducción con la identidad de Livefyre.

Consulte Identidad de Livefyre para obtener más información sobre las cadenas específicas que puede personalizar para Identidad de Livefyre.

## Habilitar inicio de sesión con correo electrónico {#section_dlv_wzt_bbb}

Permita que los usuarios utilicen sus direcciones de correo electrónico para iniciar sesión e interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta nativa de Livefyre:

1. Vaya a **[!UICONTROL Integration Settings]** en Livefyre Studio.
1. Cambie el conmutador **[!UICONTROL Enable Login with Email]** a **[!UICONTROL On]**.

## Habilitar inicio de sesión con una cuenta de Facebook {#section_ph3_515_bbb}

Conecte su cuenta de Facebook a Livefyre para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta de Facebook:

1. Cambie el conmutador **[!UICONTROL Enable Login with Facebook]** a **[!UICONTROL ON]**.

1. Añada las **[!UICONTROL App ID]** y **[!UICONTROL App Secret]** de la aplicación de Facebook.

   Estos valores se enumeran en el panel de desarrolladores de Facebook para la aplicación, disponible en [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Habilitar inicio de sesión con Google {#section_fq3_kb5_bbb}

Conecte su cuenta de Google+ a Livefyre para permitir que los usuarios utilicen sus inicios de sesión de Google+ para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta de Google+:

1. Cambie el conmutador **[!UICONTROL Enable Login with Google]** a **[!UICONTROL ON]**.

1. Añada las **[!UICONTROL Client ID]** y **[!UICONTROL Client secret]** de la aplicación de Google.

   Estos valores se enumeran en la interfaz de proyecto de Google Cloud Platform, disponible en [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Para recuperar esta información, vaya a **[!UICONTROL API Manager > Credentials]** y haga clic en el nombre del proyecto.

## Habilitar un inicio de sesión con una cuenta de Twitter {#section_iyz_wb5_bbb}

Conecte su cuenta de Twitter a Livefyre para permitir que los usuarios utilicen sus inicios de sesión de Twitter para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta de Twitter:

1. Cambie el conmutador **[!UICONTROL Enable Login with Twitter]** a **[!UICONTROL ON]**.

1. Añada las **[!UICONTROL Consumer Key (API Key)]** y **[!UICONTROL Consumer Secret (API Secret)]** de la aplicación de Twitter.

   Estos valores se enumeran en la página **[!UICONTROL Keys and Access Tokens]** de la aplicación de Twitter, disponible en [https://apps.twitter.com/](https://apps.twitter.com/).

## Habilitar inicio de sesión con Yahoo! Cuenta {#section_s1q_3c5_bbb}

Conecte Yahoo! cuenta a Livefyre para permitir a los usuarios utilizar su Yahoo! inicios de sesión para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión con un Yahoo! account:

1. Cambie el conmutador **[!UICONTROL Enable Login with Yahoo!]** a **[!UICONTROL ON]**.

1. Añada Yahoo! **[!UICONTROL Client ID]** y **[!UICONTROL Client Secret]** de la aplicación.

   Estos valores se enumeran en Yahoo! página de detalles de la aplicación, disponible en [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Habilitar inicio de sesión con una cuenta de Microsoft Live {#section_z42_4c5_bbb}

Conecte su cuenta de Microsoft Live ID a Livefyre para permitir que los usuarios utilicen sus inicios de sesión de Microsoft Live ID para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta de Microsoft Live ID:

1. En **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**, cambie el **[!UICONTROL Enable Microsoft Live Login]** a **[!UICONTROL On]**.

1. Introduzca **[!UICONTROL Microsoft Live Client ID (Private Key)]** y **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. Haga clic **[!UICONTROL Save Settings]**.

   Los valores **[!UICONTROL Microsoft Live Client ID (Private Key)]** y **[!UICONTROL Microsoft Live Client Secret (Password)]** se enumeran en la página de detalles de la aplicación de Microsoft Live ID.

## Conecte sus aplicaciones sociales a la identidad de Livefyre {#section_on2_vc5_bbb}

Habilite a los usuarios para que utilicen la implementación de su identidad de Livefyre para las aplicaciones de su sitio.

1. Crear una aplicación.
1. Vaya a **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]** **[!UICONTROL Livefyre Identity]**.

1. Introduzca las credenciales de la aplicación necesarias para la aplicación que ha creado.
