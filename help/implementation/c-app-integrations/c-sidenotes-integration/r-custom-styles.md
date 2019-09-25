---
description: Los estilos personalizados se aplican a través de un objeto insertado en el constructor Sidenotes.
seo-description: Los estilos personalizados se aplican a través de un objeto insertado en el constructor Sidenotes.
seo-title: Identifica estilos personalizados
title: Identifica estilos personalizados
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Identifica estilos personalizados{#sidenotes-custom-styles}

Los estilos personalizados se aplican a través de un objeto insertado en el constructor Sidenotes.

Las "claves" son claves de objeto que representan elementos DOM, mientras que las "propiedades" son propiedades CSS admitidas para la clave en particular. Por ejemplo, para personalizar el estilo de blockBtn (que es el botón que inicia la ventana emergente Sidenotes), se debe crear un objeto como:

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
| `anonymousAvatar` | "height", "width" | Imagen de avatar anónima, a la izquierda del editor de área de texto. |
| `blockBtn` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | El "icono del iniciador" situado junto a los elementos especificados como tabla de sidenote. |
| `blockBtnActive` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Icono del iniciador cuando esté en estado activo. |
| `commentAvatar` | "height", "width" | Imagen de avatar a la izquierda de las notas de nivel superior. |
| `commentBody` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Cuerpo de texto de las notas enlazadas. |
| `commentDisplayName` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Nombre para mostrar del usuario que ha dejado una nota. |
| `commentDownvote` | ‘fontColor’, ‘fontSize’ | Botón de voto en una nota. |
| `commentReplyExpand` | "backgroundColor", "borderColor", "borderWidth", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Botón para expandir subprocesos con un gran número de respuestas. |
| `commentTags` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Etiquetas sobre un usuario en una nota. |
| `commentUpvote` | ‘fontColor’, ‘fontSize’ | Botón de voto superior en una nota. |
| `editorTextarea` | ‘height’, ‘width’, ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Cuadro de entrada Textarea para dejar notas. |
| `mediaBlockBtn` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Icono de iniciador de medios cuando se encuentra sobre un elemento de medios (img, video). |
| `mediaBlockBtnActive` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Icono del iniciador de medios en estado activo. |
| `numSidenotes` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’, ‘backgroundColor’, ‘borderColor’, ‘borderWidth’, ‘height’, ‘width’ | Botón seleccionable que muestra el número de Sidenotes en la colección. |
| `numSidenotesPopover` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’, ‘backgroundColor’, ‘borderColor’, ‘borderWidth’, ‘height’, ‘width’ | Pase con una breve explicación de Sidenotes para el usuario. |
| `popover` | "backgroundColor" | Ventana emergente que se muestra cuando se invoca el icono del iniciador. |
| `popoverArrowLeft` | "backgroundImage", "height", "left", "right", "top", "width" | Elemento de flecha izquierda en la ventana emergente que apunta al elemento DOM que contiene un icono de iniciador. |
| `popoverArrorRight` | "backgroundImage", "height", "left", "right", "top", "width" | Elemento de flecha derecha en la ventana emergente que apunta al elemento DOM que contiene un icono de iniciador. |
| `popoverArrowTop` | "backgroundImage", "height", "left", "right", "top", "width" | Elemento de flecha superior en la ventana emergente que apunta al elemento DOM que contiene un icono de iniciador. |
| `replyAvatar` | "height", "width" | Imagen de avatar a la izquierda de las notas del nivel de respuesta. |
| `streamPoweredBy` | "backgroundColor", "borderColor", "lineHeight" | Pie de página "Powered by" en la ventana emergente. |
| `streamQueueButton` | "backgroundColor", "borderColor", "borderWidth", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Botón para indicar cuándo las nuevas notas se transmiten a una ventana emergente abierta. |
| `userAvatar` | "height", "width" | Imagen de avatar del usuario autenticado, a la izquierda del editor de área de texto. |

