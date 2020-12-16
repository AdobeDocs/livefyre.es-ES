---
description: Añada Livefyre a su aplicación nativa de iOS.
seo-description: Añada Livefyre a su aplicación nativa de iOS.
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: bfdef31a-49fc-4b25-b0c5-300f27067302
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

Añada Livefyre a su aplicación nativa de iOS.

Utilice esta biblioteca de código abierto para integrar los servicios de Livefyre en su aplicación nativa de iOS. El SDK para iOS de Livefyre StreamHub proporciona una capa delgada alrededor de nuestros mecanismos de API comunes, basada en la excelente biblioteca de redes AFN.

Livefyre también proporciona dos aplicaciones de muestra de iOS basadas en este SDK: un flujo de comentarios y una aplicación de muestra de críticas.

## Integración del SDK en su proyecto como un pod de cacao (recomendado) {#section_qc5_h3v_zz}

La manera más conveniente de agregar el SDK de StreamHub-iOS a su proyecto es utilizar CocoaPods. Si no tiene CocoaPods, ejecute los coágulos de instalación de gem y la configuración del pod. Este es un ejemplo de Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

También necesitará agregar un repositorio de especificaciones a su instalación de CocoaPod (esto lo clonará en el directorio `~/.cocoapods/repos`):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Una vez creado el archivo Podfile en la raíz del proyecto de la aplicación y agregado el repositorio anterior, ejecute:

```
pod install
```

Esto descargará todas las dependencias y creará un archivo MyApp.xcWorkspace, que deberá utilizar a partir de ahora para abrir el proyecto de la aplicación en Xcode.

## Como subproyecto Xcode {#section_jcm_g3v_zz}

También puede clonar el repositorio:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

A continuación, agregue el proyecto Xcode (LFSClient.xcodeproj) a su aplicación como subproyecto (simplemente arrastre el archivo LFSClient.xcodeproj al panel Navegador del proyecto en Xcode).

También deberá hacer lo mismo con cualquiera de las dependencias ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

## Descargar todo a la vez (no recomendado) {#section_rpb_f3v_zz}

```
cd ~/dev 
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
cd StreamHub-iOS-SDK 
git submodule init 
git submodule update 
pod repo add livefyre https://github.com/Livefyre/cocoapods.git 
pod install 
cd examples/CommentStream 
pod install 
open CommentStream.xcworkspace
```

>[!NOTE]
>
>Para ejecutar pruebas en Xcode 6, debe agregar $(PLATFORM_DIR)/Developer/Library/Frameworks a FRAMEWORK_SEARCH_PATHS en el pod Pods-test-XCTest+OHHTTPSibSuiteCleanUp[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704).

Necesita el archivo LFSTestConfig.plist de Livefyre, que Livefyre proporciona bajo petición.

## Documentación de Xcode {#section_arl_b3v_zz}

Puede examinar la [documentación](https://livefyre.github.com/StreamHub-iOS-SDK/) o puede crear el destinatario &quot;Documentación&quot; en su Xcode (requiere que se instale appledoc) en el sistema.

## Requisitos {#section_m5l_13v_zz}

Las versiones del SDK para iOS de StreamHub desde v0.2.0 requieren iOS 6.0 o superior.

## Apéndice (compatibilidad con JSON) {#section_pcd_5hv_zz}

Para aquellos que consulten los internos del SDK de StreamHub-iOS, tenga en cuenta que usamos una versión modificada de [JSONKit](https://github.com/escherba/JSONKit) como analizador JSON predeterminado (en lugar de NSJSONSerialization proporcionado por Apple). Tuvimos que hacerlo porque el analizador proporcionado por Apple no admite la descodificación de archivos JSON que contengan enteros o números de coma flotante que sean mayores que los que puede representar el sistema. Nuestra versión modificada de JSONKit trunca números muy grandes al máximo del sistema correspondiente, en lugar de lanzar una excepción.
