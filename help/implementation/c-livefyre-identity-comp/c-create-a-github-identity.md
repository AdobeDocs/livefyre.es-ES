---
description: Puede utilizar la identidad de Livefyre con la identidad de GitHub para permitir que los usuarios utilicen sus inicios de sesión de GitHub para interactuar con las aplicaciones de su sitio.
title: Creación de una aplicación de identidad de GitHub para su uso con la identidad de Livefyre
exl-id: f25ffd0e-ea4f-42ac-abfc-c02018421b85
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---

# Crear una aplicación de identidad de GitHub para usarla con la identidad de Livefyre{#create-a-github-identity-app-for-use-with-livefyre-identity}

Puede utilizar la identidad de Livefyre con la identidad de GitHub para permitir que los usuarios utilicen sus inicios de sesión de GitHub para interactuar con las aplicaciones de su sitio.

Para permitir que los usuarios inicien sesión con sus credenciales de identidad de GitHub, Livefyre requiere la siguiente información de identidad de GitHub:

* ID del cliente (clave privada)
* Secreto del cliente (contraseña)

Para crear una aplicación de identidad de GitHub para usarla con la identidad de Livefyre:

1. Cree o inicie sesión en una cuenta de GitHub en [](https://github.com/settings/developers).
1. Registre una aplicación nueva o seleccione una existente para utilizarla con la identidad de Livefyre.
1. Introduzca toda la información del formulario. Introduzca el **[!UICONTROL Authorization callback URL]**, utilizando su nombre de red en lugar de `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. En **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, cambie el **[!UICONTROL Enable GitHub Login]** a **[!UICONTROL On]**.

1. Introduzca el ID de cliente de GitHub y el secreto de cliente de GitHub.
1. Haga clic **[!UICONTROL Save Settings]**.

Cuando se complete, la página de detalles de la aplicación de identidad de GitHub enumerará el ID de cliente (clave de consumidor) y el Secreto de cliente (secreto de consumidor) de la aplicación para su uso en la página Configuración de integración de Studio.
