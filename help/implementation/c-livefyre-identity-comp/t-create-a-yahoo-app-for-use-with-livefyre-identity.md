---
description: Puede utilizar la identidad de Livefyre con Yahoo! para permitir a los usuarios utilizar su Yahoo! inicios de sesión para interactuar con Aplicaciones en el sitio.
seo-description: Puede utilizar la identidad de Livefyre con Yahoo! para permitir a los usuarios utilizar su Yahoo! inicios de sesión para interactuar con Aplicaciones en el sitio.
seo-title: Cree un Yahoo! Aplicación para su uso con identidad de Livefyre
solution: Experience Manager
title: Cree un Yahoo! Aplicación para su uso con identidad de Livefyre
uuid: 6863 cd 2 e-eb 0 d -465 b-b 706-88 ecaccf 41 bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Cree un Yahoo! Aplicación para su uso con identidad de Livefyre{#create-a-yahoo-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con Yahoo! para permitir a los usuarios utilizar su Yahoo! inicios de sesión para interactuar con Aplicaciones en el sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de Yahoo, Livefyre requiere la siguiente información de la aplicación Yahoo:

* ID de cliente (clave del consumidor)
* Secreto del cliente (Secreto del consumidor)

Para crear un Yahoo! para su uso con la identidad de Livefyre:

1. Vaya a [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)e inicie sesión en Yahoo! para crear una nueva o seleccionar una existente para utilizarla con la identidad de Livefyre.
1. Seleccione **[!UICONTROL Application Type: Web Application]**.
1. Ingresar **[!UICONTROL Callback Domain:]**`https://identity.livefyre.com`
1. Seleccione **[!UICONTROL API Permissions: Profiles (Social Directory)]** y **[!UICONTROL Read Public]**.

   Cuando se complete, la página Detalles de la aplicación de Yahoo mostrará el ID de cliente de la aplicación (Clave del consumidor) y el Secreto del cliente (Secreto del cliente) para su uso en la página Ajustes de integración de Studio.

   >[!NOTE]
   >
   >Si activa Yahoo! iniciar sesión sin crear Yahoo! y si deja los campos ID de cliente y Secreto del cliente en Studio en blanco, Livefyre usará openid para registrar a estos usuarios en sus aplicaciones de Livefyre. En este caso, oauth y la personalización personalizada no estarán disponibles.