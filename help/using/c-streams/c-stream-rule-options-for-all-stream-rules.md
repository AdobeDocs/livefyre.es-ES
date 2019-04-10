---
description: Estas opciones se aplican a cualquier regla de flujo de todas las redes
  sociales o métodos de publicación.
seo-description: Estas opciones se aplican a cualquier regla de flujo de todas las
  redes sociales o métodos de publicación.
seo-title: Opciones de regla de flujo para todas las reglas de flujo
solution: Experience Manager
title: Opciones de regla de flujo para todas las reglas de flujo
uuid: 4072 ee 83-31 e 7-4 de 6-918 c -134 b 8 b 8032 e 1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Opciones de regla de flujo para todas las reglas de flujo{#stream-rule-options-for-all-stream-rules}

Estas opciones se aplican a cualquier regla de flujo de todas las redes sociales o métodos de publicación.

Funciones de búsqueda para campos de texto y palabra clave:

* Cuando se escriben palabras clave, Livefyre utiliza automáticamente el operador booleano **OR** cuando se para palabras individuales. Por ejemplo, para buscar anuncios con la *palabra ta* o *la fórmula*, escriba *cake*y, a continuación, introduzca *la fórmula* en **[!UICONTROL keyword]** el campo.

* Puede buscar frases exactas rodeando el texto exacto de frase entre comillas. Por ejemplo, para buscar la fórmula exacta *de la frase de frase*, escriba *"fórmula de pastel"* en **[!UICONTROL keyword]** el campo.

* Puede combinar las búsquedas booleanas y exactas en una regla de flujo. Por ejemplo, puede buscar *los pasteles*, *las fórmulas*y *la «fórmula de pastel»* introduciendo cada frase de uno en uno.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Seleccione una de las siguientes opciones:

   * **[!UICONTROL All Content.]** Permitir cualquier contenido.
   * **[!UICONTROL Media Required.]** Permitir solo contenido con imágenes y vídeos. (Para contenido de Instagram y Facebook, puede especificar **[!UICONTROL Photos]** o **[!UICONTROL Videos]** solamente).

* **[!UICONTROL Language]**. Elija el idioma en el que buscar. El inglés es el idioma predeterminado.
* **[!UICONTROL Smart Tags]**. Elija las etiquetas que se utilizarán para identificar el contenido. Livefyre utiliza la tecnología de la percepción del equipo para identificar fotos y vídeos con etiquetas inteligentes específicas para que esta búsqueda sea más precisa. Use **[!UICONTROL ANY]** el modificador para filtrar contenido en el flujo utilizando cualquier etiqueta o **[!UICONTROL ALL]** modificador para filtrar contenido en el flujo que utiliza todas las etiquetas. Utilice **[!UICONTROL Image contains none of these smart tags]** el campo para introducir etiquetas para fotografías que contengan contenido que no desee en el flujo. Esta opción no funciona para el contenido de texto.

* **[!UICONTROL Products]**. Agregue etiquetas de producto para que coincidan con la regla de flujo con productos del catálogo de productos.
* **[!UICONTROL Premoderate]**. Seleccione una de las siguientes opciones:

   * **[!UICONTROL On]**. Premoderar todo el contenido de la regla entrante. Puede ver contenido premoderado desde la sección Flujos de modq. **[!UICONTROL On]** anula la configuración en Configuración de aplicación.
   * **[!UICONTROL Off]**. No premodere ningún contenido de regla entrante. **[!UICONTROL Off]** anula la configuración en Configuración de aplicación.
   * **[!UICONTROL Inherited (Off)]**. Utilice la configuración premoderada del sitio (en **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Seleccione una de las siguientes opciones:
   * **[!UICONTROL Apply SAFE Rules]**. Aplique todas las reglas SAFE a este flujo.
   * **[!UICONTROL Apply SAFE Rules for:]** Seleccione una o varias de las opciones para aplicar reglas SEGURAS para esta regla de flujo.
   * **[!UICONTROL Disable SAFE Rules]**. No aplique ninguna regla SAFE a este flujo.

Para opciones de reglas de flujo específicas de una red social o un tipo de contenido, consulte la siguiente documentación para el tipo de contenido o red social correspondiente:

* [Páginas de Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [Correo electrónico](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
