---
description: Muestre las colecciones más activas del sitio o de la red.
seo-description: Muestre las colecciones más activas del sitio o de la red.
seo-title: Tendencias
solution: Experience Manager
title: Tendencias
uuid: 3031523d-b487-4eea-bba6-5d8f9971874f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Tendencias{#trending}

Muestre las colecciones más activas del sitio o de la red.

Utilice las tendencias para mostrar las colecciones con la actividad más reciente del sitio o la red.

## de CRM {#section_wtz_whb_c1b}

La forma más rápida de integrarse con Trending es utilizar la versión compilada alojada en la CDN de Livefyre.

Primero, agregue [Livefyre.js](https://github.com/Livefyre/Livefyre.js) a su página.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

A continuación, coloque el elemento en el que aparecerá la aplicación.

```
<div id="trending"></div>
```

Finalmente, utilice `Livefyre.require` para construir el componente.

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

Ahora tiene una aplicación de tendencias. Vea todo esto en acción en [este ejemplo](https://codepen.io/gobengo/pen/GijEy).

## Configuración {#section_k5k_qhb_c1b}

`network`

Red de la que se extraerán las colecciones. (Requerido.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Proporcione la ID del sitio para mostrar las colecciones solamente desde un solo sitio dentro de la red. (Opcional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Proporcione una única etiqueta de colección para mostrar solo las colecciones con esa etiqueta. (Opcional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

