---
description: Puede cambiar el texto de advertencia que aparece en las máscaras de vídeo utilizando.
seo-description: Puede cambiar el texto de advertencia que aparece en las máscaras de vídeo utilizando.
seo-title: Userprivacymaskdelegate
solution: Experience Manager
title: Userprivacymaskdelegate
uuid: 8 e 5 a 2750-bf 45-4 e 70-a 5 f 9-37 f 5 e 7 c 61 f 8 e
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Userprivacymaskdelegate{#userprivacymaskdelegate}

Puede cambiar el texto de advertencia que aparece en las máscaras de vídeo utilizando.

Este texto existe para cumplir con el reglamento del RGPD. Si un origen no admite un proxy, Livefyre muestra este texto y una máscara en el contenido a menos que un usuario haga clic en el vídeo y apruebe el seguimiento potencial de ese origen.

Si no utiliza `userPrivacyMaskDelegate`, aparece el siguiente texto predeterminado:

Agregue `userPrivacyMaskDelegate` después `userPrivacyOptOut`. Puede agregar todos los indicadores de privacidad de Livefyre a la vez como parte de un objeto Livefyre.

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
