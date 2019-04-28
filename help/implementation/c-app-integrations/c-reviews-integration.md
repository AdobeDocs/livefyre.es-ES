---
description: Permita que los clientes clasifiquen y revisen las ofertas de productos.
seo-description: Permita que los clientes clasifiquen y revisen las ofertas de productos.
seo-title: Críticas
solution: Experience Manager
title: Críticas
uuid: b 740 ee 28-f 6 f 9-4 ae 7-9 fe 7-61 a 5 cde 97 bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Críticas {#reviews}

Permita que los clientes clasifiquen y revisen las ofertas de productos.

Las revisiones permiten a los miembros de su comunidad mostrar clasificaciones de estrellas y revisiones cualitativas para cualquier producto o servicio.

## de CRM{#section_kk5_15b_c1b}

Para integrar una aplicación de revisiones, siga el procedimiento de integración de una aplicación de conversación. Consulte [Incrustar una aplicación](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). El siguiente es un ejemplo de una aplicación de revisiones incrustada.

### Ejemplo

```
var networkConfig = { 
   network: "client-solutions-uat.fyre.co" 
}; 
  
var convConfig = { 
   siteId: '304059', 
   articleId: 'sh_col_22_1373478370_reviews', 
   el: 'livefyre-comments', 
   app: 'reviews', 
   ratingSummaryEnabled: true, 
   maxRating: 5, 
   collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5kaXJlY3R2LmNvbS9wZXJzb24vQW5uYS1QYXF1aW4tYjJGU0wwZHJLM051YldjOS1yZXZpZXdzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAiYXJ0aWNsZUlkIjogInNoX2NvbF8yMl8xMzczNDc4MzcwX3Jldmlld3MiLCAidHlwZSI6ICJyZXZpZXdzIiwgInRpdGxlIjogIlRCX1BhcXVpbl9yYXRpbmdzX3Jldmlld3MifQ.hes3KMwygCG-fFDQlkaB-XlxGjW6-iZ68xA4RRGqUl0' 
}; 
  
Livefyre.require(['fyre.conv#3'], function (Review) { 
   new Review(networkConfig, [convConfig], function (reviewWidget) {}); 
   auth.delegate({ 
      login: function (callback) { 
         callback(null,{livefyre:'<userauthtoken>'}); 
      }, 
   }); 
});
```

Como se indica en `CollectionMeta` la sección Build, `CollectionMeta` es un objeto JSON codificado. En el ejemplo anterior, el objeto JSON toma el siguiente formato antes de codificar JWT:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## Objeto convconfig {#section_pzv_ytb_c1b}

Si ya ha completado la sección Introducción, debe estar familiarizado con el objeto convconfig. Para activar Revisiones, actualice convconfig con los siguientes campos:

* **Alwaysshoweditor** *opcional booleano* : De forma predeterminada, el editor de revisiones solo aparece una vez que el usuario pulsa el botón «revisión de escritura». Establezca este parámetro en true para mostrar siempre el editor.

* **cadena** *requerida* de la aplicación: El nombre de la aplicación que se utilizará para revisiones. Debe ser «reviews».

* **Cadena** *opcional* defaultsort: Permite seleccionar la opción de ordenación predeterminada para Revisiones. Los valores posibles son: Mosthelpful, highestrated, lowestrated, más reciente y más antiguo.

* **Disabletitle** *opcional booleano* : Desactiva y oculta el campo de título en el editor de revisiones, que es obligatorio y visible de forma predeterminada. El valor predeterminado es true.

* **Enablehalfrating** *opolean opcional* : Se utiliza para habilitar la mitad de clasificación en el módulo de selección de estrella predeterminado. El valor predeterminado es true.

* **Hideshowreviewbutton** *opcional booleano* : Controla si se mostrará [!UICONTROL Show My Review] el botón. Establezca en true para permitir a los usuarios seleccionar si mostrar o mostrar sus propias críticas.

* **Maxrating** *opcional* Used to set the number of stars that are shown on the default star selection module. El valor predeterminado es 5. Esto puede configurarse hasta 100.

* **Ratingresumen Opcional** ** Booleano opcional: Se utiliza para mostrar la vista de resumen de clasificación sobre la aplicación de revisiones. Debe estar habilitado para utilizar el ratingresumydelegate. El valor predeterminado es true.

## Revisar metadatos de la colección {#section_k1s_sqb_c1b}

* **type:***cadena requerida* : Define el tipo de colección. `reviews`Debe ser.

* **Ratingdimensions** ** opcional matriz: Matriz de cadenas para cada tipo de dimensión que utilizará esta colección. Si no se especifica, solo se permitirá 1 dimensión.

   Por ejemplo, para permitir que los usuarios clasifiquen el producto en «diseño», «características» y «rendimiento», establezca la matriz en: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **Ratingsubparts** *opcional número entero* : Número de particiones que se mostrarán en el cuadro de texto de la revisión. Las etiquetas de subparte se pasan con el parámetro como se ilustra a continuación.

   >[!NOTE]
   >Debe definir etiquetas para cada subparte.

* **Matriz** *opcional* ratingsubpartsids: Permite definir un ID para cada subsección de la colección Clasificaciones, que puede utilizarse para dirigir estos elementos de subsección en CSS y JavaScript. Cuando los usuarios publican revisiones, cada una `ratingSubpart` tendrá el atributo &quot; `data-lf-subpart-id`&quot;, rellenado con este ID.

>[!NOTE]
>
>Para utilizar `ratingSubpartsIds`, el `ratingSubparts` parámetro también debe definirse y la longitud de las dos matrices debe coincidir.

```
networkConfig["strings"] = { 
   ratingSubpartPlaceholders: ['Pros...', 'Cons...'], 
   ratingSubpartTitles: ['Pros:', 'Cons:'], 
   ratingSubpartIds: ['pros', 'cons'], 
   reviewStreamTitle: 'Description:' 
} 
fyre.conv.load(networkConfig, [{ 
   app: 'reviews', 
   ratingSubparts: 2, 
    ... // More conv config settings 
}]);
```

>[!NOTE]
>
>Si utiliza `ratingDimensions`, debe utilizar `ratingSelectionDelegate`el, `ratingDisplayDelegate`y `ratingSummaryDelegate` (si desea mostrar el resumen de clasificación).

## Personalización de revisiones {#section_khz_xmb_c1b}

### Configurar imágenes estrella

Para cambiar la imagen para estrellas completas, la clase es `goog-ratings-star`. Cambie la imagen de fondo a la imagen que desee. De forma predeterminada, las estrellas tienen 28 x 28 píxeles.

### Configurar imágenes estrella con estrellas medias

Con estrellas medias, hay dos clases, una para cada lado de la estrella. El lado izquierdo de la mitad de la estrella es `fyre-rating-half-odd` y el lado derecho `fyre-rating-half-even`es. De forma predeterminada, las estrellas medias son de 28 x 14 píxeles.

### Configurar los valores de información de objeto para las estrellas

Para configurar los valores de información sobre herramientas para las estrellas, siga el texto personalizado descrito en Personalizaciones de cadenas. Una vez configurada, utilice la clave `ratingValues` y el valor que contiene las cadenas de información sobre herramientas. Si tiene deshabilitada la mitad de las estrellas, el número de elementos de la matriz debe ser el mismo `maxRating` que (arriba). Si tiene una media de estrellas habilitadas, el número de elementos debe ser 2 x `maxRating`. El primer elemento de la matriz corresponde al elemento de estrella más a la izquierda (o a la mitad de estrella) y continúa de izquierda a derecha.

### Alternar la opción Mostrar mi revisión

Para activar o desactivar [!UICONTROL Show My Review] la opción, diríjase al `hideShowReviewButton` parámetro en la configuración de la aplicación.

### Mostrar el Editor de texto de forma predeterminada

El editor de revisiones solo aparece después de que el usuario pulse el [!UICONTROL write review] botón. Para mostrar este formulario de forma predeterminada, diríjase al `alwaysShowEditor` parámetro en la configuración de la aplicación.
