---
description: Cree aplicaciones Android con tecnología de Livefyre.
seo-description: Cree aplicaciones Android con tecnología de Livefyre.
seo-title: SDK de Android
solution: Experience Manager
title: SDK de Android
uuid: 68793 fa 9-3 ea 1-4890-b 36 d-b 631 f 1 c 6 f 7 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK de Android{#android-sdk}

Cree aplicaciones Android con tecnología de Livefyre.

Utilice esta biblioteca para integrar los servicios de Livefyre en su aplicación nativa de Android. El SDK [de Livefyre streamhub Android](https://github.com/Livefyre/StreamHub-Android-SDK) proporciona una capa delgada alrededor de nuestros mecanismos comunes de API, según el entorno de desarrollo de Gradle/Android Studio.

Livefyre también proporciona una [aplicación](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) de ejemplo de Reviews, basada en este SDK.

Este SDK de Livefyre Android se puede utilizar tanto en Eclipse como en Android Studio.

>[!NOTE]
>
>Antes de instalar el SDK para Android Android, debe tener instalado [el SDK](https://developer.android.com/sdk/index.html) para Android en su entorno. También debe incluir algunos paquetes de SDK para Android adicionales, como se describe en los documentos de desarrollador de Android >.
>[Adición de paquetes de SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilice el SDK de Android (disponible desde la barra de herramientas de Android Studio o Eclipse) para instalar todos los paquetes recomendados. Asegúrese de incluir también el repositorio de soporte de Android.

## Eclipse {#section_dtm_slv_zz}

Para agregar el SDK de Livefyre Android al proyecto en Eclipse:

1. Obtenga la última [versión de streamhub-Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) desde github.
1. Comience con un proyecto existente o cree uno nuevo.
1. Para importar el SDK de streamhub-Android en su espacio de trabajo, vaya **[!UICONTROL File > Import > General > Existing Project into Workspace]**a.
1. Examinar y seleccionar streamhub-Android-SDK; debería mostrarse en el explorador del paquete.
1. Haga clic con el botón derecho en el proyecto y seleccione **[!UICONTROL Properties,]** la ficha Android.
1. En la sección Biblioteca, seleccione **[!UICONTROL Add button,]** a continuación streamhub-Android-SDK desde la lista de bibliotecas.
1. Haga clic **[!UICONTROL Apply]** en y **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Para agregar el SDK de Livefyre Android al proyecto en Android Studio:

1. Obtenga la última [versión de streamhub-Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) desde github.
1. Comience con un proyecto existente o cree uno nuevo.
1. Haga clic con el botón secundario en el proyecto y seleccione **[!UICONTROL Open Module Settings]**.
1. Seleccione **[!UICONTROL +]** el botón en la esquina superior izquierda de la ventana.
1. Seleccionar **[!UICONTROL Import Existing Project.]** (en la nueva versión de Android, puede encontrarlo **[!UICONTROL Import Existing Project]** en **[!UICONTROL More Modules]**.)

1. Busque y seleccione streamhub-Android-SDK.

Android Studio puede solicitar que convierta el SDK a la versión de gradle; Si esto sucede, seleccione **[!UICONTROL next]** entonces **[!UICONTROL finish]**.

Vaya a **la carpeta de proyecto > carpeta de la aplicación > build. gradle** , en dependencias para agregar la siguiente dependencia:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Asegúrese de que la línea siguiente se encuentra en el archivo de la carpeta **de proyecto > settings. grade** :

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Puede personalizar configuraciones desde Config. java.

## Clientes {#section_yfq_blv_zz}

El SDK de streamhub Android expone varias clases de cliente que pueden utilizarse para solicitar puntos finales de la API de Livefyre:

* **Adminclient** Intercambia un token de autenticación de usuario para información de usuario, claves y otros metadatos.

* **Bootstrapclient** Obtenga contenido y metadatos recientes sobre una colección en particular.

* **Streamclient** Un flujo de una colección para recuperar contenido nuevo, actualizado y eliminado.

* **Writeclient** Post, flag y like contenido en una colección.

