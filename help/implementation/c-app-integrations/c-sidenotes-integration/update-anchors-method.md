---
description: Biblioteca principal de Livefyre que se utiliza para alimentar a Livefyre en su sitio.
seo-description: Biblioteca principal de Livefyre que se utiliza para alimentar a Livefyre en su sitio.
seo-title: updateAnchors (método)
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 1%

---


# updateAnchors (método) {#updateAnchorsMethod}

Utilice el método updateAnchors para añadir contenido alojado de forma dinámica a la página.

Este método resulta útil para la paginación o en otros casos en los que el contenido de la página se agrega dinámicamente a la página. Este método define nuevos anclajes para los elementos coincidentes y toma un solo argumento: newSelectors.

**newSelectors**. Los selectores que se agregarán a Sidenotes. Puede ser una cadena de selector, un objeto jQuery o una matriz de elementos (cualquiera de los tipos aceptados por el argumento selectors que se pasan durante la construcción de la aplicación).
Formato:

```
app.updateAnchors(newSelectors);
```

Ejemplo:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
