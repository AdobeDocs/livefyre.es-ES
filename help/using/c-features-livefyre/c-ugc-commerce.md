---
description: Distribuya UGC de productos específicos en puntos específicos del viaje del cliente para aumentar la intención de compra y la conversión mediante la función de comercio UGC.
seo-description: Distribuya UGC de productos específicos en puntos específicos del viaje del cliente para aumentar la intención de compra y la conversión mediante la función de comercio UGC.
seo-title: Comercio UGC
solution: Experience Manager
title: Comercio UGC
uuid: 71e64901-a2b6-4957-ba88-058e4eaca537
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Comercio UGC{#ugc-commerce}

Distribuya UGC de productos específicos en puntos específicos del viaje del cliente para aumentar la intención de compra y la conversión mediante la función de comercio UGC.

Utilice la función de comercio UGC para influir en la intención de compra y la conversión en las páginas de detalles de productos y UGC. Agilizar el tiempo de salida al mercado asociando perfectamente UGC con el inventario de productos. Cree una comunidad que utilice UGC para resaltar las historias auténticas de los clientes.

AEM Livefyre ofrece varias formas de importar información del catálogo de productos, como SKU, imágenes en miniatura, precio y nombre del producto. Administre fácilmente la asociación de productos con UGC mediante las solicitudes de derechos de AEM Livefyre, el etiquetado de reglas de flujo automático y los flujos de trabajo de moderación.

Además de influir en las compras, las capacidades de la oferta de comercio UGC de AEM Livefyre se pueden aprovechar para impulsar las conversiones de otras maneras, entre ellas:

* Generación de plomo B2B: colocar los botones de llamada a acción en UGC para capturar los leads
* Descargas de aplicaciones B2C: solicitar a los usuarios que descarguen una aplicación
* Referencias de artículos: vincular usuarios a artículos relacionados con fragmentos de UGC

Coloque las llamadas a acción del producto junto con UGC para impulsar la conversión. Puede:

* Agregue UGC específico del producto a escala a miles de páginas de detalles del producto.
* Incruste las aplicaciones de visualización de AEM Livefyre que admiten funciones de comercio UGC como Media Wall y Mosaic en las páginas de detalles del producto.
* Utilice códigos de seguimiento de referencia configurables con una solución de análisis para medir las conversiones de los CTA de productos colocados en UGC y UGC colocados en páginas de detalles del producto.

Los usuarios de AEM Commerce pueden integrar sin problemas su catálogo de productos existente en Livefyre para impulsar la participación del usuario en las aplicaciones de visualización de Livefyre. Los usuarios de Livefyre que no utilicen AEM Commerce pueden importar manualmente sus catálogos de productos en Livefyre. Consulte [Cargar productos en Livefyre mediante la carga](/help/using/c-features-livefyre/c-ugc-commerce.md)de archivos para obtener más información.

Aplicaciones que utilizan esta función:

* [Tarjeta](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)de función. Para obtener información sobre cómo utilizar el comercio de UGC en una tarjeta de características, consulte Personalizaciones de tarjetas de [características](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y).

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). Para obtener información sobre cómo utilizar el comercio UGC en una tira de película, consulte Personalizaciones de [tira de película](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations).

* [Muro](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)de los medios. Para obtener información sobre cómo utilizar el comercio UGC en un muro de medios, consulte Personalizaciones [del muro de](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations)medios.

* [Mosaico](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app). Para obtener información sobre cómo utilizar el comercio de contenido generado por usuarios en un mosaico, consulte Personalizaciones [de mosaico](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations).

## Información general: Cómo usar el botón de llamada a acción de comercio de UGC {#section_s2d_tln_n1b}

1. Cree una aplicación con un botón de llamada a acción. Consulte [Agregar un botón de llamada a acción a una aplicación](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155).
1. Agregue el catálogo de productos a Livefyre. Puede importar contenido de una de las dos maneras siguientes:

   * [Importar productos en Livefyre mediante AEM Commerce](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) si utiliza AEM Commerce.
   * [Cargue productos en Livefyre](/help/using/c-features-livefyre/c-ugc-commerce.md) si no utiliza AEM Commerce.

