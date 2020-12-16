---
description: Puede crear reglas de flujo que extraigan contenido de páginas de Facebook.
seo-description: Puede crear reglas de flujo que extraigan contenido de páginas de Facebook.
seo-title: Reglas de página de Facebook
solution: Experience Manager
title: Reglas de página de Facebook
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# Reglas de página de Facebook{#facebook-page-rules}

Puede crear reglas de flujo que extraigan contenido de páginas de Facebook.

Puede utilizar las reglas de página de Facebook para transmitir contenido publicado públicamente desde páginas de Facebook. El contenido se colocará en la aplicación o en la carpeta con la misma frecuencia que SocialSync, que cambia según los patrones de tráfico de publicaciones y páginas de Facebook. Los vínculos dentro de las páginas de Facebook también son compatibles y se mostrarán en el flujo.

Para crear reglas de página de Facebook a fin de extraer contenido de páginas de Facebook a su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL Facebook Page]**

   * Escriba el **[!UICONTROL Name]** para la página. Escriba sólo el texto final de la dirección URL. **Por ejemplo:** para agregar contenido desde  `https://facebook.com/KellysSuperFunFanPage`, escriba  ** KellysSuperFunFanPagin en el  **[!UICONTROL Name]** campo.

   * Active **[!UICONTROL Include Facebook Comments for each post]** si desea incluir comentarios de usuario en las publicaciones de la página.
   * Active **[!UICONTROL Only Show Author Posts]** si desea excluir publicaciones de otros usuarios.

Para obtener opciones de regla de flujo adicionales para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre está restringido al contenido recibido de Facebook, por lo que no puede garantizar que todas las publicaciones de una página de Facebook se incluyan en la secuencia.

>[!NOTE]
>
>Si Facebook SocialSync y una regla de página de Facebook están activadas para una página de Facebook específica y los comentarios de usuario están activados para la regla de página de Facebook, la regla de flujo omitirá SocialSync. El contenido se transmitirá en la aplicación solo en función de la regla de depuración de la página de Facebook y no mediante SocialSync.

Los tipos de contenido admitidos por el Depurador de páginas de Facebook incluyen:

* Propietario de la página o administrador

   * Estado
   * Fotos
   * Videos como vínculos

* Usuario de Facebook estándar

   * Estado
   * Fotos
   * Videos como vínculos

* Terceros

   * Estado

