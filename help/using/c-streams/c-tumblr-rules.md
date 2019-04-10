---
description: Puede crear reglas de flujo que extraigan contenido de Tumblr.
seo-description: Puede crear reglas de flujo que extraigan contenido de Tumblr.
seo-title: Reglas Tumblr
solution: Experience Manager
title: Reglas Tumblr
uuid: fe 9601 ab-aa 5 e -48 c 6-a 5 bf -5543 c 179 cb 90
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Reglas Tumblr{#tumblr-rules}

Puede crear reglas de flujo que extraigan contenido de Tumblr.

Cree reglas Tumblr basadas en un blog Tumblr y filtre por etiqueta. Los flujos Tumblr se actualizan cada 5 minutos, buscando contenido que no existe en Livefyre desde los primeros 20 elementos de la fuente. Livefyre ignora todos los primeros 20 elementos de la fuente.

Para crear reglas Tumblr para extraer contenido de Tumblr a su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL Blog]**

   * Introduzca el **[!UICONTROL Blog Name]** para el blog Tumblr. Introduzca la dirección URL (*staff.tumblr.com*) o el nombre del blog (*personal*).

   * Incluya hasta uno **[!UICONTROL Tag]** para filtrar los resultados por anuncios que incluyan una etiqueta determinada.

* **[!UICONTROL Include recent items.]** Si se establece en:

   * **[!UICONTROL Enabled]**, Livefyre agrega los primeros 20 elementos de contenido de la fuente al flujo, independientemente de la fecha de publicación.
   * **[!UICONTROL Disabled]**, Livefyre agrega los primeros 20 elementos de contenido de la fuente al flujo con una fecha de publicación que es la misma que la fecha de creación de regla de flujo o posterior.

Para obtener más opciones de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
