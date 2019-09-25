---
description: Permite a los clientes clasificar y revisar las ofertas de productos.
seo-description: Permite a los clientes clasificar y revisar las ofertas de productos.
seo-title: Reseñas
solution: Experience Manager
title: Reseñas
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Reseñas {#reviews}

Permite a los clientes clasificar y revisar las ofertas de productos.

Las críticas permiten a los miembros de su comunidad contribuir con clasificaciones de estrella y revisiones cualitativas de cualquier producto o servicio.

## de CRM {#section_kk5_15b_c1b}

Para integrar una aplicación de críticas, siga el procedimiento para integrar una aplicación de conversación. Consulte [Incrustar una aplicación](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). El siguiente es un ejemplo de una aplicación de críticas incrustada.

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

Como se indica en la sección Generación `CollectionMeta` , `CollectionMeta` es un objeto JSON codificado. En el ejemplo anterior, el objeto JSON adopta el siguiente formato antes de codificarse en JWT:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## convConfig (objeto) {#section_pzv_ytb_c1b}

Si ya ha completado la sección Introducción, debe estar familiarizado con el objeto convConfig. Para habilitar las revisiones, actualice la convConfig con los campos siguientes:

* **alwaysShowEditor** booleano *opcional* : De forma predeterminada, el editor de revisiones solo aparece después de que el usuario pulse el botón "escribir revisión". Establezca este parámetro en true para mostrar siempre el editor.

* **cadena** necesaria *para la aplicación* : El nombre de la aplicación que se va a usar para las revisiones. Debe ser "revisiones".

* **defaultSort** , cadena *opcional* : Permite seleccionar la opción de ordenación predeterminada para las revisiones. Los valores posibles son: mostHelpful, highRated, lowRated, newest y older.

* **disableTitle** booleano *opcional* : Deshabilita y oculta el campo de título en el editor de revisiones, que es obligatorio y visible de forma predeterminada. El valor predeterminado es true.

* **enableHalfRating** booleano *opcional* : Se utiliza para habilitar las clasificaciones medias en el módulo de selección de estrella predeterminado. El valor predeterminado es true.

* **hideShowReviewButton** booleano *opcional* : Controla si se mostrará el [!UICONTROL Show My Review] botón. Establezca en true para permitir a los usuarios seleccionar si mostrar o mostrar sus propias revisiones.

* **maxRating** entero *opcional* Se utiliza para establecer el número de estrellas que se muestran en el módulo de selección de estrella predeterminado. El valor predeterminado es 5. Se puede configurar hasta 100.

* **ratingSummaryEnabled** booleano *opcional* : Se utiliza para mostrar la vista de resumen de clasificación sobre la aplicación de críticas. Debe habilitarse para utilizar ratingSummaryDelegate. El valor predeterminado es true.

## Revisar metadatos de colección {#section_k1s_sqb_c1b}

* **** type: cadena *requerida* : Define el tipo de colección. Debe ser `reviews`.

* **array** opcional *ratingDimensions* : Matriz de cadenas para cada tipo de dimensión que usará esta colección. Si no se especifica, solo se permitirá 1 dimensión.

   Por ejemplo, para permitir que los usuarios califiquen su producto en ‘diseño’, ‘características’ y ‘rendimiento’, establezca la matriz en: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **ratingSubparts** entero *opcional* : Número de particiones que se mostrarán en el cuadro de texto de la revisión. Las etiquetas de subparte se pasan con el parámetro como se ilustra a continuación.

   >[!NOTE]
   >Debe definir etiquetas para cada subparte.

* **ratingSubpartsIds** matriz *opcional* : Permite definir un ID para cada subparte de la colección Clasificaciones, que se puede utilizar para dirigirse a estos elementos de subparte en su CSS y JavaScript. Cuando los usuarios publican revisiones, cada uno `ratingSubpart` tendrá el atributo " `data-lf-subpart-id`", rellenado con este ID.

>[!NOTE]
>
>Para utilizarlo `ratingSubpartsIds`, también se debe definir el `ratingSubparts` parámetro y la longitud de las dos matrices debe coincidir.

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
>Si está utilizando `ratingDimensions`, DEBE utilizar el `ratingSelectionDelegate`, `ratingDisplayDelegate`y `ratingSummaryDelegate` (si desea mostrar el resumen de clasificación).

## Personalización de revisiones {#section_khz_xmb_c1b}

### Configurar imágenes de estrella

Para cambiar la imagen de estrellas completas, la clase es `goog-ratings-star`. Cambie la imagen de fondo a la imagen que desee. De forma predeterminada, las estrellas son 28 x 28 píxeles.

### Configurar imágenes de estrella con medias estrellas

Con media estrella, hay dos clases, una para cada lado de la estrella. El lado izquierdo de la media estrella es `fyre-rating-half-odd` y el derecho es `fyre-rating-half-even`. De forma predeterminada, las estrellas medias son 28 x 14 píxeles.

### Configuración de los valores de información de objeto para las estrellas

Para configurar los valores de información de objeto para las estrellas, siga el texto personalizado descrito en Personalizaciones de cadena. Una vez configurada, utilice la clave `ratingValues` y el valor de una matriz que contenga las cadenas de información sobre herramientas. Si tiene desactivadas las dos estrellas, el número de elementos de la matriz debe ser el mismo que `maxRating` (arriba). Si tiene las mitad de estrellas activadas, el número de elementos debe ser 2x `maxRating`. El primer elemento de la matriz corresponde al elemento de estrella (o media estrella) situado más a la izquierda y continúa de izquierda a derecha.

### Alternar la opción 'Mostrar mi revisión'

Para activar o desactivar la [!UICONTROL Show My Review] opción, establezca como objetivo el `hideShowReviewButton` parámetro en la configuración de la aplicación.

### Mostrar el Editor de texto de forma predeterminada

El editor de revisiones solo aparece después de que el usuario presione el [!UICONTROL write review] botón. Para mostrar este formulario de forma predeterminada, dirija el `alwaysShowEditor` parámetro en la configuración de la aplicación.
