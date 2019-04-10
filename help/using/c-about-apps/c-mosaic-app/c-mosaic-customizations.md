---
description: Cambie las opciones de tamaño, ancho e interacción de la aplicación Mosaic.
seo-description: Cambie las opciones de tamaño, ancho e interacción de la aplicación
  Mosaic.
seo-title: Personalizaciones de mosaico
solution: Experience Manager
title: Personalizaciones de mosaico
uuid: 4 e 226 d 68-f 517-4922-bc 25-655 d 524 d 7 d 52
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Personalizaciones de mosaico{#mosaic-customizations}

Cambie las opciones de tamaño, ancho e interacción de la aplicación Mosaic.

Todas las **[!UICONTROL Style]** aplicaciones usan **[!UICONTROL Config]** y opciones en **[!UICONTROL App Designer]**la. Consulte Personalización de aplicaciones para obtener más detalles sobre el estándar **[!UICONTROL Style]** y **[!UICONTROL Config]** las opciones de todas las aplicaciones en la **[!UICONTROL App Designer.]**

Puede personalizar Mosaic con las siguientes opciones adicionales en App Designer:

* **[!UICONTROL Content interaction]**. Define el estilo con el que se cargará el nuevo contenido en la página:

   * **[!UICONTROL Hover Fade]** para atenuar al otro lado de una tarjeta cuando un visitante del sitio sitúa el ratón sobre el contenido.
   * **[!UICONTROL Hover Flip]** para voltear al otro lado de una tarjeta cuando un visitante del sitio pase el ratón sobre el contenido.
   * **[!UICONTROL Click]** para mostrar el otro lado de una tarjeta cuando un visitante del sitio hace clic en el contenido del ratón.

* **[!UICONTROL Number of Tiles to Load]**. Número de mosaicos que se cargarán en un Mosaico. Esto puede afectar a la visualización de salida. Mosaico no se mostrará en una cuadrícula a menos que elija el número correcto de mosaicos para corresponderse con el ancho del contenedor. Es posible que necesite ajustarlas para que la cuadrícula se muestre correctamente.
* **[!UICONTROL Hide social branding when rights granted]** Cambie esto para eliminar el logotipo de la red de medios sociales originada (Twitter o Instagram) cuando se otorgan derechos para un fragmento de contenido.

* **[!UICONTROL Call-to-action button]** Puede utilizar el botón Llamada a acción con un catálogo de productos para dirigir a los usuarios a un producto o a su sitio para que realicen más acciones.

   * **[!UICONTROL Call-to-action button]** Cambie la opción para mostrar el botón Llamada a acción.

   * **[!UICONTROL Require rights to display products]** Cambie la activación para que el propietario del contenido haya concedido derechos para el contenido antes de que aparezca un botón de llamada a acción para el contenido.

      >[!NOTE]
      >
      >El contenido se muestra incluso si no se conceden derechos para el contenido, pero el botón de llamada a acción no se mostrará con el contenido, a menos que se otorguen derechos para el contenido.

   * **[!UICONTROL Show call-to-action in tile]**. Elija si desea mostrar el botón llamada a acción en un mosaico Tira de película en lugar de mostrar el botón de llamada a acción solo cuando el visitante del sitio haga clic en una tarjeta y abre el contenido en una ventana más grande.
   * **[!UICONTROL Call-to-action indication text]** Texto que se muestra para pedir al usuario que haga clic en la tarjeta para abrir el modal de llamada a acción.

   * **[!UICONTROL Call-to-action header text]** Palabras que se mostrarán en el encabezado sobre el botón Llamada a acción en el modal. La redacción predeterminada es "Buy these products: ".

   * **[!UICONTROL Call-to-action button text]** Personalice el texto del botón Llamada a acción. El texto predeterminado es "Buy Now".

   * **[!UICONTROL Product display options]** Elija si desea mostrar el **[!UICONTROL Photo]** botón y el **[!UICONTROL Product name]** de llamada a acción.

   * **[!UICONTROL Product URL referral tracking]** Cambie el conmutador a para rastrear las referencias de esta aplicación a la página del producto asociada.

   * **[!UICONTROL Referral tracking key-value pairs]** Agregue parámetros para especificar el seguimiento de referencia desde el contenido de la aplicación a la página del producto asociada.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Seleccione esta opción para crear una aplicación para varias páginas de producto. Filtre el UGC específico del producto a la aplicación para cada página de producto. Puede seleccionar una o varias carpetas para asociar colecciones específicas a la aplicación.
   * **[!UICONTROL Select Product folders]**. Seleccione las carpetas de productos de nivel superior para filtrar UGC. Utilice CTRL/Comando + clic para seleccionar más de una carpeta. Livefyre utiliza la carpeta para determinar qué productos de esa carpeta se mostrarán en la aplicación en varias páginas.
   * **[!UICONTROL Show related content]**. Active esta opción para mostrar contenido publicado en la aplicación, pero etiquetado con un ID de producto distinto. Una vez que se muestra el contenido específico del producto para la aplicación, Livefyre muestra el contenido de otros productos y contenido no asociado a un producto. Livefyre prioriza primero el contenido con el mismo ID de producto, luego contenido publicado en la aplicación con otros ID de producto y, a continuación, contenido publicado en la aplicación sin ID de producto.

Consulte [Opciones de mosaico](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) para obtener más información sobre cómo personalizar un mosaico con Livefyre. js.
