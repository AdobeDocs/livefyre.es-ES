---
description: El motor de filtrado de contenido no deseado y abuso de Livefyre (SAFE) es un proceso en segundo plano que analiza todo el contenido entrante y está habilitado para todos los clientes de Livefyre.
title: Reglas SEGURAS
exl-id: 13cd8df0-c4b7-436e-ba07-64ec67321d6b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# Reglas SEFE{#safe-rules}

El motor de filtrado de contenido no deseado y abuso de Livefyre (SAFE) es un proceso en segundo plano que analiza todo el contenido entrante y está habilitado para todos los clientes de Livefyre.



SAFE usa reglas de patrones, así como modelos estadísticos para detectar spam, abuso, profanidad y anuncios masivos (repetitivos). Verá que de vez en cuando se hace referencia a él en otros productos de Livefyre, especialmente en las herramientas de moderación de Contenido y ModQ.

>[!NOTE]
>
>SAFE solo está en inglés, excepto para la clasificación de correo masivo. Si necesita soporte para otros idiomas, póngase en contacto con su administrador de cuentas estratégicas.

## Componentes de estudio que utilizan SAFE {#section_k34_4tx_vy}

Los indicadores aplicados por SAFE se pueden utilizar con los siguientes componentes de Studio:

* Reglas

   Puede definir reglas SAFE para marcar automáticamente el contenido y definir cómo se debe administrar el contenido marcado en **[!UICONTROL Network Settings]**.

   Por ejemplo, un sitio puede establecer una tolerancia muy baja para el lenguaje vulgar y definir reglas SAFE que establezcan que todo el contenido marcado como Profano sea Bozo’d. Otros sitios pueden definir reglas que establecen que el contenido del perfil se modere previamente antes de entrar en el flujo.

* ModQ

   Puede moderar el contenido marcado con reglas SAFE y otras reglas de premoderación (por ejemplo, SPAM, profanidad, etc.) en ModQ.

* Contenido de la aplicación en la biblioteca

   El contenido marcado por SAFE se muestra en el Contenido de la aplicación , en la pestaña **[!UICONTROL Library]** . Puede filtrar el contenido por indicadores para moderar el contenido.

## Opciones de filtro SEFE {#section_pg5_ttx_vy}

SAFE aplica los siguientes indicadores al contenido filtrado y puede utilizarse para crear reglas y moderar contenido desde Livefyre Studio.

* **[!UICONTROL Profanity List]**: Contenido de perfil, tal como se define en la lista de palabras clave inglesas, según el uso común.

   El filtro de profecía busca un lenguaje profano, basado en una lista de palabras probada. Si se detecta, el contenido se marca como Promedio.

   >[!NOTE]
   >
   >Livefyre también proporciona un segundo filtro de Lista de profanidad, que puede personalizar en los niveles de Sitio y Red. Las reglas creadas con la Lista de profecías tendrán prioridad sobre las reglas automatizadas que se deriven del filtro de PROBABILIDAD SEFE. Para obtener más información, consulte la sección Lista de perfiles de la documentación Configuración .

* **[!UICONTROL Mild Profanity]**: Las palabras y frases generalmente no son aceptables en conversaciones educadas, pero generalmente son aceptables en conversaciones casuales. Por lo general, estas palabras y frases están permitidas en la televisión de la red.
* **[!UICONTROL Strong Profanity]**: Lenguaje muy fuerte, como los improperios y frases no permitidos en la televisión de la red y usados con moderación en películas calificadas R y programas maduros de televisión por cable. Por lo general, estas palabras no se usan en conversaciones educadas o casuales y se dicen en una conversación descortés con la intención de dañar al oyente.
* **[!UICONTROL SPAM]**: Contenido no solicitado, generalmente comercial. Utiliza un modelo estadístico que se basa en una variedad de funciones (incluidos el contenido de los comentarios y las direcciones URL) para marcar un fragmento de contenido como SPAM. Puede ajustar los umbrales de spam para personalizar las tasas de etiquetado de SPAM para su red o sitio, mediante solicitud.
* **[!UICONTROL Mild Insult]**: El contenido insultante, tal como se define en la lista de palabras clave y patrones de frases.
* **[!UICONTROL Strong Insult]**: El contenido insultante, tal como se define en la lista de palabras clave y patrones de frases.
* **[!UICONTROL Hate Speech]**: Un insulto basado en la etnia o la religión, especialmente cuando la afiliación a un grupo destinatario es minoritaria o está protegida.
* **[!UICONTROL ALL CAPS]**: Texto presentado en mayúsculas (se lee gritando).
* **[!UICONTROL Mild Threat]**: Una amenaza o insulto que normalmente incluye algún tipo de blasfemia dirigida a otra persona. Esta opción marca las posibles amenazas con más frecuencia, pero también tiene una tasa de falsos positivos más alta que **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**: Una amenaza o insulto grave que mencione lesiones corporales procesables a una o más personas, a menudo con una gran profanidad. Esta opción marca las posibles amenazas con menor frecuencia, pero también tiene una tasa de falsos positivos menor que **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]**: Una imagen que puede tener desnudos. Esta opción marca la desnudez con menos frecuencia, pero también tiene una tasa de falsos positivos menor que **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]**: Una imagen que puede tener desnudos. Esta opción marca la desnudez con más frecuencia, pero también tiene una tasa de falsos positivos más alta que **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Información de identificación personal): Información que puede identificar al usuario. Esto puede incluir una dirección de correo electrónico, una dirección física, un número de la seguridad social (para clientes estadounidenses), un número de tarjeta de crédito, una contraseña o cualquier cosa que se pueda utilizar para cometer fraude o para obtener la identidad de alguien.
* **[!UICONTROL Livefyre Recommends Trash]**. Establezca la acción que realiza el sistema cuando la recomendación de moderación automatizada identifica el contenido que se debe rechazar.  ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Para activar Moderation Recommendations, póngase en contacto con su profesional de soporte técnico de Adobe Livefyre.

## Gestión de contenido no capturado por SAFE {#section_pjy_5tx_vy}

Hay varios medios disponibles para gestionar de forma eficaz el contenido que no captura este filtro. Las opciones siguientes se enumeran en el orden recomendado de proceso.

1. Como moderador, elimine el contenido de la emisión.
1. Cree una regla de marca que indique que si cinco usuarios marcan un contenido como correo no deseado u ofensivo, configúrelo en Bozo.
1. Prohibir al usuario que publica contenido no deseado, por lo que todo su contenido irá directamente al estado de Bozo.
1. Agregue palabras específicas que siempre deban filtrarse a su lista de profanidad.

>[!NOTE]
>
>Si un moderador publica contenido capturado por nuestro filtro de correo no deseado, sigue marcado como correo no deseado, pero se aprueba automáticamente, y no se establece en Bozo.

Si observa tendencias o patrones de contenido que SAFE no captura, envíe un correo electrónico a sus CSM con los ID de comentario y el texto.



Aplicaciones que usan esta función:

* [Carrusel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Conversación](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Tarjeta de características](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro de los medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Reseñas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Notas](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Upload Button](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
