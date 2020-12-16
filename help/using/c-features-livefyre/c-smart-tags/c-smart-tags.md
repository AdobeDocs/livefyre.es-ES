---
description: 'null'
seo-description: 'null'
seo-title: Etiquetas inteligentes
title: Etiquetas inteligentes
uuid: f978fa83-e79b-46ae-bb3e-0f9449bd0440
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Etiquetas inteligentes{#smart-tags}

Livefyre utiliza la tecnología de visión informática de Adobe Sensei para etiquetar automáticamente las imágenes y los vídeos que guarde o cargue en la biblioteca.

Las etiquetas inteligentes le permiten ahorrar un tiempo considerable, administrando, buscando y depurando contenido. Con las etiquetas inteligentes, puede:

* Busque en las imágenes y vídeos guardados y cargados contenido preciso basado en la imagen y el contenido del vídeo, en lugar de solo texto
* Recopilar contenido en flujos en función de términos de búsqueda precisos que analicen la imagen o el vídeo, en lugar de solo texto

Al guardar o cargar una imagen o un vídeo, Adobe Sensei revisa automáticamente el contenido y lo etiqueta con 135.000 clasificadores en tres categorías:

* Características (por ejemplo, gatos, perros, pirámides, hitos)
* Categorías (por ejemplo, viajes, turismo, belleza)
* Propiedades estéticas (por ejemplo, calidad de imagen, reglas de terceros)
* SFW/NSFW (esto le permite filtrar automáticamente imágenes NSFW, mejorando la seguridad de sus flujos y de la biblioteca UGC

El algoritmo de clasificación de etiquetas inteligentes filtros el contenido mediante una puntuación de confianza de etiquetas inteligentes, la novedad del contenido y la cantidad de estrellas que un usuario ha dado al contenido.

**Etiquetas inteligentes para vídeo**

Detalles de la función:

* Las etiquetas inteligentes se aplican a los formatos de vídeo MP4, .avi y .mov
* La duración máxima de los vídeos admitidos es de 60 segundos o 50 MB
* Las etiquetas inteligentes están disponibles en los archivos de búsqueda social, flujos y vídeo cargado de la biblioteca

Tipos de etiquetas:

* Etiquetas de funciones: Funciona igual que las etiquetas de características para imágenes (por ejemplo, gatos, perros, pirámides, lugares de referencia).
* Etiquetas de acción: Identifique las funciones que se producen en varios marcos en lugar de en uno solo. Son más eficaces para resumir el contenido de un vídeo.

Para obtener información adicional sobre las etiquetas inteligentes, consulte [Opciones de regla de flujo para todas las reglas de flujo](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
