---
description: Modere el contenido desde una sola interfaz inteligente.
seo-description: Modere el contenido desde una sola interfaz inteligente.
seo-title: Moderar contenido con ModQ
title: Moderar contenido con ModQ
uuid: c630fb85-7bd0-4da0-ac7e-080e970fb4f9
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---


# Moderar contenido usando ModQ{#moderate-content-using-modq}

Modere el contenido desde una sola interfaz inteligente.

ModQ crea una cola en tiempo real de todo el contenido de su sitio o red que coincide con las reglas de premoderación que ha definido, lo que permite que los moderadores se centren únicamente en el contenido que requiere su atención.

Una vez que haya definido la configuración de ModQ, se agregará a la cola el nuevo contenido que ingrese en el flujo o el contenido existente marcado por los usuarios. Los cambios realizados en las reglas no eliminarán contenido de ModQ, pero agregarán contenido nuevo a la cola según la nueva configuración.

ModQ le permite:

* Modere en contexto, vista subprocesos completos y apruebe, papelera o bozo, ya sea fragmentos individuales de contenido o subprocesos completos con un solo clic.
* Aumente la velocidad y eficacia del flujo de trabajo.
* Responda al contenido y aumente su participación en su comunidad.
* Permitir que varios moderadores trabajen a través del contenido, sin duplicar el trabajo de los demás.

El contenido de Livefyre se muestra en ModQ durante un máximo de 6 semanas y el contenido de flujos premoderado que no se ha abordado se enumera en ModQ durante 90 días.

>[!NOTE]
>
>Un solo fragmento de contenido se puede enumerar varias veces si coincide con varias reglas para su inclusión en ModQ. Por ejemplo, si un fragmento de contenido activa una regla de indicador de usuario para Offensive y luego activa otra regla para Profane, se enumerará en ModQ dos veces.

El contenido que no se muestra en ModQ incluye:

* Contenido con seguimiento.
* Contenido aprobado por un moderador.
* Contenido publicado por un usuario prohibido o marcas de usuario aplicadas por un usuario prohibido.

## Navegación de ModQ {#section_uv4_db2_yy}

ModQ se divide en dos paneles con fichas:

* **[!UICONTROL Items]** lista todo el contenido nativo de Livefyre y SocialSync programado para la moderación. Esta ficha incluye cualquier contenido de búsqueda social o flujo que se haya marcado o editado tras la moderación.
* **[!UICONTROL Streams Premoderation]** lista todo el contenido que entra en las aplicaciones desde flujos con Premoderado habilitado. (Para obtener más información, consulte Creación de flujos).

Ambas fichas oferta muchos de los mismos filtros y herramientas de moderación.

* **[!UICONTROL Item Count]** El número de elementos que quedan en la cola se muestra en la esquina superior izquierda de ModQ.
* **[!UICONTROL Filter]** Haga clic  **[!UICONTROL Filter]** para definir los parámetros según los cuales se enumerará el contenido en el panel.
* **[!UICONTROL History]** Haga clic en el  **[!UICONTROL History]** botón en la parte superior derecha de la pantalla para abrir una lista de contenido moderado recientemente, lo que le permitirá revisar su trabajo o cambiar una acción de moderación reciente. Vuelva a hacer clic en el botón para volver al contenido en cola. Solo se mostrarán las 100 acciones más recientes. **** Histórico no lista las acciones realizadas por otro moderador.

* **[!UICONTROL User Pane]** Haga clic en los botones para expandir o contraer situados en la parte superior derecha de la página para abrir o cerrar el panel Usuario.

## Explicación del contenido de ModQ {#section_oxm_kgz_y1b}

Cada parte de contenido de la lista muestra información de previsualización, incluido el sitio en el que se publicó y su autor. Al seleccionar un elemento se mostrará todo el contenido, incluidos los medios.

>[!NOTE]
>
>El contenido nativo de Livefyre mostrará más información que el contenido agregado a la aplicación mediante flujos u otras fuentes de medios sociales.

Al seleccionar un elemento, se muestra la siguiente información:

