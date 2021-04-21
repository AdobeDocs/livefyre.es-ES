---
title: Usar Livefyre con otra herramienta de análisis
description: Usar Livefyre con otra herramienta de análisis
exl-id: da29e281-5095-4e99-a248-19390f2059a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Usar Livefyre con otra herramienta de análisis{#use-livefyre-with-other-analytics-tool}

Puede utilizar las herramientas de análisis para recopilar datos sobre las interacciones del usuario con las aplicaciones de Livefyre. Puede utilizar Adobe Analytics o una herramienta de su elección.

Para utilizar Livefyre con una herramienta de su elección (no Adobe Analytics), siga el procedimiento descrito en esta página.

## Paso 1: Configuración del controlador de eventos {#section_ngm_gzl_pdb}

Configure un controlador de eventos en páginas donde use aplicaciones de Livefyre. Esto le permite recopilar datos de las aplicaciones de esa página que puede usar para análisis.

Agregue Livefyre.js a una página para configurar el controlador de eventos. Livefyre.js se carga asincrónicamente. Para reducir el tamaño de los archivos y mejorar el rendimiento de carga, los análisis no están disponibles inmediatamente. Debe sondear el objeto de análisis hasta que los datos estén disponibles. Coloque esta secuencia de comandos en cualquier lugar de la página o aúnarla con sus propios scripts compilados.

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

## Paso 2: Implementación de la función del controlador

Una vez que la funcionalidad Livefyre.analytics esté disponible en la página, implemente la función analyticsHandler para enviar los eventos recibidos al proveedor de análisis que elija.

1. El controlador de Analytics recibe una matriz de eventos que se deben iterar y enviar individualmente o como un lote, si el proveedor lo admite.
1. Asigne los datos de evento recibidos por el controlador a un formato que el proveedor de análisis necesite.
1. Envíe los datos al proveedor de análisis.
