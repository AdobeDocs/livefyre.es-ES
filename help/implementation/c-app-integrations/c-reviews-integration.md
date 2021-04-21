---
description: Permita que los clientes clasifiquen y revisen sus ofertas de productos.
title: Reseñas
exl-id: 2f10646e-59c4-459c-ae1b-749f951a06d2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Revisiones {#reviews}

Permita que los clientes clasifiquen y revisen sus ofertas de productos.

Las revisiones permiten a los miembros de su comunidad contribuir con clasificaciones de estrella y revisiones cualitativas para cualquier producto o servicio.

## de CRM {#section_kk5_15b_c1b}

Para integrar una aplicación de reseñas, siga el procedimiento para integrar una aplicación de conversación. Consulte [Incrustar una aplicación](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). A continuación se muestra un ejemplo de una aplicación de revisiones incrustada.

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

Como se indica en la sección Generación `CollectionMeta` , `CollectionMeta` es un objeto JSON codificado. En el ejemplo anterior, el objeto JSON toma el siguiente formato antes de su codificación JWT:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## objeto convConfig {#section_pzv_ytb_c1b}

Si ya ha completado la sección Introducción, debe estar familiarizado con el objeto convConfig . Para habilitar las revisiones, actualice convConfig con los campos siguientes:

* **** ** alwaysShowEditoroptionalboolean: De forma predeterminada, el editor de revisiones aparece solamente después de que el usuario presione el botón &quot;reseña de escritura&quot;. Establezca este parámetro en true para mostrar siempre el editor.

* **** ** apprequiredstring: El nombre de la aplicación que se utiliza para las revisiones. Debe ser &quot;revisiones&quot;.

* **** ** defaultSortoptionalstring: Permite seleccionar la opción de ordenación predeterminada para las revisiones. Los valores posibles son: MostHelpful, highRated, lowRated, newest y más antiguo.

* **** ** disableTitleoptionalboolean: Desactiva y oculta el campo de título en el editor de revisiones, que es obligatorio y visible de forma predeterminada. El valor predeterminado es true.

* **** ** enableHalfRatingoptionalboolean: Se utiliza para habilitar las clasificaciones medias en el módulo de selección de estrellas predeterminado. El valor predeterminado es true.

* **** ** hideShowReviewButtonoptionalboolean: Controla si se mostrará el  [!UICONTROL Show My Review] botón. Configúrelo en true para permitir a los usuarios seleccionar si desean mostrar o mostrar sus propias revisiones.

* **** ** maxRatingoptionalinteger Se utiliza para establecer el número de estrellas que se muestran en el módulo de selección de estrellas predeterminado. El valor predeterminado es 5. Se puede configurar hasta 100.

* **** ** ratingSummaryEnabled optionalboolean: Se utiliza para mostrar la vista de resumen de clasificación encima de la aplicación de revisiones. Debe habilitarse para utilizar ratingSummaryDelegate. El valor predeterminado es true.

## Revisar metadatos de colección {#section_k1s_sqb_c1b}

* **type:** ** required string: Define el tipo de colección. Debe ser `reviews`.

* **** ** ratingDimensionsoptionalarray: Matriz de cadenas para cada tipo de dimensión que utilizará esta colección. Si no se especifica esto, solo se permitirá 1 dimensión.

   Por ejemplo, para permitir que los usuarios clasifiquen su producto en &quot;diseño&quot;, &quot;funciones&quot; y &quot;rendimiento&quot;, establezca la matriz en: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **** ** ratingSubpartsoptionalinteger: Número de particiones que se mostrarán en el cuadro de texto de la revisión. Las etiquetas de subparte se pasan con el parámetro como se ilustra a continuación.

   >[!NOTE]
   >Debe definir etiquetas para cada subparte.

* **** ** ratingSubpartsIdsoptionalarray: Permite definir un ID para cada subparte de la colección de clasificaciones, que se puede utilizar para dirigirse a estos elementos de subparte en el CSS y JavaScript. Cuando los usuarios publican revisiones, cada `ratingSubpart` tendrá el atributo &quot;`data-lf-subpart-id`&quot;, rellenado con este ID.

>[!NOTE]
>
>Para utilizar `ratingSubpartsIds`, el parámetro `ratingSubparts` también debe definirse y la longitud de las dos matrices debe coincidir.

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
>Si utiliza `ratingDimensions`, DEBE utilizar `ratingSelectionDelegate`, `ratingDisplayDelegate` y `ratingSummaryDelegate` (si desea mostrar el resumen de clasificación).

## Revisa la personalización {#section_khz_xmb_c1b}

### Configurar imágenes de estrella

Para cambiar la imagen para estrellas completas, la clase es `goog-ratings-star`. Cambie la imagen de fondo a la imagen que desee. De forma predeterminada, las estrellas son de 28 por 28 píxeles.

### Configurar imágenes de estrella con medias estrellas

Con media estrella, hay dos clases, una para cada lado de la estrella. El lado izquierdo de la media estrella es `fyre-rating-half-odd` y el lado derecho es `fyre-rating-half-even`. De forma predeterminada, las estrellas medias son de 28 por 14 píxeles.

### Configurar los valores de información del objeto para las estrellas

Para configurar los valores de información sobre herramientas para las estrellas, siga el texto personalizado descrito en Personalizaciones de cadenas. Una vez configurada la configuración, utilice la clave `ratingValues` y el valor de una matriz que contenga las cadenas de información del objeto. Si tiene deshabilitadas las estrellas medias, el número de elementos en la matriz debe ser el mismo que `maxRating` (arriba). Si tiene la mitad de las estrellas habilitadas, el número de elementos debe ser 2x `maxRating`. El primer elemento de la matriz corresponde al elemento estrella (o media estrella) del extremo izquierdo y continúa de izquierda a derecha.

### Alternar la opción &quot;Mostrar mi revisión&quot;

Para activar o desactivar la opción [!UICONTROL Show My Review], establezca como objetivo el parámetro `hideShowReviewButton` en la configuración de la aplicación.

### Mostrar el Editor de texto de forma predeterminada

El editor de revisiones solo aparece después de que el usuario presione el botón [!UICONTROL write review]. Para mostrar este formulario de forma predeterminada, establezca como objetivo el parámetro `alwaysShowEditor` en la configuración de la aplicación.
