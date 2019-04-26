---
description: Implementar notas utilizando .js.
seo-description: Implementar notas utilizando .js.
seo-title: Implementación de Sidenotes
solution: Experience Manager
title: Implementación de Sidenotes
uuid: aa 13852 e-e 2 b 0-4 a 86-97 cd-d 08 ab 5 e 2 cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Implementación de Sidenotes{#sidenotes-implementation}

## Implementar notas utilizando .js

Para implementar esta función, pase una asignación de objeto 1-1 de las cadenas que desee sobrescribir al objeto de configuración Javascript. Si no proporciona un campo, se utilizará el texto predeterminado.

### Ejemplo

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