* **[!UICONTROL Time in Queue:]** lista la cantidad de tiempo que se agregó el contenido a ModQ.
* **[!UICONTROL App name:]** la aplicación en la que aparece el contenido. Vínculos al sitio con la aplicación.
* **[!UICONTROL Content Body:]** texto y miniaturas de medios, si están disponibles.
* **[!UICONTROL Status:]** el estado actual del contenido (pendiente, con seguimiento, etc.).
* **[!UICONTROL Author information:]** nombre y nombre de usuario del autor.
* **[!UICONTROL Timestamp:]** la marca de tiempo relativa del momento en que se creó el contenido. Permite vincular el contenido de la página Contenido de la aplicación de Studio.
* **[!UICONTROL Flag Type:]** Ofensiva, en desacuerdo, spam, etc.

   * Indicadores SAFE: Correo no deseado y masivo.
   * Indicador aplicado por la Lista de rentabilidad de la red y del sitio: Profanidad.
   * Indicadores aplicados por SAFE: Discurso de odio, PII (Información de Identificación Personal), Insulto y Profanidad.
   * Indicadores de usuario: Correo no deseado, fuera de tema, Ofensivo y Rechazo.

* **[!UICONTROL Flag origin:]** el origen del indicador de la lista. Puede ser SAFE, un nombre de usuario o Livefyre.
* **[!UICONTROL More info:]** Detalles de listas para el contenido, incluido el número de &quot;Me gusta&quot;, Marcas de usuario, Respuestas y cualquier etiqueta aplicada al contenido. Al hacer clic en el sitio se abre la página de nivel superior del sitio en el que se encuentra el contenido. Al hacer clic en la marca de tiempo, se abre una vista enlazada del contenido en contexto en la página.

## Opciones de filtro en ModQ {#section_r2c_qc2_yy}

Haga clic **[!UICONTROL Filter]** en la parte superior izquierda de la ventana de ModQ para abrir un panel con opciones de filtro disponibles para el contenido de la lista. A medida que seleccione las opciones, ModQ se actualizará automáticamente a la lista únicamente el contenido filtrado. Haga clic en **[!UICONTROL Clear filters]** para borrar todas las opciones seleccionadas y vuelva a cargar la lista completa de los elementos.

Hay diferentes opciones de filtro disponibles para las fichas **[!UICONTROL Items]** y **[!UICONTROL Streams Premoderation]**.

Las siguientes opciones están disponibles para ModQ en **[!UICONTROL Items]** y **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**. Utilice el campo Buscar aplicaciones para filtrar los resultados por aplicación. Se pueden seleccionar varias aplicaciones.
* **[!UICONTROL System Flags]**. Filtre el contenido por reglas como Correo no deseado, Profanidad, SAFE y Premoderación.

   * Al seleccionar **[!UICONTROL Spam]** se lista todo el contenido etiquetado como correo no deseado por SAFE.
   * Al seleccionar **[!UICONTROL Profanity]** se lista todo el contenido etiquetado con Prospecane por su Lista de Provocación de la red o del sitio.
   * Al seleccionar **[!UICONTROL SAFE]** se lista todo el contenido que ingrese a ModQ como resultado de las reglas de SAFE.
   * Al seleccionar **[!UICONTROL Premoderation]** se lista todo el contenido etiquetado para la premoderación por la configuración de red, flujo o aplicación.

* **[!UICONTROL User Flags]** Filtre el contenido por indicadores de usuario. Las opciones incluyen Offensive, Spam, Off-topic y Dispuestas.
* **[!UICONTROL Rights Requests.]** Para mostrar solo el contenido con derechos concedidos, haga clic en la casilla de verificación.
* **[!UICONTROL Entered the queue.]** Filtre el contenido según el intervalo de tiempo durante el cual se envió a ModQ. La hora en la que se envió el contenido a ModQ no es necesariamente la hora en la que se publicó en la aplicación.

Las siguientes opciones están disponibles para ModQ en **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** Filtre el contenido según la fuente social desde la que se originó el contenido. Por ejemplo, las opciones de fuentes sociales incluyen Twitter, Instagram, Facebook y RSS.

La siguiente opción está disponible para ModQ en **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**. Filtre el contenido según la recomendación proporcionada por la recomendación de moderación automatizada.

Las siguientes imágenes muestran el aspecto de Moderación de Recommendations en ModQ:  ![](assets/mod_reco1.png)

La recomendación de moderación se proporciona para el contenido cuando se configura en **[!UICONTROL Network Settings > Moderation]** y **[!UICONTROL Network Settings > ModQ]**.

