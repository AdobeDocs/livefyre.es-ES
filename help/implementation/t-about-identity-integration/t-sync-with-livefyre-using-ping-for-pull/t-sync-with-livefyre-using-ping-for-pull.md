---
description: Utilice Ping para extraer para mantener Livefyre en sincronización con
  su sistema de administración de usuarios.
seo-description: Utilice Ping para extraer para mantener Livefyre en sincronización
  con su sistema de administración de usuarios.
seo-title: Sincronizar con Livefyre usando Ping para extracción
solution: Experience Manager
title: Sincronizar con Livefyre usando Ping para extracción
uuid: 7 b 059064-1 cca -46 d 7-8055-dfe 59 f 493 ac 1
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Sincronizar con Livefyre usando Ping para extracción{#sync-with-livefyre-using-ping-for-pull}

Utilice Ping para extraer para mantener Livefyre en sincronización con su sistema de administración de usuarios.

En general ***, Ping*** Livefyre cada vez que un usuario de su sitio web/aplicación actualiza su perfil (nombre para mostrar, avatar, etc.) y Livefyre ***extrae*** el perfil actualizado del usuario.

![](assets/Ping-for-Pull.png)

Ping para secuencia de extracción:

1. El cliente envía una solicitud Ping a Livefyre (incluido el usuario que se va a actualizar).
1. Livefyre confirma la recepción de Ping con HTTP 200/Success.
1. Livefyre procesa la solicitud de extracción.
1. Solicitud de salida de Livefyre.
1. Livefyre ejecuta la solicitud de extracción al punto final para capturar información de usuario actualizada.
1. El cliente recibe la respuesta Extraer y se valida.
1. Livefyre actualiza perfiles remotos con la información de perfil externa incluida en el extremo de extracción.

Ping Livefyre siempre que un usuario actualice la información de su perfil. Mientras que Ping para el tiempo de finalización de extracción puede variar según la carga de la red, se actualizará la información de usuario entre 1 y 10 minutos. Los cambios de perfil actualizados se mostrarán primero en Livefyre Studio > Usuarios.

La información de perfil actualizada aparecerá en las aplicaciones de Livefyre después de dos eventos:

* Un usuario cierra sesión y luego vuelve a la aplicación. Los valores de nombre para mostrar en userauthtoken tienen prioridad sobre Ping para las actualizaciones de extracción. Si un usuario cierre la sesión o inicia sesión, se actualizará el token para actualizar la sesión.

   Para generar nuevos userauthtokens cuando se actualice la información de perfil, utilice SSO authdelegate para cerrar sesión de nuevo en segundo plano en segundo plano.

* Una actualización de bootstrap a la colección incluirá la información actualizada (a su vez cada 5-10 minutos).

Para implementar Ping para Extraer para el sistema Perfil de usuario:

1. [Cree el extremo de extracción](#t_build_the_pull_endpoint).

   >[!NOTE]
   >
   >La biblioteca de Livefyre incluye un método syncuser para mantener los perfiles de usuario actualizados. Omita los dos pasos siguientes si utiliza la biblioteca de Livefyre.

1. [Registre el extremo de extracción en Studio](#register_the_endpoint_with_studio).
1. [Genere el ping](#t_build_the_ping).
1. [Genere el ping para Respuesta de extracción].(# reference_ n 3 x_ pzb_ mz)
