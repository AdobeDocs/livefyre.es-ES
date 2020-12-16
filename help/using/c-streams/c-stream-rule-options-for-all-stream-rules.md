---
description: Estas opciones se aplican a cualquier regla de flujo de todas las redes sociales o métodos de publicación.
seo-description: Estas opciones se aplican a cualquier regla de flujo de todas las redes sociales o métodos de publicación.
seo-title: Opciones de regla de flujo para todas las reglas de flujo
solution: Experience Manager
title: Opciones de regla de flujo para todas las reglas de flujo
uuid: 4072ee83-31e7-4de6-918c-134b8b8032e1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 1%

---


# Opciones de regla de flujo para todas las reglas de flujo{#stream-rule-options-for-all-stream-rules}

Estas opciones se aplican a cualquier regla de flujo de todas las redes sociales o métodos de publicación.

Buscar funciones para campos de texto y palabras clave:

* Al introducir palabras clave, Livefyre utiliza automáticamente el operador booleano **OR** cuando se trata de palabras individuales. Por ejemplo, para buscar publicaciones con la palabra *pastel* o *fórmula*, introduzca *pastel* y luego escriba *fórmula* en el campo **[!UICONTROL keyword]**.

* Puede buscar frases exactas rodeando el texto exacto de la frase entre comillas. Por ejemplo, para buscar la frase exacta *fórmula de tarta*, introduzca *&quot;fórmula de tarta&quot;* en el campo **[!UICONTROL keyword]**.

* Puede combinar las búsquedas de palabras booleanas y exactas en una regla de flujo. Por ejemplo: puede buscar *pastel*, *fórmula* y *&quot;fórmula de tarta&quot;* ingresando cada frase de una en una.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Seleccione una de las siguientes opciones:

   * **[!UICONTROL All Content.]** Permitir cualquier contenido.
   * **[!UICONTROL Media Required.]** Permitir solo contenido con imágenes y vídeos. (Para el contenido de Instagram y Facebook, solo puede especificar **[!UICONTROL Photos]** o **[!UICONTROL Videos]**).

* **[!UICONTROL Language]**. Elija el idioma en el que desea buscar. El inglés es el idioma predeterminado.
* **[!UICONTROL Smart Tags]**. Elija las etiquetas que se utilizarán para identificar el contenido. Livefyre utiliza la tecnología de la visión informática para identificar fotos y vídeos con etiquetas inteligentes específicas para que esta búsqueda sea más precisa. Utilice el modificador **[!UICONTROL ANY]** para filtrar el contenido en el flujo mediante cualquier etiqueta o el modificador **[!UICONTROL ALL]** para filtrar el contenido en el flujo que utiliza todas las etiquetas. Utilice el campo **[!UICONTROL Image contains none of these smart tags]** para introducir etiquetas para las fotografías que contengan contenido que no desee en el flujo. Esta opción no funciona para el contenido de texto.

* **[!UICONTROL Products]**. Añada las etiquetas de producto para que coincidan con la regla de flujo con los productos del catálogo de productos.
* **[!UICONTROL Premoderate]**. Seleccione una de las siguientes opciones:

   * **[!UICONTROL On]**. Premoderar todo el contenido de reglas entrantes. Puede vista de contenido premoderado desde la sección Flujos de ModQ. **[!UICONTROL On]** anula la configuración en Configuración de aplicación.
   * **[!UICONTROL Off]**. No premodere ningún contenido de regla entrante. **[!UICONTROL Off]** anula la configuración en Configuración de aplicación.
   * **[!UICONTROL Inherited (Off)]**. Utilice la configuración premoderada del sitio (en **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Seleccione una de las siguientes opciones:
   * **[!UICONTROL Apply SAFE Rules]**. Aplicar todas las reglas SAFE a este flujo.
   * **[!UICONTROL Apply SAFE Rules for:]** Seleccione una o varias de las opciones para aplicar reglas SAFE a esta regla de flujo.
   * **[!UICONTROL Disable SAFE Rules]**. No aplique ninguna regla SAFE a esta secuencia.

Para obtener información sobre las opciones de regla de flujo específicas de una red social o un tipo de contenido, consulte la siguiente documentación sobre el tipo de contenido o red social correspondiente:

* [Páginas de Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [Correo electrónico](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
