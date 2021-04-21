---
description: La biblioteca principal de Livefyre utilizada para impulsar Livefyre en su sitio.
title: Livefyre.js
uuid: null
exl-id: 5f60ce54-5669-4768-912d-c1b13946d8b8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# updateAnchors (método {#updateAnchorsMethod})

Utilice el método updateAnchors para añadir contenido con guiones a la página de forma dinámica.

Este método es útil para la paginación o en otros casos en los que el contenido que se puede usar en las listas de direcciones se agrega a la página de forma dinámica. Este método define nuevos anclajes para los elementos coincidentes y toma un solo argumento: newSelectors.

**newSelectors**. Los selectores que se agregarán a las notas. Puede ser una cadena de selector, un objeto jQuery o una matriz de elementos (cualquiera de los tipos aceptados por el argumento selectors pasado durante la construcción de la aplicación).
Formato:

```
app.updateAnchors(newSelectors);
```

Ejemplo:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
