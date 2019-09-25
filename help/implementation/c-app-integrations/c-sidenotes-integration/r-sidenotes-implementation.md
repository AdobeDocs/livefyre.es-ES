---
description: Implementar notas utilizando .js.
seo-description: Implementar notas utilizando .js.
seo-title: Implementación de Sidenotes
solution: Experience Manager
title: Implementación de Sidenotes
uuid: aa13852e-e2b0-4a86-97cd-d08ab5e2cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Implementación de Sidenotes{#sidenotes-implementation}

## Implementar notas utilizando .js

Para implementar esta función, pase una asignación de objetos 1-1 de las cadenas que desee reemplazar al objeto de configuración de Javascript. Si no proporciona un campo, se utilizará el texto predeterminado.

### Ejemplo

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
