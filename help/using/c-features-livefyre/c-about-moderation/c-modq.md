---
description: Modere contenido de una interfaz única e inteligente.
title: Moderar contenido con ModQ
exl-id: 694b1f45-2b24-4e80-99a1-788e2cecc8a4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1454'
ht-degree: 0%

---

# Moderar contenido usando ModQ{#moderate-content-using-modq}

Modere contenido de una interfaz única e inteligente.

ModQ crea una cola en tiempo real de todo el contenido de su sitio o red que coincide con las reglas de premoderación que ha definido, lo que permite que los moderadores se centren únicamente en el contenido que requiere su atención.

Una vez que haya definido la configuración de ModQ, el nuevo contenido que entre en el flujo o el contenido existente marcado por los usuarios, se agregará a la cola. Los cambios en las reglas no eliminarán contenido de ModQ, sino que agregarán contenido nuevo a la cola según la nueva configuración.

ModQ le permite:

* Moderar en contexto, ver subprocesos completos y Aprobar, Papelera o Bozo, ya sea fragmentos individuales de contenido o subprocesos completos en un solo clic.
* Aumente la velocidad y la eficacia del flujo de trabajo.
* Responda al contenido y aumente su participación en su comunidad.
* Permita que varios moderadores trabajen a través del contenido, sin duplicar el trabajo de los demás.

El contenido de Livefyre está listado en ModQ durante un máximo de 6 semanas, y el contenido de transmisiones premoderadas que no se ha abordado aparece en ModQ durante 90 días.

>[!NOTE]
>
>Un solo fragmento de contenido puede aparecer varias veces si coincide con varias reglas para su inclusión en ModQ. Por ejemplo, si un fragmento de contenido déclencheur una regla de marca de usuario para Offensive, luego déclencheur otra regla para Profane, aparecerá en ModQ dos veces.

El contenido que no se muestra en ModQ incluye:

* Contenido enviado a la papelera.
* Contenido aprobado por un moderador.
* Contenido publicado por un usuario prohibido, o indicadores aplicados por un usuario prohibido.

## Navegación por ModQ {#section_uv4_db2_yy}

ModQ se divide en dos paneles con pestañas:

* **[!UICONTROL Items]** enumera todo el contenido nativo de Livefyre y SocialSync planeado para moderación. Esta ficha incluye cualquier contenido de Búsqueda social o Flujo que se haya marcado o editado después de la moderación.
* **[!UICONTROL Streams Premoderation]** enumera todo el contenido que entra en las aplicaciones desde flujos con Premoderar habilitado. (Para obtener más información, consulte Creación de flujos).

Ambas pestañas ofrecen muchos de los mismos filtros y herramientas de moderación.

* **[!UICONTROL Item Count]** El número de elementos que quedan en la cola se muestra en la esquina superior izquierda de ModQ.
* **[!UICONTROL Filter]** Haga clic en  **[!UICONTROL Filter]** para definir los parámetros según los cuales se enumerará el contenido en el panel.
* **[!UICONTROL History]** Haga clic en el  **[!UICONTROL History]** botón en la parte superior derecha de la pantalla para abrir una lista de contenido moderado recientemente, lo que le permite revisar su trabajo o cambiar una acción de moderación reciente. Vuelva a hacer clic en el botón para volver al contenido en cola. Solo se mostrarán las 100 acciones más recientes. **** El historial no enumera las acciones realizadas por otro moderador.

* **[!UICONTROL User Pane]** Haga clic en los botones para expandir o contraer situados en la parte superior derecha de la página para abrir o cerrar el panel Usuario.

## Explicación del contenido de ModQ {#section_oxm_kgz_y1b}

Cada parte de contenido de la lista muestra información de vista previa, incluido el sitio en el que se publicó y su autor. Si se selecciona un elemento, se mostrará todo el contenido, incluidos los medios.

>[!NOTE]
>
>El contenido nativo de Livefyre mostrará más información que el contenido agregado a su aplicación mediante Streams u otras fuentes de medios sociales.

La siguiente información se muestra al seleccionar un elemento:

