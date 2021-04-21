---
description: Defina la configuración para solicitar derechos para anuncios de Instagram y Twitter.
title: Configuración del Rights Management
exl-id: d3d3e837-0ed0-47a8-ac5c-7b9da431d149
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Configurar Rights Management{#set-up-rights-management}

Defina la configuración para solicitar derechos para anuncios de Instagram y Twitter.

Para poder definir la Configuración de solicitud de derechos, debe configurar una o varias cuentas sociales para Instagram o Twitter. Para obtener más información sobre cómo configurar una cuenta de Social, consulte [Agregar una cuenta de Social](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram).

>[!NOTE]
>
>Puede configurar la administración de derechos solo en el nivel de red. No puede configurar la administración de derechos específicos del sitio.

1. En Livefyre Studio, vaya a **[!UICONTROL Network]** **[!UICONTROL Settings > Rights Management]**.

   >[!NOTE]
   >
   >Necesitará permisos de nivel de red de Moderador o Administrador para configurar cuentas de Rights Management.

1. Seleccione **[!UICONTROL +Add New Account]** si no tiene ninguna cuenta de Rights Management configurada.
1. Haga clic **[!UICONTROL Create New Setting]** en la red social que desee usar para el Rights Management.

   >[!NOTE]
   >
   >Para las cuentas de Instagram, debe tener una cuenta comercial de Instagram para solicitar derechos con automatización parcial. Para obtener más información sobre los distintos tipos de cuentas de Instagram y cómo utilizarlas, consulte [Acerca de las cuentas de Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

1. Rellene los campos mostrados. Todos los campos son obligatorios.

   * **[!UICONTROL Display name:]** Introduzca un nombre para mostrar para identificar la cuenta de Twitter o Instagram que se utilizará para la cuenta de Solicitud de derechos. Este nombre es solo interno.
   * **[!UICONTROL Enabled:]**Establézcalo en de forma predeterminada. Habilita la administración de derechos para la cuenta.
   * **[!UICONTROL Approval hashtag:]** El hashtag que el propietario del contenido utilizará para indicar que acepta usar su contenido.
   * **[!UICONTROL Terms and conditions:]** Un vínculo a los Términos y condiciones de su red para la reutilización de contenido. Este campo distingue entre mayúsculas y minúsculas.
   * **[!UICONTROL Network and sites:]** Red o sitio para el cual esta cuenta puede solicitar derechos de reutilización de contenido. Para que esta cuenta esté disponible en toda la red, seleccione el primer elemento de la lista o limite a sitios específicos mediante la tecla Comando/CTRL.
   * **[!UICONTROL Default message:]** Mensaje que se mostrará con la solicitud de derechos. Puede anular este mensaje cuando solicite derechos.

      * Livefyre presenta uno de los mensajes predeterminados a los moderadores cuando un moderador envía una solicitud a un autor de contenido. Los moderadores pueden generar otro mensaje predeterminado o editarlo antes de enviarlo. Los mensajes deben incluir el identificador de Twitter o Instagram del autor ({handle}), el hashtag de aprobación ({grantTag}) y un vínculo a los términos y condiciones ({termsLink}).

         **[!UICONTROL Note:]** {handle}, {grantTag} y {termsLink} distinguen entre mayúsculas y minúsculas.

         **[!UICONTROL Note:]** Para evitar el uso malintencionado, Twitter ajusta todas las direcciones URL incluidas con  [formato ](https://t.co/) t. Para evitar que el mensaje predeterminado supere los 140 caracteres, Livefyre recomienda no incluir direcciones URL en el mensaje predeterminado.

      * Prácticas recomendadas para escribir mensajes de solicitud de derechos:

         * Cree varios mensajes predeterminados para que no suene como un robot. Guarde cada mensaje predeterminado antes de crear el siguiente mensaje predeterminado.
         * Recomiende a los moderadores que personalicen esta nota antes de enviarla para evitar que las solicitudes de su red se etiqueten como correo no deseado.

1. Haga clic en **[!UICONTROL Save Settings]** para agregar su cuenta de solicitud de derechos.
Envíe una solicitud de derechos desde la biblioteca de recursos. Consulte [Enviar una solicitud de derechos](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) para obtener más información sobre cómo enviar una solicitud de derechos desde la biblioteca de recursos.
