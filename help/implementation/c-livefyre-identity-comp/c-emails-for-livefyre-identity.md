---
title: Correos electrónicos para la identidad de Livefyre
description: Correos electrónicos para la identidad de Livefyre
exl-id: c8127eef-8fb8-4703-ba34-ef12453f1754
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 1%

---

# Correos electrónicos para la identidad de Livefyre{#emails-for-livefyre-identity}

La identidad de Livefyre envía los siguientes correos electrónicos:

* [Correo electrónico de restablecimiento de contraseña](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Correo electrónico de verificación](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Envío de verificación de correo electrónico para usuarios](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Mensaje de correo electrónico de bienvenida](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Enviar correo electrónico de bienvenida a los usuarios](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Puede personalizar el aspecto de todos los correos electrónicos de identidad de Livefyre en **[!UICONTROL Integration Settings > Email Notifications.]**

## Correo electrónico de restablecimiento de contraseña {#section_nd1_whs_p1b}

Livefyre envía automáticamente un correo electrónico de restablecimiento de contraseña cuando un usuario intenta restablecer su contraseña.

El correo electrónico de restablecimiento de contraseña tiene este aspecto:

**Asunto:** Restablecer contraseña

**Cuerpo:**

Oye ahí *&lt;username>*,

Hubo una solicitud para cambiar la contraseña de su perfil en *&lt;nombre de red>*.

Si lo solicitó, haga clic en el siguiente enlace para elegir una nueva contraseña: *&lt;URL de restablecimiento de contraseña>*.

*&lt;username>*,  *&lt;network name=&quot;&quot;>*, y  *&lt;password reset=&quot;&quot; URL=&quot;&quot;>* se generan de forma dinámica en función del visitante del sitio y de la red.

## Correo electrónico de verificación {#section_ak5_xhs_p1b}

Puede enviar un correo electrónico que compruebe la dirección de correo electrónico de un usuario. Para enviar correos electrónicos de verificación, debe activar la opción en **Configuración de integración > Identidad de Livefyre**.

El correo electrónico de verificación tiene este aspecto:

**Asunto: Verificación por** correo electrónico

**Cuerpo:**

Hola *&lt;username>*,

Haga clic en el siguiente vínculo (o pegue en su navegador) para verificar su cuenta: *&lt;URL de verificación>*.

Este vínculo caducará en 24 horas.

Gracias,

El equipo *&lt;nombre de cliente>*

*&lt;username>*,  *&lt;network name=&quot;&quot;>*, y  *&lt;verification URL=&quot;&quot;>* se generan de forma dinámica en función del visitante del sitio y de la red.

## Enviar una verificación de correo electrónico a los usuarios {#section_vyv_yhs_p1b}

Puede enviar un correo electrónico a un usuario para verificar la dirección de correo electrónico que utiliza para registrarse en una cuenta. Para enviar un correo electrónico de verificación:

1. En Studio, haga clic en el icono de engranaje para modificar la configuración de red.
1. Haga clic en **Configuración de integración > Identidad de Livefyre.**

1. Vaya a **Tipos de inicio de sesión**.
1. Haga clic en **Requerir verificación de correo electrónico** para enviar un correo electrónico a los usuarios que verifique la dirección de correo electrónico que utilizan para registrarse en una cuenta.
1. Vaya a **Network Email** para configurar el **Logo for Email**, la dirección de correo electrónico que se utilizará como dirección de (**Correo electrónico de**) y el nombre para mostrar que se utilizará para la dirección de correo electrónico de origen (**Nombre para mostrar del correo electrónico**).

## Mensaje de correo electrónico de bienvenida {#section_z2v_zhs_p1b}

Puede enviar un correo electrónico de bienvenida a los usuarios. Para enviar correos electrónicos de bienvenida, debe activar la opción en **Configuración de integración** > **Identidad de Livefyre**.

El correo electrónico de bienvenida tiene este aspecto:

**Asunto:** Bienvenido a  *&lt;customer name=&quot;&quot;>*

**Cuerpo:**

Hola *&lt;username>*,

Se ha creado una cuenta para usted en *&lt;customer name>*.

Esta cuenta se creó en *&lt;URL de referencia>* desde la dirección IP *&lt;Dirección IP>*.

Si lo ha hecho, puede ignorar este correo electrónico con seguridad.

Si no lo hizo, póngase en contacto con `support@livefyre.com`

Gracias

El equipo *&quot;customer name&quot;*

*&quot;Nombre de usuario&quot;, &quot;nombre de cliente&quot;, &quot;URL de referencia&quot;*  y &quot;Dirección IP&quot; se generan de forma dinámica en función del visitante del sitio y de la red.

## Enviar un correo electrónico de bienvenida a un usuario {#section_kjp_c3s_p1b}

Puede enviar un correo electrónico de bienvenida a un usuario después de que se registre en una cuenta. Studio envía este correo electrónico después de enviar un correo electrónico de verificación, si configura un correo electrónico de verificación. Para enviar un correo electrónico de bienvenida:

1. En Studio, haga clic en el icono de engranaje para modificar la configuración de red.
1. Haga clic **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Vaya a **[!UICONTROL Email Settings]**.

1. Haga clic en **[!UICONTROL Send Welcome Emails To New Users]** para habilitar el envío de correos electrónicos.
1. Vaya a **[!UICONTROL Network Email]** para configurar el *logotipo para correo electrónico*, la dirección de correo electrónico que se utilizará como dirección de (**Correo electrónico de**) y el nombre para mostrar que se utilizará para la dirección de correo electrónico de origen (**Nombre para mostrar del correo electrónico**).
