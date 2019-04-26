---
description: Cambie las opciones de tamaño, ancho e interacción de la aplicación Mapa.
seo-description: Cambie las opciones de tamaño, ancho e interacción de la aplicación
  Mapa.
seo-title: Personalizaciones de la tarjeta de funciones
solution: Experience Manager
title: Personalizaciones de la tarjeta de funciones
uuid: dd 43 c 076-027 f -42 c 8-be 2 e -7 d 863 d 4 e 3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8

---


# Personalizaciones de la tarjeta de funciones{#feature-card-customizations}

Cambie las opciones de tamaño, ancho e interacción de la aplicación Mapa.

<!-- 
r_feature_card_customization.dita
 -->

Las aplicaciones de tarjeta de funciones incluyen solo personalizaciones estándar: ** [!UICONTROL Theme]**, color de marca, familia Fuente y tamaño de fuente.

Puede personalizar tarjetas de funciones utilizando:

* **[!UICONTROL Style]** y **[!UICONTROL Config]** opciones para todas las aplicaciones del **[!UICONTROL App Designer]**. Consulte Personalización de aplicaciones para obtener más detalles sobre el estándar **[!UICONTROL Style]** y **[!UICONTROL Config]** las opciones de todas las aplicaciones en **[!UICONTROL App Designer]**la.

* Herramientas de integración. Consulte Integraciones de aplicación para obtener más información sobre cómo personalizar aplicaciones mediante herramientas de integración.
* **[!UICONTROL Call-to-action button]** Puede utilizar el botón Llamada a acción con un catálogo de productos para dirigir a los usuarios a un producto o a su sitio para que realicen más acciones.

   * **[!UICONTROL Call-to-action button]** Cambie la opción para mostrar el botón Llamada a acción.
   * **[!UICONTROL Require rights to display products]** Cambie la activación para que el propietario del contenido haya concedido derechos para el contenido antes de que aparezca un botón de llamada a acción para el contenido.

      >[!NOTE]
      >
      >El contenido se muestra incluso si no se conceden derechos para el contenido, pero el botón de llamada a acción no se mostrará con el contenido, a menos que se otorguen derechos para el contenido.

   * **[!UICONTROL Call-to-action header text]** Palabras que se mostrarán en el encabezado sobre el botón Llamada a acción en el modal. La redacción predeterminada es "Buy these products: ".
   * **[!UICONTROL Call-to-action button text]** Personalice el texto del botón Llamada a acción. El texto predeterminado es "Buy Now".
   * **[!UICONTROL Product display options]** Elija si desea mostrar el **[!UICONTROL Photo]** botón y el **[!UICONTROL Product name]** de llamada a acción.
   * **[!UICONTROL Product URL referral tracking]** Cambie el conmutador a para rastrear las referencias de esta aplicación a la página del producto asociada.
   * **[!UICONTROL Referral tracking key-value pairs]** Agregue parámetros para especificar el seguimiento de referencia desde el contenido de la aplicación a la página del producto asociada.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Seleccione esta opción para crear una aplicación para varias páginas de producto. Filtre el UGC específico del producto a la aplicación para cada página de producto. Puede seleccionar una o varias carpetas para asociar colecciones específicas a la aplicación.
   * **[!UICONTROL Select Product folders]**. Seleccione las carpetas de productos de nivel superior para filtrar UGC. Utilice `CTRL/Command + click` para seleccionar más de una carpeta. Livefyre utiliza la carpeta para determinar qué productos de esa carpeta se mostrarán en la aplicación en varias páginas.
   * **[!UICONTROL Show related content]**. Active esta opción para mostrar contenido publicado en la aplicación, pero etiquetado con un ID de producto distinto. Una vez que se muestra el contenido específico del producto para la aplicación, Livefyre muestra el contenido de otros productos y contenido no asociado a un producto. Livefyre prioriza primero el contenido con el mismo ID de producto, luego contenido publicado en la aplicación con otros ID de producto y, a continuación, contenido publicado en la aplicación sin ID de producto.

