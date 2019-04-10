---
description: Registre el extremo de URL para que Livefyre pueda utilizar la URL para
  extraer información de perfil actualizada.
seo-description: Registre el extremo de URL para que Livefyre pueda utilizar la URL
  para extraer información de perfil actualizada.
seo-title: Registrar el extremo con Studio
solution: Experience Manager
title: Registrar el extremo con Studio
uuid: 4 eb 816 ee-d 743-43 bf-bfee-d 9 b 9 fd 98 b 482
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Registrar el extremo con Studio{#register-the-endpoint-with-studio}

Registre el extremo de URL para que Livefyre pueda utilizar la URL para extraer información de perfil actualizada.

Registre el ping para la URL de extracción solo una vez por red. Una vez configurada, este valor no debe cambiar a menos que el punto final para recuperar los datos de perfil de usuario de los sistemas de administración de usuarios cambie.

1. Utilice Studio para registrar este punto final de URL con Livefyre.
1. Registre la URL desde la que Livefyre recuperará la información actualizada del perfil de usuario, vaya a **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**e introdúzcala en **[!UICONTROL Ping for Pull URL]** el campo.

   Por ejemplo, la dirección URL puede tener el aspecto siguiente: `https://example.yoursite.com/some_path/?id={id}`

