---
description: Puede crear reglas de flujo que extraigan contenido de reglas de YouTube.
seo-description: Puede crear reglas de flujo que extraigan contenido de reglas de YouTube.
seo-title: Reglas de YouTube
solution: Experience Manager
title: Reglas de YouTube
uuid: ec6a3780-7119-45c3-8ab2-fb0f9803d161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b

---


# Reglas de YouTube {#youtube-rules}

Puede crear reglas de flujo que extraigan contenido de reglas de YouTube.

Cree reglas de YouTube basadas en Usuario, Canal o Lista de reproducción.

Para crear reglas de YouTube para extraer contenido de YouTube a su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL User]**
   * Introduzca la cadena de vanidad de un **[!UICONTROL User]** para incluir vídeos del usuario en el flujo.
   * Por ejemplo, si la dirección URL de la fuente de usuario que desea introducir es `https://www.youtube.com/user/livefyresupport`, simplemente ingrese `livefyresupport`.

* **[!UICONTROL Channel]**
   * Introduzca la cadena de vanidad de un **[!UICONTROL Channel]** para incluir vídeos de un canal en el flujo.
   * Por ejemplo, si la dirección URL de la fuente de canal que desea introducir es `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`, simplemente ingrese `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * Introduzca la cadena de vanidad de un **[!UICONTROL Playlist]** para incluir vídeos de una lista de reproducción en el flujo.
   * Por ejemplo, si la dirección URL de la fuente de lista de reproducción que desea introducir es `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`, simplemente introduzca `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Si se establece en:
   * **[!UICONTROL Enabled]**, Livefyre agrega los primeros 15 elementos de contenido de la fuente al flujo, independientemente de la fecha de publicación.
   * **[!UICONTROL Disabled]**, Livefyre agrega los primeros 15 elementos de contenido de la fuente al flujo con una fecha de publicación que coincide con la fecha de creación de la regla de flujo o posterior.

Para obtener opciones de regla de flujo adicionales para todas las reglas de flujo, consulte Opciones de regla [de flujo para todas las reglas](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de flujo.
