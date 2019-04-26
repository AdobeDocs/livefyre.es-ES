---
description: Filtrar UGC por ID de producto le permite incrustar la misma aplicación
  en varias páginas al mismo tiempo que se muestra un contenido UGC específico de
  producto específico para cada página.
seo-description: Filtrar UGC por ID de producto le permite incrustar la misma aplicación
  en varias páginas al mismo tiempo que se muestra un contenido UGC específico de
  producto específico para cada página.
seo-title: Filtrar UGC por ID de producto
title: Filtrar UGC por ID de producto
uuid: 98108 ddb -5710-4331-891 b -7 e 1 bbb 106059
translation-type: tm+mt
source-git-commit: 76efa427b59a709009a3c2d3744ea65e0c959816

---


# Filtrar UGC por ID de producto {#filter-ugc-product-id}

Filtrar UGC por ID de producto le permite incrustar la misma aplicación en varias páginas al mismo tiempo que se muestra un contenido UGC específico de producto específico para cada página.

Para filtrar UGC por ID de producto, siga estos pasos:

1. En Livefyre Studio, vaya a **[!UICONTROL Apps]** la ficha.

1. Seleccione la aplicación que desee modificar.

1. Seleccione la ficha Designer en el carril izquierdo.

1. Enable **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Seleccione las carpetas de productos de nivel superior que contengan el producto o productos a los que quiera filtrar UGC.
Utilice CTRL/Comando + clic para seleccionar varias carpetas.

1. Disable **[!UICONTROL Show related content]**.
Cuando está activado, el contenido filtrado con `data-lf-attr-product` el atributo se mostrará primero, seguido de todos los demás contenidos de la aplicación.

1. Haga clic **[!UICONTROL Publish]**en.

1. Inserte los ID de producto que desee filtrar en el código resultante.

>[!NOTE]
>
>Para localizar ID de productos, vaya **[!UICONTROL Settings > Products]**a. Busque el producto deseado y selecciónelo y se muestra el ID.

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

Para etiquetar un producto, reemplace `<product 1>` en el `data-lf-attr-product` atributo por el ID de producto deseado. Puede etiquetar un producto o más añadiendo ID de productos separados por comas adicionales. Los productos deben estar contenidos en la carpeta de producto de nivel superior o en las carpetas seleccionadas en el paso 5.

El segmento de código modificado aparecería como:

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