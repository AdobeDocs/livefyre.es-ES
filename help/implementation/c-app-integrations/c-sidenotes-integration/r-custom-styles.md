---
description: Los estilos personalizados se aplican a través de un objeto insertado
  en el constructor Sidenotes.
seo-description: Los estilos personalizados se aplican a través de un objeto insertado
  en el constructor Sidenotes.
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
| `anonymousAvatar` | ' height ',' width ' | Imagen de avatar anónima, a la izquierda del editor de área de texto. |
| `blockBtn` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | El «icono del Iniciador» situado junto a los elementos especificados como «sidenote». |
| `blockBtnActive` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | Icono Iniciador cuando se encuentra en estado activo. |
| `commentAvatar` | ' height ',' width ' | Imagen avatar a la izquierda de las notas de nivel superior. |
| `commentBody` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Cuerpo de texto de notas de subproceso. |
| `commentDisplayName` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Nombre para mostrar del usuario que ha dejado una nota. |
| `commentDownvote` | ' Fontcolor ',' fontsize ' | Botón de voto en una nota. |
| `commentReplyExpand` | ' Backgroundcolor ',' bordercolor ',' borderwidth ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Botón para expandir los hilos con un gran número de respuestas. |
| `commentTags` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Etiquetas sobre un usuario en una nota. |
| `commentUpvote` | ' Fontcolor ',' fontsize ' | Botón Ortovotación en una nota. |
| `editorTextarea` | ' height ',' width ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Cuadro de entrada de texto para dejar notas. |
| `mediaBlockBtn` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | Icono del iniciador multimedia cuando se encuentra encima de un elemento de medios (img, vídeo). |
| `mediaBlockBtnActive` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | Icono del iniciador de medios en estado activo. |
| `numSidenotes` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ',' backgroundcolor ',' bordercolor ',' borderwidth ',' height ',' width ' | Botón en el que se puede hacer clic que muestra el número de Sidenotes en la colección. |
| `numSidenotesPopover` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ',' backgroundcolor ',' bordercolor ',' borderwidth ',' height ',' width ' | Ventana emergente con una breve explicación de Sidenotes para el usuario. |
| `popover` | ' Backgroundcolor ' | Ventana emergente que se abre cuando se invoca el icono del iniciador. |
| `popoverArrowLeft` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | Elemento de flecha izquierda en la ventana emergente que apunta al elemento DOM que contiene un icono de iniciador. |
| `popoverArrorRight` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | Elemento de flecha derecha en la ventana emergente que apunta al elemento DOM que contiene un icono de iniciador. |
| `popoverArrowTop` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | Elemento de flecha superior de la ventana emergente que apunta al elemento DOM que contiene un icono de iniciador. |
| `replyAvatar` | ' height ',' width ' | Imagen avatar a la izquierda de las notas del nivel de respuesta. |
| `streamPoweredBy` | ' Backgroundcolor ',' bordercolor ',' lineheight ' | " Equipado con "pie de página en la ventana emergente. |
| `streamQueueButton` | ' Backgroundcolor ',' bordercolor ',' borderwidth ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Botón que indica cuándo hay nuevo flujo de notas en una ventana emergente abierta. |
| `userAvatar` | ' height ',' width ' | Imagen del avatar del usuario autenticado, a la izquierda del editor de área de texto. |

