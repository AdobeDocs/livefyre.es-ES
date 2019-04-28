---
description: Genere la respuesta Ping for Pull para transmitir información de usuario actualizada a Livefyre.
seo-description: Genere la respuesta Ping for Pull para transmitir información de usuario actualizada a Livefyre.
seo-title: Generar ping para respuesta de extracción
solution: Experience Manager
title: Generar ping para respuesta de extracción
uuid: f 90871 d 5-601 f -40 dc-b 3 d 2-ab 78635 e 4 a 88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Generar ping para respuesta de extracción{#build-the-ping-for-pull-response}

Genere la respuesta Ping for Pull para transmitir información de usuario actualizada a Livefyre.

| Tipo | Propiedad | Descripción |
|--- |--- |--- |
| Cadena *requerida* | id | ID de usuario del usuario en el sistema de perfiles. Debe ser único en todos los usuarios de la red y nunca debe cambiar. |
| Cadena *requerida* | display_ name | Nombre para mostrar del usuario. Se procesará con el contenido de Livefyre publicado por el usuario. |
| Objeto *opcional, pero recomendado* | name | Cadenas para definir los nombres de los usuarios, primero, central y apellidos. |
| Cadena *opcional, pero recomendada* | correo electrónico | Dirección de correo electrónico del usuario. Se utiliza para enviar notificaciones por correo electrónico. |
| Cadena *opcional, pero recomendada* | image_ url | URL a un avatar que se mostrará al usuario. Livefyre escala las imágenes cargadas a 100 × 100, 75 × 75 o 50 × 50 píxeles, según sea necesario. Para obtener los mejores resultados, los usuarios deben cargar una imagen cuadrada a 100 × 100 píxeles. Para asegurarse de que la imagen avatar se actualiza en Livefyre, modifique la imagen_ url de cada actualización de imagen para que Ping para Extract detecte que se cambió la imagen. Por ejemplo, adjunte una marca de hora al nombre de archivo o aumente la imagen. Nota: Todas las direcciones URL deben ser completas y accesibles. |
| Cadena *opcional, pero recomendada* | profile_ url | URL a la página de perfil del usuario en su sitio. |
| Cadena *opcional, pero recomendada* | settings_ url | URL a una página donde los usuarios pueden configurar la configuración de perfil del usuario para el sitio. |
| Matriz *opcional, pero recomendada* | tags | Se utiliza para asignar usuarios a grupos de usuarios. Las etiquetas pueden incluir caracteres alfanuméricos y de guiones bajos 1-63. |
| Booleano *opcional, pero recomendado* | autofollow_ conversaciones | Define si un usuario desea seguir automáticamente una colección después de publicarla. Cuando se sigue una colección, los usuarios reciben notificaciones por correo electrónico cuando participan otros usuarios. Puede ser verdadero o falso. El valor predeterminado es true. |
| Objeto *opcional, pero recomendado* | email_ notifications | Define la frecuencia de las notificaciones de correo electrónico disponibles de Livefyre. Se pueden configurar distintas frecuencias para cada tipo de notificación. De forma predeterminada, no se enviarán notificaciones. <br><ul><li> emite inmediatamente notificaciones sobre el evento de la lista. </li><li>a menudo emite notificaciones en lotes. </li><li> nunca enviará notificación por correo electrónico de la actividad. </li><li>*comentarios*: Define cuándo se envían las notificaciones cuando otros usuarios publican contenido en colecciones que este usuario sigue. </li><li>*respuestas*: Define cuándo se envían las notificaciones cuando otro usuario responde al contenido de este usuario.</li><li>*&quot; Me gusta &quot;*: Define cuándo se envían las notificaciones cuando otro usuario le gusta el contenido de este usuario.</li><li>*moderator_ comments*: Define cuándo se envían las notificaciones a los moderadores cuando los usuarios publican contenido en cualquier colección de la red.</li><li>*moderator_ flags*: Define cuándo se envían las notificaciones a los moderadores cuando otros usuarios señalan el contenido de cualquier colección de la red.</li></ul> |
| Cadena *opcional* | ubicación | Una ubicación enviada por el usuario. |
| Cadena *opcional* | biografía | Autobiografía enviada por el usuario. |
| Matriz *opcional* | sitios web | Una matriz de sitios enviados por el usuario. Máx. = 2. |
| Objeto *opcional* | display_ rules | Define qué propiedades de perfil son visibles públicamente para otros usuarios. Cada parámetro disponible toma true o false Booleano. Parámetros disponibles: <br><ul><li>biografía </li><li> ubicación</li><li>  sexo </li><li>nameimage </li><li> remote_ profile_ url</li></ul> |
| Booleano *opcional* | moderador | Define si el usuario tiene privilegios de moderador en la red. |
| Booleano *opcional* | gravatar_ disabled | Define si se deshabilita el uso de un gravatar por parte de Livefyre si no se proporciona image_ url. |

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
