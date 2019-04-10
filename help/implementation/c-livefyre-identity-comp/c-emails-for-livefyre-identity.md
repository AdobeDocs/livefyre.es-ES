---
description: null
seo-description: null
seo-title: Correos electrónicos para la identidad de Livefyre
solution: Experience Manager
title: Correos electrónicos para la identidad de Livefyre
uuid: 4 e 807803-687 e -4 df 0-94 d 1-b 18 a 48 d 024 e 8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Correos electrónicos para la identidad de Livefyre{#emails-for-livefyre-identity}

La identidad de Livefyre envía los siguientes correos electrónicos:

* [Contraseña restablecida por correo electrónico](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Correo electrónico de verificación](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Enviar verificación de correo electrónico para usuarios](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Correo electrónico de bienvenida](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Enviar correo electrónico de bienvenida a los usuarios](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Puede personalizar el aspecto y la presentación de todos los correos electrónicos de identidad de Livefyre **[!UICONTROL Integration Settings > Email Notifications.]**

## Contraseña restablecida por correo electrónico {#section_nd1_whs_p1b}

Livefyre envía automáticamente un correo electrónico de restablecimiento de contraseña cuando un usuario intenta restablecer su contraseña.

El correo electrónico de restablecimiento de contraseña tiene este aspecto:

**Asunto:** Restablecer contraseña

**Cuerpo:**

Hola there *< username >*,

Se ha producido una solicitud para cambiar la contraseña del perfil en *< nombre de red >*.

Si lo ha solicitado, haga clic en el vínculo siguiente para elegir una nueva contraseña: *< URL de restablecimiento de contraseña >*.

*< Nombre de usuario >*, *< nombre de red >*y *< URL de restablecimiento de contraseña >* se generan de forma dinámica en función del visitante del sitio y de la red.

## Correo electrónico de verificación {#section_ak5_xhs_p1b}

Puede enviar un correo electrónico verificación de la dirección de correo electrónico de un usuario. Para enviar correos electrónicos de verificación, debe activar la opción en Ajustes **de integración > Identidad de Livefyre**.

El correo electrónico de verificación tiene este aspecto:

**Asunto:** Verificación de correo electrónico

**Cuerpo:**

Hola *< nombre de usuario >*,

Haga clic en el vínculo siguiente (o pegue el navegador) para verificar su cuenta: *< URL de verificación >*.

Este vínculo caducará en 24 horas.

Gracias,

El *< nombre del cliente >* Equipo

*< Nombre de usuario >*, *< nombre de red >*y *< URL de verificación >* se generan de forma dinámica en función del visitante del sitio y de la red.

## Envío de una verificación de correo electrónico a los usuarios {#section_vyv_yhs_p1b}

Puede enviar un correo electrónico a un usuario para verificar la dirección de correo electrónico que utilizan para registrarse en una cuenta. Para enviar un correo electrónico de verificación:

1. En Studio, haga clic en el icono de engranaje para modificar los ajustes de red.
1. Haga clic **en Ajustes de integración > Identidad de Livefyre.**

1. Vaya a Tipos **de inicio de sesión**.
1. Haga clic **en Requerir verificación de correo electrónico** para enviar un correo electrónico a los usuarios que verifican la dirección de correo electrónico que utilizan para registrarse en una cuenta.
1. Vaya a Correo electrónico **de red** para configurar **el logotipo de correo electrónico**, la dirección de correo electrónico que se utilizará como dirección de la dirección (**Correo electrónico desde**) y el nombre para mostrar que se utilizará en la dirección de correo electrónico (**Nombre para mostrar por correo electrónico**).

## Correo electrónico de bienvenida {#section_z2v_zhs_p1b}

Puede enviar un correo electrónico de bienvenida a los usuarios. Para enviar correos electrónicos de bienvenida, debe activar la opción Ajustes **de integración** > **Identidad de Livefyre**.

El correo electrónico de bienvenida tiene este aspecto:

**Asunto:** Bienvenido a *< nombre del cliente >*

**Cuerpo:**

Hola *< nombre de usuario >*,

Se creó una cuenta en *< nombre del cliente >*.

Esta cuenta se creó en *< URL de referencia >* desde dirección IP *< dirección IP >*.

Si lo hizo, puede ignorar este mensaje de correo electrónico de forma segura.

Si no lo hizo, comuníquese con `support@livefyre.com`

Gracias

The *"customer name"* Team

*" Nombre de usuario "," nombre del cliente "," URL de referencia "y* " Dirección IP "se generan de forma dinámica en función del visitante del sitio y de la red.

## Envío de un correo electrónico de bienvenida a un usuario {#section_kjp_c3s_p1b}

Puede enviar un correo electrónico de bienvenida a un usuario después de registrarse para una cuenta. Studio envía este mensaje de correo electrónico después de enviar un correo electrónico de verificación, si se configura un correo electrónico de verificación. Para enviar un mensaje de correo electrónico de bienvenida:

1. En Studio, haga clic en el icono de engranaje para modificar los ajustes de red.
1. Haga clic **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Vaya **[!UICONTROL Email Settings]**a.

1. Haga clic en **[!UICONTROL Send Welcome Emails To New Users]** para habilitar el envío de correos electrónicos.
1. Navegue hasta **[!UICONTROL Network Email]** Configurar *el logotipo de correo electrónico*, la dirección de correo electrónico que se utilizará como dirección de la dirección (**Correo electrónico desde**) y el nombre que se mostrará para la dirección de correo electrónico (**Nombre para mostrar por correo electrónico**).
