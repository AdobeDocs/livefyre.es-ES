---
description: Permitir que los usuarios seleccionen su frecuencia de notificación y
  contenido.
seo-description: Permitir que los usuarios seleccionen su frecuencia de notificación
  y contenido.
seo-title: Notificaciones por correo electrónico
solution: Experience Manager
title: Notificaciones por correo electrónico
uuid: 27 dad 133-bd 8 d -4949-8146-1254 c 160 d 3 af
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Notificaciones por correo electrónico{#email-notifications}

Permitir que los usuarios seleccionen su frecuencia de notificación y contenido.

**Habilite las notificaciones por correo electrónico para los usuarios y moderadores.**

Las aplicaciones de Livefyre permiten habilitar las notificaciones por correo electrónico para los usuarios y moderadores, en función de acciones específicas. Las notificaciones se basan en la hora en la que se publica el contenido en el flujo, permitiendo que los usuarios sigan participando en conversaciones que les interesan y se les notifique cuando alguien le gusta o responde a uno de sus comentarios.

Los usuarios y moderadores pueden activar o desactivar la notificación por correo electrónico y pueden establecer la frecuencia con la que se reciben los correos electrónicos. En esta sección se describe cómo configurar y personalizar estas notificaciones por correo electrónico.

* Opciones de correo electrónico del usuario: opciones de notificación de usuario disponibles.
* Opciones de correo electrónico del moderador: opciones de notificación de moderador disponibles.
* Opciones de correo electrónico de identidad de Livefyre: correos electrónicos enviados como parte de la identidad de Livefyre. Estos correos electrónicos solo son relevantes para los clientes de identidad de Livefyre.
* Sincronización de datos con Livefyre: mantener sincronización con Livefyre.
* Personalización de correos electrónicos: personalizaciones de correo electrónico disponibles.

Use las opciones **Configuración > Configuración de integración > Configuración** de notificaciones por correo electrónico para personalizar las notificaciones por correo electrónico de su red.

>[!NOTE]
>
>Para garantizar que los usuarios finales no reciban correo no deseado, no se envían notificaciones por correo electrónico desde el entorno de UAT de Livefyre.

**Opciones de correo electrónico del usuario**

Livefyre permite permitir a los usuarios recibir notificaciones por correo electrónico de la actividad del sitio. Utilice la configuración de integración del perfil de usuario de Livefyre para permitir a los usuarios seleccionar sus preferencias de programaciones de notificaciones.

>[!NOTE]
>
>Los mensajes de correo electrónico se envían solamente para contenido publicado manualmente en el flujo y no para el contenido extraído de socialsync.

Para permitir que los usuarios establezcan sus preferencias de notificación, incluya una sección Notificación por correo electrónico en la Configuración del usuario para el sistema de perfiles de usuario. Agregue los campos correspondientes a su esquema de base de datos de perfil de usuario y, a continuación, administre la configuración de usuario utilizando Ping para Extraer. (Trabaje con el administrador de integración técnica para definir las frecuencias predeterminadas de la red. Si es cliente de perfiles Enterprise, pase el valor predeterminado seleccionado al equipo de entrega de Livefyre para su configuración en la base de datos de Livefyre).

Los usuarios del sitio pueden seguir una conversación y comenzar a recibir notificaciones por correo electrónico haciendo clic en **[!UICONTROL +Follow]** el botón del editor de comentarios. Las preferencias de notificación se definen en el nivel de red de Livefyre. Cualquier configuración de usuario se aplicará a todos los sitios y conversaciones de la red.

**Valores predeterminados recomendados**

* Alguien comenta en una conversación que estoy siguiendo: ** Compendio por hora**
* A alguien le gusta uno de mis comentarios: ** Compendio por hora**
* Alguien responde a uno de mis comentarios: ** inmediatamente**
* Seguir automáticamente conversaciones cuando se deje un comentario: ** off** (sin marcar)

**Nota**: Las notificaciones por correo electrónico se basan en la aprobación del contenido temporal para incluirlo en el flujo.

Livefyre ofrece dos opciones de frecuencia de correo electrónico:

* Inmediatamente
* Compendio por hora

**Inmediatamente**

Los correos electrónicos enviados inmediatamente muestran el texto del anuncio, el título del artículo, el nombre de usuario del autor y un **vínculo de respuesta** que lleva al usuario al contenido de la página. Estos correos electrónicos también incluyen un **vínculo de cancelación de suscripción** en el pie de página, lo que permite a los usuarios cancelar la suscripción a las notificaciones por correo electrónico de dicha colección. Al hacer clic** cancelar suscripción** se les dirigirá a una página de confirmación que les avisará de que se han cancelado la suscripción de la colección.

**Compendio por hora**

Los mensajes de correo electrónico enviados en un resumen por hora muestran todo el contenido, las respuestas al contenido y "Me gusta" en el contenido de la última hora (o so) por aplicación que el usuario sigue. Si el usuario sigue varias aplicaciones en la red, recibirá un correo electrónico de compendio por cada aplicación.

>[!NOTE]
>
>En conversaciones sin contenido nuevo durante más de varias horas, los usuarios con compendio por hora activado recibirán aviso inmediatamente sobre una nueva publicación de contenido.

**Opciones de correo electrónico del moderador**

Los moderadores pueden optar por recibir correos electrónicos para el contenido publicado en una aplicación que siguen, y para comentarios marcados como Correo no deseado o Ofensiva en una aplicación moderando. **Nota:** No se enviarán correos electrónicos cuando los usuarios marquen un comentario con Rechazar o Desactivar tema, ya que estas categorías no se consideran importantes para la notificación del moderador.

Los campos moderator_ comments y moderator_ indicadores deben agregarse también al esquema de la base de datos de la página de ajustes del perfil de moderador para permitir que los moderadores actualicen la frecuencia de sus notificaciones por correo electrónico y desactivar si desean. Livefyre recomienda que configure los dos campos de notificación de correo electrónico de moderador como **nunca**. Las opciones incluyen **nunca** (predeterminado) **, inmediatamente**y **con frecuencia**.

**Correo electrónico del moderador (contenido marcado):**

Cuando el contenido se marca en una aplicación moderada, el correo electrónico enviado al moderador mostrará el contenido marcado, el nombre de usuario que marcó el contenido y un vínculo de regreso a la página de contenido.

Cuando un usuario cambie las preferencias de notificación por correo electrónico del sitio en su sistema de perfiles, sincronice la actualización al sistema de perfiles remoto Livefyre utilizando el ping de Livefyre para Extraer.

**Sincronización de datos con Livefyre**

## Personalización de correos electrónicos {#section_jxb_c5k_yy}

Varios campos de las plantillas de notificación por correo electrónico pueden cambiarse para adaptarse a su estilo y marca.

* **[!UICONTROL From Email Address]**

   La «dirección de correo electrónico» de todas las notificaciones por correo electrónico puede personalizarse para ser coherente con su marca. Livefyre recomienda **noreply@customerdomain.com**, reemplazando **customerdomainwith**su nombre de dominio. (El valor predeterminado es **noreply@livefyre.com**.) Pase el «desde la dirección de correo electrónico» que prefiera al administrador de integración técnica para su configuración en la base de datos de Livefyre para su red.

   >[!NOTE]
   >
   >Deje este campo en blanco para deshabilitar las notificaciones por correo electrónico de la red

* **[!UICONTROL Email Logo]**

   El logotipo mostrado en las notificaciones por correo electrónico puede personalizarse para mostrar el logotipo de su empresa, en lugar del logotipo predeterminado de Livefyre, con la ficha Marca de **la** página Configuración de red de Studio. Esta personalización solo está disponible en el nivel de red, no en el nivel del sitio, y solo está disponible para los clientes de pago de Livefyre.

* **[!UICONTROL Custom Templates]**

   Si lo desea, puede implementar una plantilla de correo electrónico totalmente personalizada. Sin embargo, esto requiere cierto esfuerzo de desarrollo y podría incurrir en costos de servicios profesionales. Comuníquese con el administrador de cuentas para obtener más detalles.



Aplicaciones que utilizan esta función:

* [Carrusel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Tarjeta de función](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Muro de medios](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Críticas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

