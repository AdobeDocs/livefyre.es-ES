---
description: El filtrado de UGC por ID de producto le permite incrustar exactamente la misma aplicación en varias páginas y, al mismo tiempo, mostrar distintos UGC específicos del producto para cada página.
seo-description: El filtrado de UGC por ID de producto le permite incrustar exactamente la misma aplicación en varias páginas y, al mismo tiempo, mostrar distintos UGC específicos del producto para cada página.
seo-title: Filtrar UGC por ID de producto
title: Filtrar UGC por ID de producto
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 76efa427b59a709009a3c2d3744ea65e0c959816

---


# Filtrar UGC por ID de producto {#filter-ugc-product-id}

El filtrado de UGC por ID de producto le permite incrustar exactamente la misma aplicación en varias páginas y, al mismo tiempo, mostrar distintos UGC específicos del producto para cada página.

Para filtrar UGC por ID de producto, siga estos pasos:

1. En Livefyre Studio, vaya a la **[!UICONTROL Apps]** ficha.

1. Seleccione la aplicación que desee modificar.

1. Seleccione la ficha Designer en el carril izquierdo.

1. Enable **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Seleccione las carpetas de productos de nivel superior que contienen el producto o los productos por los que desea filtrar UGC.
Utilice CTRL/Comando + clic para seleccionar varias carpetas.

1. Disable **[!UICONTROL Show related content]**.
Cuando está activado, el contenido filtrado mediante el `data-lf-attr-product` atributo se mostrará primero, seguido del resto del contenido de la aplicación.

1. Haga clic en **[!UICONTROL Publish]**.

1. Inserte los ID de producto que desee filtrar en el código resultante.

>[!NOTE]
>
>Para localizar los ID de producto, vaya a **[!UICONTROL Settings > Products]**. Busque el producto deseado, selecciónelo y se muestra el ID.

Por ejemplo, se genera el siguiente código para una aplicación de Media Wall:

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

Para etiquetar un producto, reemplace `<product 1>` en el `data-lf-attr-product` atributo por el ID de producto deseado. Puede etiquetar un producto o más agregando ID de producto separados por comas adicionales. Los productos deben estar contenidos en la carpeta o carpetas de productos de nivel superior seleccionadas en el paso 5.

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

La aplicación solo mostrará los ID de producto etiquetados.