---
description: Creación de aplicaciones de Android con Livefyre.
seo-description: Creación de aplicaciones de Android con Livefyre.
seo-title: Android SDK
solution: Experience Manager
title: SDK para Android
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 1%

---


# Android SDK{#android-sdk}

Creación de aplicaciones de Android con Livefyre.

Utilice esta biblioteca para integrar los servicios de Livefyre en su aplicación nativa de Android. El [SDK para Android de Livefyre StreamHub](https://github.com/Livefyre/StreamHub-Android-SDK) proporciona una capa delgada alrededor de nuestros mecanismos de API comunes, según el entorno de desarrollo de Gradle/Android Studio.

Livefyre también proporciona una aplicación de ejemplo de [Reviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App), basada en este SDK.

Este SDK para Android de Livefyre se puede utilizar tanto en Eclipse como en Android Studio.

>[!NOTE]
>
>Antes de instalar el SDK para Android de Livefyre, debe tener el [SDK para Android](https://developer.android.com/sdk/index.html) instalado en el entorno. También debe incluir algunos paquetes adicionales de SDK para Android, como se describe en Documentos para desarrolladores de Android > .
>[Añadir paquetes de SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilice el Administrador de SDK para Android (disponible en la barra de herramientas de Android Studio o Eclipse) para instalar todos los paquetes recomendados. Asegúrese de incluir también el Repositorio de soporte de Android.

## Eclipse {#section_dtm_slv_zz}

Para agregar el SDK de Android de Livefyre a su proyecto en Eclipse:

1. Obtenga lo más reciente [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) de GitHub.
1. Inicio con un proyecto existente o creación de uno nuevo.
1. Para importar StreamHub-Android-SDK en su espacio de trabajo, vaya a **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Examinar y seleccionar StreamHub-Android-SDK; ahora debería mostrarse en el explorador de paquetes.
1. Haga clic con el botón derecho en el proyecto y seleccione **[!UICONTROL Properties,]** y luego la ficha Android.
1. En la sección Biblioteca, seleccione **[!UICONTROL Add button,]** y luego StreamHub-Android-SDK de la lista de bibliotecas.
1. Haga clic en **[!UICONTROL Apply]** y **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Para agregar el SDK de Android de Livefyre al proyecto en Android Studio:

1. Obtenga lo más reciente [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) de GitHub.
1. Inicio con un proyecto existente o creación de uno nuevo.
1. Haga clic con el botón derecho en el proyecto y seleccione **[!UICONTROL Open Module Settings]**.
1. Seleccione el botón **[!UICONTROL +]** en la esquina superior izquierda de la ventana.
1. Seleccione **[!UICONTROL Import Existing Project.]** (en la nueva versión de Android studio, puede encontrar **[!UICONTROL Import Existing Project]** en **[!UICONTROL More Modules]**).

1. Busque y seleccione StreamHub-Android-SDK.

Android Studio puede solicitar que convierta el SDK a la versión de gradle; si esto sucede, seleccione **[!UICONTROL next]** y luego **[!UICONTROL finish]**.

Vaya a **carpeta de proyecto > carpeta de la aplicación > archivo build.gradle** en dependencias para agregar la siguiente dependencia:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Asegúrese de que la siguiente línea se encuentra en su archivo **carpeta de proyecto > settings.gradle**:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Puede personalizar configuraciones desde Config.java.

## Clientes {#section_yfq_blv_zz}

El SDK para Android de StreamHub expone varias clases de cliente que pueden utilizarse para solicitar extremos de la API de Livefyre:

* **** AdminClientExchange proporciona un autentificador de autenticación de usuario para la información del usuario, las claves y otros metadatos.

* **** BootstrapClientObtenga contenido y metadatos recientes sobre una colección concreta.

* **** StreamClientPoll un flujo de una colección para recuperar contenido nuevo, actualizado y eliminado.

* **** WriteClientPost, marca y contenido de &quot;Me gusta&quot; en una colección.

