---
description: Los estilos personalizados se aplican a través de un objeto insertado en el constructor Sidenotes .
title: Estilos personalizados de segmentos
exl-id: 846605b7-a21e-4600-bf17-18841d2ed96d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Muestra los estilos personalizados{#sidenotes-custom-styles}

Los estilos personalizados se aplican a través de un objeto insertado en el constructor Sidenotes .

Las &quot;claves&quot; son claves de objeto que representan elementos DOM, mientras que las &quot;propiedades&quot; son propiedades CSS compatibles con la clave en particular. Por ejemplo, para personalizar el estilo de blockBtn (que es el botón que inicia la ventana emergente Notas), se debe construir un objeto como:

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
| `anonymousAvatar` | &quot;altura&quot;, &quot;anchura&quot; | Imagen de avatar anónima, a la izquierda del editor de área de texto. |
| `blockBtn` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | El &quot;icono del lanzador&quot; situado junto a los elementos especificados como tabla de sidenote. |
| `blockBtnActive` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Icono del iniciador cuando esté en estado activo. |
| `commentAvatar` | &quot;altura&quot;, &quot;anchura&quot; | Imagen de avatar a la izquierda de las notas de nivel superior. |
| `commentBody` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Cuerpo de texto de las notas con subprocesos. |
| `commentDisplayName` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Mostrar el nombre del usuario que ha dejado una nota. |
| `commentDownvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Botón para rechazar una nota. |
| `commentReplyExpand` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Botón para expandir subprocesos con un gran número de respuestas. |
| `commentTags` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Etiquetas sobre un usuario en una nota. |
| `commentUpvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Botón de voto superior de una nota. |
| `editorTextarea` | &quot;height&quot;, &quot;width&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Cuadro de entrada del área de texto para dejar notas. |
| `mediaBlockBtn` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Icono de lanzador de contenido multimedia al principio de un elemento multimedia (img, vídeo). |
| `mediaBlockBtnActive` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Icono del lanzador de medios en estado activo. |
| `numSidenotes` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Botón en el que se puede hacer clic que muestra el número de notas en la colección. |
| `numSidenotesPopover` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Pase con una breve explicación de Sidenotes para el usuario. |
| `popover` | &quot;backgroundColor&quot; | La ventana emergente que aparece cuando se invoca el icono del lanzador. |
| `popoverArrowLeft` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento de flecha izquierda en la ventana emergente que señala al elemento DOM que contiene un icono de lanzador. |
| `popoverArrorRight` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento de flecha derecha en la ventana emergente que señala al elemento DOM que contiene un icono de lanzador. |
| `popoverArrowTop` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento de flecha superior en la ventana emergente que señala al elemento DOM que contiene un icono de lanzador. |
| `replyAvatar` | &quot;altura&quot;, &quot;anchura&quot; | Imagen de avatar a la izquierda de las notas de nivel de respuesta. |
| `streamPoweredBy` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;lineHeight&quot; | Pie de página &quot;Powered by&quot; en la ventana emergente. |
| `streamQueueButton` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Botón para indicar cuándo las notas nuevas se transmiten a una ventana emergente. |
| `userAvatar` | &quot;altura&quot;, &quot;anchura&quot; | Imagen de avatar del usuario autenticado, a la izquierda del editor de área de texto. |
