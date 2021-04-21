---
description: Puede crear reglas de flujo que extraigan contenido de Twitter.
title: Reglas de twitter
exl-id: 3a5081eb-048d-4dcf-80a2-366af2cb2c86
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Reglas de twitter{#twitter-rules}

Puede crear reglas de flujo que extraigan contenido de Twitter.

Cree reglas de Twitter basadas en hashtags, palabras clave, @mentions o autor.

Al agregar **[!UICONTROL Words]** y **[!UICONTROL Username]** para la regla, se devolverá contenido que incluye ambas entradas.

>[!NOTE]
>
>Livefyre se adhiere a las directrices de visualización de Twitter y los clientes también son responsables de cumplir estas directrices. Para obtener más información, consulte la documentación de Twitter sobre sus [requisitos de visualización](https://dev.twitter.com/terms/display-requirements).

Para crear reglas de Twitter para extraer contenido de fuentes de Twitter a su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL Keywords]**
   * Introduzca **[!UICONTROL Keywords]** para incluirlo en el flujo de Twitter o excluirlo de él. Si se especifican valores para los campos **[!UICONTROL Contains any of these words]** y **[!UICONTROL Does not contain any of these words]** , se devolverán los tweets que contienen el primero y no el segundo. Se pueden introducir varios valores para un único campo y devolverá resultados que contengan cualquiera de los valores. Para utilizar el operador booleano AND y buscar tweets con dos o más palabras, utilice dos ampersands (*&amp;*) para separar las dos palabras.
   * Por ejemplo, si se introducen las palabras clave **[!UICONTROL Contains any of these words]** Giants, Posey y **[!UICONTROL Does not contain any of these words]** Dodger, se devolverán todos los tweets que incluyan la palabra *Giants* o *Posey* y no la palabra *Dodger*.
Para buscar tweets que incluyan las palabras *Giants* y *Posey*, introduzca &quot;Giants &amp;&amp; Posey&quot;. Esta función solo se admite para los campos **[!UICONTROL Contains any of these words]** y **[!UICONTROL Does not contain any of these words]** en las reglas de Twitter.

* **[!UICONTROL Hashtags]**.
   * Introduzca **[!UICONTROL Hashtags]** para incluirlo en el flujo de Twitter o excluirlo de él. Si se especifican valores para los campos **[!UICONTROL Contains any of these words]** y **[!UICONTROL Does not contain any of these words]** , se devolverán los tweets que contienen hashtags en el primer campo y no contienen hashtags en el segundo campo. Puede introducir varios valores para un único campo. La secuencia devuelve resultados que contienen cualquiera de los valores.

* **[!UICONTROL Usernames]**
   * Introduzca **[!UICONTROL @mentions]** o **[!UICONTROL authors]** para extraer el flujo o excluir del flujo. Utilice las casillas de verificación para definir si **[!UICONTROL Retweets]** o **[!UICONTROL replies]** de los autores seleccionados también deben incluirse.

   >[!NOTE]
   >
   >Puede incluir o excluir autores; no puede combinar estos dos campos en una sola regla de Twitter.

* **[!UICONTROL Minimum number of followers.]** Seleccione el número mínimo de seguidores que el usuario debe tener para extraer información de sus anuncios.
* **[!UICONTROL Location]**

   * Introduzca la ubicación (ciudad, código postal, dirección o código geográfico en el formato común de latitud/longitud (+/- 90, +/- 180) ). Empiece a escribir una ubicación para mostrar un menú desplegable con sugerencias. Seleccione una ubicación en la lista desplegable. El mapa muestra un pin de esa ubicación. Ajuste el control deslizante para seleccionar un radio de una milla a 25 millas para cada ubicación. Si no elige un radio, Livefyre selecciona automáticamente un valor predeterminado de ocho millas.
   >[!NOTE]
   >
   >Para ambos campos, la distancia se calculará desde el centro de la ubicación de entrada.

   * Puede agregar más de una ubicación y un radio. Para eliminar una ubicación, haga clic en la X situada junto al nombre de una ubicación del cuadro.
   * Combine los campos **[!UICONTROL Is near this location]** y **[!UICONTROL Is not near this location]** para extraer contenido dentro de las ubicaciones en el campo **[!UICONTROL Is near this location]**, pero no cerca de las ubicaciones en el campo **[!UICONTROL Is not near this location]**.


* **[!UICONTROL Additional Filters]**
   * Utilice filtros adicionales para restringir aún más la regla de Twitter. Defina si:
      * Incluir **[!UICONTROL Replies]** en los tweets de destino (si el flujo llega a ser de alta velocidad, esta función se desactivará automáticamente).
      * Incluir tweets de **[!UICONTROL Verified Twitter accounts only.]**
      * Incluir **[!UICONTROL All Content]**, **[!UICONTROL Vines Only]** o **[!UICONTROL Images Only.]**
      * Incluir solo los tweets que se originen de cuentas con el **[!UICONTROL Minimum number of followers]** seleccionado (cualquiera, 100, 500, 1000, 10 000 o 100 000).

Para obtener opciones adicionales de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
