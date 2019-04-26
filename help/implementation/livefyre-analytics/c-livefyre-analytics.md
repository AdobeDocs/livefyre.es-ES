---
description: null
seo-description: null
seo-title: Utilizar Livefyre con otras herramientas de Analytics
solution: Experience Manager
title: Utilizar Livefyre con otras herramientas de Analytics
uuid: 26 c 835 f 6-approved -41 f 7-aabe -418 afce 8 a 829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utilizar Livefyre con otras herramientas de Analytics{#use-livefyre-with-other-analytics-tool}

Puede utilizar herramientas de análisis para recopilar datos sobre interacciones de usuario con aplicaciones de Livefyre. Puede utilizar Adobe Analytics o una herramienta de su elección.

Para utilizar Livefyre con una herramienta de su elección (no Adobe Analytics), siga el procedimiento descrito en esta página.

## Paso 1: Configurar el controlador de eventos {#section_ngm_gzl_pdb}

Configure un controlador de eventos en las páginas donde utilice aplicaciones de Livefyre. Esto le permite recopilar datos de aplicaciones de esa página que puede utilizar para análisis.

Agregue Livefyre. js a una página para configurar el controlador de eventos. Livefyre. js se carga asincrónicamente. Para reducir el tamaño de archivo y mejorar el rendimiento de carga, los análisis no están disponibles inmediatamente. Debe sondear el objeto de Analytics hasta que los datos estén disponibles. Coloque esta secuencia de comandos en cualquier lugar de la página o empaquete dentro de sus propias secuencias de comandos compiladas.

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

## Paso 2: Implementar función de controlador

Una vez que la funcionalidad de Livefyre. analytics esté disponible en la página, implemente la función analyticshandler para enviar los eventos recibidos al proveedor de análisis de su elección.

1. El controlador de Analytics recibe una matriz de eventos que deben iterarse a través de un lote o enviarse por lotes, si el proveedor lo admite.
1. Asigne los datos del evento recibidos por el controlador a un formato que requiera su proveedor de Analytics.
1. Envíe los datos a su proveedor de Analytics.

