---
description: Implementar notas utilizando .js.
title: Implementación de notas
exl-id: 07a68677-c67e-4128-8cb7-c5fb9e0ecc60
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 22%

---

# Implementación de notas{#sidenotes-implementation}

## Implementar notas utilizando .js

Para implementar esta función, pase una asignación de objeto 1-1 de las cadenas que desee reemplazar al objeto de configuración de Javascript. Si no proporciona un campo, se utilizará el texto predeterminado.

### Ejemplo

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
