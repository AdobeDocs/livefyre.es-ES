---
description: Cambie el tamaño, la anchura y las opciones de interacción de la aplicación de Media Wall.
title: Personalizaciones de Muro de Medios
exl-id: bc34d8da-9e14-4226-b38d-128889bc31cc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# Personalizaciones de Muro de Medios{#media-wall-customizations}

Cambie el tamaño, la anchura y las opciones de interacción de la aplicación de Media Wall.



Media Walls transmite imágenes en vivo y otro contenido a un muro social en tiempo real, visualizando toda la actividad que rodea a un evento.

Si está habilitado, los usuarios pueden publicar texto, imágenes o vídeos directamente en esta aplicación. Entro los tipos de archivos admitidos se incluyen:

* Imagen: JPEG, GIF, PNG
* Vídeo: Quicktime/MOV, MP4, MPEG, WebM
* Audio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Define el número inicial de elementos de contenido mostrados.

* **[!UICONTROL Load content with animation.]** Active esta opción para cargar el muro de medios en una página con animación. Desactive esta opción para cargar el muro de medios en una página sin animación.
* **[!UICONTROL Number of columns.]** Establezca el número de columnas para el muro de medios. El número de columnas es el mismo, independientemente del tamaño de la ventana o del explorador. Si selecciona Automático, el número de columnas se ajusta para mostrar un número optimizado de columnas para el tamaño de pantalla.
* **[!UICONTROL Fit content to width]**. Cuando esta opción está desactivada, el contenido se recorta a un cuadrado. Active esta opción para mostrar una imagen entera en la tarjeta, tanto si llena la tarjeta como si no.
* **[!UICONTROL Include content modal]**

   Permite a los usuarios hacer clic en una foto del flujo para abrirla en una ventana emergente superpuesta.

* **[!UICONTROL Require rights]**. Active esta opción para mostrar solo contenido con el estado de solicitud de derechos &quot;Concedido&quot;.
* **[!UICONTROL Hide social branding when rights granted]** Active esta opción para eliminar el logotipo de la red de medios sociales de origen (Twitter o Instagram) cuando se concedan derechos para un fragmento de contenido.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Seleccione si permitirá que los usuarios anuncien texto, foto o vídeo con el botón de carga.
   * **[!UICONTROL Require Media]**. Cambie a activado para requerir que los usuarios solo carguen contenido de fotos o vídeos mediante el botón Cargar .
   * Puede editar el texto predeterminado de los siguientes campos de Botón de carga:

      * **[!UICONTROL Upload Button Text]**. Texto para el botón Cargar. El texto predeterminado es &quot;¿Qué tienes en mente?&quot;
      * **[!UICONTROL Comment Modal Title]**. Título del sitio modal que los visitantes utilizan para anunciar contenido. El texto predeterminado es &quot;Publicar su comentario&quot;.
      * **[!UICONTROL Comment Modal Button]**. Texto de botón en el que hacen clic los visitantes del sitio para anunciar contenido. El texto predeterminado es &quot;Publicar su comentario&quot;.

* **[!UICONTROL Call-to-action button]** Puede utilizar el botón Llamada a acción con un catálogo de productos para dirigir a los usuarios a un producto o a su sitio para que realicen más acciones.

   * **[!UICONTROL Call-to-action button]** Cambie el conmutador a activado para mostrar el botón Llamada a acción .
   * **[!UICONTROL Require rights to display products]** Cambie el conmutador a para requerir que el propietario del contenido haya concedido derechos para el contenido antes de que aparezca un botón de llamada a acción para el contenido.

      >[!NOTE]
      >
      >El contenido se muestra aunque no se hayan concedido derechos para el contenido, pero el botón Llamada a la acción no se mostrará con el contenido a menos que se concedan derechos para el contenido.

   * **[!UICONTROL Call-to-action header text]** Palabras que se mostrarán en el encabezado sobre el botón Llamada a acción en el modal de contenido. El texto predeterminado es &quot;Comprar estos productos:&quot;.
   * **[!UICONTROL Call-to-action button text]** Palabras que se mostrarán en el botón Llamada a acción del modal de contenido. El texto predeterminado es &quot;Comprar ahora:&quot;.
   * **[!UICONTROL Product display options]** Elija si desea mostrar la foto y el nombre del producto con el botón Llamada a la acción .

      >[!NOTE]
      >
      >Los botones Foto y Nombre del producto resaltan en azul cuando están activados.

   * **[!UICONTROL Product URL referral tracking]** Cambie el conmutador a para rastrear las referencias de esta aplicación a la página de producto asociada.
   * **[!UICONTROL Referral tracking key-value pairs]** Añada parámetros para especificar aún más el seguimiento de referencia del contenido de su aplicación a la página de producto asociada.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Seleccione esta opción para crear una aplicación para varias páginas de producto. Filtre el UGC específico del producto a la aplicación para cada página de producto. Puede seleccionar una o varias carpetas para asociar colecciones específicas a la aplicación.
   * **[!UICONTROL Select Product folders]**. Seleccione las carpetas de producto de nivel superior que desea utilizar para filtrar UGC. Utilice CTRL/Comando + clic para seleccionar más de una carpeta. Livefyre utiliza la carpeta para determinar qué productos de esa carpeta se mostrarán en la aplicación en varias páginas.
   * **[!UICONTROL Show related content]**. Alterne esta opción para mostrar el contenido publicado en la aplicación, pero etiquetado con un ID de producto diferente. Una vez que se muestra el contenido específico del producto para la aplicación, Livefyre muestra el contenido de otros productos y contenido no asociado a un producto. Livefyre prioriza primero el contenido con el mismo ID de producto, después el contenido publicado en la aplicación con otros ID de producto, y después el contenido publicado en la aplicación sin ID de producto.

Puede personalizar el muro de medios mediante:

* **[!UICONTROL Style]** y  **[!UICONTROL Config]** para todas las aplicaciones de  **[!UICONTROL App Designer]**. Consulte Personalización de aplicaciones para obtener más información sobre las opciones estándar **[!UICONTROL Style]** y **[!UICONTROL Config]** para todas las aplicaciones de **[!UICONTROL App Designer]**.

* Herramientas de integración. Consulte [Integración de muro de medios](/help/implementation/c-app-integrations/c-media-wall-integration.md) para obtener más información sobre cómo personalizar un muro de medios mediante las herramientas de integración.
