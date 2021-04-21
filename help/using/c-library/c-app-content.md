---
description: Administración de contenido en la red de Livefyre.
title: Pestaña Contenido de la aplicación
exl-id: 8b3e5281-59ba-4321-8fee-4160ab7a5d5e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---

# Pestaña Contenido de la aplicación{#app-content-tab}

Administración de contenido en la red de Livefyre.

La ficha Contenido de la aplicación de la biblioteca le permite buscar y moderar contenido publicado en las aplicaciones. La pestaña **[!UICONTROL App Content]** permite varios filtros de búsqueda con la búsqueda comodín, para permitirle definir los parámetros de búsqueda de forma más rápida y sencilla.

Utilice la pestaña Contenido de la aplicación para:

* Buscar contenido
* Ver el historial de contenido
* Moderar contenido
* Agregar una etiqueta
* Contenido de la función
* Asociar contenido con productos del catálogo de productos

Para obtener más información sobre cómo moderar contenido mediante la ficha Contenido de la aplicación, consulte [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Búsqueda de comodín {#section_jvr_ntm_zz}

Los campos de búsqueda de Livefyre admiten caracteres comodín, que permiten agregar un asterisco ( * ) a las palabras (o fragmentos de palabras) para capturar coincidencias parciales.

Por ejemplo:

* bola devuelve sólo bola
* ball* devuelve bola y globo
* *la bola devuelve pelota y fútbol
* *bola* devuelve bola y uniball y snballed

## Buscar contenido {#section_fw1_mtm_zz}

El panel Contenido de la aplicación le permite limitar la búsqueda con varias opciones de filtrado de contenido diferentes.

![](assets/PublishedState-1024x367.png)

Utilice el menú desplegable **[!UICONTROL Quick Filters]** para reducir el contenido devuelto a los estados **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]** o **[!UICONTROL Rights Requests]**. A continuación, seleccione una opción **[!UICONTROL Filter by]** y utilice las casillas de verificación o los campos de entrada disponibles para restringir la búsqueda.

Utilice el menú desplegable para ordenar el contenido de la lista por **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** o **[!UICONTROL Most liked]**.

## Filtrar por opciones {#section_aqn_xqm_zz}

Utilice la barra **[!UICONTROL Filter by]** para filtrar por las siguientes opciones:

* **** EstadoLe permite filtrar por el estado de moderación actual del contenido:**  [!UICONTROL All Content]**,  **[!UICONTROL Approved]**,  **[!UICONTROL Pending]** o  **[!UICONTROL Bozo]**.

* **** FuenteLe permite filtrar por la fuente del contenido. Seleccione **[!UICONTROL Livefyre]** para enumerar el contenido generado por el usuario publicado directamente en el flujo. Seleccione **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** o **[!UICONTROL RSS]** para incluir contenido extraído de esas fuentes en sus aplicaciones.

* **** MarcasAl seleccionar los indicadores, puede filtrar por  **[!UICONTROL User Flags]** (Correo no deseado, Fuera del tema, Ofensivo o En desacuerdo),  **[!UICONTROL System Flags]** aplicado por SAFE (Correo no deseado, o Moderado mágicamente) o  **[!UICONTROL Moderation Recommendations]**.  ![](assets/appcontentfilter.png)

* **Fecha/** HoraPermite filtrar por el momento en que el contenido se introdujo originalmente  **[!UICONTROL Created]** (o se introdujo en la aplicación a través de SocialSync o un flujo), o por último  **[!UICONTROL Modified]** (editado, marcado o modificado).

* **** AutorLe permite filtrar por la  **[!UICONTROL IP]** dirección del autor,  **[!UICONTROL Display Name]** (que se encuentra en el panel Usuarios o desde encima del contenido publicado por el autor) o  **[!UICONTROL User ID]**(que se encuentra en el panel Usuarios).

* **** ContieneLe permite filtrar el contenido de los últimos 90 días por  **[!UICONTROL Keyword]** o  **[!UICONTROL Content Tag]**. Seleccione la casilla de verificación **[!UICONTROL Media]** para devolver solo contenido que contenga medios. (Para buscar todo el contenido, desplácese hacia abajo por todo el contenido de la lista y haga clic en **[!UICONTROL Search full data]**).

   **Nota:** No se admite la búsqueda de varias palabras clave y etiquetas de contenido. Si se introducen varias palabras clave o etiquetas, se utilizará la última palabra para la búsqueda.

   Al buscar por etiqueta de contenido, las etiquetas sugeridas se rellenarán automáticamente al escribir en el campo de búsqueda. Los resultados de búsqueda devolverán todo el contenido que se haya asignado a la etiqueta. (Utilice este campo para buscar contenido destacado o haga clic en la etiqueta **[!UICONTROL Featured]** de cualquier contenido destacado de Studio).

   **Nota:** Utilice un signo menos (-) antes del nombre de una etiqueta para buscar contenido que no incluya esa etiqueta. Por ejemplo: Busque &quot;-Miley&quot; para buscar todo el contenido que no incluya la etiqueta &quot;Miley&quot;.

* **** AplicaciónLe permite filtrar por  **[!UICONTROL Collection ID]**,  **[!UICONTROL App Tag]** o  **ID principal**. El filtrado por ID principal devuelve todo el contenido que es una respuesta al ID de contenido de entrada. (Filtre por varias etiquetas introduciendo etiquetas separadas por una coma).

* **** DerechosPermite filtrar por Estado de solicitudes de derechos:**  [!UICONTROL Requested]**,  **[!UICONTROL Granted]**,  **[!UICONTROL Replied]** o  **[!UICONTROL Expired]**.

## Contenido Bozo {#section_afl_vqm_zz}

En las aplicaciones, el contenido **[!UICONTROL Bozo]** solo se muestra al autor del contenido. Esto permite al usuario creer que su contenido se ha aprobado, ocultándolo al mismo tiempo a todos los demás usuarios y moderadores.

>[!NOTE]
>
>El contenido social que se origina con SocialSync o Streams **[!UICONTROL cannot]** se debe establecer en Bozo.

Puede usar contenido de Bozo por los siguientes motivos:

* El contenido identificado como correo no deseado por SAFE se establece automáticamente en el estado Bozo.
* Todo el contenido de los usuarios prohibidos se establece automáticamente en Bozo.
* El contenido puede marcarse como Bozo desde Studio.
* Los moderadores pueden ocultar contenido directamente en el flujo.

## Ver el historial de contenido {#section_ayz_tqm_zz}

El panel de contenido le permite revisar el historial de todo el contenido enumerado, incluida la moderación previa, el filtrado de contenido no deseado, la fecha de la publicación y cualquier indicador o nota de usuario asignada al elemento.

Utilice las pestañas de la parte inferior del panel de contenido para ver su historial.

* **[!UICONTROL More Info:]** enumera todas las actividades relacionadas con este contenido, incluidos el envío, la edición, la comprobación de correo no deseado, el cambio de estado y las notas. El ID de contenido de Livefyre y la dirección IP del usuario también se muestran en esta sección.
* **[!UICONTROL Replies:]** lista un máximo de 6 respuestas. Haga clic en **[!UICONTROL Show all replies]** para mostrar todas las respuestas a la publicación.

* **[!UICONTROL Flags & Reports:]** enumera todos los indicadores de usuario, con el avatar del usuario que marcó el contenido y cualquier informe (notas que agregó el usuario al marcar el contenido).
* **[!UICONTROL Add a note:]** le permite agregar una nota, visible para otros administradores o moderadores.
* **[!UICONTROL Request Rights:]** abre el  **[!UICONTROL New Rights Request]** cuadro de diálogo desde el que se puede emitir una solicitud de derechos.

* **[!UICONTROL Save as Asset:]**abre el cuadro de diálogo **[!UICONTROL Advanced Options]**, que permite guardar el elemento seleccionado en la biblioteca de recursos, publicarlo en una aplicación o solicitar derechos de reutilización a su autor.

![](assets/PublishedMoreInfo-1024x462.png)

## Agregar una etiqueta al contenido {#section_xb4_mxr_rdb}

El etiquetado de contenido le permite categorizar y organizar el contenido para facilitar la recuperación y la personalización de estilo, o marcar el contenido como destacado.

Para agregar etiquetas, simplemente haga clic en el icono de signo más ( **[!UICONTROL +]**) debajo del contenido. Introduzca una etiqueta nueva o seleccione una de una lista de etiquetas existentes.

![](assets/PublishedAddTag-1024x338.png)

## Búsqueda de imágenes en todos los recursos {#section_zxf_hsf_wcb}

Una vez añadido el contenido a la biblioteca, puede buscar el contenido mediante etiquetas inteligentes.

En la biblioteca, en Todos los recursos, puede buscar las imágenes existentes haciendo clic en **[!UICONTROL Show Filters]** y, a continuación:

* Introducción de texto para buscar en el campo de búsqueda
* Clasificación por relevancia
* Introduzca texto en el campo **[!UICONTROL Tags]** para buscar por Etiquetas inteligentes. El algoritmo de clasificación de etiquetas inteligentes filtra el contenido mediante una puntuación de confianza de etiquetas inteligentes, cuán nuevo es el contenido y cuántas estrellas ha dado un usuario al contenido.

## Contenido destacado {#section_emb_kqm_zz}

Seleccione la etiqueta predeterminada **[!UICONTROL Featured]** para marcar el contenido como destacado y resaltarlo como importante para los usuarios. Una vez etiquetados, utilice opciones de estilo personalizadas para personalizar el Contenido destacado en sus aplicaciones.

## Para Función o Desactivar Contenido {#section_ojx_3qm_zz}

* En Studio, haga clic en el signo **[!UICONTROL +]** situado junto a un fragmento de contenido, seleccione la etiqueta **[!UICONTROL Featured]** en la lista desplegable y haga clic en **[!UICONTROL Enter]** para mostrar el contenido de las funciones. La etiqueta se guarda y se muestra junto al contenido.

* Para anular la función, haga clic en **[!UICONTROL x]** en la etiqueta **[!UICONTROL Featured]** que se muestra en el contenido.

* Desde la aplicación Comentarios, Live Blog o Reseñas, pase el ratón sobre el contenido que desea mostrar y haga clic en **[!UICONTROL Feature]**. Para desactivar la función, simplemente pase el ratón sobre el contenido y haga clic en **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>Debido a limitaciones de espacio, el contenido de Chat solo se puede mostrar o dejar de publicar con Studio, y puede que no aparezca desde la propia aplicación.

## Edición del contenido destacado {#section_pyw_hqm_zz}

La mayoría de las acciones habituales sobre el contenido se pueden realizar en el contenido destacado, con la excepción de lo siguiente:

* El contenido destacado no se puede marcar.
* Los usuarios no pueden editar su contenido después de haberlo destacado, aunque sí pueden eliminarlo si lo desean. Los moderadores pueden editar el contenido destacado.
