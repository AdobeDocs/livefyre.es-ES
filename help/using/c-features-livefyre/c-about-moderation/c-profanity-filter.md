---
description: 'null'
seo-description: 'null'
seo-title: Uso del filtro de obscenidad
solution: Experience Manager
title: Uso del filtro de obscenidad
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Uso del filtro de obscenidad{#using-the-profanity-filter}

Todo el contenido publicado en una aplicación de Livefyre se comprueba en busca de blasfemias. Si una palabra incluida en la lista de palabras obscenas se encuentra en el contenido o en el nombre para mostrar de un usuario, ese contenido se marcará como "Profundidad", permitiéndole filtrar por Premoderación, Reglas, ModQ o búsquedas generales en Contenido de la aplicación.

>[!NOTE]
>
>El contenido de los administradores y administradores de estudios no está sujeto a la comprobación de reglas de lenguaje obsceno y el contenido publicado por un moderador no se marcará.

Livefyre proporciona una lista de blasfemias predeterminada. Puede optar por aplicar esta lista a nivel de red, proporcionar su propia lista o utilizar un agregado de los dos. Los sitios individuales dentro de la red pueden heredar la Lista de beneficios de la red o utilizar una lista personalizada para ser específica del sitio.

Para proporcionar su propia lista de profanidad personalizada como predeterminada de su red, envíela a su administrador de cuentas de Livefyre.

## Activación del filtro de rentabilidad {#section_yqc_qsk_f1b}

Habilite y configure el filtro de profanidad tanto a nivel de red como de sitio. Deshabilite el filtro de profanidad a nivel de red para deshabilitar automáticamente el filtro de profanidad para todos los sitios que heredan de la red.

>[!NOTE]
>
>Todo el contenido que pasa por Livefyre se comprueba en busca de blasfemias. Si se encuentra contenido que incluye palabras incluidas en la lista de profanidad de SAFE predeterminada o en la lista de profanidad personalizada, se marca como "Profanidad". Para configurar Livefyre para que realice acciones automáticamente en estos elementos, seleccione **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**.

## Habilitar el filtro de ganancias para una red {#section_twd_ssk_f1b}

1. Seleccione **[!UICONTROL Network]** en el menú desplegable de red.
1. Ir a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Desplácese hacia abajo hasta el **[!UICONTROL Profanity List]** y defina **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL ON]**.

1. Utilice el **[!UICONTROL Update Network Profanity List]** campo para agregar palabras a la lista o haga clic en una palabra para eliminarla de la lista.

>[!NOTE]
>
>La edición de la Lista de beneficios a nivel de red no afectará a ninguna Lista a nivel de sitio que ya esté en vigor. Para asegurarse de que los cambios de la red se realizan en el sitio, seleccione **[!UICONTROL Restore Network List]** para el sitio una vez realizados los cambios.

## Habilitar el filtro de ganancias para un sitio {#section_fld_wsk_f1b}

1. Seleccione el sitio en el menú desplegable de red.
1. Ir a **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Desplácese hacia abajo hasta el **[!UICONTROL Profanity List]** y defina **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL ON]**.

1. Elija una de las siguientes opciones:

   * Para heredar la Lista de beneficios de la red (esto no es común), establezca **[!UICONTROL Use Site Profanity List]** en **[!UICONTROL OFF]**.

   * Para editar la Lista de beneficios específica para el sitio, defina **[!UICONTROL Use Site Profanity List]** para **[!UICONTROL On]** abrir el **[!UICONTROL Update Profanity List]** campo, donde puede editar la lista:

      * Para eliminar una palabra, haga clic en ella.
      * Para agregar una palabra, escriba la palabra en el **[!UICONTROL Add new word]** cuadro y pulse **[!UICONTROL Return]**.

      * Para ver si una palabra está incluida en la lista, escriba la palabra en el **[!UICONTROL Test profanity filter]** cuadro.
   * Para volver a importar la Lista de beneficios de red y aplicarla al sitio, haga clic en **[!UICONTROL Restore Network List]**.
   * Para borrar todo el contenido de la lista y empezar desde cero, haga clic en **[!UICONTROL Clear List]**.


## Uso de contenido que contiene lenguaje obsceno {#section_epy_dtk_f1b}

Utilice la Lista de palabras clave para filtrar las búsquedas de contenido y crear reglas de premoderación para ModQ.

Para buscar contenido que contenga blasfemias, vaya a **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** y marque la **[!UICONTROL Profanity]** casilla. Se mostrará todo el contenido capturado por el filtro de ganancias para el sitio o la red seleccionada. Esta lista incluirá el contenido extraído en la aplicación mediante SocialSync y Streams.

Para crear reglas de premoderación, seleccione **[!UICONTROL Settings > Network Settings > Moderation]** en Estudio. Una vez activado el filtro de profanidad, aparecerá una nueva regla que le permitirá marcar o premoderar contenido que contenga profanidad. De forma predeterminada, esta regla habilita automáticamente **[!UICONTROL Premoderate]** el contenido profano, que puede cambiarse a **[!UICONTROL Trash it]** o **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Si un solo fragmento de contenido está sujeto a varios tipos de reglas (como las reglas SAFE y Flag), se aplicará la más estricta. Por ejemplo: Si la regla de premoderación indica que se debe premoderar un fragmento de contenido, pero una regla de seguridad indica que se debe truncarlo, se lo ocultará.

## Ver y actualizar la lista de beneficios para una red {#section_qdb_btk_f1b}

1. Ir a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Desplácese hacia abajo hasta la **[!UICONTROL Profanity List]** sección.
1. Configure **[!UICONTROL Enable Profanity Checking]** para mostrar **[!UICONTROL On]** la lista habilitada para su red (valor predeterminado de Livefyre o la lista personalizada cargada) y edítela. Puede editar la lista de las siguientes formas:
   * Para eliminar una palabra, haga clic en ella.
   * Para agregar una palabra, escriba la palabra en el **[!UICONTROL Add new word]** cuadro y pulse **[!UICONTROL Return]**.
   * Para ver si una palabra está incluida en la lista, escriba la palabra en el **[!UICONTROL Test profanity filter]** cuadro.

>[!NOTE]
>
>Solo los administradores y moderadores de Studio pueden editar listas de palabras clave.

