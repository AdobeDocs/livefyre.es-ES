---
title: Uso del filtro de propensión
description: Uso del filtro de propensión
exl-id: 6ea7d913-f562-42a5-a6ea-241aa4e1089a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Uso del filtro de propensión{#using-the-profanity-filter}

Todo el contenido publicado en una aplicación de Livefyre se comprueba por profanidad. Si una palabra incluida en la lista de profanidad se encuentra en el contenido o en el nombre para mostrar de un usuario, ese contenido se marcará como &quot;Profundidad&quot;, lo que le permitirá filtrarlo para Premoderación, Reglas, ModQ o búsquedas generales en Contenido de aplicación.

>[!NOTE]
>
>El contenido de los administradores y administradores de Studio no está sujeto a la comprobación de reglas de perfil y el contenido publicado por un moderador no estará marcado.

Livefyre proporciona una lista de profanidad predeterminada. Puede elegir aplicar esta lista a nivel de red, proporcionar su propia lista o utilizar un agregado de los dos. Los sitios individuales dentro de la red pueden heredar la Lista de profanidad de la red o utilizar una lista personalizada para que sea específica del sitio.

Para proporcionar su propia lista de profanidad personalizada como predeterminada de red, envíela a su gestor de cuentas de Livefyre.

## Habilitar el filtrado de profecías {#section_yqc_qsk_f1b}

Habilite y configure el filtro de profanidad tanto a nivel de red como de sitio. Deshabilite el filtro de profanidad a nivel de red para deshabilitar automáticamente el filtro de profanidad para todos los sitios que heredan de la red.

>[!NOTE]
>
>Se comprueba si todo el contenido que pasa por Livefyre es profano. Si se encuentra contenido que incluye palabras incluidas en la lista predeterminada de blasfemias SAFE o en la lista personalizada de profecía, se marca &quot;Profundidad&quot;. Para configurar Livefyre para que realice acciones automáticamente en estos elementos, active **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL ON]**.

## Habilitar el filtro de propensión para una red {#section_twd_ssk_f1b}

1. Seleccione **[!UICONTROL Network]** en el menú desplegable de red.
1. Ir a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Desplácese hacia abajo hasta **[!UICONTROL Profanity List]** y establezca **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL ON]**.

1. Utilice el campo **[!UICONTROL Update Network Profanity List]** para agregar palabras a la lista o haga clic en una palabra para eliminarla de la lista.

>[!NOTE]
>
>La edición de la Lista de profecía a nivel de red no afectará a ninguna Lista a nivel de sitio que ya esté en su lugar. Para asegurarse de que se realizan cambios desde la red al sitio, seleccione **[!UICONTROL Restore Network List]** para el sitio después de realizar los cambios.

## Habilitar el filtro de propensión para un sitio {#section_fld_wsk_f1b}

1. Seleccione el sitio en el menú desplegable de red.
1. Ir a **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Desplácese hacia abajo hasta **[!UICONTROL Profanity List]** y establezca **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL ON]**.

1. Elija una de las siguientes opciones:

   * Para heredar la Lista de profecías de la red (esto no es común), establezca **[!UICONTROL Use Site Profanity List]** en **[!UICONTROL OFF]**.

   * Para editar la Lista de perfiles específicamente para el sitio, establezca **[!UICONTROL Use Site Profanity List]** en **[!UICONTROL On]** para abrir el campo **[!UICONTROL Update Profanity List]**, donde puede editar la lista:

      * Para eliminar una palabra, haga clic en la palabra.
      * Para agregar una palabra, escriba la palabra en el cuadro **[!UICONTROL Add new word]** y pulse **[!UICONTROL Return]**.

      * Para ver si una palabra está incluida en la lista, escriba la palabra en el cuadro **[!UICONTROL Test profanity filter]**.
   * Para volver a importar la Lista de profecía de red y aplicarla al sitio, haga clic en **[!UICONTROL Restore Network List]**.
   * Para borrar todo el contenido de la lista y empezar desde cero, haga clic en **[!UICONTROL Clear List]**.


## Trabajo con contenido que contiene obscenidad {#section_epy_dtk_f1b}

Utilice la Lista de profecía para filtrar las búsquedas de contenido y crear reglas de premoderación para ModQ.

Para buscar contenido que contenga obscenidades, vaya a **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** y marque la casilla de verificación **[!UICONTROL Profanity]**. Se mostrará todo el contenido que haya sido capturado por el filtro de destreza para el sitio o la red seleccionados. Esta lista incluirá el contenido extraído en la aplicación mediante SocialSync y Streams.

Para crear reglas de premoderación, en Studio, seleccione **[!UICONTROL Settings > Network Settings > Moderation]**. Una vez habilitado el filtro de profanidad, aparecerá una nueva regla que le permitirá marcar o premoderar contenido que contenga profanidad. De forma predeterminada, esta regla habilita automáticamente **[!UICONTROL Premoderate]** para el contenido profano, que puede cambiarse a **[!UICONTROL Trash it]** o **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Si un solo fragmento de contenido está sujeto a varios tipos de reglas (como las reglas SAFE y Flag), se aplicará la más estricta. Por ejemplo: Si la regla de premoderación indica a Premoderar un fragmento de contenido, pero una regla SEGURA dice que lo convierta en papelera, se le enviará a la papelera.

## Ver y actualizar la lista de profecía de una red {#section_qdb_btk_f1b}

1. Ir a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Desplácese hacia abajo hasta la sección **[!UICONTROL Profanity List]**.
1. Configure **[!UICONTROL Enable Profanity Checking]** en **[!UICONTROL On]** para mostrar la Lista habilitada para su red (Livefyre predeterminado o la lista personalizada cargada) y edítela. Puede editar la lista de las siguientes maneras:
   * Para eliminar una palabra, haga clic en la palabra.
   * Para agregar una palabra, escriba la palabra en el cuadro **[!UICONTROL Add new word]** y pulse **[!UICONTROL Return]**.
   * Para ver si una palabra está incluida en la lista, escriba la palabra en el cuadro **[!UICONTROL Test profanity filter]**.

>[!NOTE]
>
>Solo los administradores y moderadores de Studio pueden editar listas de perfiles.
