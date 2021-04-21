---
description: Puede crear reglas de flujo que extraigan contenido de las páginas de Facebook.
title: Reglas de página de facebook
exl-id: 1dc728c6-81fa-4c6c-acba-d9a4aea71ed2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# Reglas de página de facebook{#facebook-page-rules}

Puede crear reglas de flujo que extraigan contenido de las páginas de Facebook.

Puede utilizar las reglas de página de Facebook para transmitir contenido publicado públicamente desde páginas de Facebook. El contenido se extraerá de la aplicación o de la carpeta con la misma frecuencia que SocialSync, que cambia según los patrones de tráfico de la página de Facebook y las publicaciones. Los vínculos de las páginas de Facebook también se admiten y se mostrarán en el flujo.

Para crear reglas de página de Facebook para extraer contenido de páginas de Facebook a su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL Facebook Page]**

   * Introduzca el **[!UICONTROL Name]** para la página. Introduzca solo el texto final de la URL. **Por ejemplo:** para añadir contenido de  `https://facebook.com/KellysSuperFunFanPage`, escriba  ** KellysSuperFunFanPagein en el  **[!UICONTROL Name]** campo .

   * Active **[!UICONTROL Include Facebook Comments for each post]** si desea incluir los comentarios del usuario en las publicaciones de la página.
   * Active **[!UICONTROL Only Show Author Posts]** si desea excluir publicaciones de otros usuarios.

Para obtener opciones adicionales de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre está restringido al contenido recibido de Facebook y, por lo tanto, no puede garantizar que todos los anuncios de una página de Facebook se incluyan en el flujo.

>[!NOTE]
>
>Si Facebook SocialSync y una regla de página de Facebook están habilitadas para una página específica de Facebook y los comentarios del usuario están habilitados para la regla de página de Facebook, la regla de flujo anulará SocialSync. El contenido se transmitirá a la aplicación solo en función de la regla de organización de páginas de Facebook y no mediante SocialSync.

Los tipos de contenido compatibles con Facebook Page Deate son:

* Propietario de página o administrador

   * Estado
   * Fotos
   * Vídeos como vínculos

* Usuario de Facebook estándar

   * Estado
   * Fotos
   * Vídeos como vínculos

* Terceros

   * Estado
