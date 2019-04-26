---
description: Puede crear reglas de flujo que extraigan contenido de Twitter.
seo-description: Puede crear reglas de flujo que extraigan contenido de Twitter.
seo-title: Reglas de Twitter
solution: Experience Manager
title: Reglas de Twitter
uuid: a 7 fd 2398-fd 6 b -4 c 24-92 b 2-7471176 d 7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Reglas de Twitter{#twitter-rules}

Puede crear reglas de flujo que extraigan contenido de Twitter.

Cree reglas de Twitter basadas en hashtags, palabras clave, @ mentions o autor.

Agregar **[!UICONTROL Words]** y un **[!UICONTROL Username]** para la regla devolverá contenido que incluya ambas entradas.

>[!NOTE]
>
>Livefyre se adhiere a las directrices de visualización de Twitter, y los clientes también son responsables de cumplir estas directrices. Para obtener más información, consulte la documentación de Twitter sobre los requisitos [de visualización](https://dev.twitter.com/terms/display-requirements).

Para crear reglas de Twitter para extraer contenido de fuentes de Twitter a su aplicación o carpeta, puede filtrar por:

* **[!UICONTROL Keywords]**
   * Escriba **[!UICONTROL Keywords]** para incluirlo en la secuencia de Twitter o excluirla. Si se especifican valores para **[!UICONTROL Contains any of these words]** ambos **[!UICONTROL Does not contain any of these words]** campos, se devolverán los tweets que contengan el primero y no contienen el segundo. Se pueden introducir varios valores para un único campo y devolverá resultados que contengan alguno de los valores. Para utilizar el operador booleano AND para buscar tweets con dos o más palabras en ellas, utilice dos ampersands (*& &*) para separar las dos palabras.
   * Por ejemplo, si se introducen **[!UICONTROL Contains any of these words]** palabras clave Giants, Posey y la **[!UICONTROL Does not contain any of these words]** palabra clave Dodger, se devolverán todos los tweets que incluyan la palabra *Giants* o *Posey* y no incluyan la palabra *Dodger*.
Para buscar tweets que incluyan tanto las palabras *Giants* y *el Posey*, escriba «Giants & & Posey». Esta función solo se admite para **[!UICONTROL Contains any of these words]** los **[!UICONTROL Does not contain any of these words]** campos y las reglas de Twitter.

* **[!UICONTROL Hashtags]**.
   * Escriba **[!UICONTROL Hashtags]** para incluirlo en la secuencia de Twitter o excluirla. Si se especifican valores para **[!UICONTROL Contains any of these words]** y **[!UICONTROL Does not contain any of these words]** campos, se devolverán tweets que contengan hashtags en el primer campo y no contienen hashtags en el segundo campo. Puede introducir varios valores para un solo campo. El flujo devuelve resultados que contienen alguno de los valores.

* **[!UICONTROL Usernames]**
   * Introduzca **[!UICONTROL @mentions]** o **[!UICONTROL authors]** para extraer el flujo o excluir del flujo. Utilice las casillas para definir si **[!UICONTROL Retweets]****[!UICONTROL replies]** también deben incluirse los autores seleccionados.
   >[!NOTE]
   >
   >Puede incluir o excluir autores; no puede combinar estos dos campos en una sola regla de Twitter.

* **[!UICONTROL Minimum number of followers.]** Seleccione el número mínimo de seguidores que el usuario debe tener para extraer información de sus publicaciones.
* **[!UICONTROL Location]**

   * Introduzca la ubicación (ciudad, código postal, dirección o código geográfico en el formato común latitud/longitud (+/- 90, +/- 180)). Empiece a escribir una ubicación para mostrar un menú desplegable con sugerencias. Seleccione una ubicación en la lista desplegable. El mapa muestra una chincheta de esa ubicación. Ajuste el control deslizante para seleccionar un radio de una milla a 25 millas para cada ubicación. Si no elige un radio, Livefyre elige automáticamente un valor predeterminado de ocho millas.
   >[!NOTE]
   >
   >Para ambos campos, la distancia se calculará desde el centro de la ubicación de entrada.

   * Puede agregar más de una ubicación y radio. Puede eliminar una ubicación haciendo clic en la X junto al nombre de una ubicación en el cuadro.
   * Combine los **[!UICONTROL Is near this location]** campos y **[!UICONTROL Is not near this location]** los campos para extraer contenido dentro de ubicaciones del **[!UICONTROL Is near this location]** campo, pero no cerca de las ubicaciones del **[!UICONTROL Is not near this location]** campo.


* **[!UICONTROL Additional Filters]**
   * Utilice Filtros adicionales para restringir aún más la regla de Twitter. Defina si lo hace:
      * Incluir **[!UICONTROL Replies]** a los tweets objetivo (si el flujo se convierte en una velocidad alta, esta función se desactivará automáticamente).
      * Incluir tweets desde **[!UICONTROL Verified Twitter accounts only.]**
      * Incluir **[!UICONTROL All Content]**, o **[!UICONTROL Vines Only]**, o **[!UICONTROL Images Only.]**
      * Incluir solo los tweets que proceden de cuentas con la selección **[!UICONTROL Minimum number of followers]** (cualquiera, 100, 500, 1000, 10.000 o 100.000).

Para obtener más opciones de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
