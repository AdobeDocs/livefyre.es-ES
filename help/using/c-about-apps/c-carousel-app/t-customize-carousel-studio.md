---
description: Cambie las opciones de tamaño, ancho e interacción de la aplicación Carrusel.
seo-description: Cambie las opciones de tamaño, ancho e interacción de la aplicación Carrusel.
seo-title: Personalizar un carrusel con Studio
solution: Experience Manager
title: Personalizar un carrusel con Studio
uuid: 24 f 080 fc -37 bf -40 d 4-8 c 1 a-a 502 ee 8 ac 978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizar un carrusel con Studio{#customize-a-carousel-using-studio}

Cambie las opciones de tamaño, ancho e interacción de la aplicación Carrusel.

Todas las **[!UICONTROL Style]** aplicaciones usan **[!UICONTROL Config]** y opciones en **[!UICONTROL App Designer]** la. Consulte Personalización de aplicaciones para obtener más detalles sobre el estándar **[!UICONTROL Style]** y **[!UICONTROL Config]** las opciones de todas las aplicaciones en **[!UICONTROL App Designer]** la.

Puede personalizar un carrusel con las siguientes opciones adicionales en App Designer:

* **[!UICONTROL Max Number of Items]**

   Define el número de elementos que se mostrarán en el Carrusel. El valor predeterminado es 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Solo para pantallas de equipos

   * Si el contenido tiene más de 600 píxeles, aparece horizontalmente
   * Si el contenido es inferior a 600 píxeles, aparece verticalmente
   * **Vertical.** Para pantallas de ordenador o dispositivos móviles. En los dispositivos móviles, la tarjeta se reduce para ajustarse al tamaño de la pantalla.

* **[!UICONTROL Call-to-action button]** Puede utilizar el botón Llamada a acción con un catálogo de productos para dirigir a los usuarios a un producto o a su sitio para que realicen más acciones.

   * **[!UICONTROL Call-to-action button]** Cambie la opción para mostrar el botón llamada a acción.
   * **[!UICONTROL Require rights to display products]** Cambie la activación para que el propietario del contenido haya concedido derechos para el contenido antes de que aparezca un botón de llamada a acción para el contenido.
   >[!NOTE]
   >
   >El contenido se muestra incluso si no se conceden derechos para el contenido, pero el botón de llamada a acción no se mostrará con el contenido, a menos que se otorguen derechos para el contenido.

   * **[!UICONTROL Show call-to-action in tile]**. Elija si se mostrará el botón llamada a acción en un mosaico en lugar de mostrar el botón de llamada a acción solo cuando el visitante del sitio haga clic en una tarjeta y abre el contenido en una ventana más grande.
   * **[!UICONTROL Call-to-action indication text]** Texto que se muestra para pedir al usuario que haga clic en la tarjeta para abrir el modal de llamada a acción.
   * **[!UICONTROL Call-to-action header text]** Palabras que se mostrarán en el encabezado sobre el botón Llamada a acción en el modal. El texto predeterminado es &quot;Buy these products: &quot;.
   * **[!UICONTROL Call-to-action button text]** Palabras que se mostrarán en el botón de llamada a acción del modal. El texto predeterminado es &quot;Buy Now: &quot;.
   * **[!UICONTROL Product display options]** Elija si desea mostrar el **[!UICONTROL Photo]** botón y el **[!UICONTROL Product name]** de llamada a acción.
   >[!NOTE]
   >
   >Los botones de fotografía y de producto destacan azul cuando están activados.

   * **[!UICONTROL Product URL referral tracking]** Cambie el conmutador a para rastrear las referencias de esta aplicación a la página del producto asociada.
   * **[!UICONTROL Referral tracking key-value pairs]** Agregue parámetros para especificar el seguimiento de referencia desde el contenido de la aplicación a la página del producto asociada.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Seleccione esta opción para crear una aplicación para varias páginas de producto. Filtre el UGC específico del producto a la aplicación para cada página de producto. Puede seleccionar una o varias carpetas para asociar colecciones específicas a la aplicación.
   * **[!UICONTROL Select Product folders]**. Seleccione las carpetas de productos de nivel superior para filtrar UGC. Utilice CTRL/Comando + clic para seleccionar más de una carpeta. Livefyre utiliza la carpeta para determinar qué productos de esa carpeta se mostrarán en la aplicación en varias páginas.
   * **[!UICONTROL Show related content]**. Active esta opción para mostrar contenido publicado en la aplicación, pero etiquetado con un ID de producto distinto. Una vez que se muestra el contenido específico del producto para la aplicación, Livefyre muestra el contenido de otros productos y contenido no asociado a un producto. Livefyre prioriza primero el contenido con el mismo ID de producto, luego contenido publicado en la aplicación con otros ID de producto y, a continuación, contenido publicado en la aplicación sin ID de producto.
