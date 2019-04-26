---
description: Puede utilizar la identidad de Livefyre con Identidad de github para
  permitir a los usuarios utilizar sus inicios de sesión de github para interactuar
  con Aplicaciones en el sitio.
seo-description: Puede utilizar la identidad de Livefyre con Identidad de github para
  permitir a los usuarios utilizar sus inicios de sesión de github para interactuar
  con Aplicaciones en el sitio.
seo-title: Creación de una aplicación de identidad de github para su uso con la identidad
  de Livefyre
title: Creación de una aplicación de identidad de github para su uso con la identidad
  de Livefyre
uuid: cf 56164 c -1521-4 a 42-89 cb -39483764807 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creación de una aplicación de identidad de github para su uso con la identidad de Livefyre{#create-a-github-identity-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con Identidad de github para permitir a los usuarios utilizar sus inicios de sesión de github para interactuar con Aplicaciones en el sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de identidad de github, Livefyre requiere la siguiente información de identidad de github:

* ID de cliente (clave privada)
* Secreto del cliente (Contraseña)

Para crear una aplicación de identidad github para utilizarla con la identidad de Livefyre:

1. Cree o inicie sesión en una cuenta de github en [](https://github.com/settings/developers).
1. Registre una nueva o seleccione una existente para utilizarla con la identidad de Livefyre.
1. Introduzca toda la información del formulario. Escriba **[!UICONTROL Authorization callback URL]**el nombre de la red en lugar `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`de.

1. En **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, cambie **[!UICONTROL Enable GitHub Login]** a **[!UICONTROL On]**.

1. Introduzca el ID del cliente de github y el secreto del cliente de github.
1. Haga clic **[!UICONTROL Save Settings]**en.

Una vez completada, la página Detalles de la aplicación de la Identidad de github enumera el ID de cliente de la aplicación (Clave del consumidor) y el Secreto del cliente (Secreto del cliente) para su uso en la página Ajustes de integración de Studio.
