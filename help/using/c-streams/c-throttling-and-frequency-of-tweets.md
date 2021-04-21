---
description: No todos los tweets que coinciden con una regla aparecen en una secuencia.
title: Ritmo y frecuencia de los tweets
exl-id: 6b963f8a-1b61-4252-866b-567d7f556aca
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Restricción y frecuencia de los tweets{#throttling-and-frequency-of-tweets}

No todos los tweets que coinciden con una regla aparecen en una secuencia.

La restricción de reglas de twitter y las interrupciones de fuentes de Twitter pueden limitar el número de tweets visibles en el flujo.

>[!NOTE]
>
>Para garantizar que se incluyan tweets específicos en el flujo, utilice la opción Cargar recurso de la página Todos los recursos .

* Las reglas de twitter reducen el contenido, obteniendo 1 tweet por regla cada 5 segundos. Esto permite que el contenido que aparece en las aplicaciones de Livefyre sea más equilibrado y no se vea abrumado por los tweets. Limitar los tweets entrantes de esta manera también ayuda a evitar que el flujo se inunde o sea ilegible durante períodos de mucho tráfico.

   >[!NOTE]
   >
   >Para garantizar que el contenido de los autores de alto valor aparezca en las aplicaciones, incluso en flujos de alta velocidad, las reglas para autores específicos nunca se limitan.

* Las interrupciones de la fuente de twitter pueden producirse por varios motivos. En algunos casos, Twitter no elimina los tweets, por lo que Livefyre no recibe notificación del nuevo contenido y no se puede mostrar. Las interrupciones del servicio de las API de Twitter, o el tráfico en hashtags/palabras clave de gran volumen, también pueden resultar en la pérdida de tweets.
