---
description: 'null'
seo-description: 'null'
seo-title: Uso del filtro de obscenidad
solution: Experience Manager
title: Uso del filtro de obscenidad
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 1%

---


# Uso del filtro de obscenidad{#using-the-profanity-filter}

Todo el contenido publicado en una aplicación de Livefyre se comprueba en busca de blasfemias. Si una palabra incluida en la lista de blasfemias se encuentra en el contenido o en el nombre para mostrar de un usuario, ese contenido se marcará como &quot;Profanidad&quot;, permitiéndole filtrar por Premoderación, Reglas, ModQ o búsquedas generales en Contenido de la aplicación.

>[!NOTE]
>
>El contenido de los administradores y administradores de estudios no está sujeto a la comprobación de reglas de lenguaje obsceno y el contenido publicado por un moderador no se marcará.

Livefyre proporciona una lista de blasfemias predeterminada. Puede optar por aplicar esta lista a nivel de red, proporcionar su propia lista o utilizar un acumulado de los dos. Los sitios individuales dentro de la red pueden heredar la Lista de la rentabilidad de la red o utilizar una lista personalizada para ser específica del sitio.

Para proporcionar su propia lista personalizada de blasfemia como predeterminada de la red, envíela a su administrador de cuentas de Livefyre.

## Activación del filtro de rentabilidad {#section_yqc_qsk_f1b}

Habilite y configure el filtro de obscenidad tanto a nivel de red como de sitio. Deshabilite el filtro de profanidad a nivel de red para deshabilitar automáticamente el filtro de profanidad para todos los sitios que heredan de la red.

>[!NOTE]
>
>Todo el contenido que pasa por Livefyre se comprueba en busca de blasfemias. Si se encuentra contenido que incluye palabras contenidas en la lista de blasfemia SAFE predeterminada o en la lista de blasfemias personalizada, se marca como &quot;Profanidad&quot;. Para configurar Livefyre para que realice acciones automáticamente en estos elementos, gire **[!UICONTROL Enable Profanity Checking]** a **[!UICONTROL ON]**.

## Habilitar el filtro de rentabilidad para una red {#section_twd_ssk_f1b}

1. Seleccione **[!UICONTROL Network]** en el menú desplegable de red.
1. Ir a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Desplácese hacia abajo hasta **[!UICONTROL Profanity List]** y establezca **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL ON]**.

1. Utilice el campo **[!UICONTROL Update Network Profanity List]** para agregar palabras a la lista o haga clic en una palabra para eliminarla de la lista.

>[!NOTE]
>
>La edición de la Lista de privacidad a nivel de red no afectará a ninguna Lista a nivel de sitio que ya esté en vigor. Para asegurarse de que se realizan cambios desde la red al sitio, seleccione **[!UICONTROL Restore Network List]** para el sitio después de que se hayan realizado los cambios.

## Habilitar el filtro de ganancias para un sitio {#section_fld_wsk_f1b}

1. Seleccione el sitio en el menú desplegable de red.
1. Ir a **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Desplácese hacia abajo hasta **[!UICONTROL Profanity List]** y establezca **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL ON]**.

1. Elija una de las siguientes opciones:

   * Para heredar la Lista Profanity de la red (esto no es común), establezca **[!UICONTROL Use Site Profanity List]** en **[!UICONTROL OFF]**.

   * Para editar la Lista de rentabilidad específicamente para el sitio, establezca **[!UICONTROL Use Site Profanity List]** en **[!UICONTROL On]** para abrir el campo **[!UICONTROL Update Profanity List]**, donde puede editar la lista:

      * Para eliminar una palabra, haga clic en ella.
      * Para agregar una palabra, escriba la palabra en el cuadro **[!UICONTROL Add new word]** y pulse **[!UICONTROL Return]**.

      * Para ver si una palabra está incluida en la lista, escriba la palabra en el cuadro **[!UICONTROL Test profanity filter]**.
   * Para volver a importar la Lista de la rentabilidad de la red y aplicarla al sitio, haga clic en **[!UICONTROL Restore Network List]**.
   * Para borrar todo el contenido de la lista y el inicio desde cero, haga clic en **[!UICONTROL Clear List]**.


## Uso de contenido que contiene lenguaje obsceno {#section_epy_dtk_f1b}

Utilice la Lista de grosor para filtrar las búsquedas de contenido y crear reglas de premoderación para ModQ.

Para buscar contenido que contenga blasfemias, vaya a **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** y marque la casilla **[!UICONTROL Profanity]**. Se mostrará todo el contenido capturado por el filtro de ganancias para el sitio o la red seleccionada. Esta lista incluirá el contenido extraído en la aplicación mediante SocialSync y Streams.

Para crear reglas de premoderación, seleccione **[!UICONTROL Settings > Network Settings > Moderation]** en Estudio. Una vez activado el filtro de obscenidad, aparecerá una nueva regla que le permitirá marcar o premoderar contenido que contenga obscenidades. De forma predeterminada, esta regla habilita automáticamente **[!UICONTROL Premoderate]** para el contenido profano, que puede cambiarse a **[!UICONTROL Trash it]** o **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Si un solo fragmento de contenido está sujeto a varios tipos de reglas (como las reglas SAFE y Flag), se aplicará la más estricta. Por ejemplo: Si la regla de premoderación indica que se debe premoderar un fragmento de contenido, pero una regla de seguridad indica que se debe truncarlo, se lo ocultará.

## Vista y actualización de la Lista de rentabilidad para una red {#section_qdb_btk_f1b}

1. Ir a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Desplácese hacia abajo hasta la sección **[!UICONTROL Profanity List]**.
1. Establezca **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL On]** para mostrar la Lista habilitada para la red (valor predeterminado de Livefyre o la lista personalizada cargada) y editarla. Puede editar la lista de las siguientes formas:
   * Para eliminar una palabra, haga clic en ella.
   * Para agregar una palabra, escriba la palabra en el cuadro **[!UICONTROL Add new word]** y pulse **[!UICONTROL Return]**.
   * Para ver si una palabra está incluida en la lista, escriba la palabra en el cuadro **[!UICONTROL Test profanity filter]**.

>[!NOTE]
>
>Solo los administradores y moderadores de Studio pueden editar Listas de privacidad.

