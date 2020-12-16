---
description: Puede utilizar la Identidad de Livefyre con Yahoo! para permitir que los usuarios utilicen su inicios de sesión para interactuar con las aplicaciones del sitio.
seo-description: Puede utilizar la Identidad de Livefyre con Yahoo! para permitir que los usuarios utilicen su inicios de sesión para interactuar con las aplicaciones del sitio.
seo-title: Crear un Yahoo! Aplicación para usar con la identidad de Livefyre
solution: Experience Manager
title: Crear un Yahoo! Aplicación para usar con la identidad de Livefyre
uuid: 6863cd2e-eb0d-465b-b706-88ecaccf41bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Crear un Yahoo! Aplicación para usar con la identidad de Livefyre{#create-a-yahoo-app-for-use-with-livefyre-identity}

Puede utilizar la Identidad de Livefyre con Yahoo! para permitir que los usuarios utilicen su inicios de sesión para interactuar con las aplicaciones del sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de Yahoo, Livefyre requiere la siguiente información de la aplicación para Yahoo:

* ID del cliente (Clave del cliente)
* Secreto del cliente (Secreto de cliente)

Para crear un aplicación para usar con Livefyre Identity:

1. Vaya a [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/) e inicie sesión en su para crear una aplicación nueva o seleccionar una existente para utilizarla con la identidad de Livefyre.
1. Select **[!UICONTROL Application Type: Web Application]**.
1. Entrar **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. Seleccione **[!UICONTROL API Permissions: Profiles (Social Directory)]** y **[!UICONTROL Read Public]**.

   Una vez completada, la página de detalles de la aplicación de Yahoo lista el ID de cliente (Clave del cliente) y el Secreto de cliente (Secreto de cliente) de la aplicación para utilizarlos en la página Ajustes de integración de Studio.

   >[!NOTE]
   >
   >Si habilita Yahoo! iniciar sesión sin crear un y si deja los campos ID de cliente y Secreto de cliente en Studio en blanco, Livefyre utilizará OpenID para registrar a estos usuarios en sus aplicaciones de Livefyre. OAuth y la marca personalizada no estarán disponibles en este caso.