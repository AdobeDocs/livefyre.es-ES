---
description: Cambie el tamaño, el ancho y las opciones de interacción de la aplicación de mapa.
seo-description: Cambie el tamaño, el ancho y las opciones de interacción de la aplicación de mapa.
seo-title: Personalizaciones de tarjetas de características
solution: Experience Manager
title: Personalizaciones de tarjetas de características
uuid: dd43c076-027f-42c8-be2e-7d863d4e3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---


# Personalizaciones de tarjetas de características{#feature-card-customizations}

Cambie el tamaño, el ancho y las opciones de interacción de la aplicación de mapa.

<!-- 
r_feature_card_customization.dita
 -->

Las aplicaciones de tarjetas de características solo incluyen personalizaciones estándar:** [!UICONTROL Theme]**, color de la marca, familia de fuentes y tamaño de fuente.

Puede personalizar las tarjetas de funciones mediante:

* **[!UICONTROL Style]** y  **[!UICONTROL Config]** opciones para todas las aplicaciones de la  **[!UICONTROL App Designer]**. Consulte Personalización de aplicaciones para obtener más información sobre las opciones estándar **[!UICONTROL Style]** y **[!UICONTROL Config]** para todas las aplicaciones en **[!UICONTROL App Designer]**.

* Herramientas de integración. Consulte Integraciones de aplicaciones para obtener más información sobre cómo personalizar aplicaciones mediante las herramientas de integración.
* **[!UICONTROL Call-to-action button]** Puede utilizar el botón Llamada a acción con un catálogo de productos para dirigir a los usuarios a un producto o a su sitio para que realicen acciones adicionales.

   * **[!UICONTROL Call-to-action button]** Cambie el conmutador a activado para mostrar el botón Llamada a acción.
   * **[!UICONTROL Require rights to display products]** Cambie el conmutador a activado para requerir que el propietario del contenido haya concedido derechos para el contenido antes de que aparezca un botón de llamada a acción para el contenido.

      >[!NOTE]
      >
      >El contenido se muestra aunque no se hayan concedido derechos para el contenido, pero el botón Llamada a acción no se mostrará con el contenido a menos que se concedan derechos para el contenido.

   * **[!UICONTROL Call-to-action header text]** Palabras que se mostrarán en el encabezado encima del botón Llamada a acción en el modal de contenido. El texto predeterminado es &quot;Comprar estos productos:&quot;.
   * **[!UICONTROL Call-to-action button text]** Personalice el texto en el botón Llamada a acción. El texto predeterminado es &quot;Comprar ahora&quot;.
   * **[!UICONTROL Product display options]** Elija si desea mostrar  **[!UICONTROL Photo]** y  **[!UICONTROL Product name]** con el botón Llamada a acción.
   * **[!UICONTROL Product URL referral tracking]** Cambie el conmutador a activado para rastrear las referencias de esta aplicación a la página de producto asociada.
   * **[!UICONTROL Referral tracking key-value pairs]** Añada los parámetros para especificar aún más el seguimiento de referencia desde el contenido de la aplicación a la página del producto asociada.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Seleccione esta opción para crear una aplicación para varias páginas de productos. Filtre el UGC específico del producto en la aplicación para cada página del producto. Puede seleccionar una o varias carpetas para asociar colecciones específicas a la aplicación.
   * **[!UICONTROL Select Product folders]**. Seleccione las carpetas de productos de nivel superior que desee utilizar para filtrar UGC. Utilice `CTRL/Command + click` para seleccionar más de una carpeta. Livefyre utiliza la carpeta para determinar qué productos de esa carpeta se mostrarán en la aplicación en varias páginas.
   * **[!UICONTROL Show related content]**. Alterne esta opción para mostrar el contenido publicado en la aplicación, pero etiquetado con un ID de producto diferente. Una vez que se muestra el contenido específico del producto para la aplicación, Livefyre muestra el contenido para otros productos y el contenido no asociado a un producto. Livefyre prioriza primero el contenido con el mismo ID de producto, después el contenido publicado en la aplicación con otros ID de producto y, a continuación, el contenido publicado en la aplicación sin ID de producto.

