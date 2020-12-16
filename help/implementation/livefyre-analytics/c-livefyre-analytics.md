---
description: 'null'
seo-description: 'null'
seo-title: Uso de Livefyre con otras herramientas de Analytics
solution: Experience Manager
title: Uso de Livefyre con otras herramientas de Analytics
uuid: 26c835f6-aced-41f7-aabe-418afce8a829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# Usar Livefyre con otras herramientas de Analytics{#use-livefyre-with-other-analytics-tool}

Puede utilizar las herramientas de análisis para recopilar datos sobre las interacciones de los usuarios con las aplicaciones de Livefyre. Puede usar Adobe Analytics o una herramienta de su elección.

Para utilizar Livefyre con una herramienta de su elección (no Adobe Analytics), siga el procedimiento descrito en esta página.

## Paso 1: Configurar el controlador de evento {#section_ngm_gzl_pdb}

Configure un controlador de evento en las páginas en las que utilice aplicaciones de Livefyre. Esto le permite recopilar datos de las aplicaciones de esa página que puede utilizar para el análisis.

Añada Livefyre.js en una página para configurar el controlador de evento. Livefyre.js se carga de forma asíncrona. Para reducir el tamaño del archivo y mejorar el rendimiento de la carga, los análisis no están disponibles inmediatamente. Debe sondear el objeto analytics hasta que los datos estén disponibles. Coloque esta secuencia de comandos en cualquier lugar de la página o inclúyala dentro de sus propios scripts compilados.

```
/** 
 * Handler for Livefyre analytics batch events. 
 * @param {Array.<string>} events Array of events that have been fired since 
 * the last batch send. 
 */ 
function analyticsHandler(events) { 
  // Send to analytics 
  console.log(events); 
} 
 
var attempts = 0; 
 
function pollForAnalytics() { 
  if (Livefyre && Livefyre.analytics) { 
    Livefyre.analytics.addHandler(analyticsHandler); 
    return; 
  } 
  if (attempts === 10) { 
    return; 
  } 
  attempts++; 
  setTimeout(pollForAnalytics, 500); 
} 
 
pollForAnalytics(); 
```

## Paso 2: Implementar la función de controlador

Una vez que la funcionalidad Livefyre.analytics esté disponible en la página, implemente la función analyticsHandler para enviar las eventos recibidas al proveedor de análisis de su elección.

1. El controlador de Analytics recibe una matriz de eventos que se deben iterar y enviar de forma individual o por lotes, si el proveedor lo admite.
1. Asigne los datos de evento recibidos por el controlador a un formato que el proveedor de análisis necesite.
1. Envíe los datos a su proveedor de análisis.