## Acciones que puede utilizar en ModQ {#section_h4g_wrn_z1b}

Puede decidir qué hacer con cada fragmento de contenido en ModQ.

Seleccione una de las siguientes opciones:

* El icono **[!UICONTROL Checkbox]** para aprobar el contenido
* El icono **[!UICONTROL Trash can]** para enviar el contenido a la papelera
* **[!UICONTROL Request Rights]** para solicitar los derechos del propietario del contenido al contenido.

   >[!NOTE]
   >
   >No se pueden solicitar derechos en ModQ para el contenido desde Instagram. Debe usar la biblioteca o el contenido de la aplicación para enviar solicitudes de derechos de contenido desde Instagram.

* **[!UICONTROL Feature and Approve]** para aprobar el contenido y también presentar el contenido.
* **[!UICONTROL Product Tag and Approve]** para agregar un producto del catálogo de productos al contenido y luego aprobarlo.
* **[!UICONTROL Mark as Pending]** para marcar el contenido como pendiente.

>[!NOTE]
>
>Una vez que se deshace un fragmento de contenido, el fragmento de contenido y todas las respuestas al fragmento de contenido se eliminan de ModQ de forma permanente. Para colocar un fragmento de contenido en la papelera en una aplicación, consulte [Añadir un elemento en la papelera de nuevo en una aplicación](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Si el contenido ya se encuentra en el estado deseado, al elegir Papelera, Bozo o Aprobar se confirmará el estado y se eliminará el elemento de la lista. Moderar un fragmento de contenido lo eliminará inmediatamente de la cola y lo desactivará en las colas de otros moderadores.

>[!NOTE]
>
>Es posible que el contenido del flujo no sea Bozo&#39;d. El contenido del flujo de seguimiento lo eliminará del flujo de forma permanente y no se podrá deshacer.

Una vez moderado el contenido, se eliminará del ModQ del moderador y su autor ya no podrá editarlo desde el flujo. Si un moderador rechaza un elemento o si un usuario elimina su comentario, aparecerá atenuado en las colas de otros moderadores en tiempo real. Cuando el contenido se ha atenuado, el botón **[!UICONTROL Clear Moderated]** se muestra en la página, lo que permite a los moderadores eliminarlo de sus listas y mantener su lugar en la página independientemente de la actividad de otros moderadores.

## Uso de la función Papelera en ModQ {#section_tpx_qgz_y1b}

Utilice la sección de configuración para seleccionar las opciones disponibles cuando el contenido se marca como Con seguimiento.

* ****[!UICONTROL Confirm Trash]**** Active esta opción para requerir que los moderadores confirmen su acción al configurar el contenido en Papelera. Cuando se habilita, al seleccionar **[!UICONTROL Trash]** para el contenido se muestra un cuadro de diálogo en el que se solicita un **[!UICONTROL Reason for Moderation]** y se oferta un campo en el que se puede introducir un **[!UICONTROL Note]**.

   (Esta configuración está disponible **[!UICONTROL only]** a nivel de red y se aplicará a todos los sitios de la red).

* ****[!UICONTROL Hide Replies]**** Active esta opción para que las respuestas se descarguen automáticamente cuando un comentario principal se deseche o se borre Bozo’d.

## Cambiar el estado del usuario en ModQ {#section_tmw_lg1_z1b}

Haga clic en el botón **[!UICONTROL User actions]** del panel Resumen del usuario para silenciar, prohibir o permitir la lista del usuario.

* **[!UICONTROL Mute:]** le permite silenciar los indicadores del usuario que marcó el contenido de la lista. Utilice esta opción para excluir los indicadores del usuario de los filtros de premoderación. El contenido que marquen no entrará en ModQ como resultado del indicador y sus indicadores no se incluirán en las reglas de marca.
* **[!UICONTROL Ban:]** le permite prohibir el acceso del usuario de la lista a su sitio o red. (Solo los administradores de estudios o los administradores de usuarios pueden prohibir un usuario en la red).
* **[!UICONTROL Whitelist:]** le permite permitir-enumerar al usuario de su sitio o red. (Solo los administradores de estudios o los administradores de usuarios pueden permitir la lista de usuarios en red).



Aplicaciones que utilizan ModQ:

* [Conversación](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reseñas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Notas de identidad](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Upload Button](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

