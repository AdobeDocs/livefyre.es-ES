---
description: Para habilitar un inicio de sesión social, utilice Studio para agregar las credenciales de sus aplicaciones sociales a la integración de Livefyre y personalice el modelo de inicio de sesión.
seo-description: Para habilitar un inicio de sesión social, utilice Studio para agregar las credenciales de sus aplicaciones sociales a la integración de Livefyre y personalice el modelo de inicio de sesión.
seo-title: Uso de Studio para conectar las aplicaciones sociales a la implementación de Livefyre
title: Uso de Studio para conectar las aplicaciones sociales a la implementación de Livefyre
uuid: be14869c-e0df-48cd-a1f3-99eb953dd9ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Uso de Studio para conectar las aplicaciones sociales a la implementación de Livefyre{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Para habilitar un inicio de sesión social, utilice Studio para agregar las credenciales de sus aplicaciones sociales a la integración de Livefyre y personalice el modelo de inicio de sesión.

## Personalización del modelo de inicio de sesión {#section_v4c_hv2_3z}

El modo de inicio de sesión le permite personalizar la información que verán los usuarios al iniciar sesión en sus aplicaciones. Puede personalizar la ventana modal.

* **** Logotipo: Cargue un logotipo para utilizarlo en los modelos de inicio de sesión.
* **** Familia de fuentes: Seleccione una fuente que coincida con la marca.
* **** Color de marca: Introduzca un color hexadecimal para el texto específico dentro del modal.
* **** URL de términos y condiciones: Introduzca la dirección URL de la página Términos y condiciones de su empresa. Este campo es necesario para su uso con la identidad de Livefyre.

## Traduciendo identidad de Livefyre {#section_xxt_z52_3z}

Puede crear y modificar conjuntos de traducción para cadenas de texto en la identidad de Livefyre.

Consulte Conjuntos de traducción para obtener más información sobre el uso de conjuntos de traducción con la identidad de Livefyre.

Consulte Identidad de Livefyre para obtener más información sobre las cadenas específicas que puede personalizar para Identidad de Livefyre.

## Habilitar inicio de sesión con correo electrónico {#section_dlv_wzt_bbb}

Permita que los usuarios utilicen sus direcciones de correo electrónico para iniciar sesión e interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta nativa de Livefyre:

1. Vaya a **[!UICONTROL Integration Settings]** Livefyre Studio.
1. Cambie el **[!UICONTROL Enable Login with Email]** conmutador a **[!UICONTROL On]**.

## Habilitar inicio de sesión con una cuenta de Facebook {#section_ph3_515_bbb}

Conecte su cuenta de Facebook a Livefyre para permitir a los usuarios utilizar sus inicios de sesión de Facebook con el fin de interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta de Facebook:

1. Cambie el **[!UICONTROL Enable Login with Facebook]** conmutador a **[!UICONTROL ON]**.

1. Añada las **[!UICONTROL App ID]** y **[!UICONTROL App Secret]** las aplicaciones de Facebook.

   Estos valores se enumeran en el panel de desarrolladores de Facebook de la aplicación, disponible en [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Habilitar inicio de sesión con Google {#section_fq3_kb5_bbb}

Conecte su cuenta de Google+ a Livefyre para permitir que los usuarios puedan utilizar sus inicios de sesión de Google+ con el fin de interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta de Google+:

1. Cambie el **[!UICONTROL Enable Login with Google]** conmutador a **[!UICONTROL ON]**.

1. Añada las **[!UICONTROL Client ID]** y **[!UICONTROL Client secret]** las aplicaciones de Google.

   Estos valores se enumeran en la interfaz de proyecto de la plataforma de Google Cloud, disponible en [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Para recuperar esta información, vaya a **[!UICONTROL API Manager > Credentials]** y haga clic en el nombre del proyecto.

## Habilitar un inicio de sesión con una cuenta de Twitter {#section_iyz_wb5_bbb}

Conecte su cuenta de Twitter a Livefyre para permitir a los usuarios utilizar sus inicios de sesión de Twitter para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta de Twitter:

1. Cambie el **[!UICONTROL Enable Login with Twitter]** conmutador a **[!UICONTROL ON]**.

1. Añada las **[!UICONTROL Consumer Key (API Key)]** y **[!UICONTROL Consumer Secret (API Secret)]** las aplicaciones de Twitter.

   Estos valores se muestran en la página de la aplicación de Twitter, disponible en **[!UICONTROL Keys and Access Tokens]** https://apps.twitter.com/ [](https://apps.twitter.com/).

## Habilitar inicio de sesión con Yahoo! Cuenta {#section_s1q_3c5_bbb}

Conectar su Yahoo! a Livefyre para permitir a los usuarios utilizar su cuenta de Yahoo! inicios de sesión para interactuar con las aplicaciones del sitio.

Para habilitar el inicio de sesión mediante Yahoo! account:

1. Cambie el **[!UICONTROL Enable Login with Yahoo!]** conmutador a **[!UICONTROL ON]**.

1. Agregar su Yahoo! de la aplicación **[!UICONTROL Client ID]** y **[!UICONTROL Client Secret]**.

   Estos valores se enumeran en Yahoo! página de detalles de la aplicación, disponible en [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Habilitar inicio de sesión con una cuenta de Microsoft Live {#section_z42_4c5_bbb}

Conecte su cuenta de Microsoft Live ID a Livefyre para permitir que los usuarios puedan utilizar sus inicios de sesión de Microsoft Live ID para interactuar con las aplicaciones de su sitio.

Para habilitar el inicio de sesión con una cuenta de Microsoft Live ID:

1. En **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**, cambie el **[!UICONTROL Enable Microsoft Live Login]** conmutador a **[!UICONTROL On]**.

1. Introduzca el **[!UICONTROL Microsoft Live Client ID (Private Key)]** y **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. Haga clic en **[!UICONTROL Save Settings]**.

   Los valores **[!UICONTROL Microsoft Live Client ID (Private Key)]** y **[!UICONTROL Microsoft Live Client Secret (Password)]** se muestran en la página de detalles de la aplicación de Microsoft Live ID.

## Conectar las aplicaciones sociales a la identidad de Livefyre {#section_on2_vc5_bbb}

Permita que los usuarios utilicen la implementación de la identidad de Livefyre para las aplicaciones del sitio.

1. Crear una aplicación.
1. Vaya a **[!UICONTROL Studio]** &gt; **[!UICONTROL Settings]** &gt; **[!UICONTROL Integration Settings]**&gt; **[!UICONTROL Livefyre Identity]**.

1. Introduzca las credenciales de aplicación necesarias para la aplicación que ha creado.