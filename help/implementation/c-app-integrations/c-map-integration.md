---
description: Trazar el contenido del usuario a un mapa interactivo.
title: Mapa
exl-id: 836b475e-0ec6-49f8-b89f-3af3209cf1f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# Mapa{#map}

Trazar el contenido del usuario a un mapa interactivo.

El mapa le permite transmitir contenido con geolocalización a un mapa mundial, lo que le permite localizar el zumbido social alrededor de las noticias de última hora o un evento en vivo. Se mostrará todo el contenido aplicable, incluyendo texto, comentarios, fotos y tweets.

>[!NOTE]
>
>Los mapas utilizan [ ©OpenStreetMap](https://www.openstreetmap.org/copyright), que proporciona los datos que Livefyre utiliza para procesar sus mapas.

## de CRM {#section_w2m_db2_d1b}

La forma más rápida de usar Map es usar la versión compilada alojada en la CDN de Livefyre.

Primero, agregue [Livefyre.js](https://github.com/Livefyre/Livefyre.js) a su página.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

A continuación, coloque el elemento en el que aparecerá la aplicación de mapa.

```
<div id="map" style="height: 500px;"></div>
```

Finalmente, use Livefyre.required para construir el mapa, y obtener una colección para canalizar desde streamhub-sdk. Tenga en cuenta que Mapa solo puede mostrar Contenido con metadatos geoetiquetados. Twitter y Instagram Deate admiten esta función. Para garantizar el mejor rendimiento, incluya un filtro de geolocalización en todas las reglas de depuración de la colección.

```
<script> 
Livefyre.require(['streamhub-map#1', 'streamhub-sdk#2'], 
function (Map, SDK) { 
    var map = new Map({ 
        el: document.getElementById('map') 
    }); 
    var collection = new SDK.Collection({ 
        network: 'strategy-prod.fyre.co', 
        siteId: 340628, 
        articleId: 'custom-1389845009515' 
    }); 
    collection.pipe(map); 
}); 
</script>
```

Consulte este [ejemplo activo](https://codepen.io/cheung31/pen/wkmbF).

## Configuración {#section_jc5_gxb_c1b}

`initial`

El número inicial de elementos que se van a cargar desde la colección y se muestran en el mapa. Una vez cargado este número, los usuarios pueden hacer clic en un botón para mostrar más. (Opcional. El valor predeterminado es 50).

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Opciones para pasar al mapa de [Prospecto](https://leafletjs.com/) subyacente que Mapa utiliza para el procesamiento. Utilice esta opción para establecer las [Opciones del mapa de prospecto](https://leafletjs.com/reference.html#map-options), incluido el punto central inicial del mapa, y los niveles de zoom inicial y máximo. (Opcional.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```
