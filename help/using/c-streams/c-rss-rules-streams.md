---
description: Puede crear reglas de flujo que extraigan contenido de fuentes RSS.
seo-description: Puede crear reglas de flujo que extraigan contenido de fuentes RSS.
seo-title: Reglas RSS
solution: Experience Manager
title: Reglas RSS
uuid: 3c9e2069-bb85-41dc-8b35-6237642a538a
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Reglas RSS{#rss-rules}

Puede crear reglas de flujo que extraigan contenido de fuentes RSS.

Los flujos RSS se actualizan cada 5 minutos, buscando contenido que no existe en Livefyre desde los primeros 50 elementos de la fuente. Livefyre ignora todo lo que haya pasado después de los 50 primeros elementos de la fuente.

Para crear reglas RSS para extraer contenido de fuentes RSS en la aplicación o la carpeta, puede filtrar por:

* **[!UICONTROL URL]** de la fuente RSS.
* **[!UICONTROL Include recent items.]** Si se establece en:

   * **[!UICONTROL Enabled]**, Livefyre agrega los primeros 50 elementos de contenido de la fuente al flujo, independientemente de la fecha de publicación.
   * **[!UICONTROL Disabled]**, Livefyre agrega los 50 primeros elementos de contenido de la fuente al flujo con una fecha de publicación que es la misma que la fecha de creación de la regla de flujo o posterior.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Extraiga información del vínculo del elemento o del XML.

**Reglas RSS**

Livefyre analiza las fuentes RSS basándose en las siguientes especificaciones RSS:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [Media RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Fuente Atom](https://validator.w3.org/feed/docs/atom.html)

Livefyre no lee las fuentes que no se adhieren a estas especificaciones y su contenido no se extrae en el flujo. Utilice el servicio de validación de fuentes WC3 para comprobar la sintaxis de su fuente RSS y asegurarse de que es válida.

Para obtener opciones de regla de flujo adicionales para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
