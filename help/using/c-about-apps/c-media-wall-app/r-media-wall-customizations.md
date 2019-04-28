---
description: Cambie las opciones de tamaño, ancho e interacción de la aplicación de Muro de medios.
seo-description: Cambie las opciones de tamaño, ancho e interacción de la aplicación de Muro de medios.
seo-title: Personalizaciones de muro de medios
solution: Experience Manager
title: Personalizaciones de muro de medios
uuid: 79 adev 92-3937-4 bb 4-a 1 a 6-b 090 fb 39 afb 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizaciones de muro de medios{#media-wall-customizations}

Cambie las opciones de tamaño, ancho e interacción de la aplicación de Muro de medios.



Paredes de medios transmite imágenes en directo y otro contenido a un muro social en tiempo real, visualizando toda la actividad que rodea a un evento.

Si se habilita, los usuarios pueden publicar texto, imágenes o vídeo directamente en esta aplicación. Los tipos de archivo admitidos son:

* Imagen: JPEG, GIF, PNG
* Vídeo: Quicktime/MOV, MP 4, MPEG, webm
* Audio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Define el número inicial de elementos de contenido mostrados.

* **[!UICONTROL Load content with animation.]** Active esta opción para cargar el Muro de medios en una página con animación. Desactive esta opción para cargar el Muro de medios en una página sin animación.
* **[!UICONTROL Number of columns.]** Defina el número de columnas para el muro de medios. El número de columnas sigue siendo el mismo, independientemente del tamaño de la ventana o del navegador. Si selecciona Automático, el número de columnas se ajusta para mostrar un número optimizado de columnas para el tamaño de pantalla.
* **[!UICONTROL Fit content to width]**. Cuando esta opción está desactivada, el contenido se recorta a un cuadrado. Active esta opción para mostrar toda una imagen en la tarjeta, si llena toda la tarjeta o no.
* **[!UICONTROL Include content modal]**

   Permite que los usuarios hagan clic en una fotografía del flujo para abrirla en una ventana emergente superpuesta.

* **[!UICONTROL Require rights]**. Active esta opción para mostrar solo el contenido con un estado de solicitud de derechos de &quot;Concedido&quot;.
* **[!UICONTROL Hide social branding when rights granted]** Cambie esto para eliminar el logotipo de la red de medios sociales originada (Twitter o Instagram) cuando se otorgan derechos para un fragmento de contenido.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Seleccione si desea permitir que los usuarios anuncien texto, foto o vídeo con el botón de carga.
   * **[!UICONTROL Require Media]**. Active la opción para solicitar a los usuarios que carguen solo contenido de vídeo o foto mediante el botón Cargar.
   * Puede editar el texto predeterminado para los siguientes campos de botón de carga:

      * **[!UICONTROL Upload Button Text]**. Texto para el botón de carga. El texto predeterminado es &quot;¿Qué hay en mente?&quot;
      * **[!UICONTROL Comment Modal Title]**. Título del sitio modal que utilizan los visitantes para publicar contenido. El texto predeterminado es &quot;Publicar comentario&quot;.
      * **[!UICONTROL Comment Modal Button]**. El texto de los visitantes del sitio del sitio hace clic para anunciar contenido. El texto predeterminado es &quot;Publicar comentario&quot;.

* **[!UICONTROL Call-to-action button]** Puede utilizar el botón Llamada a acción con un catálogo de productos para dirigir a los usuarios a un producto o a su sitio para que realicen más acciones.

   * **[!UICONTROL Call-to-action button]** Cambie la opción para mostrar el botón Llamada a acción.
   * **[!UICONTROL Require rights to display products]** Cambie la activación para que el propietario del contenido haya concedido derechos para el contenido antes de que aparezca un botón de llamada a acción para el contenido.

      >[!NOTE]
      >
      >El contenido se muestra incluso si no se conceden derechos para el contenido, pero el botón de llamada a acción no se mostrará con el contenido, a menos que se otorguen derechos para el contenido.

   * **[!UICONTROL Call-to-action header text]** Palabras que se mostrarán en el encabezado sobre el botón Llamada a acción en el modal. La redacción predeterminada es &quot;Buy these products: &quot;.
   * **[!UICONTROL Call-to-action button text]** Palabras que se mostrarán en el botón de llamada a acción del modal. El texto predeterminado es &quot;Buy Now: &quot;.
   * **[!UICONTROL Product display options]** Elija si desea mostrar el nombre de la foto y del producto con el botón Llamada a acción.

      >[!NOTE]
      >
      >Los botones de fotografía y de producto destacan azul cuando están activados.

   * **[!UICONTROL Product URL referral tracking]** Cambie el conmutador a para rastrear las referencias de esta aplicación a la página del producto asociada.
   * **[!UICONTROL Referral tracking key-value pairs]** Agregue parámetros para especificar el seguimiento de referencia desde el contenido de la aplicación a la página del producto asociada.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Seleccione esta opción para crear una aplicación para varias páginas de producto. Filtre el UGC específico del producto a la aplicación para cada página de producto. Puede seleccionar una o varias carpetas para asociar colecciones específicas a la aplicación.
   * **[!UICONTROL Select Product folders]**. Seleccione las carpetas de productos de nivel superior para filtrar UGC. Utilice CTRL/Comando + clic para seleccionar más de una carpeta. Livefyre utiliza la carpeta para determinar qué productos de esa carpeta se mostrarán en la aplicación en varias páginas.
   * **[!UICONTROL Show related content]**. Active esta opción para mostrar contenido publicado en la aplicación, pero etiquetado con un ID de producto distinto. Una vez que se muestra el contenido específico del producto para la aplicación, Livefyre muestra el contenido de otros productos y contenido no asociado a un producto. Livefyre prioriza primero el contenido con el mismo ID de producto, luego contenido publicado en la aplicación con otros ID de producto y, a continuación, contenido publicado en la aplicación sin ID de producto.

Puede personalizar el muro de medios mediante:

* **[!UICONTROL Style]** y **[!UICONTROL Config]** opciones para todas las aplicaciones del **[!UICONTROL App Designer]**. Consulte Personalización de aplicaciones para obtener más detalles sobre el estándar **[!UICONTROL Style]** y **[!UICONTROL Config]** las opciones de todas las aplicaciones en **[!UICONTROL App Designer]** la.

* Herramientas de integración. Consulte [Integración de muro de medios](/help/implementation/c-app-integrations/c-media-wall-integration.md) para obtener más información sobre cómo personalizar un muro de medios mediante Herramientas de integración.

