---
description: Rastree los clics de vuelta a la página desde el tráfico de referencia.
seo-description: Rastree los clics de vuelta a la página desde el tráfico de referencia.
seo-title: Seguimiento de referencia
solution: Experience Manager
title: Seguimiento de referencia
uuid: 7daf615d-0c07-49d1-adb2-1ac67ea563e7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Seguimiento de referencia{#referral-tracking}

Rastree los clics de vuelta a la página desde el tráfico de referencia.

Livefyre anexa una variable de referencia a la dirección URL cuando se publica o comparte un comentario en una red social y para vínculos permanentes incluidos en los correos electrónicos de Livefyre. Utilice esta variable para rastrear el tráfico de referencia de las aplicaciones de Livefyre a sus propiedades sociales o propias.

Las aplicaciones de Livefyre permiten rastrear los flujos de datos resultantes del tráfico de referencia, lo que permite analizar el tráfico del sitio.

## Seguimiento del tráfico de referencia de Livefyre {#section_nsy_qp4_xz}

El tráfico de referencia de Livefyre desde las redes sociales y los correos electrónicos puede rastrearse inspeccionando los parámetros de cadena de consulta en las direcciones URL de las páginas e implementando código en la página para rastrearlo a través del proveedor de análisis. Livefyre anexa un vínculo de referencia a la URL cuando se publica o comparte un comentario en una red social y para vínculos permanentes incluidos en los correos electrónicos de Livefyre.

## Ejemplo de implementación {#section_xvs_x44_xz}

Si el tráfico procedía de una notificación basada en StreamHub, habrá un parámetro de cadena de consulta hubRefSrc con un valor de correo electrónico, facebook, twitter, linkedin o permalink. El equipo de entrega de Livefyre puede configurar el nombre del parámetro hubRefSrc a nivel de red.

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

* [Conversación](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reseñas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Notas de identidad](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

