---
description: Utilice eventos de Javascript para detectar eventos que ocurren en un
  muro de medios y enviarlos a la herramienta de análisis que elija.
seo-description: Utilice eventos de Javascript para detectar eventos que ocurren en
  un muro de medios y enviarlos a la herramienta de análisis que elija.
seo-title: Eventos de javascript para muro de medios
solution: Experience Manager
title: Eventos de javascript para muro de medios
uuid: 8 afc 0529-4640-476 a-b 207-91 b 2 c 70101 f 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Eventos de javascript para muro de medios{#javascript-events-for-media-wall}

Utilice eventos de Javascript para detectar eventos que ocurren en un muro de medios y enviarlos a la herramienta de análisis que elija.

Livefyre proporciona eventos de JavaScript para rastrear la actividad de los usuarios en sus aplicaciones de Livefyre. Por ejemplo, puede que desee actualizar la página cuando los usuarios hagan "Me gusta" o compartir contenido en Twitter o Facebook, o cuando se publique contenido nuevo.

Este es un ejemplo de cómo recibir los eventos. Sustituya `console.log` por su código para asignar y enviar el evento a su integración de Analytics (Administración dinámica de etiquetas, JS de Adobe Analytics, Google Analytics, etc.):

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
| `Load` | Cuando se cargó el muro de medios en una página, independientemente de su posición. |
| `PostButtonClick` | Cuando un usuario hace clic en un botón de carga en un muro de medios. |
| `RequestMore` | Cuando el usuario carga más contenido en un muro de medios. |
| `TwitterReplyClick` | Cuando un usuario hace clic en el botón Respuesta de Twitter desde el Muro de medios. |
| `TwitterRetweetClick` | Cuando un usuario hace clic en el botón Retweet de Twitter desde el Muro de medios. |
| `TwitterLikeClick` | Cuando un usuario hace clic en el botón "Me gusta"/"Me gusta" de Twitter desde el muro de medios. |
| `ModalView` | Cuando el usuario hace clic para ver el contenido de Muro de medios en una ventana modal más grande. |
| `Like` | Cuando un usuario hace clic en el botón "Me gusta" desde el Muro de medios. |
| `ShareButtonClick` | Cada vez que un usuario hace clic en el botón Compartir en una tarjeta de muro de medios. |
| `ShareURL` | Cuando el área de texto Compartir con URL está seleccionada o copiada desde el Muro de medios. |
| `ShareFacebook` | Cuando se hace clic en Compartir en Facebook desde el Muro de medios. |
| `ShareTwitter` | Cuando se hace clic en Compartir en Twitter, se hace clic en el muro de medios. |
