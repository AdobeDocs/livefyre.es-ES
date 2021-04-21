---
description: Vuelva a colocar el logotipo de Livefyre en la página.
title: Mover el logotipo de Livefyre
exl-id: dc6c26cf-e0b9-4af3-8a3c-e58ea4ecbc44
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Mover el logotipo de Livefyre{#move-the-livefyre-logo}

Vuelva a colocar el logotipo de Livefyre en la página.

Si su acuerdo con Livefyre lo permite, puede mover el logotipo de Livefyre de la parte superior del flujo de contenido a la parte inferior.

Por ejemplo, agregue el siguiente HTML a su página inmediatamente después del elemento que contiene la aplicación Livefyre:

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

A continuación, agregue lo siguiente a la hoja de estilo de su página:

```
/* Hide the top logo */ 
.fyre-widget .fyre-logo-drop, .fyre-widget .fyre-logo-help, .fyre-widget .fyre-help { 
    display:none !important; 
} 
  
/* Style the bottom logo */ 
#powered_by_livefyre_new a {    background: url(https://cdn.livefyre.com/libs/fyre.conv/v3.0.0/images/poweredbylivefyre.png) no-repeat left top; 
    display: block; 
    height: 24px; 
    font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
} 
#powered_by_livefyre_new a:hover { 
    text-decoration: underline; 
}
```
