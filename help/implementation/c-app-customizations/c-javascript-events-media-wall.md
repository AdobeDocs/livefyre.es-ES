---
description: Utilice eventos de Javascript para detectar eventos que se produzcan en un muro de medios y enviarlos a la herramienta de análisis que elija.
title: Eventos de Javascript para el muro multimedia
exl-id: 3fe76467-65e2-4f8b-bd75-5a2ffc3e7e15
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Eventos de Javascript para Media Wall{#javascript-events-for-media-wall}

Utilice eventos de Javascript para detectar eventos que se produzcan en un muro de medios y enviarlos a la herramienta de análisis que elija.

Livefyre proporciona eventos de JavaScript para rastrear la actividad de los usuarios en sus aplicaciones de Livefyre. Por ejemplo, puede que desee actualizar la página cuando los usuarios quieran o compartan contenido en Twitter o Facebook, o cuando se publique contenido nuevo.

A continuación, se muestra un ejemplo de cómo recibir los eventos. Reemplace `console.log` por su código para asignar y enviar el evento a su integración de Analytics (Dynamic Tag Management, Adobe Analytics JS, Google Analytics, etc.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Lista de eventos de muro de medios admitidos:

## Eventos de muro de medios

| Evento | Definición |
|---|---|
| `Init` | Cuando se incluye un muro de medios en una página. |
| `Load` | Cuando se cargó el muro de medios en una página independientemente de su posición. |
| `PostButtonClick` | Cuando un usuario hace clic en un botón de carga en un muro de medios. |
| `RequestMore` | Cuando el usuario carga más contenido en un muro de medios. |
| `TwitterReplyClick` | Cuando un usuario hace clic en el botón Responder de Twitter desde el Muro de medios. |
| `TwitterRetweetClick` | Cuando un usuario hace clic en el botón Retweet de Twitter desde el Muro de medios. |
| `TwitterLikeClick` | Cuando un usuario hace clic en el botón &quot;Me gusta&quot;/Favorito de Twitter en el Muro de medios. |
| `ModalView` | Cuando el usuario hace clic para ver el contenido de Muro de medios en una ventana modal más grande. |
| `Like` | Cuando un usuario hace clic en el botón &quot;Me gusta&quot; del Muro de medios. |
| `ShareButtonClick` | Cada vez que un usuario hace clic en el botón Compartir de una tarjeta de Media Wall. |
| `ShareURL` | Cuando se selecciona o copia el área de texto Compartir en URL desde el muro de medios. |
| `ShareFacebook` | Cuando se hace clic en Compartir en Facebook desde el muro de medios. |
| `ShareTwitter` | Cuando se hace clic en Compartir en Twitter desde el muro de medios. |
