---
description: Creación de aplicaciones de Android con tecnología de Livefyre.
title: Android SDK
exl-id: 54ea6537-5f27-4174-af25-d17257f23e48
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# Android SDK{#android-sdk}

Creación de aplicaciones de Android con tecnología de Livefyre.

Utilice esta biblioteca para integrar los servicios de Livefyre en su aplicación nativa de Android. El [SDK para Android de Livefyre StreamHub](https://github.com/Livefyre/StreamHub-Android-SDK) proporciona una capa fina en torno a nuestros mecanismos comunes de API, según el entorno de desarrollo de Gradle/Android Studio.

Livefyre también proporciona una aplicación de ejemplo de [Reviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) basada en este SDK.

Este SDK para Android de Livefyre se puede utilizar tanto en Eclipse como en Android Studio.

>[!NOTE]
>
>Antes de instalar el SDK para Android de Livefyre, debe tener el [SDK para Android](https://developer.android.com/sdk/index.html) instalado en su entorno. También debe incluir algunos paquetes adicionales de SDK para Android, como se describe en los documentos para desarrolladores de Android > .
>[Adición de paquetes de SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilice el Administrador de SDK para Android (disponible en la barra de herramientas de Android Studio o Eclipse) para instalar todos los paquetes recomendados. Asegúrese de incluir también el repositorio de soporte de Android.

## Eclipse {#section_dtm_slv_zz}

Para agregar el SDK de Android de Livefyre a su proyecto en Eclipse:

1. Obtenga la más reciente [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) de GitHub.
1. Comience con un proyecto existente o cree uno nuevo.
1. Para importar el SDK de StreamHub-Android a su espacio de trabajo, vaya a **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Examine y seleccione StreamHub-Android-SDK; ahora debería mostrarse en el explorador de paquetes.
1. Haga clic con el botón derecho en el proyecto y seleccione **[!UICONTROL Properties,]** y luego la pestaña Android.
1. En la sección Biblioteca , seleccione **[!UICONTROL Add button,]** y luego seleccione StreamHub-Android-SDK de la lista de bibliotecas.
1. Haga clic en **[!UICONTROL Apply]** y **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Para agregar el SDK de Android de Livefyre a su proyecto en Android Studio:

1. Obtenga la más reciente [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) de GitHub.
1. Comience con un proyecto existente o cree uno nuevo.
1. Haga clic con el botón derecho en el proyecto y seleccione **[!UICONTROL Open Module Settings]**.
1. Seleccione el botón **[!UICONTROL +]** en la esquina superior izquierda de la ventana.
1. Seleccione **[!UICONTROL Import Existing Project.]** (en la nueva versión de Android Studio, puede encontrar **[!UICONTROL Import Existing Project]** en **[!UICONTROL More Modules]**).

1. Busque y seleccione StreamHub-Android-SDK.

Android Studio puede solicitar la conversión del SDK a la versión de gradle; si esto ocurre, seleccione **[!UICONTROL next]** y luego **[!UICONTROL finish]**.

Vaya a **carpeta del proyecto > carpeta de la aplicación > archivo build.gradle** en dependencias para añadir la siguiente dependencia:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Asegúrese de que la siguiente línea se encuentra en la carpeta **del proyecto > settings.gradle** archivo:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Puede personalizar las configuraciones desde Config.java.

## Clientes {#section_yfq_blv_zz}

El SDK para Android de StreamHub expone varias clases de cliente que se pueden usar para solicitar extremos de API de Livefyre:

* **** AdminClientExchange es un token de autenticación de usuario para información de usuario, claves y otros metadatos.

* **** BootstrapClientObtenga contenido y metadatos recientes sobre una colección en particular.

* **** StreamClientPoll muestra un flujo de una colección para recuperar contenido nuevo, actualizado y eliminado.

* **** WriteClientPost, marca y contenido &quot;Me gusta&quot; en una colección.
