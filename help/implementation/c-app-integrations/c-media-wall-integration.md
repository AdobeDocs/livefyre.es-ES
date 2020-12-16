---
description: Cree un muro de medios con flujo continuo de contenido en tiempo real.
seo-description: Cree un muro de medios con flujo continuo de contenido en tiempo real.
seo-title: Muro de los medios
solution: Experience Manager
title: Muro de los medios
uuid: c6087c80-a35b-44d2-9dd4-ba9cd471172d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---


# Muro de medios{#media-wall}

Cree un muro de medios con flujo continuo de contenido en tiempo real.

Media Wall le permite crear un muro social en tiempo real para su sitio. Utilice el paquete de optimizaciones del SDK de JavaScript de Livefyre para mostrar las fuentes sociales de Livefyre como una experiencia de contenido en mosaico de pantalla completa y visualmente atractiva que es buena por cubrir eventos en directo, alojar concursos de fotografías y activar secciones sociales del sitio web.

## de CRM {#section_jfm_bwb_c1b}

La forma más rápida de agregar un muro multimedia es utilizar la versión compilada alojada en la CDN de Livefyre.

Primero, agregue [Livefyre.js](https://github.com/Livefyre/Livefyre.js) a su sitio.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

A continuación, coloque el elemento en el que aparecerá el Muro de medios.

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

¡Ahora tienes un muro! Consulte todo esto en acción en [este ejemplo](https://codepen.io/gobengo/pen/dFwDL).

**¿Se produjo un error?** Compruebe que está pasando el parámetro de entorno correcto. Las opciones incluyen `livefyre.com` (producción) o `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Cualquier personalización de estilo de los tweets representados por su aplicación de Media Wall debe realizarse de acuerdo con los [requisitos de visualización](https://dev.twitter.com/terms/display-requirements) de Twitter.

## Opciones de configuración {#section_ucv_qvb_c1b}

`columns`

Permite definir el número de columnas para el muro de medios al construir el muro. Si se establece esta opción, la anchura de cada columna se adaptará automáticamente al tamaño de contenedor del Muro de medios, manteniendo al mismo tiempo el número especificado de columnas.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

El número de elementos de contenido que se van a procesar al cargar la página. El valor predeterminado es 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Permite definir el ancho mínimo (píxeles) de cada columna dentro del elemento de contenedor de Media Wall. (El muro multimedia seleccionará automáticamente un número adecuado de columnas, según el ancho del elemento de contenedor. De forma predeterminada, la anchura del muro de medios dividida por la anchura mínima del contenido (300 píxeles, si no está definida) determina el número de columnas.

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

De forma predeterminada, cuando hay datos adjuntos para un fragmento de contenido, Media Walls mostrará una miniatura en la que se puede hacer clic. Cuando se hace clic en ella, la aplicación abre un modal que muestra los datos adjuntos de la fotografía y el vídeo en su totalidad. Para desactivar esta opción, establezca modal en false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Define el botón [!UICONTROL Post Content] para que aparezca en la pared. Esta opción requiere que pase `opts.collection` y agregue una integración de autenticación de Livefyre.js a la página.

`postButton` parámetros:

* `false` (predeterminado): No mostrar un botón de contenido de anuncio. (Crea un muro de medios de solo lectura).
* `true` (o  `LiveMediaWall.postButtons.contentWithPhotos`): Incluya un botón que permita a los usuarios añadir contenido de texto con fotos adjuntas.

* `LiveMediaWall.postButtons.content`:: Incluya un botón que permita a los usuarios añadir contenido de texto, pero no adjuntar fotos.
* `LiveMediaWall.postButtons.photo`:: Incluya un botón que permita a los usuarios añadir una fotografía, pero sin texto.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Define el número de elementos de contenido que se agregarán al muro cuando se haga clic en el botón [!UICONTROL Show More].

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Opciones de configuración de estilo {#section_ztv_dvb_c1b}

Media Wall también oferta varias opciones de configuración que le permiten personalizar el color, el estilo y el tamaño del texto. Para implementar estas opciones, utilice la sintaxis siguiente:

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

* **bodyFontSize** *(Cadena de tamaño de fuente CSS)* El tamaño de fuente del texto del cuerpo del contenido.

* **bodyLineHeight** *(Cadena de altura de línea de CSS)* Altura de línea del texto del cuerpo del contenido.

* **buttonActiveBackgroundColor** *(CSS Color String)** El color del fondo del botón cuando está activo.

* **buttonBorderColor** *(CSS Color String)** El color de los bordes de los botones.

* **buttonHoverBackgroundColor** *(CSS Color String)* El color del fondo del botón al pasar el ratón por encima.

* **buttonTextColor** *(Cadena de color CSS)* El color de las etiquetas de botón.

* **cardBackgroundColor** *(Cadena de color CSS)* El color de fondo de las tarjetas de contenido en el muro de medios.

* **displayNameColor** *(CSS Color String)* El color de los nombres de pantalla en el byline.

* **fontFamily** *(Cadena de familia de fuentes CSS)* La familia de fuentes del texto principal.

* **pieDePáginaColor** *(Cadena de color CSS)* El color del texto secundario (como el texto del pie de página y el nombre de usuario en el byline).

* **linkAttachmentBackgroundColor** *(CSS Color String)* El color de fondo de los archivos adjuntos de vínculo (archivos adjuntos apilados).

* **linkAttachmentBorderColor** *(Cadena de color CSS)* El color del borde de los datos adjuntos del vínculo (datos adjuntos apilados).

* **linkAttachmentTextColor** *(CSS Color String)* El color del texto adjunto del vínculo.

* **linkColor** *(Cadena de color CSS)* El color de los hipervínculos (como vínculos en texto principal y vínculos de nombre para mostrar).

* **textColor** *(CSS Color String)* El color del texto principal.

* **titleFontSize** *(Cadena de tamaño de fuente CSS)* El tamaño de fuente de los títulos de contenido.

* **titleLineHeight** *(Cadena de altura de línea de CSS)* Altura de línea para títulos de contenido.

* **sourceLogoColor** *(Cadena de color CSS)* El color del logotipo de origen.

* **usernameColor** *(Cadena de color CSS)* El color de los nombres de usuario del byline.
