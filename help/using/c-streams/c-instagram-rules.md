---
description: Puede crear reglas de flujo que extraigan contenido de Instagram.
seo-description: Puede crear reglas de flujo que extraigan contenido de Instagram.
seo-title: Reglas de Instagram
title: Reglas de Instagram
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---


# Reglas de Instagram{#instagram-rules}

Puede crear reglas de flujo que extraigan contenido de Instagram.

>[!NOTE]
>
>Antes de crear un flujo de Instagram, debe agregar al menos una cuenta comercial de Instagram a la sección **[!UICONTROL Social Accounts]** de **[!UICONTROL Network Settings]**. Para obtener más información sobre cómo configurar una cuenta de Instagram, consulte [Acerca de las cuentas de Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Cree reglas de Instagram basadas en @mentions o hashtag.

>[!NOTE]
>
>Todas las reglas de Instagram requieren al menos una etiqueta. Añadir palabras clave y un nombre de usuario para la regla devolverá contenido que incluye ambas entradas.

Para crear reglas de Instagram para extraer contenido de las fuentes de Instagram en la aplicación o la carpeta, filtre por:

* **[!UICONTROL Words]**

   * Escriba **[!UICONTROL hashtags]** para incluirlo o excluirlo del flujo de Instagram. Si se especifican valores para los campos **[!UICONTROL Contains]** y **[!UICONTROL Does not contain]**, se devolverán las imágenes que contengan la primera y no contengan la segunda.

   * Por ejemplo: si se introducen **[!UICONTROL Contains]** palabras clave Giants, Posey y **[!UICONTROL Does not contain]** palabra clave Dodger, se devolverán todas las publicaciones que incluyan la palabra Giants o Posey y no se incluya la palabra Dodger.

      >[!NOTE]
      >
      >Las reglas de Instagram devolverán publicaciones que incluyan el hashtag enumerado en los comentarios del autor, que pueden no aparecer en la secuencia.

* **[!UICONTROL Mentions]**

   * Introduzca **[!UICONTROL @mentions]** para extraer el flujo o excluirlo del flujo.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Debe tener una cuenta comercial de Instagram configurada en Livefyre para utilizar la búsqueda de autor en una regla de flujo de Instagram. Para obtener más información sobre la configuración de cuentas comerciales de Instagram en Livefyre, consulte [Acerca de las cuentas de Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Introduzca **[!UICONTROL @usernames]** para extraer el flujo. La cuenta asociada con el **@username** debe ser una cuenta comercial de Instagram.

   * Escriba **@usernames** para excluir del flujo.

* **[!UICONTROL Additional Filters]**

   * Seleccione si desea incluir **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** o **[!UICONTROL Photos Only]** en el flujo.

Para obtener opciones de regla de flujo adicionales para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
