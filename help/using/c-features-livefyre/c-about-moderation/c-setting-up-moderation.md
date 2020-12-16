---
description: Utilice la ficha Moderación para establecer reglas de premoderación para el contenido entrante, incluidas listas de profanidad, reglas de marca y direcciones IP prohibidas.
seo-description: Utilice la ficha Moderación para establecer reglas de premoderación para el contenido entrante, incluidas listas de profanidad, reglas de marca y direcciones IP prohibidas.
seo-title: Configuración de la moderación
solution: Experience Manager
title: Configuración de la moderación
uuid: 0ec53fdb-08c2-4058-88cb-2f6f4b56a95b
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 0%

---


# Configuración de moderación{#setting-up-moderation}

Utilice la ficha Moderación para establecer reglas de premoderación para el contenido entrante, incluidas listas de profanidad, reglas de marca y direcciones IP prohibidas.

## Cómo funciona la moderación {#section_kyf_gvc_t1b}

Puede moderar el contenido de las siguientes formas:

* Premoderar contenido automáticamente para filtrar el contenido no deseado según las reglas que haya configurado antes de publicar el contenido.
* Elimine o apruebe manualmente el contenido marcado con la moderación previa automática mediante ModQ o Contenido de la aplicación en la biblioteca.
* Identifique los visitantes del sitio que publican contenido ofensivo repetidamente para evitar que se publiquen prohibiendo usuarios específicos de Livefyre, usuarios sociales o direcciones IP.
* Identifique a las personas y el contenido que siempre se pueden mostrar permitiendo enumerar usuarios o desactivando filtros para flujos, sitios o redes específicos.

El contenido se puede premoderar automáticamente de las siguientes maneras:

* Configure reglas para marcar automáticamente determinados tipos de contenido:

   * Configure las reglas de marca para el contenido marcado por el indicador de visitantes del sitio mediante **[!UICONTROL Settings > Moderation > Rules]**
   * Configure reglas SAFE mediante **[!UICONTROL Settings > Moderation > Rules]**
   * Prohibir usuarios específicos de Twitter mediante **[!UICONTROL Settings > Streams]**
   * Prohibir direcciones IP mediante **[!UICONTROL Settings > Bans]**
   * Prohibir regiones IP por código de país mediante solicitud. El contenido prohibido se marcará como SPAM.

* Cree una lista de palabras que considere profanas en la Lista de Profanidad en **[!UICONTROL Settings > Moderation > Rules]** para su red o sitio.
* Permitir la visualización de contenido de estos usuarios mediante la utilización o desactivación de filtros para flujos, sitios o redes específicos.

