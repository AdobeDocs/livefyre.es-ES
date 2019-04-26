---
description: No todos los tweets que coinciden con una regla aparecen en un flujo.
seo-description: No todos los tweets que coinciden con una regla aparecen en un flujo.
seo-title: Aceleración y frecuencia de tweets
solution: Experience Manager
title: Aceleración y frecuencia de tweets
uuid: b 9 edfb 1 e-e 6 cf -4 a 48-8756-05 f 5 f 18 d 8799
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Aceleración y frecuencia de tweets{#throttling-and-frequency-of-tweets}

No todos los tweets que coinciden con una regla aparecen en un flujo.

Las interrupciones de regla de Twitter y de fuente de Twitter pueden limitar el número de tweets visibles en el flujo.

>[!NOTE]
>
>Para garantizar que los tweets específicos se incluyen en el flujo, utilice la opción Cargar recurso desde la página Todos los recursos.

* Las reglas de Twitter aceleran el contenido, extrayendo 1 Tweet por regla cada 5 segundos. Esto permite que el contenido que aparece en las aplicaciones de Livefyre esté más equilibrado y que no se vea abrumado con Tweets. Limitar los tweets entrantes de esta manera también ayuda a evitar que el flujo se quede inundado o no sea legible durante los períodos de tráfico alto.

   >[!NOTE]
   >
   >Para garantizar que el contenido de los autores de alto valor aparezca en las aplicaciones, incluso en flujos de alta velocidad, nunca se aceleran las reglas para autores específicos.

* Las interrupciones de fuente de Twitter pueden producirse por varios motivos. En algunos casos, Twitter no expulsa Tweets, por lo tanto Livefyre no recibe notificaciones del nuevo contenido y no se puede mostrar. Las interrupciones del servicio de las API de Twitter o el tráfico en hashtags/palabras clave de gran volumen también pueden resultar en tweets perdidos.

