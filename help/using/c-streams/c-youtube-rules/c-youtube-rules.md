---
description: Puede crear reglas de flujo que extraigan contenido de las reglas de YouTube.
title: Reglas de YouTube
exl-id: 720a6fc6-d5de-4c78-a14e-51bced6e8dda
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Reglas de YouTube {#youtube-rules}

Puede crear reglas de flujo que extraigan contenido de las reglas de YouTube.

Cree reglas de YouTube basadas en Usuario, Canal o Lista de reproducción.

Para crear reglas de YouTube para extraer contenido de YouTube a su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL User]**
   * Introduzca la cadena mnemónica de un **[!UICONTROL User]** para incluir vídeos del usuario en el flujo.
   * Por ejemplo, si la dirección URL de la fuente de usuario que desea introducir es `https://www.youtube.com/user/livefyresupport`, simplemente introduzca `livefyresupport`.

* **[!UICONTROL Channel]**
   * Introduzca la cadena mnemónica de un **[!UICONTROL Channel]** para incluir vídeos de un canal en el flujo.
   * Por ejemplo, si la dirección URL de la fuente de canal que desea introducir es `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`, simplemente introduzca `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * Introduzca la cadena mnemónica de un **[!UICONTROL Playlist]** para incluir vídeos de una lista de reproducción en el flujo.
   * Por ejemplo, si la dirección URL de la fuente de la lista de reproducción que desea introducir es `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`, simplemente introduzca `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Si se configura como:
   * **[!UICONTROL Enabled]**, Livefyre agrega los primeros 15 elementos de contenido de la fuente al flujo, independientemente de la fecha de publicación.
   * **[!UICONTROL Disabled]**, Livefyre agrega los primeros 15 elementos de contenido de la fuente al flujo con una fecha de publicación que es la misma que la fecha de creación de la regla de flujo o posterior.

Para obtener opciones adicionales de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
