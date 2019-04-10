---
description: Exhiba las colecciones más activas del sitio o de la red.
seo-description: Exhiba las colecciones más activas del sitio o de la red.
seo-title: Tendencias
solution: Experience Manager
title: Tendencias
uuid: 3031523 d-b 487-4 eea-bba 6-5 d 8 f 9971874 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Tendencias{#trending}

Exhiba las colecciones más activas del sitio o de la red.

Utilice Tendencias para exhibir las colecciones con la actividad más reciente del sitio o de la red.

## de CRM{#section_wtz_whb_c1b}

La manera más rápida de integrar Tendencias es utilizar la versión compilada alojada en CDN de Livefyre.

En primer lugar, agregue [Livefyre. js](https://github.com/Livefyre/Livefyre.js) a su página.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

A continuación, posicione el elemento en el que aparecerá la aplicación.

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

Ahora tiene una aplicación de tendencias. Ver todo en acción en [este ejemplo](https://codepen.io/gobengo/pen/GijEy).

## Configuración {#section_k5k_qhb_c1b}

`network`

La red desde la que se extraerán las colecciones. (Obligatorio.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Proporcione el ID del sitio para mostrar las colecciones solo desde un sitio único dentro de la red. (Opcional).

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Proporcione una sola etiqueta Colección para mostrar solo Colecciones con esa etiqueta. (Opcional).

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

