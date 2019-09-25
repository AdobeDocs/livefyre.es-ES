---
description: 'null'
seo-description: 'null'
seo-title: Personalizaciones de tiras de película
solution: Experience Manager
title: Personalizaciones de tiras de película
uuid: 99f8b697-4aa3-4813-bcac-d0e0bdee252d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Personalizaciones de tiras de película{#filmstrip-customizations}

Todas las aplicaciones utilizan **[!UICONTROL Style]** y **[!UICONTROL Config]** las opciones del **[!UICONTROL App Designer]**. Consulte Personalización de aplicaciones para obtener más información sobre las opciones estándar **[!UICONTROL Style]** y **[!UICONTROL Config]** las opciones de todas las aplicaciones en la sección **[!UICONTROL App Designer.]**

Puede personalizar la tira de película con las siguientes opciones adicionales en App Designer:

* **[!UICONTROL Content fit]**. Elija **[!UICONTROL crop]** recortar el contenido para rellenar la tarjeta o **[!UICONTROL Aspect Ratio]** mostrar una imagen completa en la tarjeta, rellene o no toda la tarjeta.
* **[!UICONTROL Tile Size]**. Introduzca el tamaño de los mosaicos en píxeles.
* **[!UICONTROL Show Notifications]**. Elija si desea mostrar una notificación para el nuevo contenido a medida que se transmite en la aplicación Tira de película.
* **[!UICONTROL Require rights]**. Active esta opción para mostrar solo el contenido con el estado de solicitud de derechos "Concedido".
* **[!UICONTROL Hide social branding when rights granted]** Active esta opción para eliminar el logotipo de la red de medios sociales de origen (Twitter o Instagram) cuando se concedan derechos para un contenido.
* **[!UICONTROL Call-to-action button]** Puede utilizar el botón de llamada a acción con un catálogo de productos para dirigir a los usuarios a un producto o a su sitio para que realicen acciones adicionales.

   * **[!UICONTROL Call-to-action button]** Cambie el conmutador a activado para mostrar el botón de llamada a acción.
   * **[!UICONTROL Require rights to display products]** Cambie el conmutador a activado para requerir que el propietario del contenido haya concedido derechos para el contenido antes de que aparezca un botón de llamada a acción para el contenido.

      >[!NOTE]
      >
      >El contenido se muestra aunque no se hayan concedido derechos para el contenido, pero el botón de llamada a acción no se mostrará con el contenido a menos que se concedan derechos para el contenido.

   * **[!UICONTROL Show call-to-action in tile]**. Elija si desea mostrar el botón de llamada a acción en un mosaico de tira de película en lugar de mostrar el botón de llamada a acción solo cuando el visitante del sitio hace clic en una tarjeta y abre el contenido en una ventana más grande.
   * **[!UICONTROL Call-to-action indication text]** Texto que se muestra para pedir al usuario que haga clic en la tarjeta para abrir el modal de llamada a acción.
   * **[!UICONTROL Call-to-action header text]** Palabras que se mostrarán en el encabezado encima del botón de llamada a acción en el modal de contenido. El texto predeterminado es "Comprar estos productos:".
   * **[!UICONTROL Call-to-action button text]** Palabras que se mostrarán en el botón de llamada a acción en el modal de contenido. El texto predeterminado es "Comprar ahora:".
   * **[!UICONTROL Product display options]** Elija si desea mostrar el **[!UICONTROL Photo]** y el **[!UICONTROL Product name]** con el botón de llamada a acción.

      >[!NOTE]
      >
      >Los botones Foto y Nombre del producto resaltan el azul cuando están activados.

   * **[!UICONTROL Product URL referral tracking]** Cambie el conmutador a activado para rastrear las referencias de esta aplicación a la página de producto asociada.
   * **[!UICONTROL Referral tracking key-value pairs]** Agregue parámetros para especificar aún más el seguimiento de referencia desde el contenido de la aplicación a la página del producto asociada.

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Seleccione esta opción para crear una aplicación para varias páginas de productos. Filtre el UGC específico del producto en la aplicación para cada página del producto. Puede seleccionar una o varias carpetas para asociar colecciones específicas a la aplicación.
   * **[!UICONTROL Select product folders]**. Seleccione las carpetas de productos de nivel superior que desee utilizar para filtrar UGC. Utilice CTRL/Comando + clic para seleccionar más de una carpeta. Livefyre utiliza la carpeta para determinar qué productos de esa carpeta se mostrarán en la aplicación en varias páginas.
   * **[!UICONTROL Show related content]**. Alterne esta opción para mostrar el contenido publicado en la aplicación, pero etiquetado con un ID de producto diferente. Una vez que se muestra el contenido específico del producto para la aplicación, Livefyre muestra el contenido para otros productos y el contenido no asociado a un producto. Livefyre prioriza primero el contenido con el mismo ID de producto, después el contenido publicado en la aplicación con otros ID de producto y, a continuación, el contenido publicado en la aplicación sin ID de producto.

Consulte Opciones [de](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) tira de película para obtener más información sobre cómo personalizar una tira de película con Livefyre.js.

