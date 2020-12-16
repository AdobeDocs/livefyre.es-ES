---
description: Puede cambiar el texto de advertencia que se muestra en las máscaras de vídeo mediante .
seo-description: Puede cambiar el texto de advertencia que se muestra en las máscaras de vídeo mediante .
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: 8e5a2750-bf45-4e70-a5f9-37f5e7c61f8e
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

Puede cambiar el texto de advertencia que se muestra en las máscaras de vídeo mediante .

Este texto existe para cumplir con el Reglamento del RGPD. Si un origen no admite un proxy, Livefyre muestra este texto y una máscara en el contenido a menos que un usuario haga clic en el vídeo y apruebe el seguimiento potencial de ese origen.

Si no utiliza `userPrivacyMaskDelegate`, se muestra el siguiente texto predeterminado:

Añada `userPrivacyMaskDelegate` después de `userPrivacyOptOut`. Puede agregar todos los indicadores de privacidad de Livefyre a la vez como parte de un objeto de Livefyre.

A continuación se muestra un ejemplo de cómo utilizar `userPrivacyMaskDelegate`:

```
userPrivacyMaskDelegate: function () { 
    var container = document.createElement('div'); 
    var firstParagraph = document.createElement('p'); 
    firstParagraph.innerHTML = 'Text of first paragraph'; 
    var secondParagraph = document.createElement('p'); 
    secondParagraph.innerHTML = 'Text of second paragraph'; 
    container.appendChild(firstParagraph); 
    container.appendChild(secondParagraph); 
    return container; 
}
```
