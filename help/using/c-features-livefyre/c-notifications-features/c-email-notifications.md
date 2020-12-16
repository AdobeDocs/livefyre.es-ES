---
description: Permite a los usuarios seleccionar su frecuencia y contenido de notificación.
seo-description: Permite a los usuarios seleccionar su frecuencia y contenido de notificación.
seo-title: Notificaciones de correo electrónico
solution: Experience Manager
title: Notificaciones de correo electrónico
uuid: 27dad133-bd8d-4949-8146-1254c160d3af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 1%

---


# Notificaciones de correo electrónico{#email-notifications}

Permite a los usuarios seleccionar su frecuencia y contenido de notificación.

**Habilite las notificaciones por correo electrónico para los usuarios y moderadores.**

Las aplicaciones de Livefyre permiten activar las notificaciones por correo electrónico para los usuarios y moderadores, en función de acciones específicas. Las notificaciones se basan en el momento en el que el contenido se publica en el flujo, lo que permite a los usuarios seguir participando en conversaciones que les interesan y recibir notificaciones cuando alguien les gusta o responde a uno de sus comentarios.

Los usuarios y moderadores pueden adhesión o no recibir notificaciones por correo electrónico y pueden establecer la frecuencia con la que se reciben los mensajes. En esta sección se describe cómo configurar y personalizar estas notificaciones de correo electrónico.

* Opciones de correo electrónico del usuario: opciones de notificación del usuario disponibles.
* Opciones de correo electrónico del moderador: opciones de notificación del moderador disponibles.
* Opciones de correo electrónico de identidad de Livefyre: correos electrónicos enviados como parte de la Identidad de Livefyre. Estos correos electrónicos solo son relevantes para los clientes de identidad de Livefyre.
* Sincronización de datos con Livefyre: manteniendo la sincronización de preferencias con Livefyre.
* Personalización de correos electrónicos: personalizaciones de correo electrónico disponibles.

Utilice las opciones **Configuración > Configuración de integración > Configuración de notificación de correo electrónico** para personalizar las notificaciones de correo electrónico para la red.

>[!NOTE]
>
>Para asegurarse de que los usuarios finales no reciben correo no deseado, no se envían notificaciones por correo electrónico desde el entorno UAT de Livefyre.

**Opciones de correo electrónico del usuario**

Livefyre permite a los usuarios recibir notificaciones por correo electrónico de la actividad del sitio. Utilice la configuración de integración de Perfil de usuario proporcionada por Livefyre para permitir que los usuarios seleccionen sus preferencias para los programas de notificaciones.

>[!NOTE]
>
>Los mensajes de correo electrónico solo se envían para el contenido publicado manualmente en el flujo y no para el contenido extraído de SocialSync.

Para permitir que los usuarios definan sus preferencias de notificación, incluya una sección Notificación de correo electrónico en la Configuración de usuario del sistema de perfil de usuario. Añada los campos correspondientes al esquema de la base de datos de perfil de usuario y, a continuación, gestione la configuración de usuario con Ping for Pull. (Póngase en contacto con el administrador de integración técnica para definir las frecuencias predeterminadas de la red. Si es cliente de Perfiles empresariales, pase los valores predeterminados seleccionados a su equipo de envío de Livefyre para que los configure en la base de datos de Livefyre).

Los usuarios del sitio pueden seguir una conversación y empezar a recibir notificaciones por correo electrónico haciendo clic en el botón **[!UICONTROL +Follow]** del editor de comentarios. Las preferencias de notificación se definen en el nivel de red de Livefyre. Cualquier configuración de usuario se aplicará a todos los sitios y conversaciones de la red.

**Valores predeterminados recomendados**

* Alguien comenta en una conversación que estoy siguiendo:** compendio por hora**
* A alguien le gusta uno de mis comentarios:** digest por hora**
* Alguien responde a uno de mis comentarios:** inmediatamente**
* Conversaciones de seguimiento automático cuando dejo un comentario:** desactivado** (sin marcar)

**Nota**: Las notificaciones por correo electrónico se basan en la hora en que se aprueba la inclusión del contenido en el flujo.

Livefyre oferta dos opciones de frecuencia de correo electrónico:

* Inmediatamente
* Resumen por hora

