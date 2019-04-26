---
description: Agregue Livefyre a la aplicación nativa de iOS.
seo-description: Agregue Livefyre a la aplicación nativa de iOS.
seo-title: SDK de Livefyre iOS
solution: Experience Manager
title: SDK de Livefyre iOS
uuid: bfdef 31 a -49 fc -4 b 25-b 0 c 5-300 f 27067302
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK de Livefyre iOS{#livefyre-ios-sdk}

Agregue Livefyre a la aplicación nativa de iOS.

Utilice esta biblioteca de código abierto para integrar los servicios de Livefyre en su aplicación nativa de iOS. El SDK de Livefyre streamhub iOS proporciona una capa delgada alrededor de nuestros mecanismos de API comunes, según la excelente biblioteca de afnetworking.

Livefyre también proporciona dos aplicaciones de muestra de iOS basadas en este SDK: un flujo de comentarios y una aplicación de muestra de revisiones.

## Integración del SDK en el proyecto como pod Cocoa (recomendado) {#section_qc5_h3v_zz}

La manera más práctica de añadir SDK de streamhub-iOS al proyecto es utilizar cocoapds. Si no tiene cocoapds, ejecute la instalación de un pod y cocoapds de instalación gem. Este es un ejemplo de Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

También tendrá que agregar un repositorio de Especificaciones a su instalación de cocoapod (clonar en `~/.cocoapods/repos` directorio):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Una vez creado el Podfile en la raíz del proyecto de la aplicación y el repositorio superior agregado, ejecute:

```
pod install
```

Esto descargará todas las dependencias y creará un archivo myapp. xcworkspace, que debe utilizar desde ahora para abrir el proyecto de la aplicación en Xcode.

## Como subproyecto Xcode {#section_jcm_g3v_zz}

Como alternativa, clone el repositorio:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

A continuación, agregue el proyecto Xcode (lfsclient. xcodeproj) a la aplicación como subproyecto (fácil de conseguir simplemente arrastrando el archivo lfsclient. xcodeproj al panel Navegador de proyectos en Xcode).

También tendrá que hacer lo mismo con cualquiera de las dependencias ([afnetworking](https://github.com/AFNetworking/AFNetworking), [jsonkit](https://github.com/escherba/JSONKit)).

## Descargue todo a la vez (no se recomienda) {#section_rpb_f3v_zz}

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
>Para ejecutar pruebas en Xcode 6, debe agregar $ (PLATFORM_ DIR)/Developer/Library/Frameworks a FRAMEWORK_ SEARCH_ PATHS en Pods-test-xctest + ohhttpstubsuitecleanup podhttps://stackoverflow.com/a/24651704[](https://stackoverflow.com/a/24651704).

Necesita el archivo lfstestconfig. plist desde Livefyre, que Livefyre proporciona a petición.

## Documentación Xcode {#section_arl_b3v_zz}

Puede examinar [la documentación](https://livefyre.github.com/StreamHub-iOS-SDK/) o crear el destino «Documentación» en Xcode (requiere que se instale appledoc) en el sistema.

## Requisitos {#section_m5l_13v_zz}

Las versiones de SDK para iOS de streamhub desde la versión 0.2.0 requieren iOS 6.0 o superior.

## Apéndice (compatibilidad con JSON) {#section_pcd_5hv_zz}

Para quienes están mirando las internas streamhub-iOS SDK, tenga en cuenta que utilizamos una versión modificada de [jsonkit](https://github.com/escherba/JSONKit) como analizador JSON predeterminado (en lugar de nsjsonserialization de Apple). Esto se debe a que el analizador proporcionado por Apple no admite la descodificación de archivos JSON que contienen enteros o números de coma flotante mayores que los que pueden representar el sistema. Nuestra versión modificada de jsonkit trunca números muy grandes al máximo del sistema, en lugar de emitir una excepción.
