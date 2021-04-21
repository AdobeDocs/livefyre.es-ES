---
description: Puede crear reglas de flujo que extraigan contenido de Instagram.
title: Reglas de instagram
exl-id: ac00a12c-94b1-4464-ad3f-991382759d71
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Reglas de instagram{#instagram-rules}

Puede crear reglas de flujo que extraigan contenido de Instagram.

>[!NOTE]
>
>Antes de crear un flujo de Instagram, debe agregar al menos una cuenta comercial de Instagram a la sección **[!UICONTROL Social Accounts]** en **[!UICONTROL Network Settings]**. Para obtener más información sobre cómo configurar una cuenta de Instagram, consulte [Acerca de las cuentas de Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Cree reglas de Instagram basadas en @mentions o hashtag.

>[!NOTE]
>
>Todas las reglas de Instagram requieren al menos un hashtag. Agregar palabras clave y un nombre de usuario para la regla devolverá contenido que incluye ambas entradas.

Para crear reglas de Instagram para extraer contenido de fuentes de Instagram a su aplicación o carpeta, filtre por:

* **[!UICONTROL Words]**

   * Introduzca **[!UICONTROL hashtags]** para incluirlo en el flujo de Instagram o excluirlo de él. Si se especifican valores para los campos **[!UICONTROL Contains]** y **[!UICONTROL Does not contain]** , se devuelven imágenes que contienen la primera y no la segunda.

   * Por ejemplo: al introducir las palabras clave **[!UICONTROL Contains]** Giants, Posey y **[!UICONTROL Does not contain]** Dodger, se devolverán todas las publicaciones que incluyan la palabra Giants o Posey y no la palabra Dodger.

      >[!NOTE]
      >
      >Las reglas de instagram devolverán las publicaciones que incluyan el hashtag enumerado en los comentarios del autor, que puede que no aparezcan en el flujo.

* **[!UICONTROL Mentions]**

   * Introduzca **[!UICONTROL @mentions]** para extraer el flujo o excluirlo del flujo.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Debe tener una cuenta comercial de Instagram configurada en Livefyre para usar la búsqueda de autor en una regla de flujo de Instagram. Para obtener más información sobre la configuración de cuentas comerciales de Instagram en Livefyre, consulte [Acerca de las cuentas de Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Introduzca **[!UICONTROL @usernames]** para extraer el flujo. La cuenta asociada con **@username** debe ser una cuenta comercial de Instagram.

   * Introduzca el **@usernames** para excluir del flujo.

* **[!UICONTROL Additional Filters]**

   * Seleccione si desea incluir **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** o **[!UICONTROL Photos Only]** en el flujo.

Para obtener opciones adicionales de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
