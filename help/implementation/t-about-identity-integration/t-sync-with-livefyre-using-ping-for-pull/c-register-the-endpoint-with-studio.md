---
description: Registre el punto final de la URL para que Livefyre pueda usar la URL para extraer la información actualizada del perfil.
seo-description: Registre el punto final de la URL para que Livefyre pueda usar la URL para extraer la información actualizada del perfil.
seo-title: Registro del extremo con Studio
solution: Experience Manager
title: Registro del extremo con Studio
uuid: 4eb816ee-d743-43bf-bfee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Registro del extremo con Studio{#register-the-endpoint-with-studio}

Registre el punto final de la URL para que Livefyre pueda usar la URL para extraer la información actualizada del perfil.

Registre la URL de Ping para extracción solo una vez por red. Una vez establecido, este valor no debe cambiar a menos que cambie el punto final para recuperar datos de perfil de usuario del sistema de administración de usuarios.

1. Utilice Studio para registrar este extremo de URL en Livefyre.
1. Registre la dirección URL desde la cual Livefyre recuperará la información de perfil de usuario actualizada, vaya a **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** e introdúzcala en el **[!UICONTROL Ping for Pull URL]** campo.

   Por ejemplo: la dirección URL puede tener el siguiente aspecto: `https://example.yoursite.com/some_path/?id={id}`

