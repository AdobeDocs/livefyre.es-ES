---
description: Limite el tipo de contenido que entra en el flujo de la aplicación.
title: Restringir contenido multimedia
exl-id: ae09a058-41de-4b63-8654-cc82f5abad14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# Restringir medios{#restrict-media}

Limite el tipo de contenido que entra en el flujo de la aplicación.

De forma predeterminada, todos los archivos adjuntos de contenidos se pueden incrustar en aplicaciones. Livefyre le permite cambiar esta opción para evitar que los usuarios anuncien los tipos de datos adjuntos seleccionados en sus aplicaciones.

>[!NOTE]
>
>Livefyre se asocia con Embedly para la integración de medios. Para obtener más información, consulte Integración de contenido > Integración con Embedly . Póngase en contacto con su administrador técnico de cuentas para obtener más información sobre la expansión o las fuentes de los vínculos.

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
