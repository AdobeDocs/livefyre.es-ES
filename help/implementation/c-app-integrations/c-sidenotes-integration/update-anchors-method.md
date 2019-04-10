---
description: La biblioteca principal de Livefyre utilizada para poder completar Livefyre
  en su sitio.
seo-description: La biblioteca principal de Livefyre utilizada para poder completar
  Livefyre en su sitio.
seo-title: Método updateanchors
solution: Experience Manager
title: Livefyre. js
uuid: null
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método updateanchors {#updateAnchorsMethod}

Utilice el método updateanchors para agregar contenido transferido a la página dinámicamente.

Este método resulta útil para la paginación, o en otros casos en los que el contenido con capacidad de transferencia se agrega a la página dinámicamente. Este método define los nuevos anclajes para los elementos coincidentes y toma un solo argumento: Newselectors.

**Newselectors**. Selectores que agregar a Sidenotes. Puede ser una cadena de selector, un objeto jquery o una matriz de elementos (cualquiera de los tipos aceptados por el argumento selectores pasado durante la construcción de la aplicación).
Formato:

```
app.updateAnchors(newSelectors);
```

Ejemplo:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
