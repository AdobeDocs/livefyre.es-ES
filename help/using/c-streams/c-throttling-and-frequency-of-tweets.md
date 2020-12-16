---
description: No todos los tweets que coinciden con una regla aparecen en un flujo.
seo-description: No todos los tweets que coinciden con una regla aparecen en un flujo.
seo-title: Throttling y frecuencia de los tweets
solution: Experience Manager
title: Throttling y frecuencia de los tweets
uuid: b9edfb1e-e6cf-4a48-8756-05f5f18d8799
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# Ritmo y frecuencia de los tweets{#throttling-and-frequency-of-tweets}

No todos los tweets que coinciden con una regla aparecen en un flujo.

La limitación de reglas de Twitter y las interrupciones de fuentes de Twitter pueden limitar el número de tweets visibles en el flujo.

>[!NOTE]
>
>Para garantizar que los tweets específicos se incluyen en el flujo, utilice la opción Cargar recurso de la página Todos los recursos.

* Las reglas de Twitter reducen el contenido, obteniendo 1 tweet por regla cada 5 segundos. Esto permite que el contenido que aparece en las aplicaciones de Livefyre sea más equilibrado y no se vea abrumado por los tweets. Limitar los tweets entrantes de esta manera también ayuda a evitar que el flujo se inunde o se pueda leer durante períodos de mucho tráfico.

   >[!NOTE]
   >
   >Para garantizar que el contenido de los autores de alto valor aparezca en las aplicaciones, incluso en flujos de alta velocidad, nunca se reducen las reglas para autores específicos.

* Las interrupciones de fuentes de Twitter pueden producirse por varios motivos. En algunos casos, Twitter no envía tweets, por lo tanto Livefyre no recibe notificación del nuevo contenido y no se puede mostrar. Las interrupciones del servicio de las API de Twitter, o el tráfico en hashtags/palabras clave de gran volumen, también pueden resultar en la pérdida de tweets.

