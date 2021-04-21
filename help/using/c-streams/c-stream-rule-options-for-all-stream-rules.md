---
description: Estas opciones se aplican a cualquier regla de flujo de todas las redes sociales o métodos de publicación.
title: Opciones de reglas de flujo para todas las reglas de flujo
exl-id: eff1a3cb-395f-4eb1-be93-f0f09bba95e2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 2%

---

# Opciones de reglas de flujo para todas las reglas de flujo{#stream-rule-options-for-all-stream-rules}

Estas opciones se aplican a cualquier regla de flujo de todas las redes sociales o métodos de publicación.

Funciones de búsqueda para campos de texto y palabra clave:

* Al introducir palabras clave, Livefyre utiliza automáticamente el operador booleano **OR** cuando se trata de palabras individuales. Por ejemplo, para buscar anuncios con la palabra *pastel* o *fórmula*, introduzca *pastel* y, a continuación, introduzca *fórmula* en el campo **[!UICONTROL keyword]**.

* Puede buscar frases exactas rodeando el texto exacto de la frase entre comillas. Por ejemplo, para buscar la frase exacta *pastel recipe*, introduzca *&quot;pastel recipe&quot;* en el campo **[!UICONTROL keyword]**.

* Puede combinar las búsquedas de frases booleanas y exactas en una regla de flujo. Por ejemplo, puede buscar *pastel*, *fórmula* y *&quot;fórmula de pastel&quot;* introduciendo cada frase de una en una.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Seleccione una de las siguientes opciones:

   * **[!UICONTROL All Content.]** Permitir cualquier contenido.
   * **[!UICONTROL Media Required.]** Permitir solo contenido con imágenes y vídeos. (Para el contenido de Instagram y Facebook, solo puede especificar **[!UICONTROL Photos]** o **[!UICONTROL Videos]**).

* **[!UICONTROL Language]**. Elija el idioma en el que desea buscar. El inglés es el idioma predeterminado.
* **[!UICONTROL Smart Tags]**. Elija las etiquetas que desea utilizar para identificar el contenido. Livefyre utiliza la tecnología de visión informática para identificar fotos y vídeos con etiquetas inteligentes específicas para que esta búsqueda sea más precisa. Utilice el modificador **[!UICONTROL ANY]** para filtrar contenido en el flujo mediante cualquier etiqueta o el modificador **[!UICONTROL ALL]** para filtrar contenido en el flujo que utiliza todas las etiquetas. Utilice el campo **[!UICONTROL Image contains none of these smart tags]** para introducir etiquetas para fotos que contengan contenido que no desee en la emisión. Esta opción no funciona para el contenido de texto.

* **[!UICONTROL Products]**. Agregue etiquetas de producto para que coincidan con la regla de flujo con los productos del catálogo de productos.
* **[!UICONTROL Premoderate]**. Seleccione una de las siguientes opciones:

   * **[!UICONTROL On]**. Premoderar todo el contenido de reglas entrantes. Puede ver el contenido premoderado desde la sección Emisiones de ModQ. **[!UICONTROL On]** anula la configuración en Configuración de aplicación.
   * **[!UICONTROL Off]**. No premodere ningún contenido de regla entrante. **[!UICONTROL Off]** anula la configuración en Configuración de aplicación.
   * **[!UICONTROL Inherited (Off)]**. Utilice la configuración premoderada del sitio (en **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Seleccione una de las siguientes opciones:
   * **[!UICONTROL Apply SAFE Rules]**. Aplique todas las reglas SAFE a esta secuencia.
   * **[!UICONTROL Apply SAFE Rules for:]** Seleccione una o más de las opciones para aplicar reglas SAFE para esta regla de flujo.
   * **[!UICONTROL Disable SAFE Rules]**. No aplique ninguna regla SAFE a esta secuencia.

Para ver las opciones de reglas de flujo específicas de una red social o un tipo de contenido, consulte la siguiente documentación para la red social o el tipo de contenido respectivos:

* [Páginas de Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [Correo electrónico](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
