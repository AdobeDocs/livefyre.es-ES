---
title: Adición de notas a una página
description: Adición de notas a una página
exl-id: 3ec089d0-3d51-4918-b510-d30ef645c9c2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Adición de notas a una página {#adding-sidenotes-to-a-page}

Livefyre proporciona varias opciones de configuración para colocar las notas en la página:

* La opción Selectores define los elementos en los que deben aparecer notas.
* Los delimitadores representan elementos que se pueden desmarcar.
* El contenedor de subprocesos personalizado le permite definir dónde se ubicará el subproceso Sidenotes en relación con el contenido especificado por el usuario.
* La opción Recuento de notas permite mostrar el número de notas añadidas en una ubicación determinada.
* Utilice varios objetos `ConvConfig` para agregar notas a varios artículos en una sola página.

## Selectores {#section_wyj_4sv_sy}

La opción selectores permite que las notas encuentren contenido en la página. El valor de esta opción le permite determinar dinámicamente los elementos que se utilizarán. Puede ser una cadena de selector (como ‘#content p, #content img’), un objeto jQuery (como `$(‘#content’)`), una matriz de elementos DOM o un objeto con dos propiedades: incluir y excluir. A continuación, la aplicación Notas utilizará los elementos especificados o los elementos coincidentes de la página. Si se utilizan las propiedades de inclusión y exclusión, primero se analizará la página para buscar todos los elementos en la propiedad include y, a continuación, se eliminarán los elementos encontrados en la propiedad exclude.

## Anclajes {#section_ehq_psv_sy}

Los delimitadores representan un elemento cuyo contenido se puede colocar en la ubicación. Un elemento de anclaje puede contener texto o una imagen. La opción de selectores que se pasa durante la construcción de la aplicación determina los elementos de anclaje.

## ID de anclaje {#section_rsb_rsv_sy}

Los anclajes de la página se identifican usando un `data-lf-anchor-id`.

Para establecer el ID de un anclaje, añada el atributo `data-lf-custom-anchor-id` al elemento que desea asignar a un anclaje. Esto resulta útil en casos en los que la detección automática de anclajes podría fallar.

Por ejemplo, si planea utilizar una dirección URL diferente para las versiones de escritorio y móvil de una imagen, es posible que se asignen dos direcciones URL diferentes a distintos anclajes. Si, en su lugar, el HTML proporciona un `data-lf-custom-anchor-id` que es el mismo tanto en dispositivos móviles como de escritorio, el elemento de imagen se tratará como un anclaje único.

Los delimitadores tienen un tipo que se determina dinámicamente, pero también se puede establecer explícitamente mediante el atributo `data-lf-custom-anchor-type`.

>[!NOTE]
>
>Se debe utilizar el valor del número de enumeración.

Los tipos disponibles son:

* **Texto:** 1
* **Imagen:** 2
* **Medios:** 3
* **Enriquecido:** 4

Consulte [updateAnchors method](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) para obtener más información sobre cómo utilizar el método `updateAnchors` para añadir contenido de Sidenote a la página de forma dinámica.

## Contenedor de subprocesos personalizado {#section_jdh_btv_sy}

Utilice la opción `threadContainerEl` para especificar una ubicación para un subproceso Sidenotes, que no sea la posición predeterminada. De forma predeterminada, cuando se activa un anclaje, las notas aparecerán junto o debajo del contenido relevante. Para cambiar este valor predeterminado, utilice `threadContainerEl` para especificar el elemento en el que debe aparecer el subproceso.

Este valor para esta opción funciona igual que la opción de selectores, excepto que solo se utilizará el primer elemento válido.

## Recuento de notas {#section_pld_ntv_sy}

Utilice la opción `numSidenotesEl` para incrustar un widget de recuento de notas opcional en la página. Esta opción acepta la misma entrada que la opción de selectores, pero utiliza únicamente el primer elemento válido de la matriz de entrada.

La utilidad decorará el elemento proporcionado o coincidente e incluirá el icono de entrada Notas de la lista, el número de Notas introducidas en esta posición y un icono de ayuda.

Al hacer clic en el widget se mostrará una ventana emergente con una breve explicación de las notas y cómo utilizarlas.

Tanto la explicación como el texto de ejemplo se pueden configurar mediante cadenas personalizadas ( `questionExplanation` y `questionMockText`, respectivamente). El aspecto del widget de recuento y la ventana emergente también se pueden configurar utilizando estilos personalizados ( `numSidenotes` y `numSidenotesPopover`, respectivamente).

## Adición de varias colecciones de notas a una sola página {#section_pjl_ptv_sy}

Livefyre permite agregar varias colecciones Sidenotes a una sola página. Por ejemplo, si la página incluye tres artículos, es posible que desee incluir tres iteraciones independientes de la aplicación Notas. Para ello, debe definir un objeto `ConvConfig` independiente para cada instancia de Sidenotes que desee crear. Por ejemplo:

```
<html> 
   <head> 
      <script src="//cdn.livefyre.com/Livefyre.js"></script> 
   </head> 
<body> 
   <h2>Story #1</h2> 
   <div id="story1"> 
      <p class="sidenotes">stuff #1</p> 
      <p class="sidenotes">more stuff #1</p> 
   </div> 
   <hr /> 
   <h2>Story #2</h2> 
   <div id="story2"> 
      <p class="sidenotes">stuff #2</p> 
      <p class="sidenotes">more stuff #2</p> 
      <p class="sidenotes">more and more stuff</p> 
   </div> 
   <hr /> 
   <script type="text/javascript"> 
      var convConfig_story1 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Article ID>', 
         selectors: '#story1 > p.sidenotes', 
         collectionMeta: '<First collectionMeta>' 
      }; 
  
      var convConfig_story2 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Second Article ID>', 
         selectors: '#story2 > p.sidenotes', 
         collectionMeta: '<Second collectionMeta>' 
      }; 
  
      Livefyre.require(['sidenotes#1', 'auth'], function(Sidenotes, auth) { 
         new Sidenotes(convConfig_story1); 
         new Sidenotes(convConfig_story2); 
         auth.delegate({ 
            login: function (callback) { 
               callback(null,{livefyre: '<Login Token>'}); 
            } 
         }); 
      }); 
   </script> 
</body> 
</html>
```
