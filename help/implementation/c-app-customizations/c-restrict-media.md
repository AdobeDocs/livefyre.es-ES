---
description: Limite el tipo de medio que entra en el flujo de la aplicación.
seo-description: Limite el tipo de medio que entra en el flujo de la aplicación.
seo-title: Restringir medios
solution: Experience Manager
title: Restringir medios
uuid: c470c985-d221-4f39-8bd4-4e44ec14db95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Restringir medios{#restrict-media}

Limite el tipo de medio que entra en el flujo de la aplicación.

De forma predeterminada, todos los archivos adjuntos de medios se pueden incrustar en las aplicaciones. Livefyre le permite cambiar esta opción para evitar que los usuarios publiquen tipos de datos adjuntos seleccionados en sus aplicaciones.

>[!NOTE]
>
>Livefyre se asocia con Embedere para la integración de medios. Para obtener más información, consulte Integración de contenido > Integración indirecta. Póngase en contacto con el administrador técnico de cuentas para obtener información sobre la expansión o las fuentes de los vínculos.

Este ejemplo bloquea las incrustaciones de YouTube y Vimeo del flujo de comentarios:

```
var attachmentDelegate = function(embedObj) { 
   var providersToBlock = ['youtube', 'vimeo']; 
   for (var i=0, len=providersToBlock.length; i<len; i++) { 
      if (embedObj.provider_url.indexOf(providersToBlock[i]) > -1) { 
         return false; 
      } 
   } 
   return true; 
};
```

Al cargar la conversación:

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```

