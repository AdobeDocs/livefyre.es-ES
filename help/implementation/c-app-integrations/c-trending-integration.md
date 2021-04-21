---
description: Muestre las colecciones más activas de su sitio o red.
title: Tendencias
exl-id: a3129e95-90e7-4107-bfd9-ed3b0dce20aa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 5%

---

# Tendencias{#trending}

Muestre las colecciones más activas de su sitio o red.

Utilice Tendencias para mostrar las Colecciones con la actividad más reciente de su Sitio o Red.

## de CRM {#section_wtz_whb_c1b}

La forma más rápida de integrarse con Trending es utilizar la versión creada alojada en la CDN de Livefyre.

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

¡Ahora tiene una aplicación de tendencias! Vea todo esto en acción en [este ejemplo](https://codepen.io/gobengo/pen/GijEy).

## Configuración {#section_k5k_qhb_c1b}

`network`

La red de la que se extraerán las colecciones. (Requerido.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Proporcione el ID del sitio para mostrar las colecciones únicamente de un solo sitio dentro de la red. (Opcional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Proporcione una sola etiqueta de colección para mostrar solo las colecciones con esa etiqueta. (Opcional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```
