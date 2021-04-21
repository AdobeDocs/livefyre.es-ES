---
description: Cree un muro de medios, con la transmisión de contenido en tiempo real.
title: Muro de los medios
exl-id: 597af7e1-9ada-4893-9071-e17c21ef0d04
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Muro de medios{#media-wall}

Cree un muro de medios, con la transmisión de contenido en tiempo real.

El muro de medios le permite crear un muro social en tiempo real para su sitio. Utilice el paquete de aerohub-wallpackage del SDK de JavaScript de Livefyre para mostrar las fuentes sociales de Livefyre como una experiencia de contenido en mosaico de pantalla completa y visualmente atractiva que es buena para cubrir eventos en vivo, alojar concursos de fotos y potentes secciones sociales de su sitio web.

## de CRM {#section_jfm_bwb_c1b}

La forma más rápida de añadir un muro de medios es utilizar la versión creada alojada en la CDN de Livefyre.

Primero, agregue [Livefyre.js](https://github.com/Livefyre/Livefyre.js) a su sitio.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

A continuación, coloque el elemento en el que aparecerá el muro de medios.

```
<div id="wall"></div>
```

Finalmente, utilice `Livefyre.require` para construir el componente.

```
<script> 
Livefyre.require([ 
    'streamhub-wall#5' 
], function(MediaWall) {     
    var wall = window.wall = new MediaWall({ 
        el: document.getElementById("wall"), 
        collection: { 
            "network": "client-solutions.fyre.co", 
            "siteId": "364309", 
            "articleId": "answers-mediawall" 
        } 
    }); 
}); 
</script>
```

¡Ahora tienes un muro! Vea todo esto en acción en [este ejemplo](https://codepen.io/gobengo/pen/dFwDL).

**¿Ha llegado a un error?** Compruebe que está pasando el parámetro de entorno correcto. Las opciones incluyen `livefyre.com` (producción) o `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Cualquier personalización de estilo de los tweets procesados por su aplicación de muro de medios debe realizarse de acuerdo con los [Requisitos de visualización](https://dev.twitter.com/terms/display-requirements) de Twitter.

## Opciones de configuración {#section_ucv_qvb_c1b}

`columns`

Permite definir el número de columnas para el muro de medios al crear el muro. Si se establece esta opción, el ancho de cada columna se adaptará automáticamente al tamaño del contenedor del muro de medios, al tiempo que se mantiene el número especificado de columnas.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

Número de elementos de contenido que se van a procesar al cargar la página. El valor predeterminado es 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Permite establecer el ancho mínimo (píxeles) para cada columna dentro del elemento contenedor del muro de medios. (El muro multimedia seleccionará automáticamente un número adecuado de columnas, según la anchura del elemento contenedor correspondiente. De forma predeterminada, el ancho del muro de medios dividido por el ancho mínimo del contenido (300 píxeles, si no está definido) determina el número de columnas.

>[!NOTE]
>
>No utilice esta opción en combinación con la opción de columnas.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

De forma predeterminada, cuando hay archivos adjuntos para un fragmento de contenido, Media Walls mostrará una miniatura en la que se puede hacer clic. Cuando se hace clic, la aplicación abre un modal que muestra el adjunto de fotografía/vídeo en su totalidad. Para desactivar esta opción, establezca modal en false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Define el botón [!UICONTROL Post Content] que aparecerá en su muro. Esta opción requiere que pase `opts.collection` y agregue una integración de autenticación de Livefyre.js a la página.

`postButton` parámetros:

* `false` (predeterminado): No mostrar un botón Contenido del anuncio . (Crea un muro de medios de sólo lectura).
* `true` (o  `LiveMediaWall.postButtons.contentWithPhotos`): Incluya un botón que permita a los usuarios agregar contenido de texto, con fotos adjuntas.

* `LiveMediaWall.postButtons.content`: Incluya un botón que permita a los usuarios agregar contenido de texto, pero no adjuntar fotos.
* `LiveMediaWall.postButtons.photo`: Incluya un botón que permita a los usuarios agregar una foto, pero sin texto.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Define el número de elementos de Contenido que se agregarán al muro cuando se haga clic en el botón [!UICONTROL Show More].

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Opciones de configuración de estilo {#section_ztv_dvb_c1b}

El muro de medios también ofrece varias opciones de configuración que permiten personalizar el color, el estilo y el tamaño del texto. Para implementar estas opciones, utilice la siguiente sintaxis:

```
var wall2 = window.wall2 = new MediaWall({ 
   el: document.getElementById("listView1"), 
   collection: collection, 
   cardBackgroundColor: '#333', 
   textColor: 'magenta', 
   linkColor: 'orange', 
   footerTextColor: 'lime', 
   displayNameColor: 'cyan', 
   usernameColor: 'red', 
   fontFamily: 'Helvetica, Arial', 
   linkAttachmentBackgroundColor: '#555', 
   linkAttachmentBorderColor: '#888' 
}); 
```

Para obtener información válida, consulte los estándares W3C para las propiedades CSS [Font Family](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Font Size](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [Line Height,](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) y [Color](https://www.w3.org/TR/css3-color/#colorunits).

* **bodyFontSize** *(CSS Font Size String)* El tamaño de fuente del texto del cuerpo del contenido.

* **bodyLineHeight** *(cadena de altura de línea CSS)* Altura de línea del texto del cuerpo del contenido.

* **buttonActiveBackgroundColor** *(CSS Color String)** El color del fondo del botón en la posición activa.

* **buttonBorderColor** *(CSS Color String)** El color de los bordes de los botones.

* **buttonHoverBackgroundColor** *(CSS Color String)* El color del fondo del botón al pasar el ratón por encima.

* **buttonTextColor** *(CSS Color String)* El color de las etiquetas de los botones.

* **cardBackgroundColor** *(CSS Color String)* El color de fondo de las tarjetas de contenido en el muro de medios.

* **displayNameColor** *(CSS Color String)* El color de los nombres para mostrar en el byline.

* **fontFamily** *(CSS Font Family String)* La familia de fuentes para el texto del cuerpo.

* **footerTextColor** *(CSS Color String)* El color del texto secundario (como el texto del pie de página y el nombre de usuario del subtítulo).

* **linkAttachmentBackgroundColor** *(CSS Color String)* El color de fondo de los archivos adjuntos de los vínculos (archivos adjuntos apilados).

* **linkAttachmentBorderColor** *(CSS Color String)* El color del borde de los archivos adjuntos de los vínculos (archivos adjuntos apilados).

* **linkAttachmentTextColor** *(CSS Color String)* El color del texto del adjunto del vínculo.

* **linkColor** *(CSS Color String)* El color de los hipervínculos (como vínculos en texto principal y vínculos de nombre para mostrar).

* **textColor** *(CSS Color String)* El color del texto del cuerpo.

* **titleFontSize** *(CSS Font Size String)* El tamaño de fuente de los títulos de contenido.

* **titleLineHeight** *(Cadena de altura de línea CSS)* Altura de línea para títulos de contenido.

* **sourceLogoColor** *(cadena de color CSS)* El color del logotipo de origen.

* **usernameColor** *(CSS Color String)* El color de los nombres de usuario en el byline.
