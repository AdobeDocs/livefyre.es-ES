---
description: Puede crear reglas de flujo que extraigan contenido de Tumblr.
title: Reglas de Tumblr
exl-id: 5d49b266-6d1f-4ec2-8891-5e98fcab14a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Reglas de Tumblr{#tumblr-rules}

Puede crear reglas de flujo que extraigan contenido de Tumblr.

Cree reglas de Tumblr basadas en un blog de Tumblr y filtradas por etiqueta. Los flujos de Tumblr se actualizan cada 5 minutos, buscando contenido que no exista en Livefyre desde los primeros 20 elementos de la fuente. Livefyre ignora todo lo que haya pasado de los primeros 20 elementos de la fuente.

Para crear reglas de Tumblr para extraer contenido de Tumblr a su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL Blog]**

   * Introduzca el **[!UICONTROL Blog Name]** para el blog de Tumblr. Introduzca la URL (*staff.tumblr.com*) o el nombre del blog (*staff*).

   * Incluya hasta un **[!UICONTROL Tag]** para filtrar los resultados por publicaciones, incluida una etiqueta determinada.

* **[!UICONTROL Include recent items.]** Si se configura como:

   * **[!UICONTROL Enabled]**, Livefyre agrega al flujo los 20 primeros elementos de contenido de la fuente, independientemente de la fecha de publicación.
   * **[!UICONTROL Disabled]**, Livefyre agrega los primeros 20 elementos de contenido de la fuente al flujo con una fecha de publicación que es la misma que la fecha de creación de la regla de flujo o posterior.

Para obtener opciones adicionales de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
