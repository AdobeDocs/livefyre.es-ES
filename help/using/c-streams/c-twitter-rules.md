---
description: Puede crear reglas de flujo que extraigan contenido de Twitter.
seo-description: Puede crear reglas de flujo que extraigan contenido de Twitter.
seo-title: Reglas de Twitter
solution: Experience Manager
title: Reglas de Twitter
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Reglas de Twitter{#twitter-rules}

Puede crear reglas de flujo que extraigan contenido de Twitter.

Cree reglas de Twitter basadas en hashtags, palabras clave, @mentions o autor.

Si agrega **[!UICONTROL Words]** y agrega un **[!UICONTROL Username]** para la regla, se devolverá contenido que incluye ambas entradas.

>[!NOTE]
>
>Livefyre cumple con las pautas de visualización de Twitter, y los clientes también son responsables de cumplir estas pautas. Para obtener más información, consulte la documentación de Twitter sobre sus requisitos de [visualización](https://dev.twitter.com/terms/display-requirements).

Para crear reglas de Twitter para extraer contenido de las fuentes de Twitter en su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL Keywords]**
   * Introduzca **[!UICONTROL Keywords]** para incluirlo o excluirlo del flujo de Twitter. Si se especifican valores para los campos **[!UICONTROL Contains any of these words]** y **[!UICONTROL Does not contain any of these words]** , se devolverán los tweets que contienen el primero y no contienen el segundo. Se pueden introducir varios valores para un solo campo y se devolverán resultados que contengan cualquiera de los valores. Para utilizar el operador booleano AND y buscar tweets con dos o más palabras, utilice dos ampersands (*&amp;&amp;*) para separar las dos palabras.
   * Por ejemplo: al introducir **[!UICONTROL Contains any of these words]** palabras clave Giants, Posey y **[!UICONTROL Does not contain any of these words]** palabra clave Dodger, se devolverán todos los tweets que incluyan la palabra *Giants* o *Posey* y no incluyan la palabra *Dodger*.
Para buscar tweets que incluyan las palabras *Giants* y *Posey*, ingrese "Giants &amp;&amp; Posey". Esta función solo se admite en los campos **[!UICONTROL Contains any of these words]** y **[!UICONTROL Does not contain any of these words]** de las reglas de Twitter.

* **[!UICONTROL Hashtags]**.
   * Introduzca **[!UICONTROL Hashtags]** para incluirlo o excluirlo del flujo de Twitter. Si se especifican valores para los campos **[!UICONTROL Contains any of these words]** y **[!UICONTROL Does not contain any of these words]** , se devolverán los tweets que contienen hashtags en el primer campo y que no contienen hashtags en el segundo campo. Puede introducir varios valores para un solo campo. El flujo devuelve resultados que contienen cualquiera de los valores.

* **[!UICONTROL Usernames]**
   * Introduzca **[!UICONTROL @mentions]** o **[!UICONTROL authors]** extraiga el flujo, o excluya el flujo. Utilice las casillas de verificación para definir si **[!UICONTROL Retweets]** o **[!UICONTROL replies]** de los autores seleccionados también deben incluirse.
   >[!NOTE]
   >
   >Puede incluir o excluir autores; no puede combinar estos dos campos en una sola regla de Twitter.

* **[!UICONTROL Minimum number of followers.]** Seleccione el número mínimo de seguidores que el usuario debe tener para extraer información de sus anuncios.
* **[!UICONTROL Location]**

   * Introduzca la ubicación (ciudad, código postal, dirección o código geográfico en el formato común de latitud/longitud (+/- 90, +/- 180)). Comience escribiendo una ubicación para mostrar un menú desplegable con sugerencias. Seleccione una ubicación en el menú desplegable. El mapa muestra un pin de esa ubicación. Ajuste el control deslizante para seleccionar un radio de una milla a 25 millas por cada ubicación. Si no elige un radio, Livefyre elige automáticamente un valor predeterminado de ocho millas.
   >[!NOTE]
   >
   >Para ambos campos, la distancia se calculará desde el centro de la ubicación de entrada.

   * Puede agregar más de una ubicación y un radio. Puede eliminar una ubicación haciendo clic en la X junto al nombre de una ubicación en el cuadro.
   * Combine los campos **[!UICONTROL Is near this location]** y **[!UICONTROL Is not near this location]** para extraer contenido dentro de las ubicaciones del **[!UICONTROL Is near this location]** campo, pero no cerca de las ubicaciones del **[!UICONTROL Is not near this location]** campo.


* **[!UICONTROL Additional Filters]**
   * Utilice filtros adicionales para reducir aún más la regla de Twitter. Defina si desea:
      * Incluya **[!UICONTROL Replies]** los tweets objetivo (si el flujo se convierte en velocidad alta, esta función se desactivará automáticamente).
      * Incluir tweets de **[!UICONTROL Verified Twitter accounts only.]**
      * Incluir **[!UICONTROL All Content]** o **[!UICONTROL Vines Only]**, o **[!UICONTROL Images Only.]**
      * Incluir solo los tweets que se originan de cuentas con la selección **[!UICONTROL Minimum number of followers]** (cualquiera, 100, 500, 1000, 10 000 o 100 000).

Para obtener opciones de regla de flujo adicionales para todas las reglas de flujo, consulte Opciones de regla [de flujo para todas las reglas](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de flujo.
