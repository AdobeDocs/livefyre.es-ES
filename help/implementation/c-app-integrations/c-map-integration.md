---
description: Coloque el contenido de usuario en un mapa interactivo.
seo-description: Coloque el contenido de usuario en un mapa interactivo.
seo-title: Mapa
solution: Experience Manager
title: Mapa
uuid: 1 c 3 e 399 d-a 610-4 b 80-a 3 b 2-a 5502 b 31480 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mapa{#map}

Coloque el contenido de usuario en un mapa interactivo.

Mapa le permite transmitir contenido geoetiquetado a un mapa mundial, lo que le permite encontrar el buzón social alrededor de las noticias break o un evento en directo. Se mostrará todo el contenido aplicable, incluyendo texto, comentarios, fotos y tweets.

>[!NOTE]
>
>Los mapas son proporcionados por [© openstreetmap](https://www.openstreetmap.org/copyright), que proporciona los datos que utiliza Livefyre para procesar sus mapas.

## de CRM{#section_w2m_db2_d1b}

La manera más rápida de utilizar Mapa es utilizar la versión compilada alojada en CDN de Livefyre.

En primer lugar, agregue [Livefyre. js](https://github.com/Livefyre/Livefyre.js) a su página.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

A continuación, posicione el elemento en el que aparecerá la aplicación de mapa.

```
<div id="map" style="height: 500px;"></div>
```

Finalmente, utilice Livefyre. require para construir el mapa y obtener una colección para colocarla en streamhub-sdk. Tenga en cuenta que Mapa solo puede mostrar contenido con metadatos geoetiquetados. Twitter e Instagram Depure admiten esta función. Para garantizar un mejor rendimiento, incluya un filtro de geolocalización en todas las reglas de depuración de la colección.

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

Consulte este [ejemplo en directo](https://codepen.io/cheung31/pen/wkmbF).

## Configuración {#section_jc5_gxb_c1b}

`initial`

Número inicial de elementos que se cargarán desde la colección y se muestran en el mapa. Después de cargar este número, los usuarios pueden hacer clic en un botón para mostrar más. (Opcional. Defaults to 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Opciones para pasar al mapa [folleto](https://leafletjs.com/) subyacente, que Mapa utiliza para procesar. Utilice esta opción para definir [Opciones](https://leafletjs.com/reference.html#map-options)de mapa de folleto, incluido el punto central inicial del mapa y los niveles de zoom inicial y máximo. (Opcional).

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

