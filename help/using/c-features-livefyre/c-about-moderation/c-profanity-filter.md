---
description: 'null'
seo-description: 'null'
seo-title: Uso del filtro de profanidad
solution: Experience Manager
title: Uso del filtro de profanidad
uuid: b 0 b 1 fbae-c 88 c -403 c -9 b 91-df 6620675 f 39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Uso del filtro de profanidad{#using-the-profanity-filter}

Todo el contenido publicado en una aplicación de Livefyre está marcado como profanidad. Si una palabra incluida en la lista de profanidad se encuentra en el contenido o en el nombre para mostrar de un usuario, el contenido se marcará como «Profanity», lo que le permitirá filtrar para Premoderación, Reglas, modq o Búsquedas generales en el Contenido de la aplicación.

>[!NOTE]
>
>El contenido de los administradores y gestores de estudios no está sujeto a la comprobación de la regla de profanidad y el contenido publicado por un moderador no se señalizará.

Livefyre proporciona una lista de profanidad predeterminada. Puede elegir aplicar esta lista a nivel de red, proporcionar su propia lista o utilizar un agregado de ambos. Los sitios individuales de la red pueden heredar la lista de profanidad de la red o utilizar una lista personalizada para ser específica del sitio.

Para proporcionar su propia lista de profanidad personalizada como predeterminada de red, envíela al administrador de cuentas de Livefyre.

## Activación de filtros de profanidad {#section_yqc_qsk_f1b}

Habilite y configure el filtro de profanidad tanto en la red como en el sitio. Deshabilite el filtro de profanidad en el nivel de red para deshabilitar automáticamente el filtro de profanidad de todos los sitios que heredan de la red.

>[!NOTE]
>
>Todo el contenido que pasa por Livefyre está marcado como profanidad. Si se encuentra contenido que incluye palabras contenidas en la lista de profanidad SAFE predeterminada o en la lista de Profanity personalizada, se marcará como «Profanity. »» Para configurar Livefyre para que tome medidas automáticamente sobre estos elementos, vaya **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]** a.

## Habilitar el filtro de profanidad para una red {#section_twd_ssk_f1b}

1. Seleccione **[!UICONTROL Network]** en el menú desplegable de red.
1. Vaya **[!UICONTROL Settings > Network Settings > Moderation]** a.
1. Desplácese hacia abajo **[!UICONTROL Profanity List]** hasta **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]** llegar a.

1. Utilice **[!UICONTROL Update Network Profanity List]** el campo para agregar palabras a la lista o haga clic en una palabra para quitarla de la lista.

>[!NOTE]
>
>La edición de la lista de puntuaciones de nivel de red no afectará a las listas de nivel de sitio que ya estén en su sitio. Para asegurarse de que se realicen cambios de la red en el sitio, seleccione **[!UICONTROL Restore Network List]** para el sitio una vez realizados los cambios.

## Habilitar el filtro de profanidad para un sitio {#section_fld_wsk_f1b}

1. Seleccione el sitio en el menú desplegable de red.
1. Vaya **[!UICONTROL Settings > Site Settings > Moderation]** a.
1. Desplácese hasta el **[!UICONTROL Profanity List]** y defina **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL ON]**.

1. Elija una de las siguientes opciones:

   * Para heredar la Lista de profanidad de la red (esto no es común), defina **[!UICONTROL Use Site Profanity List]** en **[!UICONTROL OFF]**.

   * Para editar la lista de profanidad específicamente para el sitio, configure **[!UICONTROL Use Site Profanity List]** en **[!UICONTROL On]** para abrir **[!UICONTROL Update Profanity List]** el campo, donde puede editar la lista:

      * Para eliminar una palabra, haga clic en la palabra.
      * To add a word, type the word into the **[!UICONTROL Add new word]** box and hit **[!UICONTROL Return]**.

      * Para ver si una palabra se incluye en la lista, escriba la palabra en **[!UICONTROL Test profanity filter]** el cuadro.
   * Para volver a importar la lista de profanidad de red y aplicarla al sitio, haga clic **[!UICONTROL Restore Network List]** en.
   * Para borrar todo el contenido de la lista y empezar desde cero, haga clic **[!UICONTROL Clear List]** en.


## Trabajar con contenido que contiene profanidad {#section_epy_dtk_f1b}

Utilice la Lista de profanidad para filtrar las búsquedas de contenido y crear reglas de premoderación para modq.

Para buscar contenido que contenga profanidad, vaya a **[!UICONTROL Library > App Content]** la **[!UICONTROL Filter by Flags]** casilla de verificación y marque la **[!UICONTROL Profanity]** casilla. Se mostrará todo el contenido que haya capturado el filtro de profanidad para el sitio o la red seleccionada. Esta lista incluirá contenido extraído en la aplicación con socialsync y Flujos.

Para crear reglas de premoderación, seleccione Estudio **[!UICONTROL Settings > Network Settings > Moderation]**. Una vez habilitado el filtro de profanidad, aparecerá una nueva regla que le permitirá marcar o premoderar contenido que contenga profanidad. De forma predeterminada, esta regla habilita **[!UICONTROL Premoderate]** automáticamente el contenido profane, que puede cambiarse a **[!UICONTROL Trash it]** o **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Si un solo fragmento de contenido está sujeto a múltiples tipos de reglas (como las reglas SAFE y Flag), se aplicará más estricto. Por ejemplo: Si la regla de premoderación dice Premoderar un fragmento de contenido, pero una regla SAFE indica que desea Papelera, se borrará.

## Ver y actualizar la lista de profanidad de una red {#section_qdb_btk_f1b}

1. Vaya **[!UICONTROL Settings > Network Settings > Moderation]** a.
1. Desplácese hacia abajo hasta **[!UICONTROL Profanity List]** la sección.
1. Configúrelo para **[!UICONTROL Enable Profanity Checking]****[!UICONTROL On]** mostrar la lista habilitada para su red (predeterminada de Livefyre o la lista personalizada cargada) y edítela. Puede editar la lista de las siguientes maneras:
   * Para eliminar una palabra, haga clic en la palabra.
   * To add a word, type the word into the **[!UICONTROL Add new word]** box and hit **[!UICONTROL Return]**.
   * Para ver si una palabra se incluye en la lista, escriba la palabra en **[!UICONTROL Test profanity filter]** el cuadro.

>[!NOTE]
>
>Solo los administradores y moderadores de estudios pueden editar listas de profanidad.

