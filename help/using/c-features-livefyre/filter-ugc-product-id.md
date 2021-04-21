---
description: El filtrado de UGC por ID de producto le permite incrustar exactamente la misma aplicación en varias páginas, al mismo tiempo que muestra UGC específicas de cada producto para cada página.
title: Filtrar UGC por ID de producto
exl-id: c98ee899-fcac-45dd-a26a-f678814776fd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Filtrar UGC por ID de producto {#filter-ugc-product-id}

El filtrado de UGC por ID de producto le permite incrustar exactamente la misma aplicación en varias páginas, al mismo tiempo que muestra UGC específicas de cada producto para cada página.

Para filtrar UGC por ID de producto, siga estos pasos:

1. En Livefyre Studio, vaya a la pestaña **[!UICONTROL Apps]**.

1. Seleccione la aplicación que desee modificar.

1. Seleccione la ficha Designer en el carril izquierdo.

1. Activar **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Seleccione las carpetas de producto de nivel superior que contienen el producto o los productos por los que desea filtrar UGC.
Use CTRL/Comando + clic para seleccionar varias carpetas.

1. Deshabilite **[!UICONTROL Show related content]**.
Cuando está habilitado, el contenido que se filtra con el atributo `data-lf-attr-product` se muestra primero, seguido del resto del contenido de la aplicación.

1. Haga clic **[!UICONTROL Publish]**.

1. Inserte los ID de producto que desee filtrar en el código resultante.

>[!NOTE]
>
>Para localizar los ID de producto, vaya a **[!UICONTROL Settings > Products]**. Busque el producto deseado, selecciónelo y se mostrará el ID.

Por ejemplo, se genera el siguiente código para una aplicación de muro de medios:

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published" datalf-
env="prod" data-lf-read-only="" data-lf-attr-product="<product
 1>,<product 2>"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

Para etiquetar un producto, reemplace `<product 1>` en el atributo `data-lf-attr-product` por el ID de producto deseado. Puede etiquetar un producto o más agregando ID de producto separados por coma adicionales. Los productos deben estar contenidos en la carpeta de productos de nivel superior o en las carpetas seleccionadas en el paso 5.

El segmento de código modificado aparecerá como:

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published"
 data-lf-env="prod" data-lf-read-only="" data-lf-attrproduct="
109,47"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

La aplicación ahora solo mostrará los ID de producto etiquetados.
