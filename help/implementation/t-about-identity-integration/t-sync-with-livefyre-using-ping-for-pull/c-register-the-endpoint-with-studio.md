---
description: Registre el punto final de la URL para que Livefyre pueda usar la URL para extraer información de perfil actualizada.
title: Registro del extremo con Studio
exl-id: 2910a13a-ae88-41d7-ba7c-88d7a1dbe445
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Registre el extremo con Studio{#register-the-endpoint-with-studio}

Registre el punto final de la URL para que Livefyre pueda usar la URL para extraer información de perfil actualizada.

Registre el Ping para la URL de extracción solo una vez por red. Una vez establecido, este valor no debe cambiar a menos que cambie el punto final para recuperar datos de perfil de usuario del sistema de administración de usuarios.

1. Use Studio para registrar este extremo de URL con Livefyre.
1. Registre la dirección URL desde la que Livefyre recuperará la información actualizada del perfil de usuario, vaya a **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** e introdúzcala en el campo **[!UICONTROL Ping for Pull URL]**.

   Por ejemplo, la dirección URL puede tener el siguiente aspecto: `https://example.yoursite.com/some_path/?id={id}`
