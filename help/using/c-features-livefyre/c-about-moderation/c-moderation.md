---
description: El motor de filtrado de correo no deseado y abuso de Livefyre (SAFE) es un proceso en segundo plano que analiza todo el contenido entrante y está habilitado para todos los clientes de Livefyre.
seo-description: El motor de filtrado de correo no deseado y abuso de Livefyre (SAFE) es un proceso en segundo plano que analiza todo el contenido entrante y está habilitado para todos los clientes de Livefyre.
seo-title: Reglas SEGURAS
title: Reglas SEGURAS
uuid: 2f91d0d4-dffe-4651-88af-79bbb96c1b5c
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 0%

---


# Reglas SAFE{#safe-rules}

El motor de filtrado de correo no deseado y abuso de Livefyre (SAFE) es un proceso en segundo plano que analiza todo el contenido entrante y está habilitado para todos los clientes de Livefyre.



SAFE usa reglas de patrones, así como modelos estadísticos para detectar spam, abuso, profanidad y anuncios masivos (repetitivos). Verá que de vez en cuando se hace referencia a ella en otros productos de Livefyre, especialmente en las herramientas de moderación de contenido y en ModQ.

>[!NOTE]
>
>SAFE solo está disponible en inglés, excepto para la clasificación de correo masivo. Si necesita asistencia para otros idiomas, póngase en contacto con el administrador de cuentas estratégicas.

## Componentes de estudio que utilizan SAFE {#section_k34_4tx_vy}

Los indicadores aplicados por SAFE se pueden utilizar con los siguientes componentes de Studio:

* Reglas

   Puede definir reglas SAFE para marcar automáticamente el contenido y definir cómo debe manejarse el contenido marcado en **[!UICONTROL Network Settings]**.

   Por ejemplo, un sitio puede establecer una tolerancia muy baja para la Profanidad y definir reglas SAFE que establezcan que todo el contenido marcado como Profane sea Bozo’d. Otros sitios pueden definir reglas que establecen que el contenido de Promedio se moderará previamente antes de entrar en el flujo.

* ModQ

   Puede moderar el contenido marcado por reglas SAFE y otras reglas de premoderación (por ejemplo, SPAM, profanidad, etc.) en ModQ.

* Contenido de la aplicación en la biblioteca

   El contenido marcado por SAFE aparece en la lista Contenido de la aplicación de la ficha **[!UICONTROL Library]**. Puede filtrar el contenido por indicadores para moderar el contenido.

## Opciones de filtro SAFE {#section_pg5_ttx_vy}

SAFE aplica los siguientes indicadores al contenido filtrado y puede utilizarse para crear reglas y moderar contenido desde Livefyre Studio.

* **[!UICONTROL Profanity List]**:: Contenido del perfil, según se define en una lista de palabras clave inglesas, según el uso común.

   El Filtro de lenguaje obsceno busca lenguaje vulgar, basado en una lista de palabras probada. Si se detecta, el contenido se marca como Promedio.

   >[!NOTE]
   >
   >Livefyre también proporciona un segundo filtro de Lista de la vulnerabilidad, que puede personalizar tanto en el nivel de sitio como en el de red. Las reglas creadas con la Lista Profanidad tendrán prioridad sobre las reglas automatizadas que se deriven del filtro PROBABILIDAD SEGURA. Para obtener más información, consulte la sección Lista de la rentabilidad en la documentación de Configuración.

* **[!UICONTROL Mild Profanity]**:: Las palabras y frases generalmente no son aceptables en conversaciones corteses, pero generalmente son aceptables en conversaciones casuales. Generalmente, estas palabras y frases están permitidas en la televisión de red.
* **[!UICONTROL Strong Profanity]**:: Lenguaje muy fuerte, como los improperios y frases no permitidos en la televisión en red y usados con moderación en películas clasificadas como R y programas maduros de televisión por cable. Por lo general, estas palabras no se utilizan en una conversación educada o casual y se dicen en una conversación descortés con la intención de dañar al oyente.
* **[!UICONTROL SPAM]**:: Contenido no solicitado, generalmente comercial. Utiliza un modelo estadístico que se basa en una variedad de funciones (incluyendo contenido de comentarios y direcciones URL) para marcar un fragmento de contenido como SPAM. Puede ajustar los umbrales de correo no deseado para personalizar las tasas de etiquetado de SPAM para su red o sitio, mediante solicitud.
* **[!UICONTROL Mild Insult]**:: Contenido insultante, tal como se define en una lista de palabras clave y patrones de frase.
* **[!UICONTROL Strong Insult]**:: Contenido insultante, tal como se define en una lista de palabras clave y patrones de frase.
* **[!UICONTROL Hate Speech]**:: Un insulto basado en la etnia o la religión, especialmente cuando la afiliación de grupo destinatario es minoritaria o está protegida.
* **[!UICONTROL ALL CAPS]**:: Texto presentado en todas las letras mayúsculas (se lee gritando).
* **[!UICONTROL Mild Threat]**:: Una amenaza o insulto que normalmente incluye algún tipo de blasfemia dirigida a otra persona. Esta opción marca las posibles amenazas con más frecuencia, pero también tiene una tasa de falsos positivos más alta que **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**:: Una amenaza o insulto grave que menciona daños corporales procesables a una o más personas, a menudo con una gran blasfemia. Esta opción marca las posibles amenazas con menor frecuencia, pero también tiene una tasa de falsos positivos menor que **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]**:: Imagen que puede tener desnudos. Esta opción marca la desnudez con menos frecuencia, pero también tiene una tasa de falsos positivos más baja que **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]**:: Imagen que puede tener desnudos. Esta opción marca la desnudez con más frecuencia, pero también tiene una tasa de falsos positivos más alta que **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Información de identificación personal): Información que puede identificar al usuario. Esto puede incluir una dirección de correo electrónico, una dirección física, un número de seguridad social (para clientes estadounidenses), un número de tarjeta de crédito, una contraseña o cualquier cosa que pueda utilizarse en fraude o para obtener la identidad de alguien.
* **[!UICONTROL Livefyre Recommends Trash]**. Configure la acción que realiza el sistema cuando la recomendación de moderación automatizada identifica el contenido que se debe rechazar.  ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Para activar Moderación de Recommendations, póngase en contacto con el profesional de soporte técnico de Adobe Livefyre.

## Administración de contenido no capturado por SAFE {#section_pjy_5tx_vy}

Existen varios medios disponibles para gestionar eficazmente el contenido no capturado por este filtro. Las opciones siguientes se enumeran en el orden de proceso recomendado.

1. Como moderador, elimine el contenido del flujo.
1. Cree una regla de marca que indique si cinco usuarios marcan un contenido como correo no deseado u ofensivo, configúrelo en Bozo.
1. Prohibir al usuario que publica contenido no deseado, de modo que todo su contenido irá directamente al estado de Bozo.
1. Añada palabras específicas que siempre deben filtrarse a su lista de blasfemias.

>[!NOTE]
>
>Si un moderador publica contenido capturado por nuestro filtro de correo no deseado, sigue marcado como correo no deseado, pero se aprueba automáticamente y no se establece en Bozo.

Si observa tendencias o patrones de contenido no capturados por SAFE, envíe un mensaje de correo electrónico a sus CSM con las ID de comentarios y el texto.



Aplicaciones que utilizan esta función:

* [Carrusel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Conversación](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Tarjeta de función](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro de los medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Reseñas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Notas de identidad](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Upload Button](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

