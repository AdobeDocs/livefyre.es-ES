---
description: Limite el tipo de medios que llegan al flujo de la aplicación.
seo-description: Limite el tipo de medios que llegan al flujo de la aplicación.
seo-title: Restringir medios
solution: Experience Manager
title: Restringir medios
uuid: c 470 c 985-d 221-4 f 39-8 bd 4-4 e 44 ec 14 db 95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Restringir medios{#restrict-media}

Limite el tipo de medios que llegan al flujo de la aplicación.

De forma predeterminada, todos los archivos adjuntos de medios se pueden incrustar en Aplicaciones. Livefyre permite cambiar esta opción para evitar que los usuarios anuncien tipos de adjuntos seleccionados en sus aplicaciones.

>[!NOTE]
>
>Socios de Livefyre con la integración de medios. Para obtener más información, consulte Integración de contenido > Integración encadenada. Póngase en contacto con su administrador de cuentas técnico para obtener preguntas sobre la expansión o las fuentes de vínculos.

Este ejemplo bloquea YouTube y Vimeo se incrusta en el flujo de comentarios:

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

