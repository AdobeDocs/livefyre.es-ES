---
description: Para habilitar un inicio de sesión social, utilice Studio para agregar
  las credenciales de sus aplicaciones sociales a la integración de Livefyre y personalice
  el modal de inicio de sesión.
seo-description: Para habilitar un inicio de sesión social, utilice Studio para agregar
  las credenciales de sus aplicaciones sociales a la integración de Livefyre y personalice
  el modal de inicio de sesión.
seo-title: Uso de Studio para conectar sus aplicaciones sociales con la implementación
  de Livefyre
title: Uso de Studio para conectar sus aplicaciones sociales con la implementación
  de Livefyre
uuid: be 14869 c-e 0 df -48 cd-a 1 f 3-99 eb 953 dd 9 ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Uso de Studio para conectar sus aplicaciones sociales con la implementación de Livefyre{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Para habilitar un inicio de sesión social, utilice Studio para agregar las credenciales de sus aplicaciones sociales a la integración de Livefyre y personalice el modal de inicio de sesión.

## Personalización del modal de inicio de sesión {#section_v4c_hv2_3z}

El modal de inicio de sesión permite personalizar la información que los usuarios verán al iniciar sesión en las aplicaciones. Puede personalizar la ventana modal.

* **Logotipo:** Cargue un logotipo para usarlo en sus modales de inicio de sesión.
* **Familia de fuentes:** Seleccione una fuente para que coincida con la marca.
* **Color de marca:** Introduzca un color hexadecimal para utilizarlo para texto específico dentro del modal.
* **URL de términos y condiciones:** Introduzca la dirección URL de la página Términos y condiciones de la empresa. Este campo es necesario para su uso con la identidad de Livefyre.

## Traducción de identidad de Livefyre {#section_xxt_z52_3z}

Puede crear y modificar conjuntos de traducción para cadenas de texto en la identidad de Livefyre.

Consulte Conjuntos de traducción para obtener más información sobre el uso de conjuntos de traducción con Identidad de Livefyre.

Consulte Identidad de Livefyre para obtener más información sobre las cadenas específicas que puede personalizar para la identidad de Livefyre.

## Activar inicio de sesión con correo electrónico {#section_dlv_wzt_bbb}

Permita que los usuarios utilicen sus direcciones de correo electrónico para iniciar sesión e interactuar con aplicaciones en el sitio.

Para habilitar el inicio de sesión con una cuenta nativa de Livefyre:

1. Vaya a **[!UICONTROL Integration Settings]** Livefyre Studio.
1. Cambie **[!UICONTROL Enable Login with Email]** a **[!UICONTROL On]**.

## Habilitar inicio de sesión con una cuenta de Facebook {#section_ph3_515_bbb}

Conecte su cuenta de Facebook a Livefyre para permitir que los usuarios utilicen sus inicios de sesión de Facebook para interactuar con Aplicaciones en el sitio.

Para habilitar el inicio de sesión con una cuenta de Facebook:

1. Cambie **[!UICONTROL Enable Login with Facebook]** a **[!UICONTROL ON]**.

1. Agregue las aplicaciones de Facebook **[!UICONTROL App ID]** y **[!UICONTROL App Secret]**.

   Estos valores se enumeran en el tablero de desarrolladores de Facebook para la aplicación, disponible en [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Activar inicio de sesión con Google {#section_fq3_kb5_bbb}

Conecte su cuenta de Google + a Livefyre para permitir que los usuarios utilicen los inicios de sesión de Google + para interactuar con Aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta de Google +:

1. Cambie **[!UICONTROL Enable Login with Google]** a **[!UICONTROL ON]**.

1. Agregue las aplicaciones de Google **[!UICONTROL Client ID]** y **[!UICONTROL Client secret]**.

   Estos valores se enumeran en la interfaz de proyecto de la plataforma de Google Cloud, disponible en [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Para recuperar esta información, vaya a **[!UICONTROL API Manager > Credentials]**y haga clic en el nombre del proyecto.

## Habilitar un inicio de sesión con una cuenta de Twitter {#section_iyz_wb5_bbb}

Conecte su cuenta de Twitter a Livefyre para permitir que los usuarios utilicen sus inicios de sesión de Twitter para interactuar con Aplicaciones del sitio.

Para habilitar el inicio de sesión con una cuenta de Twitter:

1. Cambie **[!UICONTROL Enable Login with Twitter]** a **[!UICONTROL ON]**.

1. Agregue las aplicaciones de Twitter **[!UICONTROL Consumer Key (API Key)]** y **[!UICONTROL Consumer Secret (API Secret)]**.

   Estos valores se enumeran en **[!UICONTROL Keys and Access Tokens]** la página de la aplicación Twitter, disponible en [https://apps.twitter.com/](https://apps.twitter.com/).

## Habilite Iniciar sesión con Yahoo! Cuenta {#section_s1q_3c5_bbb}

Conecte su Yahoo! cuenta con Livefyre para permitir a los usuarios utilizar su Yahoo! inicios de sesión para interactuar con Aplicaciones en el sitio.

Para habilitar el inicio de sesión con un Yahoo! cuenta:

1. Cambie **[!UICONTROL Enable Login with Yahoo!]** a **[!UICONTROL ON]**.

1. Agregue su Yahoo! de la aplicación **[!UICONTROL Client ID]** y **[!UICONTROL Client Secret]**.

   Estos valores se enumeran en Yahoo! página de detalles de la aplicación, disponible en [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Activar inicio de sesión con una cuenta de Microsoft Live {#section_z42_4c5_bbb}

Conecte su cuenta de ID Live de Microsoft a Livefyre para permitir que los usuarios utilicen sus inicios de sesión de ID Live ID para interactuar con Aplicaciones en el sitio.

Para habilitar el inicio de sesión con una cuenta de ID Live de Microsoft:

1. En **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**, cambie **[!UICONTROL Enable Microsoft Live Login]** a **[!UICONTROL On]**.

1. Introduzca el **[!UICONTROL Microsoft Live Client ID (Private Key)]** y **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. Haga clic **[!UICONTROL Save Settings]**en.

   Los **[!UICONTROL Microsoft Live Client ID (Private Key)]** valores y los **[!UICONTROL Microsoft Live Client Secret (Password)]** valores se enumeran en la página de detalles de la aplicación de ID de Microsoft Live.

## Conectar las aplicaciones sociales a la identidad de Livefyre {#section_on2_vc5_bbb}

Permite a los usuarios utilizar la implementación de identidad de Livefyre para aplicaciones en el sitio.

1. Crear una aplicación.
1. Vaya a **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]**> **[!UICONTROL Livefyre Identity]**.

1. Introduzca las credenciales de la aplicación requeridas para la aplicación que ha creado.