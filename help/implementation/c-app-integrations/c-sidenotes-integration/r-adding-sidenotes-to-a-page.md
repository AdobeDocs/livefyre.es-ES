---
description: null
seo-description: null
seo-title: Adición de sidenotes a una página
solution: Experience Manager
title: Adición de sidenotes a una página
uuid: 6499 c 45 a -3773-4 adb-a 6 c 7-22 a 628309 afd
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Adición de sidenotes a una página {#adding-sidenotes-to-a-page}

Livefyre proporciona varias opciones de configuración para colocar Sidenotes en la página:

* La opción Selectores define los elementos en los que debe aparecer Sidenotes.
* Los anclajes representan elementos que se pueden transferir.
* El contenedor de subprocesos personalizado permite definir dónde se ubicará el subproceso Sidenotes en relación con el contenido que se ha cambiado.
* La opción de recuento Sidenotes permite mostrar el número de Sidenotes agregados en la ubicación dada.
* Utilice varios `ConvConfig` objetos para agregar Sidenotes a varios artículos en una sola página.

## Selectores {#section_wyj_4sv_sy}

La opción Selectores permite a Sidenotes buscar contenido en la página. El valor de esta opción permite determinar dinámicamente los elementos que se utilizarán. Puede ser una cadena de selector (como ' # content p, # content img '), un objeto jquery (como `$(‘#content’)`), una matriz de elementos DOM o un objeto con dos propiedades: incluir y excluir. La aplicación Sidenotes utilizará, a continuación, los elementos especificados o los elementos coincidentes de la página. Si se utilizan propiedades de inclusión y exclusión, Sidenotes primero analizará la página para encontrar todos los elementos de la propiedad include y, a continuación, eliminará los elementos encontrados en la propiedad exclude.

## Anclajes {#section_ehq_psv_sy}

Los anclajes representan un elemento cuyo contenido se puede transferir. Un elemento delimitador puede contener texto o una imagen. La opción de selectores que se pasa durante la construcción de la aplicación determinará los elementos delimitadores.

## ID de anclaje {#section_rsb_rsv_sy}

Los anclajes de la página se identifican usando `data-lf-anchor-id`un.

Para configurar el ID de un anclaje usted mismo, agregue el atributo `data-lf-custom-anchor-id` al elemento que desee asignar a un anclaje. Esto resulta útil en casos en los que la detección automática de los anclajes podría fallar.

Por ejemplo, si planea utilizar una URL diferente para las versiones de escritorio y móviles de una imagen, dos URL diferentes pueden asignarse a diferentes delimitadores. Si, en su lugar, el HTML proporciona una `data-lf-custom-anchor-id` misma función tanto en dispositivos móviles como en escritorio, el elemento de imagen se tratará como un anclaje único.

Los anclajes tienen un tipo determinado dinámicamente, pero también se pueden establecer explícitamente con `data-lf-custom-anchor-type` el atributo.

>[!NOTE]
>
>Se debe utilizar el valor de número de enumeración.

Los tipos disponibles son:

* **Texto:** 1
* **Imagen:** 2
* **Medios:** 3
* **Rich:** 4

Consulte [Método updateanchors](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) para obtener más información sobre cómo utilizar `updateAnchors` el método para añadir contenido Sidenote a la página dinámicamente.

## Contenedor de subprocesos personalizados {#section_jdh_btv_sy}

Utilice `threadContainerEl` la opción para especificar una ubicación para un subproceso Sidenotes, aparte de la posición predeterminada. De forma predeterminada, cuando se activa un anclaje, los Sidenotes aparecerán junto o debajo del contenido relevante. Para cambiar este valor predeterminado, utilice `threadContainerEl` para especificar el elemento donde debería aparecer el hilo.

Este valor de esta opción funciona igual que la opción selectores, excepto que se utilizará sólo el primer elemento válido.

## Recuento de Sidenotes {#section_pld_ntv_sy}

Utilice `numSidenotesEl` la opción para incrustar un widget de recuento Sidenotes opcional en la página. Esta opción acepta la misma entrada que la opción selectores pero solo utilizará el primer elemento válido en la matriz de entrada.

La utilidad decorará el elemento proporcionado o coincidente, e incluirá el icono de entrada Sidenotes, el número de Sidenotes ingresado en esta posición y un icono de ayuda.

Al hacer clic en la utilidad se mostrará una ventana emergente con una breve explicación de Sidenotes y cómo utilizarlos.

Tanto la explicación como el texto de ejemplo se pueden configurar usando cadenas personalizadas ( `questionExplanation` y `questionMockText`, respectivamente). La apariencia del widget de recuento y la ventana emergente también se pueden configurar usando estilos personalizados ( `numSidenotes` y `numSidenotesPopover`, respectivamente).

## Adición de colecciones múltiples a una sola página {#section_pjl_ptv_sy}

Livefyre le permite añadir varias colecciones Sidenotes a una sola página. Por ejemplo, si la página incluye tres artículos de noticias, es posible que desee incluir tres repeticiones independientes de la aplicación Sidenotes. Para ello, debe definir un objeto independiente `ConvConfig` para cada instancia de Sidenotes que desee crear. Por ejemplo:

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
