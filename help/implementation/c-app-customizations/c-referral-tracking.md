---
description: Rastree los clics de vuelta a la página desde el tráfico de referencia.
seo-description: Rastree los clics de vuelta a la página desde el tráfico de referencia.
seo-title: Seguimiento de referencia
solution: Experience Manager
title: Seguimiento de referencia
uuid: 5206cc16-9671-4b3d-a013-be1a3e8c029d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# Seguimiento de referencia{#referral-tracking}

Rastree los clics de vuelta a la página desde el tráfico de referencia.

Livefyre anexa una variable de referencia a la dirección URL cuando se publica o comparte un comentario en una red social y para vínculos permanentes incluidos en los correos electrónicos de Livefyre. Utilice esta variable para rastrear el tráfico de referencia de las aplicaciones de Livefyre a sus propiedades sociales o propias.

Las aplicaciones de Livefyre permiten rastrear los flujos de datos resultantes del tráfico de referencia, lo que permite analizar el tráfico del sitio.

## Seguimiento del tráfico de referencia de Livefyre {#section_nsy_qp4_xz}

El tráfico de referencia de Livefyre desde las redes sociales y los correos electrónicos puede rastrearse inspeccionando los parámetros de cadena de consulta en las direcciones URL de las páginas e implementando código en la página para rastrearlo a través del proveedor de análisis. Livefyre anexa un vínculo de referencia a la URL cuando se publica o comparte un comentario en una red social y para vínculos permanentes incluidos en los correos electrónicos de Livefyre.

## Ejemplo de implementación {#section_xvs_x44_xz}

Si el tráfico procedía de una notificación basada en StreamHub, habrá un parámetro de cadena de consulta hubRefSrc con un valor de correo electrónico, facebook, twitter, linkedin o permalink. El equipo de envío de Livefyre puede configurar el nombre del parámetro hubRefSrc a nivel de red.

Para integrarla con una plataforma de análisis, la página debe buscar hubRefSrc durante la carga y registrar el tráfico si está presente.

Por ejemplo:

```
(function () { 
   var qs = document.location.search.substring(1), 
      param = 'hubRefSrc', 
      valueRegex = new RegExp(param+'=([^&]+)'), 
      match = qs.match(valueRegex), 
      referrer; 
   if (match) { 
      // StreamHub generated traffic! 
      referrer = match[1]; 
      console.log('StreamHub referred via', referrer); 
   } else { 
      // StreamHub did not refer this traffic 
   } 
}())
```

Aplicaciones que utilizan esta función:

* [Conversación](/help/using/c-about-apps/c-chat-app/c-chat-app.md)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reseñas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md)
* [Notas de identidad](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)