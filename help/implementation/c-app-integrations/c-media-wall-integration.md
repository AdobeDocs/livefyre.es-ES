---
description: Cree un muro de medios con flujo de contenido en tiempo real.
seo-description: Cree un muro de medios con flujo de contenido en tiempo real.
seo-title: Muro de medios
solution: Experience Manager
title: Muro de medios
uuid: c 6087 c 80-a 35 b -44 d 2-9 dd 4-ba 9 cd 471172 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Muro de medios{#media-wall}

Cree un muro de medios con flujo de contenido en tiempo real.

Muro de medios permite crear un muro social en tiempo real para su sitio. Utilice el kit de desarrollo de software de JavaScript de Livefyre para mostrar las fuentes sociales de Livefyre como una experiencia de contenido en mosaico visual, con una pantalla completa y atractiva para cubrir eventos en directo, alojar concursos de fotos y crear funciones sociales de su sitio web.

## de CRM{#section_jfm_bwb_c1b}

La manera más rápida de agregar un muro de medios es utilizar la versión compilada alojada en la CDN de Livefyre.

Primero, agregue [Livefyre. js](https://github.com/Livefyre/Livefyre.js) al sitio.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

A continuación, posicione el elemento en el que aparecerá el muro de medios.

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

Ahora tiene un Muro. Ver todo en acción en [este ejemplo](https://codepen.io/gobengo/pen/dFwDL).

**¿Se ha producido un error?** Compruebe que está pasando el parámetro de entorno correcto. Las opciones incluyen `livefyre.com` (producción) o `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Toda personalización de estilo de los tweets representados por la aplicación de muro de medios debe realizarse de conformidad con los requisitos [de visualización de Twitter](https://dev.twitter.com/terms/display-requirements).

## Opciones de configuración {#section_ucv_qvb_c1b}

`columns`

Permite definir el número de columnas para el muro de medios al construir el muro. Si se configura esta opción, el ancho de cada columna se adaptará automáticamente al tamaño del contenedor de la pared de medios y mantendrá el número especificado de columnas.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

Número de elementos de contenido que se procesarán al cargar la página. Defaults to 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Permite establecer el ancho mínimo (píxel) de cada columna dentro del elemento contenedor de Muro de medios. (El muro de medios seleccionará automáticamente un número adecuado de columnas, según la anchura de su elemento contenedor. De forma predeterminada, la anchura del muro de medios dividida por la anchura de contenido mínima (300 px, si no está definida) determina el número de columnas.)

>[!NOTE]
>
>No utilice esta opción junto con la opción de columnas.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

De forma predeterminada, cuando hay adjuntos para un fragmento de contenido, los muros de medios mostrarán una miniatura seleccionable. Si se selecciona esta opción, la aplicación abrirá un modal que mostrará el adjunto de fotos/vídeo en su totalidad. Para deshabilitar esta opción, establezca modal en false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Define [!UICONTROL Post Content] el botón que aparecerá en el muro. Esta opción requiere que pase `opts.collection`y añada una integración de Autenticación de Livefyre. js a la página.

`postButton` parámetros:

* `false` (predeterminado): No mostrar un botón Contenido de anuncio. (Crea un muro de medios de solo lectura).
* `true` (o `LiveMediaWall.postButtons.contentWithPhotos`): Incluya un botón que permita a los usuarios añadir contenido de texto con fotos adjuntadas.

* `LiveMediaWall.postButtons.content`: Incluya un botón que permita a los usuarios agregar contenido de texto, pero no adjuntar fotos.
* `LiveMediaWall.postButtons.photo`: Incluya un botón que permita a los usuarios agregar una foto, pero no texto.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Define el número de elementos de contenido que se agregarán al muro cuando se hace clic en [!UICONTROL Show More] el botón.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Opciones de configuración de estilo {#section_ztv_dvb_c1b}

Muro de medios también ofrece varias opciones de configuración que permiten personalizar el color, el estilo y el tamaño del texto. Para implementar estas opciones, utilice la siguiente sintaxis:

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

Para obtener información válida, consulte las normas W 3 C para la familia [de fuentes CSS](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [el tamaño de fuente](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [la altura de línea y](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) las propiedades [de color](https://www.w3.org/TR/css3-color/#colorunits) .

* **Bodyfontsize** *(String Font Size String)* El tamaño de fuente para texto del cuerpo de contenido.

* **Bodylineheight** *(String Height Line Height String)* The line height for content body text.

* **Buttonactivebackgroundcolor** *(CSS Color String)** El color del fondo del botón activo.

* **Buttonbordercolor** *(CSS Color String)** El color de los bordes del botón.

* **Buttonhoverbackgroundcolor** *(CSS Color String)* El color del fondo del botón al pasar el ratón por encima.

* **Buttontextcolor** *(CSS Color String)* El color de las etiquetas de botón.

* **Cardbackgroundcolor** *(CSS Color String)* El color de fondo de las tarjetas de contenido del muro de medios.

* **Displaynamecolor** *(CSS Color String) El color* para los nombres de visualización en la firma.

* **Fontfamily** *(CSS Font Family String)* La familia de fuentes para texto body.

* **Footertextcolor** *(CSS Color String)* El color de texto secundario (como el texto de pie de página y el nombre de usuario en la firma).

* **Linkattachmentbackgroundcolor** *(CSS Color String)* El color de fondo para archivos adjuntos (adjuntos apilados).

* **Linkattachmentbordercolor** *(CSS Color String)* El color del borde para archivos adjuntos (adjuntos apilados).

* **Linkattachmenttextcolor** *(CSS Color String)* El color para texto adjunto de vínculo.

* **Linkcolor** *(Cadena de color CSS)* El color para hipervínculos (como vínculos en texto body y vínculos con nombre para mostrar).

* **Textcolor** *(Cadena de color CSS)* El color del texto del cuerpo.

* **Titlefontsize** *(Cadena de tamaño de fuente CSS)* El tamaño de fuente para títulos de contenido.

* **Titlelineheight** *(Cadena de altura de línea CSS)* La altura de línea para títulos de contenido.

* **Sourcelogocolor** *(CSS Color String)* El color del logotipo de origen.

* **Usernamecolor** *(CSS Color String)* El color de los nombres de usuario de la firma.
