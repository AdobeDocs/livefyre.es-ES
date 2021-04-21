---
description: Cambie el tamaño, la anchura y las opciones de interacción de la aplicación Carrusel.
title: Personalizar un carrusel con Studio
exl-id: f6f681ac-c601-40b9-9e99-bf5495f505f8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Personalizar un carrusel con Studio{#customize-a-carousel-using-studio}

Cambie el tamaño, la anchura y las opciones de interacción de la aplicación Carrusel.

Todas las aplicaciones utilizan las opciones **[!UICONTROL Style]** y **[!UICONTROL Config]** en la **[!UICONTROL App Designer]**. Consulte Personalización de aplicaciones para obtener más información sobre las opciones estándar **[!UICONTROL Style]** y **[!UICONTROL Config]** para todas las aplicaciones de **[!UICONTROL App Designer]**.

Puede personalizar un carrusel con las siguientes opciones adicionales en el Diseñador de aplicaciones:

* **[!UICONTROL Max Number of Items]**

   Define el número de elementos que se mostrarán en el carrusel. El valor predeterminado es 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Solo para pantallas de equipos

   * Si el contenido es mayor de 600 píxeles, se muestra horizontalmente
   * Si el contenido es menor de 600 píxeles, se muestra verticalmente
   * **Vertical.** Para pantallas de equipos o dispositivos móviles. En los dispositivos móviles, la tarjeta se reduce para ajustarse al tamaño de la pantalla.

* **[!UICONTROL Call-to-action button]** Puede utilizar el botón Llamada a acción con un catálogo de productos para dirigir a los usuarios a un producto o a su sitio para que realicen más acciones.

   * **[!UICONTROL Call-to-action button]** Cambie el conmutador a activado para mostrar el botón de llamada a la acción.
   * **[!UICONTROL Require rights to display products]** Cambie el conmutador a para requerir que el propietario del contenido haya concedido derechos para el contenido antes de que aparezca un botón de llamada a acción para el contenido.

   >[!NOTE]
   >
   >El contenido se muestra aunque no se hayan concedido derechos para el contenido, pero el botón de llamada a la acción no se mostrará con el contenido a menos que se concedan derechos para el contenido.

   * **[!UICONTROL Show call-to-action in tile]**. Elija si desea mostrar el botón de llamada a acción en un mosaico en lugar de mostrar el botón de llamada a acción solo cuando el visitante del sitio hace clic en una tarjeta y abre el contenido en una ventana más grande.
   * **[!UICONTROL Call-to-action indication text]** Texto que se muestra para pedir al usuario que haga clic en la tarjeta para abrir el modal de llamada a acción.
   * **[!UICONTROL Call-to-action header text]** Palabras que se mostrarán en el encabezado sobre el botón Llamada a acción en el modal de contenido. El texto predeterminado es &quot;Comprar estos productos:&quot;.
   * **[!UICONTROL Call-to-action button text]** Palabras que se mostrarán en el botón Llamada a acción del modal de contenido. El texto predeterminado es &quot;Comprar ahora:&quot;.
   * **[!UICONTROL Product display options]** Elija si desea mostrar el  **[!UICONTROL Photo]** y el  **[!UICONTROL Product name]** con el botón Llamada a acción .

   >[!NOTE]
   >
   >Los botones Foto y Nombre del producto resaltan en azul cuando están activados.

   * **[!UICONTROL Product URL referral tracking]** Cambie el conmutador a para rastrear las referencias de esta aplicación a la página de producto asociada.
   * **[!UICONTROL Referral tracking key-value pairs]** Añada parámetros para especificar aún más el seguimiento de referencia del contenido de su aplicación a la página de producto asociada.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Seleccione esta opción para crear una aplicación para varias páginas de producto. Filtre el UGC específico del producto a la aplicación para cada página de producto. Puede seleccionar una o varias carpetas para asociar colecciones específicas a la aplicación.
   * **[!UICONTROL Select Product folders]**. Seleccione las carpetas de producto de nivel superior que desea utilizar para filtrar UGC. Utilice CTRL/Comando + clic para seleccionar más de una carpeta. Livefyre utiliza la carpeta para determinar qué productos de esa carpeta se mostrarán en la aplicación en varias páginas.
   * **[!UICONTROL Show related content]**. Alterne esta opción para mostrar el contenido publicado en la aplicación, pero etiquetado con un ID de producto diferente. Una vez que se muestra el contenido específico del producto para la aplicación, Livefyre muestra el contenido de otros productos y contenido no asociado a un producto. Livefyre prioriza primero el contenido con el mismo ID de producto, después el contenido publicado en la aplicación con otros ID de producto, y después el contenido publicado en la aplicación sin ID de producto.
