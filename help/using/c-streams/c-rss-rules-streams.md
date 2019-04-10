---
description: Puede crear reglas de flujo que extraigan contenido de fuentes RSS.
seo-description: Puede crear reglas de flujo que extraigan contenido de fuentes RSS.
seo-title: Reglas RSS
solution: Experience Manager
title: Reglas RSS
uuid: 3 c 9 e 2069-bb 85-41 dc -8 b 35-6237642 a 538 a
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Reglas RSS{#rss-rules}

Puede crear reglas de flujo que extraigan contenido de fuentes RSS.

Los flujos RSS se actualizan cada 5 minutos, buscando contenido que no existe en Livefyre desde los primeros 50 elementos de la fuente. Livefyre ignora todos los primeros 50 elementos de la fuente.

Para crear reglas RSS para extraer contenido de fuentes RSS en la aplicación o la carpeta, puede filtrar por:

* **[!UICONTROL URL]** de Feed RSS.
* **[!UICONTROL Include recent items.]** Si se establece en:

   * **[!UICONTROL Enabled]**, Livefyre agrega los 50 primeros elementos de contenido de la fuente al flujo, independientemente de la fecha de publicación.
   * **[!UICONTROL Disabled]**, Livefyre agrega los 50 primeros elementos de contenido de la fuente al flujo con una fecha de publicación que es la misma que la fecha de creación de regla de flujo o posterior.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Extraiga información del vínculo de elemento o del XML.

**Reglas RSS**

Livefyre analiza fuentes RSS basándose en las siguientes especificaciones RSS:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Fuente Atom](https://validator.w3.org/feed/docs/atom.html)

Livefyre no lee las fuentes que no respetan estas especificaciones y su contenido no se extraerá al flujo. Utilice el servicio de validación de fuentes WC 3 para comprobar la sintaxis de su fuente RSS y asegurarse de que sea válida.

Para obtener más opciones de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
