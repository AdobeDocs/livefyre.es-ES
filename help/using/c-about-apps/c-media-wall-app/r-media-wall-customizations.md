---
description: Cambie el tamaño, el ancho y las opciones de interacción de la aplicación de Media Wall.
seo-description: Cambie el tamaño, el ancho y las opciones de interacción de la aplicación de Media Wall.
seo-title: Personalizaciones del muro de medios
solution: Experience Manager
title: Personalizaciones del muro de medios
uuid: 79aecd92-3937-4bb4-a1a6-b090fb39afb0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizaciones del muro de medios{#media-wall-customizations}

Cambie el tamaño, el ancho y las opciones de interacción de la aplicación de Media Wall.



Media Walls transmite imágenes en directo y otro contenido en un muro social en tiempo real, visualizando toda la actividad que rodea a un evento.

Si está activada, los usuarios pueden publicar texto, imágenes o vídeo directamente en esta aplicación. Entro los tipos de archivos admitidos se incluyen:

* Imagen: JPEG, GIF, PNG
* Vídeo: Quicktime/MOV, MP4, MPEG, WebM
* Audio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Define el número inicial de elementos de contenido que se muestran.

* **[!UICONTROL Load content with animation.]** Active esta opción para cargar el Muro de medios en una página con animación. Desactive esta opción para cargar el Muro de medios en una página sin animación.
* **[!UICONTROL Number of columns.]** Establezca el número de columnas para el Muro de medios. El número de columnas permanece igual, independientemente del tamaño de la ventana o del explorador. Si selecciona Automático, el número de columnas se ajusta para mostrar un número optimizado de columnas para el tamaño de pantalla.
* **[!UICONTROL Fit content to width]**. Cuando esta opción está desactivada, el contenido se recorta a un cuadrado. Active esta opción para mostrar toda una imagen en la tarjeta, rellene o no toda la tarjeta.
* **[!UICONTROL Include content modal]**

   Permite a los usuarios hacer clic en una fotografía del flujo para abrirla en una ventana emergente superpuesta.

* **[!UICONTROL Require rights]**. Active esta opción para mostrar solo el contenido con el estado de solicitud de derechos "Concedido".
* **[!UICONTROL Hide social branding when rights granted]** Active esta opción para eliminar el logotipo de la red de medios sociales de origen (Twitter o Instagram) cuando se concedan derechos para un contenido.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Seleccione si permitirá que los usuarios publiquen texto, fotografía o vídeo con el botón de carga.
   * **[!UICONTROL Require Media]**. Active esta opción para exigir que los usuarios solo carguen contenido de fotos o vídeos con el botón Cargar.
   * Puede editar el texto predeterminado de los siguientes campos del botón Cargar:

      * **[!UICONTROL Upload Button Text]**. Texto para el botón Cargar. El texto predeterminado es "¿Qué tienes en mente?"
      * **[!UICONTROL Comment Modal Title]**. Título para el sitio modal que los visitantes utilizan para anunciar contenido. El texto predeterminado es "Publicar su comentario".
      * **[!UICONTROL Comment Modal Button]**. Texto en el que los visitantes del sitio hacen clic para anunciar contenido. El texto predeterminado es "Publicar su comentario".

* **[!UICONTROL Call-to-action button]** Puede utilizar el botón Llamada a acción con un catálogo de productos para dirigir a los usuarios a un producto o a su sitio para que realicen acciones adicionales.

   * **[!UICONTROL Call-to-action button]** Cambie el conmutador a activado para mostrar el botón Llamada a acción.
   * **[!UICONTROL Require rights to display products]** Cambie el conmutador a activado para requerir que el propietario del contenido haya concedido derechos para el contenido antes de que aparezca un botón de llamada a acción para el contenido.

      >[!NOTE]
      >
      >El contenido se muestra aunque no se hayan concedido derechos para el contenido, pero el botón Llamada a acción no se mostrará con el contenido a menos que se concedan derechos para el contenido.

   * **[!UICONTROL Call-to-action header text]** Palabras que se mostrarán en el encabezado encima del botón Llamada a acción en el modal de contenido. El texto predeterminado es "Comprar estos productos:".
   * **[!UICONTROL Call-to-action button text]** Palabras que se mostrarán en el botón Llamada a acción en el modal de contenido. El texto predeterminado es "Comprar ahora:".
   * **[!UICONTROL Product display options]** Elija si desea mostrar la foto y el nombre del producto con el botón Llamada a acción.

      >[!NOTE]
      >
      >Los botones Foto y Nombre del producto resaltan el azul cuando están activados.

   * **[!UICONTROL Product URL referral tracking]** Cambie el conmutador a activado para rastrear las referencias de esta aplicación a la página de producto asociada.
   * **[!UICONTROL Referral tracking key-value pairs]** Agregue parámetros para especificar aún más el seguimiento de referencia desde el contenido de la aplicación a la página del producto asociada.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Seleccione esta opción para crear una aplicación para varias páginas de productos. Filtre el UGC específico del producto en la aplicación para cada página del producto. Puede seleccionar una o varias carpetas para asociar colecciones específicas a la aplicación.
   * **[!UICONTROL Select Product folders]**. Seleccione las carpetas de productos de nivel superior que desee utilizar para filtrar UGC. Utilice CTRL/Comando + clic para seleccionar más de una carpeta. Livefyre utiliza la carpeta para determinar qué productos de esa carpeta se mostrarán en la aplicación en varias páginas.
   * **[!UICONTROL Show related content]**. Alterne esta opción para mostrar el contenido publicado en la aplicación, pero etiquetado con un ID de producto diferente. Una vez que se muestra el contenido específico del producto para la aplicación, Livefyre muestra el contenido para otros productos y el contenido no asociado a un producto. Livefyre prioriza primero el contenido con el mismo ID de producto, después el contenido publicado en la aplicación con otros ID de producto y, a continuación, el contenido publicado en la aplicación sin ID de producto.

Puede personalizar Media Wall mediante:

* **[!UICONTROL Style]** y **[!UICONTROL Config]** para todas las aplicaciones de la **[!UICONTROL App Designer]**. Consulte Personalización de aplicaciones para obtener más información sobre las opciones estándar **[!UICONTROL Style]** y **[!UICONTROL Config]** para todas las aplicaciones de la **[!UICONTROL App Designer]**.

* Herramientas de integración. Consulte Integración [de](/help/implementation/c-app-integrations/c-media-wall-integration.md) Media Wall para obtener más información sobre cómo personalizar un Media Wall mediante las herramientas de integración.

