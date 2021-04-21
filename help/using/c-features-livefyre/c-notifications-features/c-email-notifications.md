---
description: Permita a los usuarios seleccionar su frecuencia y contenido de notificación.
title: Notificaciones de correo electrónico
exl-id: 46821382-ac93-4523-a0ac-84535e76d367
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Notificaciones de correo electrónico{#email-notifications}

Permita a los usuarios seleccionar su frecuencia y contenido de notificación.

**Habilite las notificaciones por correo electrónico para los usuarios y moderadores.**

Las aplicaciones de Livefyre permiten habilitar las notificaciones por correo electrónico para los usuarios y moderadores, en función de acciones específicas. Las notificaciones se basan en el momento en el que el contenido se publica en la emisión, lo que permite a los usuarios seguir participando en conversaciones que les interesen y recibir notificaciones cuando alguien les gusta o responde a uno de sus comentarios.

Los usuarios y moderadores pueden activar o desactivar la notificación por correo electrónico y pueden establecer la frecuencia con la que se reciben los correos electrónicos. En esta sección se describe cómo configurar y personalizar estas notificaciones por correo electrónico.

* Opciones de correo electrónico del usuario: opciones de notificación de usuario disponibles.
* Opciones de correo electrónico del moderador: opciones de notificación de moderador disponibles.
* Opciones de correo electrónico de identidad de Livefyre: correos electrónicos enviados como parte de la identidad de Livefyre. Estos correos electrónicos solo son relevantes para los clientes de identidad de Livefyre.
* Sincronización de datos con Livefyre: manteniendo la sincronización de preferencias con Livefyre.
* Personalización de correos electrónicos: personalizaciones de correo electrónico disponibles.

Utilice las opciones **Settings > Integration Settings > Email Notification Setup** para personalizar las notificaciones por correo electrónico de su red.

>[!NOTE]
>
>Para garantizar que los usuarios finales no reciban correo no deseado, no se envían notificaciones por correo electrónico desde el entorno de UAT de Livefyre.

**Opciones de correo electrónico del usuario**

Livefyre le permite permitir a los usuarios recibir notificaciones por correo electrónico de la actividad del sitio. Utilice la configuración de integración del perfil de usuario proporcionada por Livefyre para permitir a los usuarios seleccionar sus preferencias en las programaciones de notificaciones.

>[!NOTE]
>
>Los correos electrónicos solo se envían para el contenido publicado manualmente en el flujo y no para el contenido extraído de SocialSync.

Para permitir a los usuarios establecer sus preferencias de notificación, incluya una sección Notificación por correo electrónico en la Configuración de usuario del sistema de perfiles de usuario. Agregue los campos correspondientes al esquema de base de datos de perfiles de usuario y, a continuación, administre la configuración de usuario mediante Ping for Pull. (Póngase en contacto con el administrador de integración técnica para definir las frecuencias predeterminadas de la red. Si es cliente de perfiles empresariales, pase los valores predeterminados seleccionados a su equipo de envío de Livefyre para que los configure en la base de datos de Livefyre).

Los usuarios del sitio pueden seguir una conversación y comenzar a recibir notificaciones por correo electrónico haciendo clic en el botón **[!UICONTROL +Follow]** del editor de comentarios. Las preferencias de notificación se definen en el nivel de red de Livefyre. Cualquier configuración de usuario se aplicará a todos los sitios y conversaciones de la red.

**Valores predeterminados recomendados**

* Alguien comenta en una conversación que estoy siguiendo:** digest por hora**
* A alguien le gusta uno de mis comentarios:** digest por hora**
* Alguien responde a uno de mis comentarios:** inmediatamente**
* Seguir automáticamente las conversaciones cuando deje un comentario:** desactivado** (sin marcar)

**Nota**: Las notificaciones por correo electrónico se basan en el momento en que se aprueba la inclusión del contenido en el flujo.

Livefyre ofrece dos opciones de frecuencia de correo electrónico:

* Inmediatamente
* Resumen por hora

**Inmediatamente**

Los correos electrónicos enviados inmediatamente muestran el texto del anuncio, el título del artículo, el nombre de usuario del autor y un enlace **Reply** que lleva al usuario al contenido de la página. Estos correos electrónicos también incluyen un enlace **unsubscribe** en el pie de página, que permite a los usuarios cancelar la suscripción de las notificaciones por correo electrónico para esa colección. Al hacer clic en **cancelar suscripción **se les llevará a una página de confirmación que les informará de que se han dado de baja de la colección.

**Resumen por hora**

Los correos electrónicos enviados en un compendio por hora muestran todo el contenido, las respuestas al contenido y los &quot;Me gusta&quot; en el contenido en la última hora (o algo así) por aplicación que el usuario está siguiendo. Si el usuario está siguiendo varias aplicaciones en la red, recibirá un correo electrónico resumido para cada aplicación.

>[!NOTE]
>
>En conversaciones que no tengan contenido nuevo durante más de varias horas, los usuarios con el compendio por hora habilitado recibirán aviso inmediatamente después de una publicación de contenido nueva.

**Opciones de correo electrónico del moderador**

Los moderadores pueden aceptar recibir correos electrónicos para el contenido publicado en una aplicación que están siguiendo y, para los comentarios marcados como correo no deseado u ofensivo en una aplicación que están moderando. **Nota:** No se enviarán correos electrónicos cuando los usuarios marquen un comentario con Disconformidad o Fuera de tema, ya que estas categorías no se consideran importantes para la notificación del moderador.

Los campos moderator_comments y moderator_flag también deben agregarse al esquema de base de datos de la página de configuración del perfil de usuario del moderador para permitir que los moderadores actualicen la frecuencia de sus notificaciones por correo electrónico y excluyan si lo desean. Livefyre recomienda establecer estos dos campos de notificación de correo electrónico del moderador en **never**. Las opciones incluyen **never** (predeterminado), **inmediatamente** y **a menudo**.

**Correo electrónico del moderador (contenido marcado):**

Cuando el contenido está marcado en una aplicación moderada, el correo electrónico enviado al moderador mostrará el contenido marcado, el nombre de usuario que marcó el contenido y un vínculo de vuelta a la página de contenido.

Cuando un usuario cambia sus preferencias de notificación por correo electrónico en su sitio en el sistema de perfiles, sincronice la actualización con el sistema de perfiles remotos de Livefyre usando el ping de Livefyre para extracción.

**Sincronización de datos con Livefyre**

## Personalización de correos electrónicos {#section_jxb_c5k_yy}

Se pueden cambiar varios campos en las plantillas de notificación de correo electrónico para que se ajusten a su estilo y marca.

* **[!UICONTROL From Email Address]**

   La &quot;dirección de correo electrónico de&quot; para todas las notificaciones por correo electrónico se puede personalizar para que sea coherente con su marca. Livefyre recomienda **noreply@customerdomain.com**, reemplazar **dominio del cliente** por su nombre de dominio. (El valor predeterminado es **noreply@livefyre.com**). Pase su &quot;dirección de correo electrónico&quot; preferida a su Technical Integration Manager para configurarlo en la base de datos de Livefyre para su red.

   >[!NOTE]
   >
   >Deje este campo vacío para deshabilitar las notificaciones por correo electrónico para su red

* **[!UICONTROL Email Logo]**

   El logotipo mostrado en las notificaciones por correo electrónico se puede personalizar para que muestre el logotipo de su empresa, en lugar del logotipo predeterminado de Livefyre, mediante la pestaña Marcas de la página **Configuración de red** de Studio. Esta personalización solo está disponible a nivel de red, no a nivel de sitio, y solo está disponible para clientes de Livefyre de pago.

* **[!UICONTROL Custom Templates]**

   Si lo desea, puede implementar una plantilla de correo electrónico totalmente personalizada. Sin embargo, esto requerirá un esfuerzo de desarrollo y puede conllevar costos de servicios profesionales. Póngase en contacto con su administrador de cuentas para obtener más información.



Aplicaciones que usan esta función:

* [Carrusel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Tarjeta de características](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Muro de los medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Reseñas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