**Inmediatamente**

Los correos electrónicos enviados inmediatamente muestran el texto de la publicación, el título del artículo, el nombre de usuario del autor y un vínculo **Responder** que lleva al usuario al contenido de la página. Estos mensajes de correo electrónico también incluyen un vínculo **cancelar suscripción** en el pie de página, que permite a los usuarios cancelar la suscripción de las notificaciones por correo electrónico para esa colección. Al hacer clic en **cancelar suscripción **se los llevará a una página de confirmación que les permitirá saber que se han cancelado las suscripciones a la colección.

**Resumen por hora**

Los correos electrónicos enviados en un compendio por hora muestran todo el contenido, las respuestas al contenido y los &quot;Me gusta&quot; del contenido en la última hora (o algo así) por aplicación que el usuario esté siguiendo. Si el usuario sigue varias aplicaciones en la red, recibirá un mensaje de correo electrónico de resumen por cada aplicación.

>[!NOTE]
>
>En conversaciones sin contenido nuevo durante más de varias horas, los usuarios con compendio por hora activado recibirán aviso inmediatamente después de una nueva publicación de contenido.

**Opciones de correo electrónico del moderador**

Los moderadores pueden adhesión para recibir correos electrónicos para el contenido publicado en una aplicación que están siguiendo, y para los comentarios marcados como Correo no deseado u Ofensivo en una aplicación que están moderando. **Nota:** No se enviará ningún correo electrónico cuando los usuarios marquen un comentario con Desacuerdo o Desactivado, ya que estas categorías no se consideran importantes para la notificación del moderador.

Los campos moderator_comments y moderator_flag también deben agregarse al esquema de la base de datos de la página de configuración del perfil del usuario del moderador para permitir que los moderadores actualicen la frecuencia de las notificaciones por correo electrónico y exclusión si lo desean. Livefyre recomienda establecer estos dos campos de notificación de correo electrónico del moderador en **never**. Las opciones incluyen **never** (predeterminado), **inmediatamente** y **a menudo**.

**Correo electrónico del moderador (contenido marcado):**

Cuando el contenido se marca en una aplicación moderada, el correo electrónico enviado al moderador muestra el contenido marcado, el nombre de usuario que marcó el contenido y un vínculo de regreso a la página de contenido.

Cuando un usuario cambia sus preferencias de notificación por correo electrónico en su sitio en el sistema de perfil, sincronice la actualización con el sistema de perfil remoto de Livefyre mediante el ping de Livefyre para extracción.

**Sincronización de datos con Livefyre**

## Personalización de correos electrónicos {#section_jxb_c5k_yy}

Se pueden cambiar varios campos de las plantillas de notificación de correo electrónico para que se ajusten a su estilo y marca.

* **[!UICONTROL From Email Address]**

   La &quot;dirección de correo electrónico del remitente&quot; de todas las notificaciones de correo electrónico puede personalizarse para que sea coherente con su marca. Livefyre recomienda **noreply@customerdomain.com** reemplazar **dominio del cliente** por su nombre de dominio. (El valor predeterminado es **noreply@livefyre.com**). Envíe su dirección de correo electrónico preferida a su Administrador de integración técnica para que la configure en la base de datos de Livefyre de su red.

   >[!NOTE]
   >
   >Deje este campo en blanco para desactivar las notificaciones por correo electrónico para su red

* **[!UICONTROL Email Logo]**

   El logotipo mostrado en las notificaciones por correo electrónico se puede personalizar para que muestre el logotipo de su compañía, en lugar del logotipo predeterminado de Livefyre, mediante la ficha Marcas de la página **Configuración de red** de Studio. Esta personalización solo está disponible a nivel de red, no a nivel de sitio, y solo está disponible para clientes de Livefyre de pago.

* **[!UICONTROL Custom Templates]**

   Si lo desea, puede implementar una plantilla de correo electrónico totalmente personalizada. Sin embargo, esto requerirá un esfuerzo de desarrollo y puede acarrear costos de servicios profesionales. Comuníquese con el administrador de cuentas para obtener más detalles.



Aplicaciones que utilizan esta función:

* [Carrusel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Tarjeta de función](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Muro de los medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Reseñas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

