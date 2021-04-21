---
description: Utilice Ping para Pull para mantener Livefyre sincronizado con su sistema de administración de usuarios.
title: Sincronizar con Livefyre usando Ping para extracción
exl-id: 01b5851d-9dc0-44dc-9c0d-0c467502450d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Sincronizar con Livefyre usando Ping para extracción{#sync-with-livefyre-using-ping-for-pull}

Utilice Ping para Pull para mantener Livefyre sincronizado con su sistema de administración de usuarios.

En general, ***Ping*** Livefyre siempre que un usuario del sitio web/aplicación actualiza su perfil (nombre para mostrar, avatar, etc.) y Livefyre ***Extrae*** el perfil actualizado del usuario.

![](assets/Ping-for-Pull.png)

Ping para la secuencia de extracción:

1. El cliente envía una solicitud de Ping a Livefyre (incluido el usuario que se va a actualizar).
1. Livefyre confirma la recepción de Ping con HTTP 200/Success.
1. Livefyre procesa la solicitud Pull.
1. Liefyre queue Solicitud de extracción.
1. Livefyre ejecuta la solicitud Pull en el punto final para capturar información actualizada del usuario.
1. El cliente recibe la respuesta Pull y valida.
1. Livefyre actualiza los perfiles remotos con la información de perfil externo incluida en el extremo de extracción.

Hacer ping a Livefyre cada vez que un usuario actualiza su información de perfil. Aunque el tiempo de finalización de Ping para Pull puede variar según la carga de red, actualizará la información del usuario entre 1 y 10 minutos. Los cambios de perfil actualizados se mostrarán primero en Livefyre Studio > Usuarios.

La información de perfil actualizada aparecerá en sus aplicaciones de Livefyre después de dos eventos:

* Un usuario cierra la sesión y luego vuelve a iniciarla en la aplicación. Los valores de nombre mostrados en userAuthToken tienen prioridad sobre Ping en las actualizaciones de Pull. El usuario cierra la sesión o inicia sesión y actualizará el token para actualizar la sesión.

   Para generar un nuevo userAuthTokens cuando se actualice la información del perfil, utilice el SSO authDelegate para cerrar la sesión del usuario y volver a iniciarla en segundo plano.

* Una actualización de arranque de la colección aportará la información actualizada (como máximo cada 5-10 minutos).

Para implementar Ping para extracción para su sistema de perfil de usuario:

1. [Genere el punto final de extracción](#t_build_the_pull_endpoint).

   >[!NOTE]
   >
   >La biblioteca Livefyre incluye un método syncUser para mantener sus perfiles de usuario actualizados. Omita los dos pasos siguientes si utiliza la biblioteca Livefyre.

1. [Registre el extremo de extracción en Studio](#register_the_endpoint_with_studio).
1. [Construya el Ping](#t_build_the_ping).
1. [Cree el ping para la respuesta de extracción].(#reference_n3x_pzb_mz)
