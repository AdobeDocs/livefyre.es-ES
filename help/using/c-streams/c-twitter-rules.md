---
description: Puede crear reglas de flujo que extraigan contenido de Twitter.
seo-description: Puede crear reglas de flujo que extraigan contenido de Twitter.
seo-title: Reglas de Twitter
solution: Experience Manager
title: Reglas de Twitter
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---


# Reglas de Twitter{#twitter-rules}

Puede crear reglas de flujo que extraigan contenido de Twitter.

Cree reglas de Twitter basadas en hashtags, palabras clave, @mentions o autor.

Al añadir **[!UICONTROL Words]** y **[!UICONTROL Username]** para la regla, se devolverá contenido que incluye ambas entradas.

>[!NOTE]
>
>Livefyre cumple con las pautas de visualización de Twitter, y los clientes también son responsables de cumplir estas pautas. Para obtener más información, consulte la documentación de Twitter sobre sus [Requisitos de visualización](https://dev.twitter.com/terms/display-requirements).

Para crear reglas de Twitter para extraer contenido de las fuentes de Twitter en la aplicación o la carpeta, puede filtrar por:

* **[!UICONTROL Keywords]**
   * Escriba **[!UICONTROL Keywords]** para incluirlo o excluirlo del flujo de Twitter. Si se especifican valores para los campos **[!UICONTROL Contains any of these words]** y **[!UICONTROL Does not contain any of these words]**, se devolverán los tweets que contengan el primero y no contengan el segundo. Se pueden introducir varios valores para un solo campo y se devolverán resultados que contengan cualquiera de los valores. Para utilizar el operador booleano AND y buscar tweets con dos o más palabras, utilice dos ampersands (*&amp;*) para separar las dos palabras.
   * Por ejemplo: al introducir **[!UICONTROL Contains any of these words]** palabras clave Giants, Posey y **[!UICONTROL Does not contain any of these words]** palabra clave Dodger, se devolverán todos los tweets que incluyan la palabra *Giants* o *Posey* y no incluyan la palabra *Dodger*.
Para buscar tweets que incluyan las palabras *Giants* y *Posey*, ingrese &quot;Giants &amp;&amp; Posey&quot;. Esta función solo se admite para los campos **[!UICONTROL Contains any of these words]** y **[!UICONTROL Does not contain any of these words]** de las reglas de Twitter.

* **[!UICONTROL Hashtags]**.
   * Escriba **[!UICONTROL Hashtags]** para incluirlo o excluirlo del flujo de Twitter. Si se especifican valores para los campos **[!UICONTROL Contains any of these words]** y **[!UICONTROL Does not contain any of these words]**, se devolverán los tweets que contienen hashtags en el primer campo y que no contienen hashtags en el segundo campo. Puede introducir varios valores para un solo campo. El flujo devuelve resultados que contienen cualquiera de los valores.

* **[!UICONTROL Usernames]**
   * Introduzca **[!UICONTROL @mentions]** o **[!UICONTROL authors]** para extraer el flujo o excluirlo del flujo. Utilice las casillas de verificación para definir si **[!UICONTROL Retweets]** o **[!UICONTROL replies]** de los autores seleccionados también deben incluirse.

   >[!NOTE]
   >
   >Puede incluir o excluir autores; no puede combinar estos dos campos en una sola regla de Twitter.

* **[!UICONTROL Minimum number of followers.]** Seleccione el número de seguidores mínimo que el usuario debe tener para extraer información de sus anuncios.
* **[!UICONTROL Location]**

   * Introduzca la ubicación (ciudad, código postal, dirección o código geográfico en el formato común de latitud/longitud (+/- 90, +/- 180)). Comience escribiendo una ubicación para mostrar un menú desplegable con sugerencias. Seleccione una ubicación en el menú desplegable. El mapa muestra un pin de esa ubicación. Ajuste el control deslizante para seleccionar un radio de una milla a 25 millas por cada ubicación. Si no elige un radio, Livefyre elige automáticamente un valor predeterminado de ocho millas.
   >[!NOTE]
   >
   >Para ambos campos, la distancia se calculará desde el centro de la ubicación de entrada.

   * Puede agregar más de una ubicación y un radio. Puede eliminar una ubicación haciendo clic en la X junto al nombre de una ubicación en el cuadro.
   * Combine los campos **[!UICONTROL Is near this location]** y **[!UICONTROL Is not near this location]** para extraer contenido dentro de ubicaciones en el campo **[!UICONTROL Is near this location]**, pero no cerca de las ubicaciones en el campo **[!UICONTROL Is not near this location]**.


* **[!UICONTROL Additional Filters]**
   * Use Filtros adicionales para restringir aún más la regla de Twitter. Defina si lo hará:
      * Incluya **[!UICONTROL Replies]** en los tweets de destino (si el flujo llega a ser de alta velocidad, esta función se desactivará automáticamente).
      * Incluir tweets de **[!UICONTROL Verified Twitter accounts only.]**
      * Incluir **[!UICONTROL All Content]**, o **[!UICONTROL Vines Only]** o **[!UICONTROL Images Only.]**
      * Incluir solo los tweets que se originan de cuentas con el **[!UICONTROL Minimum number of followers]** seleccionado (cualquiera, 100, 500, 1000, 10.000 o 100.000).

Para obtener opciones de regla de flujo adicionales para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
