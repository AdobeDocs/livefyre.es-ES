---
description: Trazar el contenido del usuario a un mapa interactivo.
seo-description: Trazar el contenido del usuario a un mapa interactivo.
seo-title: Mapa
solution: Experience Manager
title: Mapa
uuid: 1c3e399d-a610-4b80-a3b2-a5502b31480d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mapa{#map}

Trazar el contenido del usuario a un mapa interactivo.

El mapa le permite transmitir contenido geoetiquetado a un mapa mundial, lo que le permite localizar el rumor social en torno a noticias de última hora o un evento en directo. Se mostrará todo el contenido aplicable, incluyendo texto, comentarios, fotos y tweets.

>[!NOTE]
>
>Los mapas son proporcionados por [©OpenStreetMap](https://www.openstreetmap.org/copyright), que proporciona los datos que Livefyre utiliza para procesar sus mapas.

## de CRM {#section_w2m_db2_d1b}

La forma más rápida de utilizar Map es utilizar la versión compilada alojada en la CDN de Livefyre.

Primero, agregue [Livefyre.js](https://github.com/Livefyre/Livefyre.js) a su página.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

A continuación, coloque el elemento en el que aparecerá la aplicación de mapa.

```
<div id="map" style="height: 500px;"></div>
```

Por último, utilice Livefyre.required para construir el mapa y obtener una colección para canalizar a partir del eje central-sdk. Tenga en cuenta que Map solo puede mostrar contenido con metadatos geográficos. Twitter y la cuenta de Instagram admiten esta función. Para garantizar el mejor rendimiento, incluya un filtro de geolocalización en todas las reglas de depuración de la colección.

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

Consulte este ejemplo [](https://codepen.io/cheung31/pen/wkmbF)en directo.

## Configuración {#section_jc5_gxb_c1b}

`initial`

El número inicial de elementos que se van a cargar desde la colección y se mostrarán en el mapa. Después de cargar este número, los usuarios pueden hacer clic en un botón para mostrar más. (Opcional. El valor predeterminado es 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Opciones para pasar al mapa [del prospecto](https://leafletjs.com/) subyacente, que Mapa utiliza para el procesamiento. Utilice esta opción para definir las opciones [del mapa del](https://leafletjs.com/reference.html#map-options)prospecto, incluido el punto central inicial del mapa, y los niveles de zoom inicial y máximo. (Opcional.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