* **[!UICONTROL Time in Queue:]** enumera la cantidad de tiempo que se agregó el fragmento de contenido a ModQ.
* **[!UICONTROL App name:]** la aplicación en la que aparece el contenido. Enlaza al sitio con la aplicación.
* **[!UICONTROL Content Body:]** texto y miniaturas de medios, si están disponibles.
* **[!UICONTROL Status:]** el estado actual del contenido (pendiente, con seguimiento, etc.).
* **[!UICONTROL Author information:]** nombre de usuario y nombre de usuario del autor.
* **[!UICONTROL Timestamp:]** la marca de tiempo relativa de cuándo se creó el contenido. Enlaza siempre a la parte de contenido de la página Contenido de aplicación de Studio.
* **[!UICONTROL Flag Type:]** Ofensiva, en desacuerdo, spam, etc.

   * Indicadores SAFE: Correo no deseado y de forma masiva.
   * Indicador aplicado por su Lista de perfiles de red y sitio: Profanidad.
   * Indicadores aplicados por SAFE: El discurso de odio, PII (información de identificación personal), el insulto y el lenguaje.
   * Indicadores de usuario: Correo no deseado, fuera de tema, Ofensivo y en desacuerdo.

* **[!UICONTROL Flag origin:]** el origen del indicador de la lista. Puede ser SAFE, un nombre de usuario o Livefyre.
* **[!UICONTROL More info:]** enumera los detalles del contenido, incluido el número de &quot;Me gusta&quot;, Marcas de usuario, Respuestas y cualquier etiqueta aplicada al contenido. Al hacer clic en el sitio se abre la página de nivel superior del sitio donde se encuentra el contenido. Al hacer clic en la marca de tiempo, se abre una vista de subprocesos del contenido en contexto en la página.

## Opciones de filtro en ModQ {#section_r2c_qc2_yy}

Haga clic **[!UICONTROL Filter]** en la parte superior izquierda de la ventana de ModQ para abrir un panel con opciones de filtro disponibles para el contenido de la lista. Al seleccionar opciones, ModQ se actualizará automáticamente para enumerar solamente el contenido filtrado. Haga clic en **[!UICONTROL Clear filters]** para borrar todas las opciones seleccionadas y vuelva a cargar la lista completa de elementos.

Hay diferentes opciones de filtro disponibles para las pestañas **[!UICONTROL Items]** y **[!UICONTROL Streams Premoderation]** .

Las siguientes opciones están disponibles para ModQ en **[!UICONTROL Items]** y **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**. Utilice el campo Buscar aplicaciones para filtrar los resultados por aplicación. Es posible que se seleccionen varias aplicaciones.
* **[!UICONTROL System Flags]**. Filtre el contenido por reglas como Correo no deseado, Profanidad, SAFE y Reglas de premoderación.

   * Al seleccionar **[!UICONTROL Spam]** se enumerarán todos los contenidos etiquetados como correo no deseado por SAFE.
   * Si selecciona **[!UICONTROL Profanity]**, se enumerarán todos los contenidos etiquetados como Perfiles por su Red o Lista de Propagación del Sitio.
   * Si selecciona **[!UICONTROL SAFE]**, se enumerarán todos los contenidos que ingresen a ModQ como resultado de sus reglas SAFE.
   * Si selecciona **[!UICONTROL Premoderation]**, se enumerarán todos los contenidos etiquetados para moderación previa por su red, emisión o configuración de aplicación.

* **[!UICONTROL User Flags]** Filtre el contenido por indicadores de usuario. Las opciones incluyen Offensivo, Correo no deseado, Fuera del tema y Discrepancia.
* **[!UICONTROL Rights Requests.]** Muestre solo contenido con derechos otorgados haciendo clic en la casilla de verificación.
* **[!UICONTROL Entered the queue.]** Filtre el contenido por el lapso de tiempo durante el cual se envió el contenido a ModQ. La hora en la que se envió el contenido a ModQ no es necesariamente la hora en la que se publicó el contenido en su aplicación.

Las siguientes opciones están disponibles para ModQ en **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** Filtre el contenido por la fuente social desde la que se originó el contenido. Por ejemplo, las opciones de las fuentes sociales incluyen Twitter, Instagram, Facebook y RSS.

La siguiente opción está disponible para ModQ en **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**. Filtre el contenido por la recomendación que proporciona la Recomendación de moderación automatizada.

Las siguientes imágenes muestran el aspecto de Moderation Recommendations en ModQ:  ![](assets/mod_reco1.png)

La recomendación de moderación se proporciona para el contenido cuando se configura en **[!UICONTROL Network Settings > Moderation]** y **[!UICONTROL Network Settings > ModQ]**.

