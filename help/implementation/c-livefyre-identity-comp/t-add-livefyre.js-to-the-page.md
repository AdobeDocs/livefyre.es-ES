---
description: Livefyre.js es una pequeña biblioteca base que proporciona autenticación para las aplicaciones del sitio.
title: Agregar Livefyre.js a la página
exl-id: 4c5dfb31-b7e5-48f7-826c-cddbee06d876
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---

# Agregar Livefyre.js a la página{#add-livefyre-js-to-the-page}

Livefyre.js es una pequeña biblioteca base que proporciona autenticación para las aplicaciones del sitio.

Para habilitar la autenticación:

1. Agregue Livefyre.js al elemento `<head>` de su página web o plantilla de sitio web.
1. Agregue una de las siguientes opciones a su página:

   * `globalwindow.Livefyre` correspondiente
   * `Livefyre.require` para cargar otros paquetes de Livefyre bajo demanda

      ```
      <script src="//cdn.livefyre.com/Livefyre.js"></script>
      ```
