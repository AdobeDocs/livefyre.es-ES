---
description: Entregue UGC específico de productos en puntos específicos del viaje
  del cliente para aumentar la intención de compra y la conversión mediante la función
  Comercio UGC.
seo-description: Entregue UGC específico de productos en puntos específicos del viaje
  del cliente para aumentar la intención de compra y la conversión mediante la función
  Comercio UGC.
seo-title: Comercio UGC
solution: Experience Manager
title: Comercio UGC
uuid: 71 e 64901-a 2 b 6-4957-ba 88-058 e 4 eaca 537
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Comercio UGC{#ugc-commerce}

Entregue UGC específico de productos en puntos específicos del viaje del cliente para aumentar la intención de compra y la conversión mediante la función Comercio UGC.

Utilice la característica Comercio UGC para influir en la intención de compra y la conversión en páginas de detalles de productos y UGC. Acelere el mercado mediante la asociación perfecta de UGC con inventario de productos. Cree fidelidad de marca mediante la creación de una comunidad mediante UGC para resaltar los artículos auténticos de los clientes.

AEM Livefyre ofrece varias formas de importar información del catálogo de productos, incluidos SKU, imágenes en miniatura, precio y nombre del producto. Administre fácilmente la asociación de productos con UGC mediante las solicitudes de derechos de AEM Livefyre, etiquetado de reglas de flujo automático y flujos de trabajo de moderación.

Además de influir en la compra, las capacidades de la empresa de comercio UGC de AEM Livefyre se pueden aprovechar para impulsar las conversiones de otras formas, entre las que se incluyen:

* Generación de posibles clientes B 2 B: colocar botones Llamada a acción debajo de UGC para capturar posibles clientes
* Descargas de la aplicación B 2 C: pedir a los usuarios que descarguen una aplicación
* Referencias de artículo: vincular usuarios a artículos relacionados con partes de UGC

Coloque llamadas a acción del producto junto con UGC para impulsar la conversión. Puede:

* Agregue UGC específico del producto a escala a miles de páginas de detalles de productos.
* Incruste las aplicaciones de visualización de AEM Livefyre que admitan funciones de comercio UGC como Muro de medios e Mosaico en páginas de detalles del producto.
* Utilice los códigos de seguimiento de referencia configurables con una solución de análisis para medir las conversiones de los CTAS del producto colocados en UGC y UGC colocados en páginas de detalles del producto.

Los usuarios de comercio de AEM pueden integrar sin problemas el catálogo de productos existente en Livefyre para fomentar la participación del usuario en las aplicaciones de visualización de Livefyre. Los usuarios de Livefyre que no utilicen el comercio de AEM pueden importar manualmente los catálogos de productos en Livefyre. Consulte [Cargar productos en Livefyre mediante Carga](/help/using/c-features-livefyre/c-ugc-commerce.md)de archivos, para obtener más información.

Aplicaciones que utilizan esta función:

* [Tarjeta de funciones](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app). Para obtener información sobre cómo utilizar el comercio UGC en una tarjeta de funciones, consulte [Personalizaciones de tarjetas de funciones](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y).

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). Para obtener información sobre cómo utilizar el comercio UGC en una tira de película, consulte [Personalizaciones tira de película](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations).

* [Muro de medios](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app). Para obtener información sobre cómo utilizar el Comercio UGC en un muro de medios, consulte [Personalizaciones de muro de medios](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations).

* [Mosaico](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app). Para obtener información sobre cómo utilizar el comercio UGC en un mosaico, consulte [Personalizaciones mosaicas](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations).

## Información general: Cómo utilizar el botón de llamada a acción de comercio UGC {#section_s2d_tln_n1b}

1. Cree una aplicación con un botón de llamada a acción. Consulte [Adición de un botón de llamada a acción a una aplicación](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155).
1. Agregue el catálogo de productos a Livefyre. Puede importar contenido de una de las dos maneras siguientes:

   * [Importe productos en Livefyre mediante Comercio AEM](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) si utiliza AEM Commerce.
   * [Cargue productos en Livefyre](/help/using/c-features-livefyre/c-ugc-commerce.md) si no utiliza Comercio AEM.

1. Asociar productos con contenido. Puede hacerlo de una de las cuatro maneras siguientes:

   * Desde la biblioteca. Consulte [Asociación de productos con contenido mediante la biblioteca](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * Desde modq. Consulte [Moderar contenido con modq](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * Desde contenido de la aplicación. Consulte [Adición de un botón de llamada a acción a una aplicación](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * Desde un flujo. Consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

## Cargar productos a Livefyre mediante Carga de archivos {#section_n1s_4hz_m1b}

Cargue productos para utilizarlos con su botón de llamada a acción para agregar productos que asociar con contenido o para editar y eliminar archivos existentes.

>[!NOTE]
>
>Al cargar un archivo en una carpeta con archivos existentes, se eliminarán todos los archivos de esa carpeta y se sobrescriben con el nuevo archivo.

1. Navegue hasta **[!UICONTROL Network Settings > Products.]**
1. Cree una **[!UICONTROL Product Folder]** o utilice una **[!UICONTROL Product Folder]**.

1. Haga clic en el **[!UICONTROL Product Folder]** para seleccionarlo.
1. Haga clic en **[!UICONTROL Upload Products]** el botón.
1. Cargue un archivo de producto en uno de los formatos siguientes:

   * Formato de archivo de Google Products
   * Formato de Livefyre (ver más abajo)
   Cargue un archivo JSON en el formato estándar. Puede descargar una plantilla para ver un ejemplo del formato estándar. A continuación se muestra un ejemplo de una línea de producto en una plantilla. Sigue la secuencia `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   La tabla explica los pares de clave y valor que necesita para cargar productos:

## Pares clave/valor para el formato estándar de carga del catálogo de productos

| Clave | Tipo | Descripción |
|--- |--- |--- |
| id | Cadena | ID única del producto. |
| oembed | Objeto | Adjunto de imagen `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | Cadena | Título del producto. |
| Isfolder | Booleano | Si es verdadera, el producto se trata como una carpeta (por ejemplo, hombre, mujer, etc.). |
| Parentid | Cadena | Define la carpeta en la que se encuentra el producto. |
| description | Cadena | Descripción del producto. |
| price | Cadena | Valor del producto en dólares. Por ejemplo,' 23.36 '. |
| sku | Cadena | Unidad de mantenimiento (SKU) del producto. |
| url | Cadena | Vínculo a la página del producto. |
| habilitado | Booleano | Un valor de True significa que el producto está activo. |
| atributos | Matriz | Tipos y valores que definen el producto (por ejemplo, color, tamaño, etc.). Es una matriz de objetos.</br>**Propiedades:**</br>type </br>Tipo: Stringdescription</br>: Color, tipo </br>de valor </br>de tamaño: </br>Descripción de cadena: Verde, XS |
| tags | Matriz | Etiquetas que definen categorías de contenido (por ejemplo, coches, zapatos, etc.). Esta es una matriz de cadenas. |

## Modq {#section_os1_v4t_n1b}

Puede asociar contenido con productos del catálogo de productos en modq en línea con sus flujos de trabajo de moderación existentes. Para obtener información sobre cómo utilizar el comercio UGC con modq, consulte [Moderar contenido mediante modq](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md).

## Flujos {#section_qtj_v4t_n1b}

Puede asociar automáticamente productos al contenido mediante reglas de flujo, luego publicar el contenido automáticamente en una aplicación, guardarlo en la Biblioteca o Moderarlo usando modq. Para obtener más información sobre cómo utilizar el Comercio UGC con reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