1. Asociar productos con contenido. Puede hacerlo de una de las cuatro maneras siguientes:

   * Desde la biblioteca. Consulte [Asociación de productos con contenido mediante la biblioteca](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * De ModQ. Consulte [Moderar contenido con ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * Desde Contenido de la aplicación. Consulte [Agregar un botón de llamada a acción a una aplicación](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * Desde un flujo. Consulte Opciones [de regla de flujo para todas las reglas](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de flujo.

## Cargar productos a Livefyre mediante la carga de archivos {#section_n1s_4hz_m1b}

Cargue productos para usarlos con el botón Llamada a acción para agregar productos que asociar con contenido o para editar y eliminar archivos existentes.

>[!NOTE]
>
>Al cargar un archivo en una carpeta con archivos existentes, se eliminarán todos los archivos de esa carpeta y se sobrescribirán con el nuevo archivo.

1. Navegue hasta **[!UICONTROL Network Settings > Products.]**
1. Cree un **[!UICONTROL Product Folder]** o utilice un **[!UICONTROL Product Folder]**.

1. Haga clic en el **[!UICONTROL Product Folder]** para seleccionarlo.
1. Click the **[!UICONTROL Upload Products]** button.
1. Cargue un archivo de producto en uno de los siguientes formatos:

   * Formato de archivo de productos de Google
   * Formato Livefyre (ver abajo)
   Cargue un archivo JSON en el formato estándar. Puede descargar una plantilla para ver un ejemplo del formato estándar. A continuación se muestra un ejemplo de una línea de producto en una plantilla. Sigue la secuencia `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   La tabla explica los pares de clave y valor que necesita para cargar productos:

## Par de clave/valor para la carga del catálogo de productos Formato estándar

| Clave | Tipo | Descripción |
|--- |--- |--- |
| id | Cadena | ID única del producto. |
| oembed | Objeto | Image attachment `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | Cadena | Título del producto. |
| isFolder | Booleano | Si es true, el producto se trata como una carpeta (por ejemplo, hombres, mujeres, etc.). |
| parentId | Cadena | Define en qué carpeta se encuentra el producto. |
| description | Cadena | Descripción del producto. |
| precio | Cadena | Valor del producto en dólares. Por ejemplo, '23.36.' |
| sku | Cadena | Unidad de mantenimiento de existencias (SKU) del producto. |
| url | Cadena | Vínculo a la página del producto. |
| enabled | Booleano | Un valor True significa que el producto está activo. |
| atributos | Matriz | Tipos y valores que definen el producto (por ejemplo, color, tamaño, etc.). Es una matriz de objetos.</br>**** Propiedades: </br>tipo </br>Tipo:</br>StringDescription: Color, </br>valor de tamaño </br>Tipo: Descripción </br>de cadena: Verde, XS |
| etiquetas | Matriz | Etiquetas que definen categorías de contenido (por ejemplo, coches, zapatos, etc.). Es una matriz de cadenas. |

## ModQ {#section_os1_v4t_n1b}

Puede asociar contenido con productos del catálogo de productos en ModQ en línea con los flujos de trabajo de moderación existentes. Para obtener información sobre cómo utilizar el comercio de contenido generado por usuarios con ModQ, consulte [Moderar contenido con ModQ](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md).

## Flujos {#section_qtj_v4t_n1b}

Puede asociar automáticamente productos al contenido mediante reglas de flujo y, a continuación, publicar el contenido automáticamente en una aplicación, guardarlo en la biblioteca o moderarlo con ModQ. Para obtener más información sobre cómo utilizar el comercio de UGC con reglas de flujo, consulte Opciones de regla [de flujo para todas las reglas](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de flujo.
