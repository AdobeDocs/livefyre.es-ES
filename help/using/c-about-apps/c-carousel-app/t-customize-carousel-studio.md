---
description: Cambie el tamaño, el ancho y las opciones de interacción de la aplicación Carrusel.
seo-description: Cambie el tamaño, el ancho y las opciones de interacción de la aplicación Carrusel.
seo-title: Personalización de un carrusel con Studio
solution: Experience Manager
title: Personalización de un carrusel con Studio
uuid: 24f080fc-37bf-40d4-8c1a-a502ee8ac978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalización de un carrusel con Studio{#customize-a-carousel-using-studio}

Cambie el tamaño, el ancho y las opciones de interacción de la aplicación Carrusel.

Todas las aplicaciones utilizan **[!UICONTROL Style]** y **[!UICONTROL Config]** las opciones del **[!UICONTROL App Designer]**. Consulte Personalización de aplicaciones para obtener más información sobre las opciones estándar **[!UICONTROL Style]** y **[!UICONTROL Config]** para todas las aplicaciones de la **[!UICONTROL App Designer]**.

Puede personalizar un carrusel con las siguientes opciones adicionales en App Designer:

* **[!UICONTROL Max Number of Items]**

   Define el número de elementos que se mostrarán en el Carrusel. El valor predeterminado es 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Solo para pantallas de equipos

   * Si el contenido es mayor que 600 píxeles, se muestra horizontalmente
   * Si el contenido es menor que 600 píxeles, se muestra verticalmente
   * **Vertical.** Para pantallas de ordenador o dispositivos móviles. En los dispositivos móviles, la tarjeta se reduce para adaptarse al tamaño de la pantalla.

* **[!UICONTROL Call-to-action button]** Puede utilizar el botón Llamada a acción con un catálogo de productos para dirigir a los usuarios a un producto o a su sitio para que realicen acciones adicionales.

   * **[!UICONTROL Call-to-action button]** Cambie el conmutador a activado para mostrar el botón de llamada a acción.
   * **[!UICONTROL Require rights to display products]** Cambie el conmutador a activado para requerir que el propietario del contenido haya concedido derechos para el contenido antes de que aparezca un botón de llamada a acción para el contenido.
   >[!NOTE]
   >
   >El contenido se muestra aunque no se hayan concedido derechos para el contenido, pero el botón de llamada a acción no se mostrará con el contenido a menos que se concedan derechos para el contenido.

   * **[!UICONTROL Show call-to-action in tile]**. Elija si desea mostrar el botón de llamada a acción en un mosaico en lugar de mostrar el botón de llamada a acción solo cuando el visitante del sitio hace clic en una tarjeta y abre el contenido en una ventana más grande.
   * **[!UICONTROL Call-to-action indication text]** Texto que se muestra para pedir al usuario que haga clic en la tarjeta para abrir el modal de llamada a acción.
   * **[!UICONTROL Call-to-action header text]** Palabras que se mostrarán en el encabezado encima del botón Llamada a acción en el modal de contenido. El texto predeterminado es "Comprar estos productos:".
   * **[!UICONTROL Call-to-action button text]** Palabras que se mostrarán en el botón Llamada a acción en el modal de contenido. El texto predeterminado es "Comprar ahora:".
   * **[!UICONTROL Product display options]** Elija si desea mostrar el **[!UICONTROL Photo]** y el **[!UICONTROL Product name]** con el botón Llamada a acción.
   >[!NOTE]
   >
   >Los botones Foto y Nombre del producto resaltan el azul cuando están activados.

   * **[!UICONTROL Product URL referral tracking]** Cambie el conmutador a activado para rastrear las referencias de esta aplicación a la página de producto asociada.
   * **[!UICONTROL Referral tracking key-value pairs]** Agregue parámetros para especificar aún más el seguimiento de referencia desde el contenido de la aplicación a la página del producto asociada.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Seleccione esta opción para crear una aplicación para varias páginas de productos. Filtre el UGC específico del producto en la aplicación para cada página del producto. Puede seleccionar una o varias carpetas para asociar colecciones específicas a la aplicación.
   * **[!UICONTROL Select Product folders]**. Seleccione las carpetas de productos de nivel superior que desee utilizar para filtrar UGC. Utilice CTRL/Comando + clic para seleccionar más de una carpeta. Livefyre utiliza la carpeta para determinar qué productos de esa carpeta se mostrarán en la aplicación en varias páginas.
   * **[!UICONTROL Show related content]**. Alterne esta opción para mostrar el contenido publicado en la aplicación, pero etiquetado con un ID de producto diferente. Una vez que se muestra el contenido específico del producto para la aplicación, Livefyre muestra el contenido para otros productos y el contenido no asociado a un producto. Livefyre prioriza primero el contenido con el mismo ID de producto, después el contenido publicado en la aplicación con otros ID de producto y, a continuación, el contenido publicado en la aplicación sin ID de producto.
