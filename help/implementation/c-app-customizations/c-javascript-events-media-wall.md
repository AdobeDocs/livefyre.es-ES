---
description: Utilice eventos de Javascript para detectar eventos que se produzcan en un muro multimedia y enviarlos a la herramienta de análisis que desee.
seo-description: Utilice eventos de Javascript para detectar eventos que se produzcan en un muro multimedia y enviarlos a la herramienta de análisis que desee.
seo-title: Eventos de Javascript para Media Wall
solution: Experience Manager
title: Eventos de Javascript para Media Wall
uuid: 8afc0529-4640-476a-b207-91b2c70101f0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Eventos de Javascript para Media Wall{#javascript-events-for-media-wall}

Utilice eventos de Javascript para detectar eventos que se produzcan en un muro multimedia y enviarlos a la herramienta de análisis que desee.

Livefyre proporciona eventos de JavaScript para rastrear la actividad de los usuarios en sus aplicaciones de Livefyre. Por ejemplo, puede que desee actualizar la página cuando los usuarios quieran o compartan contenido en Twitter o Facebook, o cuando se publique nuevo contenido.

Este es un ejemplo de cómo recibir los eventos. Reemplace `console.log` con su código para asignar y enviar el evento a su integración de análisis (Administración dinámica de etiquetas, Adobe Analytics JS, Google Analytics, etc.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Lista de eventos de Media Wall admitidos:

## Eventos de muro de medios

| Evento | Definición |
|---|---|
| `Init` | Cuando se incluye un muro de medios en una página. |
| `Load` | Cuando se cargó el Muro de medios en una página independientemente de su posición. |
| `PostButtonClick` | Cuando un usuario hace clic en un botón de carga en un muro multimedia. |
| `RequestMore` | Cuando el usuario carga más contenido en un muro multimedia. |
| `TwitterReplyClick` | Cuando un usuario hace clic en el botón Respuesta de Twitter desde el Muro de medios. |
| `TwitterRetweetClick` | Cuando un usuario hace clic en el botón Retweet de Twitter desde el Muro de medios. |
| `TwitterLikeClick` | Cuando un usuario hace clic en el botón Me gusta/Favorito de Twitter desde el Muro de medios. |
| `ModalView` | Cuando el usuario hace clic para ver el contenido de Media Wall en una ventana modal más grande. |
| `Like` | Cuando un usuario hace clic en el botón "Me gusta" desde el Muro de medios. |
| `ShareButtonClick` | Cada vez que un usuario hace clic en el botón Compartir de una tarjeta de Media Wall. |
| `ShareURL` | Cuando se selecciona o copia el área de texto Compartir con URL desde el Muro de medios. |
| `ShareFacebook` | Cuando se hace clic en Compartir en Facebook desde el muro de medios. |
| `ShareTwitter` | Cuando se hace clic en Compartir en Twitter desde el muro de medios. |
