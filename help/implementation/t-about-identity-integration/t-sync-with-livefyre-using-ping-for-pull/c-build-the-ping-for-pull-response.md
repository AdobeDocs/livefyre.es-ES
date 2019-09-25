---
description: Cree la respuesta Ping for Pull para transmitir información actualizada del usuario a Livefyre.
seo-description: Cree la respuesta Ping for Pull para transmitir información actualizada del usuario a Livefyre.
seo-title: Generar el ping para la respuesta de extracción
solution: Experience Manager
title: Generar el ping para la respuesta de extracción
uuid: f90871d5-601f-40dc-b3d2-ab78635e4a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Generar el ping para la respuesta de extracción{#build-the-ping-for-pull-response}

Cree la respuesta Ping for Pull para transmitir información actualizada del usuario a Livefyre.

| Tipo | Propiedad | Descripción |
|--- |--- |--- |
| Cadena *requerida* | id | ID de usuario del usuario en el sistema de perfiles. Debe ser único en todos los usuarios de la red y nunca debe cambiar. |
| Cadena *requerida* | display_name | Nombre para mostrar del usuario. Esto se representará con el contenido de Livefyre publicado por el usuario. |
| Objeto *opcional, pero recomendado* | name | Cadenas para definir los nombres formateados, primero, medio y último del usuario. |
| Cadena *opcional, pero recomendada* | correo electrónico | Dirección de correo electrónico del usuario. Se utiliza para enviar notificaciones por correo electrónico. |
| Cadena *opcional, pero recomendada* | image_url | Dirección URL de un avatar para mostrar al usuario. Livefyre escala las imágenes cargadas a 100 × 100, 75 × 75 o 50 × 50 píxeles, según corresponda. Para obtener los mejores resultados, los usuarios deben cargar una imagen cuadrada de 100 x 100 píxeles. Para asegurarse de que la imagen del avatar se actualiza en Livefyre, modifique image_url para cada actualización de imagen, de modo que Ping para Pull detecte que se cambió la imagen. Por ejemplo, adjunte una marca de hora al nombre de archivo o incremente los cambios de imagen. Nota:  Todas las direcciones URL deben estar completas y ser accesibles. |
| Cadena *opcional, pero recomendada* | profile_url | Dirección URL de la página de perfil del usuario en el sitio. |
| Cadena *opcional, pero recomendada* | settings_url | Dirección URL de una página en la que los usuarios pueden configurar la configuración de perfil del usuario para el sitio. |
| Matriz *opcional, pero recomendada* | etiquetas | Se utiliza para asignar usuarios a grupos de usuarios. Las etiquetas pueden incluir entre 1 y 63 caracteres alfanuméricos y de subrayado. |
| Boolean *opcional, pero recomendado* | autofollow_conversaciones | Define si un usuario desea seguir automáticamente una colección después de publicarla. Al seguir una colección, los usuarios reciben notificaciones por correo electrónico cuando participan otros usuarios. Puede ser verdadero o falso. El valor predeterminado es true. |
| Objeto *opcional, pero recomendado* | email_notifications | Define la frecuencia de las notificaciones de correo electrónico de Livefyre disponibles. Se pueden establecer distintas frecuencias para cada tipo de notificación. De forma predeterminada, no se enviará ninguna notificación. <br><ul><li> emite notificaciones inmediatamente después del evento enumerado. </li><li>a menudo emite notificaciones por lotes. </li><li> nunca enviará una notificación por correo electrónico para la actividad. </li><li>*comentarios*: Define cuándo se envían notificaciones cuando otros usuarios publican contenido en colecciones que este usuario sigue. </li><li>*respuestas*: Define cuándo se envían las notificaciones cuando otro usuario responde al contenido de este usuario.</li><li>*Me gusta*: Define cuándo se envían notificaciones cuando a otro usuario le gusta el contenido de este usuario.</li><li>*moderator_comments*: Define cuándo se envían notificaciones a los moderadores cuando los usuarios publican contenido en cualquier colección de la red.</li><li>*moderator_flag*: Define cuándo se envían notificaciones a los moderadores cuando otros usuarios marcan contenido en cualquier colección de la red.</li></ul> |
| Cadena *opcional* | ubicación | Ubicación enviada por el usuario. |
| Cadena *opcional* | bio | Una autobiografía enviada por el usuario. |
| Matriz *opcional* | sitios web | Matriz de sitios enviados por el usuario. Máx. = 2. |
| Objeto *opcional* | display_rules | Define qué propiedades de perfil son visibles públicamente para otros usuarios. Cada parámetro disponible toma la entrada booleana true o false. Parámetros disponibles:  <br><ul><li>bio </li><li> ubicación</li><li>  sexo </li><li>nameimage </li><li> remote_profile_url</li></ul> |
| Booleano *opcional* | moderador | Define si el usuario tiene privilegios de moderador en toda la red. |
| Booleano *opcional* | gravatar_disabled | Define si se deshabilitará el uso de un gravatar por Livefyre si no se proporciona image_url. |

## Respuesta de ejemplo {#section_uxt_3dd_mz}

```
{
 "id": "1234567890",
 "display_name": "Bob Dole",
 "name": {
   "formatted": "Bob Joseph Dole",
   "first": "Bob",
   "middle": "Joseph",
   "last": "Dole"
 },
   "email": "bob@dole.com",
   "image_url": "https://dole.com/images/bob.jpg",
   "profile_url": "https://site.com/bobdole",
   "settings_url":"https://site.com/settings",
   "tags": ["bob", "dole"],
   "autofollow_conversations": "true",
   "email_notifications": {
      "comments": "never",
      "replies": "immediately",
      "likes": "often",
      "moderator_comments": "immediately",
      "moderator_flags": "immediately" 
 },
  "location": "Washington D.C., USA",
  "bio": "Bob Dole speaks in the third person",
  "websites": ["https://dole.com/blog/", "https://bobdolerocks.com"],
  "display_rules": {
      "bio": "false",
      "location": "false",
      "gender": "false",
      "name": "false",
      "image": "false",
      "remote_profile_url": "false"
  },
  "moderator": "true",
  "gravatar_disabled": "false"
}
```
