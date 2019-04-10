---
description: Puede crear reglas de flujo que extraigan contenido de Instagram.
seo-description: Puede crear reglas de flujo que extraigan contenido de Instagram.
seo-title: Reglas de Instagram
title: Reglas de Instagram
uuid: 98108 ddb -5710-4331-891 b -7 e 1 bbb 106059
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Reglas de Instagram{#instagram-rules}

Puede crear reglas de flujo que extraigan contenido de Instagram.

>[!NOTE]
>
>Antes de crear un flujo de Instagram, debe agregar al menos una cuenta empresarial de Instagram a **[!UICONTROL Social Accounts]** la sección de **[!UICONTROL Network Settings]**. Para obtener más información sobre cómo configurar una cuenta de Instagram, consulte [Acerca de las cuentas de Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Cree reglas de Instagram basadas en @ mentions o hashtag.

>[!NOTE]
>
>Todas las reglas de Instagram requieren al menos un hashtag. Agregar palabras clave y un nombre de usuario para la regla devolverá contenido que incluya ambas entradas.

Para crear reglas de Instagram para extraer contenido de fuentes de Instagram en la aplicación o la carpeta, filtre por:

* **[!UICONTROL Words]**

   * Intro **[!UICONTROL hashtags]** para incluirlo en, o excluirlo del flujo de Instagram. Si se especifican valores para **[!UICONTROL Contains]** ambos **[!UICONTROL Does not contain]** campos, se devolverán imágenes que contengan el primero y no contengan el segundo.

   * Por ejemplo, si se escriben **[!UICONTROL Contains]** palabras clave Giants, Posey y palabra **[!UICONTROL Does not contain]** clave Dodger, se devolverán todas las publicaciones que incluyan la palabra Giants o Posey, y no se incluye la palabra Dodger.

      >[!NOTE]
      >
      >Las reglas de Instagram devolverán anuncios que incluyan el hashtag enumerado en los comentarios del autor, que pueden no aparecer en el flujo.

* **[!UICONTROL Mentions]**

   * Introduzca **[!UICONTROL @mentions]** para extraer el flujo o excluir del flujo.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Debe tener una cuenta comercial de Instagram configurada en Livefyre para utilizar la búsqueda Autor en una regla de flujo de Instagram. Para obtener más información sobre la configuración de cuentas comerciales de Instagram en Livefyre, consulte [Acerca de cuentas de Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Introduzca **[!UICONTROL @usernames]** para extraer el flujo. La cuenta asociada con **el nombre de usuario debe** ser una cuenta empresarial de Instagram.

   * Introduzca los **nombres de usuario que** desee excluir del flujo.

* **[!UICONTROL Additional Filters]**

   * Seleccione si desea incluir **[!UICONTROL All Content]**o **[!UICONTROL Videos Only]****[!UICONTROL Photos Only]** en el flujo.

Para obtener más opciones de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
