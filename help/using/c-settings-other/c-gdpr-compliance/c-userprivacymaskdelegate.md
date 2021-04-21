---
description: Puede cambiar el texto de advertencia que aparece en las máscaras de vídeo mediante .
title: userPrivacyMaskDelegate
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

Puede cambiar el texto de advertencia que aparece en las máscaras de vídeo mediante .

Este texto existe para cumplir con el reglamento del RGPD. Si una fuente no admite un proxy, Livefyre muestra este texto y una máscara en el contenido a menos que un usuario haga clic en el vídeo y apruebe el seguimiento potencial de dicha fuente.

Si no utiliza `userPrivacyMaskDelegate`, se muestra el siguiente texto predeterminado:

Agregue `userPrivacyMaskDelegate` después de `userPrivacyOptOut`. Puede agregar todos los indicadores de privacidad de Livefyre a la vez como parte de un objeto Livefyre.

Este es un ejemplo de cómo utilizar `userPrivacyMaskDelegate`:

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
