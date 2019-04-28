---
description: Los estilos personalizados se aplican a través de un objeto insertado en el constructor Sidenotes.
seo-description: Los estilos personalizados se aplican a través de un objeto insertado en el constructor Sidenotes.
seo-title: Estilos personalizados de Sidenotes
title: Estilos personalizados de Sidenotes
uuid: 0 f 6 d 7 ad 6-1 f 6 a -4 ed 2-b 86 a -0 d 03782 e 591 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Estilos personalizados de Sidenotes{#sidenotes-custom-styles}

Los estilos personalizados se aplican a través de un objeto insertado en el constructor Sidenotes.

Las «claves» son claves de objeto que representan elementos DOM, mientras que «propiedades» son propiedades CSS para la clave en particular. Por ejemplo, para personalizar el estilo de blockbtn (que es el botón que inicia la ventana emergente Sidenotes), se construiría un objeto como:

```
var styles = { 
   'blockBtn': { 
      'fontColor': '#555', 
      'fontSize': '18px' 
   } 
}; 
new Livefyre.Sidenotes({ 
   customStyles: styles, 
      ...  
})
```

| **Clave** | **Propiedades** | Descripción |
|---|---|---|
| `anonymousAvatar` | &#39; height &#39;,&#39; width &#39; | Imagen de avatar anónima, a la izquierda del editor de área de texto. |
| `blockBtn` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | El «icono del Iniciador» situado junto a los elementos especificados como «sidenote». |
| `blockBtnActive` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | Icono Iniciador cuando se encuentra en estado activo. |
| `commentAvatar` | &#39; height &#39;,&#39; width &#39; | Imagen avatar a la izquierda de las notas de nivel superior. |
| `commentBody` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Cuerpo de texto de notas de subproceso. |
| `commentDisplayName` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Nombre para mostrar del usuario que ha dejado una nota. |
| `commentDownvote` | &#39; Fontcolor &#39;,&#39; fontsize &#39; | Botón de voto en una nota. |
| `commentReplyExpand` | &#39; Backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Botón para expandir los hilos con un gran número de respuestas. |
| `commentTags` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Etiquetas sobre un usuario en una nota. |
| `commentUpvote` | &#39; Fontcolor &#39;,&#39; fontsize &#39; | Botón Ortovotación en una nota. |
| `editorTextarea` | &#39; height &#39;,&#39; width &#39;,&#39; fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Cuadro de entrada de texto para dejar notas. |
| `mediaBlockBtn` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | Icono del iniciador multimedia cuando se encuentra encima de un elemento de medios (img, vídeo). |
| `mediaBlockBtnActive` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | Icono del iniciador de medios en estado activo. |
| `numSidenotes` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39;,&#39; backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; height &#39;,&#39; width &#39; | Botón en el que se puede hacer clic que muestra el número de Sidenotes en la colección. |
| `numSidenotesPopover` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39;,&#39; backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; height &#39;,&#39; width &#39; | Ventana emergente con una breve explicación de Sidenotes para el usuario. |
| `popover` | &#39; Backgroundcolor &#39; | Ventana emergente que se abre cuando se invoca el icono del iniciador. |
| `popoverArrowLeft` | &#39; Backgroundimage &#39;,&#39; height &#39;,&#39; left &#39;,&#39; right &#39;,&#39; top &#39;,&#39; width &#39; | Elemento de flecha izquierda en la ventana emergente que apunta al elemento DOM que contiene un icono de iniciador. |
| `popoverArrorRight` | &#39; Backgroundimage &#39;,&#39; height &#39;,&#39; left &#39;,&#39; right &#39;,&#39; top &#39;,&#39; width &#39; | Elemento de flecha derecha en la ventana emergente que apunta al elemento DOM que contiene un icono de iniciador. |
| `popoverArrowTop` | &#39; Backgroundimage &#39;,&#39; height &#39;,&#39; left &#39;,&#39; right &#39;,&#39; top &#39;,&#39; width &#39; | Elemento de flecha superior de la ventana emergente que apunta al elemento DOM que contiene un icono de iniciador. |
| `replyAvatar` | &#39; height &#39;,&#39; width &#39; | Imagen avatar a la izquierda de las notas del nivel de respuesta. |
| `streamPoweredBy` | &#39; Backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; lineheight &#39; | &quot; Equipado con &quot;pie de página en la ventana emergente. |
| `streamQueueButton` | &#39; Backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Botón que indica cuándo hay nuevo flujo de notas en una ventana emergente abierta. |
| `userAvatar` | &#39; height &#39;,&#39; width &#39; | Imagen del avatar del usuario autenticado, a la izquierda del editor de área de texto. |

