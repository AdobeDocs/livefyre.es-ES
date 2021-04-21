---
description: Agregue Livefyre a su aplicación nativa de iOS.
title: SDK para iOS de Livefyre
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# SDK de iOS de Livefyre{#livefyre-ios-sdk}

Agregue Livefyre a su aplicación nativa de iOS.

Utilice esta biblioteca de código abierto para integrar los servicios de Livefyre en su aplicación nativa de iOS. El SDK para iOS de Livefyre StreamHub proporciona una capa fina alrededor de nuestros mecanismos comunes de API, basada en la excelente biblioteca de redes AFN.

Livefyre también proporciona dos aplicaciones de muestra de iOS basadas en este SDK: un flujo de comentarios y una aplicación de ejemplo de reseñas.

## Integración del SDK en su proyecto como un bacalao (recomendado) {#section_qc5_h3v_zz}

La manera más conveniente de agregar el SDK de StreamHub-iOS a su proyecto es usar CocoaPods. Si no tiene CocoaPods, ejecute la instalación de gem cocoapods y la configuración de pod. Este es un ejemplo de Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

También necesitará añadir un repositorio de Specs a su instalación de CocoaPod (esto lo clonará en el directorio `~/.cocoapods/repos`):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Una vez que el Podfile se haya creado en la raíz del proyecto de la aplicación y agregado el repositorio anterior, ejecute:

```
pod install
```

Esto descargará todas las dependencias y creará un archivo MyApp.xcworkspace, que debería usar a partir de ahora para abrir el proyecto de la aplicación en Xcode.

## Como subproyecto Xcode {#section_jcm_g3v_zz}

Como alternativa, clone el repositorio:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

A continuación, agregue el proyecto Xcode (LFSClient.xcodeproj) a su aplicación como subproyecto (fácilmente, arrastrando el archivo LFSClient.xcodeproj al panel Navegador de proyectos en Xcode).

También deberá hacer lo mismo con cualquiera de las dependencias ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

## Descargue todo a la vez (no recomendado) {#section_rpb_f3v_zz}

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
>Para ejecutar pruebas en Xcode 6, debe agregar $(PLATFORM_DIR)/Developer/Library/Frameworks a FRAMEWORK_SEARCH_PATHS en el pod Pods-test-XCTest+OHHTTPSzziSuiteCleanUp[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704).

Se necesita el archivo LFSTestConfig.plist de Livefyre, que Livefyre proporciona previa solicitud.

## Documentación de Xcode {#section_arl_b3v_zz}

Puede examinar la [documentación](https://livefyre.github.com/StreamHub-iOS-SDK/) o puede crear el destino &quot;Documentación&quot; en su Xcode (requiere que appledoc esté instalado) en su sistema.

## Requisitos {#section_m5l_13v_zz}

Las versiones del SDK para iOS de StreamHub desde la versión 0.2.0 requieren iOS 6.0 o superior.

## Apéndice (compatibilidad con JSON) {#section_pcd_5hv_zz}

Para aquellos que buscan en los internos del SDK de StreamHub-iOS, tenga en cuenta que utilizamos una versión modificada de [JSONKit](https://github.com/escherba/JSONKit) como analizador JSON predeterminado (en lugar de NSJSONSerialization proporcionado por Apple). Tuvimos que hacerlo porque el analizador proporcionado por Apple no admite la descodificación de archivos JSON que contengan números enteros o números de coma flotante que sean mayores que los que puede representar el sistema. Nuestra versión modificada de JSONKit trunca números muy grandes al máximo correspondiente del sistema, en lugar de lanzar una excepción.
