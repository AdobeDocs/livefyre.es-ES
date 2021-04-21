---
description: Rastree los clics de vuelta a su página desde el tráfico de recomendación.
title: Seguimiento de referencias
exl-id: 9955d4a4-184d-421f-bcde-b19342b0b181
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 2%

---

# Seguimiento de referencia{#referral-tracking}

Rastree los clics de vuelta a su página desde el tráfico de recomendación.

Livefyre anexa una variable de referente a la dirección URL cuando un comentario se publica o comparte en una red social, y para los vínculos de permanente incluidos en los correos electrónicos de Livefyre. Utilice esta variable para rastrear el tráfico de referencia de las aplicaciones de Livefyre a sus propiedades sociales o propias.

Las aplicaciones de Livefyre permiten rastrear flujos de datos resultantes del tráfico de referencia, lo que permite analizar el tráfico de su sitio.

## Seguimiento del tráfico de referencia de Livefyre {#section_nsy_qp4_xz}

El tráfico de referencia de Livefyre de redes sociales y correos electrónicos puede rastrearse inspeccionando los parámetros de cadena de consulta en las direcciones URL de las páginas e implementando código en la página para rastrearlo a través del proveedor de análisis. Livefyre adjunta un vínculo de referencia a la dirección URL cuando se publica o comparte un comentario en una red social y para los vínculos permanentes incluidos en los correos electrónicos de Livefyre.

## Ejemplo de implementación {#section_xvs_x44_xz}

Si el tráfico procedía de una notificación basada en StreamHub, habrá un parámetro de cadena de consulta hubRefSrc con un valor de correo electrónico, facebook, twitter, linkedin o permalink. El equipo de envío de Livefyre puede configurar el nombre del parámetro hubRefSrc en el nivel de red.

Para integrarse con una plataforma de análisis, la página debe buscar el hubRefSrc en la carga y registrar el tráfico si está presente.

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

Aplicaciones que usan esta función:

* [Conversación](/help/using/c-about-apps/c-chat-app/c-chat-app.md)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reseñas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md)
* [Notas](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)