Después de configurar sus listas de blasfemias, filtros SAFE y reglas, puede elegir si premoderar el contenido y aplicar los filtros SAFE en los flujos. Para obtener más información, consulte [Opciones de regla de flujo para todas las reglas de flujo](/help/using/c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

Livefyre marca el contenido como **[!UICONTROL Approved]**, **[!UICONTROL Pending]**, **[!UICONTROL Junk]**, etc. en función de la procedencia del contenido, de dónde se publicará y de las reglas que haya configurado en el sistema. En la tabla siguiente se describen detalladamente las acciones que Livefyre realiza, en función de estos factores.

## Cómo funciona la moderación

| El Contenido Proviene De: | Envío de contenido a: | Estado de aprobación |
|--- |--- |--- |
| Biblioteca | Aplicación | Contenido aprobado |
| Búsqueda social | Aplicación | Contenido aprobado |
| Regla de flujo | Aplicación | ¿El contenido está marcado como no deseado por el filtro SAFE? <br><ul><li>No: flujo de trabajo de moderación de flujo a aplicación</li><li>Sí: contenido rastreado</li></ul> |
| Biblioteca | Carpeta | Sin estado (en la carpeta, sin publicar, sin eliminar) |
| Búsqueda social | Carpeta | Sin estado (en la carpeta, sin publicar, sin eliminar) |
| Regla de flujo | Carpeta | ¿El contenido está marcado como no deseado por el filtro SAFE? <br><ul><li>No: sin estado (en la carpeta, sin publicar, sin eliminar)</li><li>Sí: contenido rastreado</li></ul> |
| Publicación de aplicación | Aplicación | ¿El contenido está marcado como no deseado por el filtro SAFE? <br><ul><li>No: flujo de trabajo de moderación posterior a la aplicación</li><li>Sí: contenido rastreado</li></ul> |

## Flujo de trabajo de moderación de flujo a aplicación {#section_z5z_w4d_t1b}

![](assets/stream_to_app_workflow.png)

Antes de publicar el contenido de un flujo en una aplicación, Livefyre realiza las siguientes comprobaciones para determinar qué hacer con el contenido:

1. Si SAFE marca el contenido como basura o colocación, Livefyre lo estropea.
1. Si SAFE no marca el contenido como basura, Livefyre comprueba si la premoderación está activada.
1. Si la premoderación está activada, Livefyre marca el contenido como pendiente.
1. Si configura las reglas de ModQ, Livefyre envía el contenido a ModQ.
1. Si la premoderación no está activada, Livefyre comprueba si SAFE marcó el contenido.
1. Si SAFE marcó el contenido, Livefyre lo aprueba y lo publica en la aplicación.
1. Si SAFE marca el contenido y no configuró reglas SAFE, Livefyre aprueba el contenido y lo publica en la aplicación.
1. Si SAFE marca el contenido y configura reglas SAFE, Livefyre comprueba si ha configurado reglas SAFE para el flujo.
1. Si configura reglas SAFE para el flujo, Livefyre aprueba el contenido y lo publica en la aplicación. Si no configuró las reglas SAFE para el flujo, Livefyre utiliza las reglas de moderación SAFE para determinar cómo manejar el contenido (enviar a ModQ, papelera, etc.).

## Flujo de trabajo de moderación posterior a la aplicación {#section_fwn_w4d_t1b}

![](assets/post_to_app_workflow.png)

Antes de publicar en una aplicación el contenido de una publicación de la aplicación, Livefyre realiza las siguientes comprobaciones para determinar qué hacer con el contenido:

1. Si el filtro SAFE marca el contenido como desplegable, Livefyre descargará el contenido.
1. Si SAFE no marca el contenido como desplegable, Livefyre comprueba si la premoderación está activada. Si la premoderación está activada, Livefyre marca el contenido como pendiente. Si configura reglas de ModQ, Livefyre envía el contenido a ModQ como pendiente. De lo contrario, el contenido permanece en estado pendiente en Contenido de la aplicación en la biblioteca.
1. Si la premoderación no está activada, Livefyre comprueba si SAFE marcó el contenido. De lo contrario, Livefyre aprueba el contenido y lo publica en la aplicación.
1. Si SAFE marca el contenido y configura reglas SAFE, Livefyre utiliza la regla SAFE para determinar cómo manejar el contenido (enviar a ModQ, basura, etc.). Si SAFE marca el contenido y no configuró reglas SAFE, Livefyre aprueba el contenido y lo publica en la aplicación.

## Filtros masivos {#section_lyk_ktx_vy}

El filtro masivo busca contenido repetitivo publicado en todas las redes de Livefyre en un breve lapso de tiempo. Si se detecta, este contenido se marca como Masivo y, a continuación, se elimina de forma predeterminada. Mientras que el contenido masivo puede ser generado por el usuario (por ejemplo, &quot;Touchdown!&quot; publicado repetidamente en un Chat durante un popular partido de fútbol), la mayoría se origina en campañas de spam. Este filtro es independiente del idioma y funciona con cualquier idioma. Para personalizar el filtro masivo, debe ponerse en contacto con la asistencia de Livefyre.

## Reglas {#section_gqz_ksk_f1b}

Utilice la sección Reglas para crear reglas de moderación previa, basadas en indicadores SAFE y aplicados por el usuario. Este panel oferta dos tipos de reglas:

* **[!UICONTROL Flag Rules:]** especifique una acción que se debe realizar en un comentario marcado por los usuarios un número definido de veces.
* **[!UICONTROL SAFE Rules:]**combinar indicadores SAFE con acciones para realizar en el contenido marcado.

Para crear reglas de marca, seleccione el indicador (Ofensivo, Desactivado, Rechazar o Correo no deseado), introduzca el número de veces que debe aplicarse a un fragmento de contenido y seleccione la acción que desee realizar. Puede establecer una regla de marca para cada opción de indicador (Ofensivo, Desactivado, Rechazado o Correo no deseado).

Puede crear reglas en los niveles Red, Sitio y Flujo. Las reglas de nivel de sitio heredan reglas de red, a menos que configure las reglas de sitio de manera diferente. Las reglas de flujo heredan las reglas del sitio a menos que las configure de forma diferente.

Acciones disponibles:

* **[!UICONTROL Trash it:]**envía el comentario marcado a la papelera.
* **[!UICONTROL Bozo it:]** oculta el comentario marcado de todos los usuarios, excepto de su autor, a quienes permanece visible.
* **[!UICONTROL Pending:]** establece el contenido como pendiente. Si establece Premoderación en ON en **[!UICONTROL Settings > ModQ]**, entonces estará en ModQ. De lo contrario, solo estará en el contenido de la aplicación.

>[!NOTE]
>
>Livefyre recomienda crear reglas para los comentarios de Bozo que cinco usuarios marcan como correo no deseado u ofensivo.

## Moderación de Recommendations {#section_ec3_vr3_2cb}

Puede utilizar las recomendaciones de moderación para ayudarle a determinar cómo moderar el contenido publicado por los visitantes del sitio en las aplicaciones de Livefyre. El indicador de recomendación de moderación recomienda cuándo es probable que se elimine un fragmento de contenido, en función de las acciones realizadas anteriormente en contenido similar. Para usar Moderación de Recommendations:

1. Active la funcionalidad Moderación de Recommendations poniéndose en contacto con el profesional de soporte técnico de Adobe Livefyre.
1. Configure las recomendaciones de moderación en Configuración de red.

   Configure las recomendaciones de moderación usando la configuración **[!UICONTROL Livefyre Recommends Trash]** en **[!UICONTROL Network Settings]**.

   ![](assets/image_mod_reco_trash.png)

1. Configure una regla de SAFE para indicar a Livefyre qué hacer con el contenido que la recomendación de moderación identifica como contenido que es probable que se elimine. Para obtener más información sobre cómo configurar una regla SAFE para la opción **[!UICONTROL Livefyre Recommends Trash]**, consulte [Moderación](/help/using/c-features-livefyre/c-about-moderation/c-moderation.md#c_moderation).

   ![](assets/modreco4.png)

1. Use **[!UICONTROL Moderation Recommendation Indicator]** en ModQ o en Contenido de la aplicación para filtrar el contenido que la recomendación de moderación identifica como probable que se elimine.

   En ModQ, el indicador tiene este aspecto:  ![](assets/mod_reco1.png)

   Para obtener más información sobre cómo usar Moderación de Recommendations para moderar contenido en ModQ, consulte [ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md#c_modq).

   En Contenido de la aplicación, las recomendaciones de moderación tienen este aspecto:  ![](assets/modreco3.png)

   Para obtener más información sobre cómo usar Moderación de Recommendations en el contenido de la aplicación, consulte [Moderar contenido usando contenido de la aplicación](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).
