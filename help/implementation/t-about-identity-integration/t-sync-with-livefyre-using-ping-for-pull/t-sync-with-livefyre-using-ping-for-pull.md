---
description: Utilice Ping para Pull para mantener Livefyre sincronizada con su sistema de administración de usuarios.
seo-description: Utilice Ping para Pull para mantener Livefyre sincronizada con su sistema de administración de usuarios.
seo-title: Sincronizar con Livefyre usando Ping para extracción
solution: Experience Manager
title: Sincronizar con Livefyre usando Ping para extracción
uuid: 7b059064-1cca-46d7-8055-dfe59f493ac1
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---


# Sincronizar con Livefyre usando Ping para extracción{#sync-with-livefyre-using-ping-for-pull}

Utilice Ping para Pull para mantener Livefyre sincronizada con su sistema de administración de usuarios.

En general, ***Ping*** Livefyre siempre que un usuario de su sitio web o aplicación actualice su perfil (nombre para mostrar, avatar, etc.) y Livefyre ***Quita*** el perfil actualizado del usuario.

![](assets/Ping-for-Pull.png)

Ping para secuencia de extracción:

1. El cliente envía una solicitud de ping a Livefyre (incluido el usuario que se va a actualizar).
1. Livefyre confirma la recepción de Ping con HTTP 200/Success.
1. Livefyre procesa la solicitud de extracción.
1. Colas de Livefyre Solicitud de extracción.
1. Livefyre ejecuta la solicitud Pull en el extremo para capturar la información actualizada del usuario.
1. El cliente recibe la respuesta de extracción y la valida.
1. Livefyre actualiza los Perfiles remotos con la información de perfil externo incluida en el extremo de extracción.

Ping Livefyre cada vez que un usuario actualiza su información de perfil. Aunque el tiempo de finalización de Ping para Pull puede variar según la carga de red, actualizará la información del usuario entre 1 y 10 minutos. Los cambios de perfil actualizados se mostrarán primero en Livefyre Studio > Usuarios.

La información de Perfil actualizada aparecerá en sus aplicaciones de Livefyre después de dos eventos:

* Un usuario cierra la sesión y, a continuación, vuelve a iniciarla en la aplicación. Los valores de nombre para mostrar en userAuthToken tienen prioridad sobre Ping para las actualizaciones de Pull. Un usuario cerrará la sesión o iniciará sesión y actualizará el token para actualizar la sesión.

   Para generar nuevos userAuthTokens cuando se actualice la información de perfil, utilice el comando authDelegate de SSO para cerrar la sesión de su usuario y volver a iniciarla en segundo plano.

* Una actualización de arranque de la colección proporcionará la información actualizada (como máximo cada 5-10 minutos).

Para implementar Ping for Pull para el sistema de Perfil de usuarios:

1. [Genere el extremo](#t_build_the_pull_endpoint) de extracción.

   >[!NOTE]
   >
   >La biblioteca Livefyre incluye un método syncUser para mantener actualizados los perfiles de usuario. Si utiliza la biblioteca Livefyre, omita los dos pasos siguientes.

1. [Registre el extremo de extracción en Studio](#register_the_endpoint_with_studio).
1. [Construya el ping](#t_build_the_ping).
1. [Genere el ping para la respuesta] de extracción.(#reference_n3x_pzb_mz)
