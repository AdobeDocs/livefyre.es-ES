---
description: Puede utilizar la Identidad de Livefyre con la Identidad de GitHub para permitir que los usuarios utilicen sus inicios de sesión de GitHub para interactuar con las Aplicaciones en su sitio.
seo-description: Puede utilizar la Identidad de Livefyre con la Identidad de GitHub para permitir que los usuarios utilicen sus inicios de sesión de GitHub para interactuar con las Aplicaciones en su sitio.
seo-title: Creación de una aplicación de identidad de GitHub para su uso con la identidad de Livefyre
title: Creación de una aplicación de identidad de GitHub para su uso con la identidad de Livefyre
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Crear una aplicación de identidad de GitHub para usar con la identidad de Livefyre{#create-a-github-identity-app-for-use-with-livefyre-identity}

Puede utilizar la Identidad de Livefyre con la Identidad de GitHub para permitir que los usuarios utilicen sus inicios de sesión de GitHub para interactuar con las Aplicaciones en su sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de identidad de GitHub, Livefyre requiere la siguiente información de identidad de GitHub:

* ID del cliente (clave privada)
* Secreto del cliente (contraseña)

Para crear una aplicación de identidad de GitHub para usar con la identidad de Livefyre:

1. Cree o inicie sesión en una cuenta de GitHub en [](https://github.com/settings/developers).
1. Registre una aplicación nueva o seleccione una existente para utilizarla con la identidad de Livefyre.
1. Introduzca toda la información del formulario. Escriba el **[!UICONTROL Authorization callback URL]**, utilizando su nombre de red en lugar de `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. En **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, cambie la **[!UICONTROL Enable GitHub Login]** a **[!UICONTROL On]**.

1. Introduzca el ID de cliente de GitHub y el secreto de cliente de GitHub.
1. Haga clic **[!UICONTROL Save Settings]**.

Una vez completada, la página de detalles de la aplicación de la identidad de GitHub lista el ID de cliente (Clave del cliente) y el secreto de cliente (Secreto de cliente) de la aplicación para utilizarlos en la página de configuración de integración de Studio.
