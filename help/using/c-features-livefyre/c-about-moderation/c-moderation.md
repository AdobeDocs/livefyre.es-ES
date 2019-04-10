---
description: El motor de filtrado de correo no deseado y correo no deseado (SAFE)
  de Livefyre es un proceso en segundo plano que analiza todo el contenido entrante
  y está habilitado para todos los clientes de Livefyre.
seo-description: El motor de filtrado de correo no deseado y correo no deseado (SAFE)
  de Livefyre es un proceso en segundo plano que analiza todo el contenido entrante
  y está habilitado para todos los clientes de Livefyre.
seo-title: Reglas SEGURAS
title: Reglas SEGURAS
uuid: 2 f 91 d 0 d 4-dffe -4651-88 af -79 bbb 96 c 1 b 5 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Reglas SEGURAS{#safe-rules}

El motor de filtrado de correo no deseado y correo no deseado (SAFE) de Livefyre es un proceso en segundo plano que analiza todo el contenido entrante y está habilitado para todos los clientes de Livefyre.



SAFE utiliza reglas de patrón, así como modelos estadísticos para detectar contenido no deseado, abuso, profanidad y publicaciones masivas (repetitivas). Le referirá cada cierto tiempo en otros productos de Livefyre, especialmente las herramientas de moderación de contenido y modq.

>[!NOTE]
>
>SAFE solo está disponible en inglés, excepto en la clasificación de correo masivo. Si necesita asistencia para otros idiomas, comuníquese con el administrador de cuentas estratégicas.

## Componentes de Studio con SAFE {#section_k34_4tx_vy}

Los indicadores aplicados por SAFE pueden utilizarse con los siguientes componentes de Studio:

* Reglas

   Puede definir reglas SEGURAS para marcar el contenido de forma automática y definir cómo se debe gestionar el contenido marcado en **[!UICONTROL Network Settings]**la.

   Por ejemplo, un sitio puede establecer una tolerancia muy baja para Profanity y definir reglas SEGURAS que concuerden con todo el contenido marcado como Profane como Bozo'd. Otros sitios pueden definir reglas que definan el contenido Profane para que se modere previamente antes de entrar en el flujo.

* Modq

   Puede moderar contenido marcado por reglas SEGURAS y otras reglas de premoderación (por ejemplo, correo no deseado, profanidad, etc.) en modq.

* Contenido de la aplicación en la biblioteca

   El contenido marcado por SAFE aparece en el contenido de la aplicación en la **[!UICONTROL Library]** ficha. Puede filtrar el contenido por indicadores para moderar el contenido.

## Opciones de filtro SEGURO {#section_pg5_ttx_vy}

SAFE aplica los siguientes indicadores al contenido filtrado y se puede utilizar para crear reglas y moderar contenido desde Livefyre Studio.

* **[!UICONTROL Profanity List]**: Contenido profane, tal como se define en una lista de palabras clave en inglés, según uso común.

   El filtro de profanidad busca un lenguaje profane basado en una lista de palabras comprobada. Si se detecta, el contenido se marca como Profane.

   >[!NOTE]
   >
   >Livefyre también proporciona un segundo filtro de Lista de profanidad, que puede personalizar tanto en los niveles de sitio como de red. Las reglas creadas con la lista de profanidad tendrán prioridad sobre las reglas automatizadas que derivan del filtro Profanity SAFE. Para obtener más información, consulte la sección Lista de profanidad en la documentación de Configuración.

* **[!UICONTROL Mild Profanity]**: Las palabras y frases generalmente no se aceptan en conversaciones polites, pero son generalmente aceptables en conversaciones informales. Por lo general, estas palabras y frases se permiten en la televisión de red.
* **[!UICONTROL Strong Profanity]**: Lenguaje muy fuerte, como explorador y frases no permitidas en televisores de red, y se usa con moderación en películas con distinción de R y televisión cable madura. Generalmente estas palabras no se utilizan en una conversación polite o casual y se dicen en una conversación inpolita con una intención de dañar al oyente.
* **[!UICONTROL SPAM]**: Contenido no solicitado, generalmente comercial. Utiliza un modelo estadístico que se basa en una variedad de funciones (incluidas contenido de comentarios y URL) para marcar un fragmento de contenido como correo no deseado. Puede ajustar los umbrales de correo no deseado para personalizar las tasas de etiquetado NO DESEADO para su red o sitio, por solicitud.
* **[!UICONTROL Mild Insult]**: Insulting content, tal como se define en una lista de palabras clave y patrones de frases.
* **[!UICONTROL Strong Insult]**: Insulting content, tal como se define en una lista de palabras clave y patrones de frases.
* **[!UICONTROL Hate Speech]**: Un insulto basado en étnica o religión, especialmente cuando la afiliación de grupo objetivo está en una minoría o protegida.
* **[!UICONTROL ALL CAPS]**: Texto presentado en todas las mayúsculas (leído como chelín).
* **[!UICONTROL Mild Threat]**: Una amenaza o un insulto que normalmente incluye algún tipo de blasfemidad leve dirigida a otra persona. Esta opción marca las posibles amenazas con mayor frecuencia, pero también tiene una tasa de falsos positivos mayor que **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**: Una grave amenaza o insulto que mencione daños bodiosos procesables a una o más personas, con frecuencia con una fuerte profanidad. Esta opción marca las posibles amenazas con menor frecuencia, pero también tiene una tasa de falsos positivos menor que **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]**: Imagen que puede tener una moderación. Esta opción marca la desnudez con menor frecuencia, pero también tiene una tasa de falsos positivos inferior **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]**: Imagen que puede tener una moderación. Esta opción marca la desnudez con más frecuencia, pero también tiene una tasa de falsos positivos mayor que **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Información de identificación personal): Información que identifica al usuario. Puede incluir una dirección de correo electrónico, una dirección física, un número de seguridad social (para clientes de EE. UU.), un número de tarjeta de crédito, una contraseña o cualquier cosa que pueda utilizarse en fraude o para ganar la identidad de alguien.
* **[!UICONTROL Livefyre Recommends Trash]**. Establezca la acción que realiza el sistema cuando la Recomendación de moderación automática identifica el contenido para el rechazo. ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Para activar las recomendaciones de moderación, póngase en contacto con su profesional de asistencia técnica de Adobe Livefyre.

## Gestión de contenido no capturado por SAFE {#section_pjy_5tx_vy}

Existen varios medios disponibles para gestionar el contenido que no se detecta con este filtro. Las opciones siguientes se enumeran en el orden de procesamiento recomendado.

1. Como moderador, elimine el contenido del flujo.
1. Cree una regla de marca que indique si un fragmento de contenido está marcado como Correo no deseado o Ofensiva por cinco usuarios, configúrelo en Bozo.
1. Prohíba al usuario que publica contenido no deseado, por lo que todo su contenido entrará directamente en el estado Bozo.
1. Agregue palabras específicas que siempre deben filtrarse a la lista de profanidad.

>[!NOTE]
>
>Si un moderador publica contenido que el filtro de correo no deseado captura, sigue marcado como Correo no deseado, pero se aprueba automáticamente, y no se establecerá en Bozo.

Si observa tendencias o patrones de contenido no capturados por SAFE, envíe un correo electrónico con los ID de comentario y el texto.



Aplicaciones que utilizan esta función:

* [Carrusel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Tarjeta de función](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro de medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Críticas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Upload Button](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

