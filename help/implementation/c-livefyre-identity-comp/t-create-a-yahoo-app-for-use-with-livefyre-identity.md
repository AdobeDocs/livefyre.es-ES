---
description: Puede utilizar la identidad de Livefyre con Yahoo! para permitir a los usuarios utilizar su Yahoo! inicios de sesión para interactuar con las aplicaciones del sitio.
title: Crear un Yahoo! Aplicación para usar con la identidad de Livefyre
exl-id: 6b4c6ea9-1cb0-4496-aabe-70811f464a3d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Crear un Yahoo! Aplicación para usar con la identidad de Livefyre{#create-a-yahoo-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con Yahoo! para permitir a los usuarios utilizar su Yahoo! inicios de sesión para interactuar con las aplicaciones del sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de Yahoo, Livefyre requiere la siguiente información de la aplicación Yahoo:

* ID de cliente (clave de consumidor)
* Secreto del cliente (Secreto del consumidor)

Para crear un aplicación para uso con la identidad de Livefyre:

1. Vaya a [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/) e inicie sesión en Yahoo! para crear una aplicación nueva o seleccionar una existente para usarla con la identidad de Livefyre.
1. Select **[!UICONTROL Application Type: Web Application]**.
1. Entrar **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. Seleccione **[!UICONTROL API Permissions: Profiles (Social Directory)]** y **[!UICONTROL Read Public]**.

   Cuando se complete, la página de detalles de la aplicación de Yahoo enumerará el ID de cliente (clave de consumidor) y el Secreto de cliente (secreto de consumidor) de la aplicación para su uso en la página Configuración de integración de Studio.

   >[!NOTE]
   >
   >Si habilita Yahoo! iniciar sesión sin crear un y si deja los campos Client ID y Client Secret en Studio en blanco, Livefyre utilizará OpenID para iniciar sesión en las aplicaciones de Livefyre. En este caso, OAuth y la personalización de marca no estarán disponibles.
