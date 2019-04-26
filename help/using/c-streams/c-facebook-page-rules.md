---
description: Puede crear reglas de flujo que extraigan contenido de Páginas de Facebook.
seo-description: Puede crear reglas de flujo que extraigan contenido de Páginas de
  Facebook.
seo-title: Reglas de página de Facebook
solution: Experience Manager
title: Reglas de página de Facebook
uuid: 2 be 63476-1 a 92-409 d-a 22 f-e 1 ec 66 b 6 dcc 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Reglas de página de Facebook{#facebook-page-rules}

Puede crear reglas de flujo que extraigan contenido de Páginas de Facebook.

Puede utilizar reglas de página de Facebook para transmitir contenido publicado públicamente desde Páginas de Facebook. El contenido se traslada a la aplicación o a la carpeta con la misma frecuencia que socialsync, que cambia según la página de Facebook y los patrones de tráfico de anuncio. También se admiten los vínculos dentro de Páginas de Facebook y se mostrarán en el flujo.

Para crear reglas de página de Facebook para extraer contenido de páginas de Facebook a su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL Facebook Page]**

   * Introduzca el **[!UICONTROL Name]** para la página. Introduzca sólo el texto final de la URL. **Por ejemplo:** Para agregar contenido, `https://facebook.com/KellysSuperFunFanPage`escriba *kellyssuperfunfanpage* en **[!UICONTROL Name]** el campo.

   * Cambie **[!UICONTROL Include Facebook Comments for each post]** si desea incluir comentarios del usuario a Publicaciones de página.
   * Cambie **[!UICONTROL Only Show Author Posts]** si desea excluir publicaciones de otros usuarios.

Para obtener más opciones de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre está restringido al contenido recibido de Facebook y, por lo tanto, no es posible garantizar que cada anuncio de una página de Facebook se incluya en el flujo.

>[!NOTE]
>
>Si Facebook socialsync y una Regla de página de Facebook están habilitadas para una Página de Facebook específica y los comentarios del usuario están habilitados para la Regla de página de Facebook, la Regla de flujo anulará socialsync. El contenido se transmitirá a la aplicación en función de la regla de depuración de página de Facebook y no se utilizará socialsync.

Los tipos de contenido admitidos por la Depuración de páginas de Facebook incluyen:

* Propietario de página o Administrador

   * Estado
   * Fotos
   * Vídeos como vínculos

* Usuario de Facebook estándar

   * Estado
   * Fotos
   * Vídeos como vínculos

* Terceros

   * Estado

