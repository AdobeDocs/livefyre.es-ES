---
description: Defina la configuración para solicitar derechos para anuncios de Instagram y Twitter.
seo-description: Defina la configuración para solicitar derechos para anuncios de Instagram y Twitter.
seo-title: Configuración de Rights Management
solution: Experience Manager
title: Configuración de Rights Management
uuid: 3 ffcbc 95-484 f -4 eba-b 817-658 c 1 d 658 bf 8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Configuración de Rights Management{#set-up-rights-management}

Defina la configuración para solicitar derechos para anuncios de Instagram y Twitter.

Antes de definir la Configuración de solicitudes de derechos, debe configurar una o varias cuentas sociales para Instagram o Twitter. Para obtener más información sobre cómo configurar una cuenta social, consulte [Agregar una cuenta social](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram).

>[!NOTE]
>
>Solo puede configurar la administración de derechos en el nivel de red. No se puede configurar la administración de derechos específicos del sitio.

1. En Livefyre Studio, vaya **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]** a.

   >[!NOTE]
   >
   >Necesitará permisos de nivel de red de Moderador o Administrador para configurar cuentas de administración de derechos.

1. Seleccione **[!UICONTROL +Add New Account]** si no tiene configurada ninguna cuenta de Rights Management.
1. Haga clic **[!UICONTROL Create New Setting]** en la red social que desee utilizar para Rights Management.

   >[!NOTE]
   >
   >Para las cuentas de Instagram, debe tener una cuenta empresarial de Instagram para solicitar derechos con automatización parcial. Para obtener más información sobre los distintos tipos de cuentas de Instagram y cómo utilizarlas, consulte [Acerca de las cuentas de Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

1. Rellene los campos mostrados. Se requieren todos los campos.

   * **[!UICONTROL Display name:]** Introduzca un nombre para mostrar para identificar la cuenta de Twitter o Instagram que se utilizará en su cuenta de Rights Request. Este nombre solo es interno.
   * ****[!UICONTROL Enabled:]Se establece en forma predeterminada. Habilita la administración de derechos para la cuenta.
   * **[!UICONTROL Approval hashtag:]** Hashtag que el propietario del contenido utilizará para indicar que aceptan utilizar su contenido.
   * **[!UICONTROL Terms and conditions:]** Vínculo a los Términos y condiciones de la red para reutilizar el contenido. Este campo distingue entre mayúsculas y minúsculas.
   * **[!UICONTROL Network and sites:]** Red o sitio para el cual esta cuenta puede solicitar derechos de reutilización de contenido. Para que esta cuenta esté disponible en toda la red, seleccione el primer elemento de la lista o limite en sitios específicos mediante la tecla Comando/CTRL.
   * **[!UICONTROL Default message:]** Mensaje que se muestra con su solicitud de derechos. Puede omitir este mensaje cuando solicite derechos.

      * Livefyre presenta uno de los mensajes predeterminados a moderadores cuando un moderador emite una solicitud a un autor de contenido. Los moderadores pueden generar otro mensaje predeterminado o editar el mensaje antes de enviarlo. Los mensajes deben incluir el control de Twitter o Instagram del autor ({handle}), su hashtag de aprobación ({granttag}) y un vínculo a sus Términos y condiciones ({termslink}).

         **[!UICONTROL Note:]** {handle}, {granttag} y {termslink} distinguen entre mayúsculas y minúsculas.

         **[!UICONTROL Note:]** Para evitar un uso malicioso, Twitter ajusta las URL incluidas con [formato t. co](https://t.co/) . Para evitar que el mensaje predeterminado supere los 140 caracteres, Livefyre recomienda no incluir direcciones URL en el mensaje predeterminado.

      * Prácticas recomendadas para escribir mensajes de solicitud de derechos:

         * Cree varios mensajes predeterminados para no sonar como un robot. Guarde cada mensaje predeterminado antes de crear el siguiente mensaje predeterminado.
         * Anime a los moderadores a personalizar esta nota antes de enviarla, para evitar que las solicitudes de la red se etiqueten como correo no deseado.

1. Haga clic para **[!UICONTROL Save Settings]** agregar su cuenta de Rights Request.
Envíe una solicitud de derechos desde la biblioteca de recursos. Consulte [Envío de una solicitud](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) de derechos para obtener más información sobre cómo enviar una solicitud de derechos desde la biblioteca de recursos.