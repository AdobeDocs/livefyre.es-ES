---
description: Modere contenido desde una interfaz única e inteligente.
seo-description: Modere contenido desde una interfaz única e inteligente.
seo-title: Moderar contenido mediante modq
title: Moderar contenido mediante modq
uuid: c 630 fb 85-7 bd 0-4 da 0-ac 7 e -080 e 970 fb 4 f 9
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Moderar contenido mediante modq{#moderate-content-using-modq}

Modere contenido desde una interfaz única e inteligente.

Modq crea una cola en tiempo real de todo el contenido de su sitio o red que concuerda con las reglas de premoderación que ha definido, permitiendo que los moderadores se centren solamente en el contenido que requiere su atención.

Una vez definido los ajustes de modq, se agregará a la cola el contenido nuevo que entra al flujo o el contenido existente marcado por los usuarios. Los cambios en las reglas no eliminarán el contenido de modq, pero agregarán contenido nuevo a la cola según la nueva configuración.

Modq permite:

* Modere en contexto, vea hilos completos y Apruebe, Papelera o Bozo, ya sea fragmentos individuales de contenido o subprocesos completos con un solo clic.
* Aumente la velocidad y eficacia del flujo de trabajo.
* Responder al contenido, aumentando su participación con su comunidad.
* Permita que varios moderadores trabajen por contenido, sin duplicar el trabajo de los demás.

El contenido de Livefyre se muestra en modq durante hasta 6 semanas y el contenido premoderado de flujos que no se ha resuelto aparece en modq durante 90 días.

>[!NOTE]
>
>Un solo fragmento de contenido puede enumerarse varias veces si coincide con varias reglas para incluirlas en modq. Por ejemplo, si un fragmento de contenido activa una regla de marca de usuario para Ofensivo y posteriormente activa otra regla para Profane, se enumerará en modq dos veces.

El contenido que no se muestra en modq incluye:

* Contenido extraído.
* Contenido aprobado por un moderador.
* Contenido publicado por un usuario prohibido o marca de usuario aplicada por un usuario prohibido.

## Desplazamiento por modq {#section_uv4_db2_yy}

Modq se divide en dos paneles con fichas:

* **[!UICONTROL Items]** Enumera todo el contenido de Livefyre nativo y socialsync para moderación. Esta ficha incluye cualquier contenido de búsqueda social o flujo que se haya marcado o editado después de la moderación.
* **[!UICONTROL Streams Premoderation]** muestra todo el contenido que entra a sus aplicaciones desde Flujos con Premoderado activado. (Para obtener más información, consulte Creación de flujos.)

Ambas fichas ofrecen muchos de los mismos filtros y herramientas de moderación.

* **[!UICONTROL Item Count]** El número de elementos restantes en la cola se muestra en la esquina superior izquierda de modq.
* **[!UICONTROL Filter]** Haga clic en **[!UICONTROL Filter]** para definir los parámetros según los cuales se enumerará el contenido en el panel.
* **[!UICONTROL History]** Haga clic en **[!UICONTROL History]** el botón situado en la parte superior derecha de la pantalla para abrir una lista de contenido moderado recientemente, permitiéndole revisar su trabajo o cambiar una acción de moderación reciente. Vuelva a hacer clic en el botón para volver al contenido en cola. Solo se mostrarán las 100 acciones más recientes. **El historial** no enumerará las acciones realizadas por otro moderador.

* **[!UICONTROL User Pane]** Haga clic en los botones Expandir o Contraer en la parte superior derecha de la página para abrir o cerrar el panel Usuario.

## Explicación de modq Content {#section_oxm_kgz_y1b}

Cada parte de contenido mostrada muestra información de vista preliminar, incluido el sitio donde se publicó y su autor. Si se selecciona un elemento, se mostrará toda la parte del contenido, incluidos los medios.

>[!NOTE]
>
>El contenido nativo de Livefyre mostrará más información que el contenido agregado a la aplicación a través de flujos u otras fuentes de medios sociales.

La siguiente información aparece cuando selecciona un elemento:

* **[!UICONTROL Time in Queue:]** indica la cantidad de tiempo que el fragmento de contenido se agregó a modq.
* **[!UICONTROL App name:]** la aplicación en la que aparece el contenido. Vínculos al sitio con la aplicación.
* **[!UICONTROL Content Body:]** text y media thumbnail, si están disponibles.
* **[!UICONTROL Status:]** el estado actual del contenido (pendiente, trasfijo, etc.).
* **[!UICONTROL Author information:]** nombre del autor y nombre de usuario.
* **[!UICONTROL Timestamp:]** la marca de tiempo relativa de cuándo se creó el contenido. Permalinks al contenido de la página Contenido de la aplicación de Studio.
* **[!UICONTROL Flag Type:]** Ofensiva, desacuerdo, correo no deseado, etc.

   * Indicadores seguros: Correo no deseado y masivo.
   * Indicador aplicado por la red y la lista de profanidad del sitio: Profanidad.
   * Indicadores aplicados por SAFE: Odio de voz, PII (Información personal identificable), Insulto y Profanidad.
   * Indicadores de usuario: Correo no deseado, Desactivado, Ofensivo y Rechazar.

* **[!UICONTROL Flag origin:]** la fuente del indicador de la lista. Puede ser SAFE, un nombre de usuario o Livefyre.
* **[!UICONTROL More info:]** enumera los detalles del contenido, incluido el número de &quot;Me gusta&quot;, Indicadores de usuario, Respuestas y cualquier etiqueta aplicada al contenido. Al hacer clic en el sitio, se abre la página de nivel superior del sitio en el que se encuentra el contenido. Al hacer clic en la marca de tiempo, se abre una vista de subprocesos del contenido en contexto en la página.

## Opciones de filtro en modq {#section_r2c_qc2_yy}

Haga clic **[!UICONTROL Filter]** en la parte superior izquierda de la ventana modq para abrir un panel con opciones de filtro disponibles para el contenido de la lista. A medida que selecciona opciones, modq actualizará automáticamente para enumerar solo el contenido filtrado. Haga clic para **[!UICONTROL Clear filters]** borrar todas las opciones seleccionadas y volver a cargar la lista completa de elementos.

Hay distintas opciones de filtro disponibles para las fichas **[!UICONTROL Items]** y **[!UICONTROL Streams Premoderation]** las fichas.

Las siguientes opciones están disponibles para modq bajo **[!UICONTROL Items]** y **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**. Utilice el campo Buscar aplicaciones para filtrar los resultados por aplicación. Se pueden seleccionar varias aplicaciones.
* **[!UICONTROL System Flags]**. Filtre contenido por reglas como las reglas de correo no deseado, profanidad, SAFE y premoderación.

   * Al seleccionar **[!UICONTROL Spam]** , se enumerará todo el contenido etiquetado como Correo no deseado por SAFE.
   * Al seleccionar **[!UICONTROL Profanity]** , se enumerará todo el contenido etiquetado Profane por su red o su lista de profanidad del sitio.
   * Al seleccionar **[!UICONTROL SAFE]** , se enumerará todo el contenido que ingresa modq como resultado de sus reglas SAFE.
   * Si selecciona **[!UICONTROL Premoderation]** , se enumerará todo el contenido etiquetado para la premoderación por su red, flujo o configuración de la aplicación.

* **[!UICONTROL User Flags]** Filtre el contenido por indicadores de usuario. Las opciones son Ofensiva, Correo no deseado, Desactivado y Rechazar.
* **[!UICONTROL Rights Requests.]** Muestre solo el contenido con derechos concedidos haciendo clic en la casilla de verificación.
* **[!UICONTROL Entered the queue.]** Filtre el contenido por el intervalo de tiempo durante el cual se envió el contenido a modq. El contenido de hora se envía a modq no necesariamente el tiempo en el que se anunció el contenido en su aplicación.

Las siguientes opciones están disponibles para modq en **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** Filtre el contenido por la fuente social desde la que se originó el contenido. Por ejemplo, las opciones de las fuentes sociales incluyen Twitter, Instagram, Facebook y RSS.

La siguiente opción está disponible para modq en **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**. Filtre el contenido según la recomendación proporcionada por la recomendación de moderación automatizada.

Las siguientes imágenes muestran qué aspecto tienen las Recomendaciones de moderación en modq: ![](assets/mod_reco1.png)

La recomendación de moderación se proporciona para el contenido cuando se configura en **[!UICONTROL Network Settings > Moderation]** y **[!UICONTROL Network Settings > ModQ]**.

## Acciones que puede utilizar en modq {#section_h4g_wrn_z1b}

Puede decidir qué hacer con cada fragmento de contenido en modq.

Seleccione una de las siguientes opciones:

* **[!UICONTROL Checkbox]** Icono para aprobar el contenido
* **[!UICONTROL Trash can]** Icono para enviar el contenido a la papelera
* **[!UICONTROL Request Rights]** para solicitar los derechos al contenido del propietario del contenido.

   >[!NOTE]
   >
   >No puede solicitar derechos en modq para contenido de Instagram. Debe utilizar la biblioteca o el contenido de la aplicación para enviar solicitudes de derechos para contenido desde Instagram.

* **[!UICONTROL Feature and Approve]** para aprobar el contenido y también destacar el fragmento de contenido.
* **[!UICONTROL Product Tag and Approve]** para agregar un producto del catálogo de productos al contenido y aprobarlo.
* **[!UICONTROL Mark as Pending]** para marcar el contenido como pendiente.

>[!NOTE]
>
>Una vez que quite la papelera, el fragmento de contenido y todas las respuestas al contenido se eliminan de modq de forma permanente. Para colocar una parte trasera de contenido en una aplicación, consulte [Agregar un elemento traslúcido a una aplicación](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Si el contenido ya está en el estado deseado, si elige Papelera, Bozo o Aprobar, se confirmará el estado y se eliminará el elemento de la lista. Al moderar un fragmento de contenido, se eliminará inmediatamente de la cola y se desactivará en otras colas de moderadores.

>[!NOTE]
>
>El contenido del flujo puede no ser Bozo&#39;d. El contenido de flujo de procesamiento la eliminará del flujo de forma permanente y no se puede deshacer.

Una vez moderado el contenido, se eliminará del modq del moderador y su autor ya no podrá editarlo desde dentro del flujo. Si un moderador cierra un elemento o si un usuario elimina su comentario, aparecerá atenuado en otras colas de moderadores en tiempo real. Cuando el contenido se ha atenuado, el **[!UICONTROL Clear Moderated]** botón se muestra en la página, permitiendo a los moderadores quitarlo de sus listas y mantener su lugar en la página, independientemente de la otra actividad del moderador.

## Uso de la función Papelera en modq {#section_tpx_qgz_y1b}

Utilice la sección de configuración para seleccionar las opciones disponibles cuando el contenido se marca como Papelera.

* ****[!UICONTROL Confirm Trash]**** Active esta opción para exigir que Moderadores confirme su acción al configurar contenido en Papelera. Cuando está activada, la selección **[!UICONTROL Trash]** de contenido mostrará un cuadro de diálogo que solicita a **[!UICONTROL Reason for Moderation]** y ofrece un campo en el que se **[!UICONTROL Note]** puede introducir una.

   (Esta opción está disponible **[!UICONTROL only]** en el nivel de red y se aplicará a todos los sitios de la red).

* ****[!UICONTROL Hide Replies]**** Active esta opción para vaciar automáticamente las respuestas cuando un comentario principal se haya liberado o Bozo&#39;d.

## Cambiar estado de usuario en modq {#section_tmw_lg1_z1b}

Haga clic **[!UICONTROL User actions]** en el botón del panel Resumen del usuario para silenciar, prohibir o incluir al usuario en la lista de direcciones permitidas.

* **[!UICONTROL Mute:]** le permite silenciar indicadores del usuario que marcó la parte de contenido que aparece. Utilice esta opción para excluir los indicadores del usuario de los filtros de premoderación. El contenido que marque no entrará en modq como resultado del indicador y sus indicadores no se incluirán en Reglas de indicación.
* **[!UICONTROL Ban:]** permite prohibir al usuario de la lista desde su sitio o red. (Sólo los administradores de estudio o los responsables de usuario pueden llamar a un usuario.)
* **[!UICONTROL Whitelist:]** permite a la lista blanca incluir el sitio o la red en la lista de usuarios enumerados. (Sólo los administradores de estudios o los responsables de usuario pueden agrupar la lista de usuarios permitidos).



Aplicaciones que usan modq:

* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Críticas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Upload Button](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

