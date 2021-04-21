---
description: Puede crear reglas de flujo que extraigan contenido de fuentes RSS.
title: Reglas RSS
exl-id: bfb3bbad-ab26-451e-b540-d6c41f54dc31
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Reglas RSS{#rss-rules}

Puede crear reglas de flujo que extraigan contenido de fuentes RSS.

Los flujos RSS se actualizan cada 5 minutos, buscando contenido que no existe en Livefyre desde los primeros 50 elementos de la fuente. Livefyre ignora todo lo que haya pasado de los 50 primeros elementos de la fuente.

Para crear reglas RSS para extraer contenido de fuentes RSS de su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL URL]** de la fuente RSS.
* **[!UICONTROL Include recent items.]** Si se configura como:

   * **[!UICONTROL Enabled]**, Livefyre agrega los primeros 50 elementos de contenido de la fuente al flujo, independientemente de la fecha de publicación.
   * **[!UICONTROL Disabled]**, Livefyre agrega los primeros 50 elementos de contenido de la fuente al flujo con una fecha de publicación que es la misma que la fecha de creación de la regla de flujo o posterior.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Extraer información del vínculo del elemento o del XML.

**Reglas RSS**

Livefyre analiza las fuentes RSS basándose en las siguientes especificaciones RSS:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [Media RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Fuente Atom](https://validator.w3.org/feed/docs/atom.html)

Livefyre no lee fuentes que no se adhieren a estas especificaciones y su contenido no se incorpora a su flujo. Utilice el servicio de validación de fuentes WC3 para comprobar la sintaxis de su fuente RSS y asegurarse de que es válida.

Para obtener opciones adicionales de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
