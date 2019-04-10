---
description: Rastree los clics de regreso a la página desde el tráfico de referencia.
seo-description: Rastree los clics de regreso a la página desde el tráfico de referencia.
seo-title: Seguimiento de referencia
solution: Experience Manager
title: Seguimiento de referencia
uuid: 7 daf 615 d -0 c 07-49 d 1-adb 2-1 ac 67 ea 563 e 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Seguimiento de referencia{#referral-tracking}

Rastree los clics de regreso a la página desde el tráfico de referencia.

Livefyre anexa una variable de referencia a la URL cuando se publica o comparte un comentario en una red social, y para los accesos permanentes incluidos en los correos electrónicos de Livefyre. Utilice esta variable para rastrear el tráfico de referencia desde aplicaciones de Livefyre a sus propiedades sociales o propias.

Las aplicaciones de Livefyre permiten rastrear flujos de datos resultantes del tráfico de referencia, lo que permite analizar el tráfico del sitio.

## Seguimiento de tráfico de referencia de Livefyre {#section_nsy_qp4_xz}

El tráfico de referencia de Livefyre desde redes sociales y correos electrónicos puede rastrearse inspeccionando los parámetros de cadena de consulta en las direcciones URL de las páginas e implementando código en su página para rastrearlo a través de su proveedor de análisis. Livefyre anexa un vínculo de referencia a la URL cuando se publica o comparte un comentario en una red social, y para los accesos permanentes incluidos en los correos electrónicos de Livefyre.

## Ejemplo de implementación {#section_xvs_x44_xz}

Si el tráfico provenía de una notificación streamhub, habrá un parámetro de cadena de consulta hubrefsrc con un valor de correo electrónico, facebook, twitter, linkedin o permalink. El equipo de entrega de Livefyre puede configurar el nombre del parámetro hubrefsrc en el nivel de red.

Para integrarse con una plataforma de análisis, la página debe buscar hubrefsrc en la carga y registrar el tráfico si está presente.

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

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentarios](/help/using/c-about-apps/c-comments/c-comments.md)
* [Críticas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