## Acciones que se pueden usar en ModQ {#section_h4g_wrn_z1b}

Puede decidir qué hacer con cada fragmento de contenido en ModQ.

Seleccione una de las siguientes opciones:

* El icono **[!UICONTROL Checkbox]** para aprobar el contenido
* El icono **[!UICONTROL Trash can]** para enviar el contenido a la papelera
* **[!UICONTROL Request Rights]** para solicitar los derechos al contenido al propietario del contenido.

   >[!NOTE]
   >
   >No puede solicitar derechos en ModQ para contenido desde Instagram. Debe usar la biblioteca o el contenido de la aplicación para enviar solicitudes de derechos de contenido desde Instagram.

* **[!UICONTROL Feature and Approve]** para aprobar el contenido y también mostrar el contenido.
* **[!UICONTROL Product Tag and Approve]** para agregar un producto del catálogo de productos al contenido y luego aprobarlo.
* **[!UICONTROL Mark as Pending]** para marcar el contenido como pendiente.

>[!NOTE]
>
>Una vez que envíe un fragmento de contenido, el fragmento de contenido y todas las respuestas al fragmento de contenido se eliminarán de ModQ de forma permanente. Para colocar un fragmento de contenido enviado a la papelera en una aplicación, consulte [Agregar un elemento enviado a la papelera de vuelta a una aplicación](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Si el contenido ya está en el estado deseado, al seleccionar Papelera, Bozo o Aprobar se confirmará el estado y se eliminará el elemento de la lista. Moderar un fragmento de contenido lo quitará inmediatamente de la cola y lo desactivará en las colas de otros moderadores.

>[!NOTE]
>
>El contenido del flujo puede no ser Bozo’d. El contenido del flujo de seguimiento lo eliminará de la emisión de forma permanente y no se puede deshacer.

Una vez que el contenido se haya moderado, se eliminará del ModQ del moderador y su autor ya no podrá editarlo desde el flujo. Si un moderador rechaza un elemento o si un usuario elimina su comentario, aparecerá atenuado en las colas de otros moderadores en tiempo real. Cuando el contenido se ha atenuado, el botón **[!UICONTROL Clear Moderated]** aparece en la página, lo que permite a los moderadores eliminarlo de sus listas y mantener su lugar en la página independientemente de otra actividad de moderador.

## Uso de la función Papelera en ModQ {#section_tpx_qgz_y1b}

Utilice la sección de configuración para seleccionar las opciones disponibles cuando el contenido se marca como Desenviado.

* ****[!UICONTROL Confirm Trash]**** Active esta opción para requerir que los moderadores confirmen su acción al configurar contenido como Papelera. Cuando está habilitado, al seleccionar **[!UICONTROL Trash]** para contenido se muestra un cuadro de diálogo que solicita un **[!UICONTROL Reason for Moderation]** y ofrece un campo en el que se puede introducir un **[!UICONTROL Note]**.

   (Esta configuración está disponible **[!UICONTROL only]** a nivel de red y se aplicará a todos los sitios de la red).

* ****[!UICONTROL Hide Replies]**** Active esta opción para enviar automáticamente a la papelera las respuestas cuando un comentario principal se haya enviado a la papelera o Bozo&#39;d.

## Cambiar el estado de usuario en ModQ {#section_tmw_lg1_z1b}

Haga clic en el botón **[!UICONTROL User actions]** del panel Resumen de usuarios para Silenciar, Prohibir o Permitir-enumerar al usuario.

* **[!UICONTROL Mute:]** le permite Silenciar los indicadores del usuario que ha marcado el contenido de la lista. Utilice esta opción para excluir los indicadores del usuario de los filtros de premoderación. El contenido que marquen no entrará en ModQ como resultado del indicador, y sus indicadores no se incluirán en las Reglas de marca.
* **[!UICONTROL Ban:]** le permite prohibir el acceso del usuario a la lista desde su sitio o red. (Solo los administradores de Studio o los administradores de usuarios pueden prohibir la red de un usuario).
* **[!UICONTROL Whitelist:]** le permite incluir en la lista de permitidos al usuario de la red o del sitio. (Solo los administradores de Studio o los administradores de usuarios pueden incluir en la lista de permitidos de un usuario).



Aplicaciones que usan ModQ:

* [Conversación](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reseñas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Notas](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Upload Button](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
