---
description: Puede crear reglas de flujo que extraigan contenido de Tumblr.
seo-description: Puede crear reglas de flujo que extraigan contenido de Tumblr.
seo-title: Reglas de Tumblr
solution: Experience Manager
title: Reglas de Tumblr
uuid: fe9601ab-aa5e-48c6-a5bf-5543c179cb90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Reglas de Tumblr{#tumblr-rules}

Puede crear reglas de flujo que extraigan contenido de Tumblr.

Cree reglas de Tumblr basadas en un blog de Tumblr y filtradas por etiqueta. Los flujos de Tumblr se actualizan cada 5 minutos, buscando contenido que no existe en Livefyre desde los primeros 20 elementos de la fuente. Livefyre ignora todo lo que haya pasado de los primeros 20 elementos de la fuente.

Para crear reglas de Tumblr para extraer contenido de Tumblr a su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL Blog]**

   * Escriba el **[!UICONTROL Blog Name]** para el blog de Tumblr. Escriba la dirección URL (*staff.tumblr.com*) o el nombre del blog (*staff*).

   * Incluya hasta un **[!UICONTROL Tag]** para filtrar los resultados por anuncios, incluida una etiqueta determinada.

* **[!UICONTROL Include recent items.]** Si se establece en:

   * **[!UICONTROL Enabled]**, Livefyre agrega los 20 primeros elementos de contenido de la fuente al flujo, independientemente de la fecha de publicación.
   * **[!UICONTROL Disabled]**, Livefyre agrega los 20 primeros elementos de contenido de la fuente al flujo con una fecha de publicación que coincide con la fecha de creación de la regla de flujo o posterior.

Para obtener opciones de regla de flujo adicionales para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
