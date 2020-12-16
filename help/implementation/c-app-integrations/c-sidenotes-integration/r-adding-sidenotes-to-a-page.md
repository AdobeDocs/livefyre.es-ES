---
description: 'null'
seo-description: 'null'
seo-title: Añadir notas a una página
solution: Experience Manager
title: Añadir notas a una página
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---


# Añadir notas a una página {#adding-sidenotes-to-a-page}

Livefyre proporciona varias opciones de configuración para colocar Sidenotes en la página:

* La opción Selectores define los elementos en los que deben aparecer las notas de identidad.
* Los delimitadores representan elementos que se pueden colocar en el lateral.
* El contenedor de subproceso personalizado le permite definir dónde se ubicará el subproceso Sidenotes en relación con el contenido especificado por el usuario.
* La opción Recuento de Sidenotes permite mostrar el número de Sidenotes agregados en una ubicación determinada.
* Utilice varios objetos `ConvConfig` para agregar Notas de identidad a varios artículos en una sola página.

## Selectores {#section_wyj_4sv_sy}

La opción de selectores permite que las notas de identidad encuentren contenido en la página. El valor de esta opción le permite determinar dinámicamente los elementos que se utilizarán. Puede ser una cadena de selector (como ‘#content p, #content img’), un objeto jQuery (como `$(‘#content’)`), una matriz de elementos DOM o un objeto con dos propiedades: incluir y excluir. La aplicación Sidenotes utilizará los elementos especificados o los elementos coincidentes de la página. Si se utilizan las propiedades de inclusión y exclusión, Sidenotes analizará primero la página para buscar todos los elementos de la propiedad de inclusión y, a continuación, eliminará los elementos encontrados en la propiedad de exclusión.

## Anclajes {#section_ehq_psv_sy}

Los delimitadores representan un elemento cuyo contenido se puede colocar en la ubicación remota. Un elemento de anclaje puede contener texto o una imagen. La opción de selectores que se pasa durante la construcción de la aplicación determinará los elementos de anclaje.

## ID de delimitador {#section_rsb_rsv_sy}

Los delimitadores de la página se identifican mediante un `data-lf-anchor-id`.

Para configurar el ID de un anclaje usted mismo, agregue el atributo `data-lf-custom-anchor-id` al elemento que desea asignar a un anclaje. Esto resulta útil en casos en los que la detección automática de anclajes podría fallar.

Por ejemplo, si planea utilizar una dirección URL diferente para las versiones de escritorio y móvil de una imagen, es posible que se asignen dos direcciones URL diferentes a distintos anclajes. Si, en su lugar, el HTML proporciona un `data-lf-custom-anchor-id` que es el mismo tanto en dispositivos móviles como de escritorio, el elemento de imagen se tratará como un solo anclaje.

Los delimitadores tienen un tipo que se determina dinámicamente, pero también se puede establecer explícitamente mediante el atributo `data-lf-custom-anchor-type`.

>[!NOTE]
>
>Se debe utilizar el valor del número de lista desglosada.

Los tipos disponibles son:

* **Texto:** 1
* **Imagen:** 2
* **Medios:** 3
* **Enriquecido:** 4

Consulte [método updateAnchors](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) para obtener más información sobre cómo utilizar el método `updateAnchors` para agregar contenido de Sidenote a la página de forma dinámica.

## Contenedor de subproceso personalizado {#section_jdh_btv_sy}

Utilice la opción `threadContainerEl` para especificar una ubicación para un subproceso Sidenotes, que no sea la posición predeterminada. De forma predeterminada, cuando se activa un anclaje, las Notas de identidad aparecerán junto o debajo del contenido relevante. Para cambiar este valor predeterminado, utilice `threadContainerEl` para especificar el elemento en el que debe aparecer el subproceso.

Este valor para esta opción funciona igual que la opción de selectores, excepto que solo se utilizará el primer elemento válido.

## Recuento de notas {#section_pld_ntv_sy}

Utilice la opción `numSidenotesEl` para incrustar un widget de recuento de Sidenotes opcional en la página. Esta opción acepta la misma entrada que la opción de selectores, pero solo usará el primer elemento válido en la matriz de entrada.

La utilidad decorará el elemento proporcionado o coincidente e incluirá el icono de entrada Notas de identidad, el número de Notas de identidad introducidas en esta posición y un icono de ayuda.

Al hacer clic en la utilidad se mostrará una ventana emergente con una breve explicación de Sidenotes y cómo utilizarlos.

Tanto la explicación como el texto de ejemplo se pueden configurar mediante cadenas personalizadas ( `questionExplanation` y `questionMockText`, respectivamente). El aspecto del widget de recuento y la ventana emergente también se pueden configurar usando estilos personalizados ( `numSidenotes` y `numSidenotesPopover`, respectivamente).

## Añadir varias colecciones de segmentos a una sola página {#section_pjl_ptv_sy}

Livefyre permite agregar varias colecciones Sidenotes a una sola página. Por ejemplo: si la página incluye tres artículos de noticias, es posible que desee incluir tres iteraciones distintas de la aplicación Sidenotes. Para ello, debe definir un objeto `ConvConfig` independiente para cada instancia de Sidenotes que desee generar. Por ejemplo:

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
