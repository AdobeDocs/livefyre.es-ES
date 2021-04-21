---
title: Etiquetas inteligentes
description: Etiquetas inteligentes
exl-id: cbbc5550-d6cf-42e5-bce7-2c270cc968cd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Etiquetas inteligentes{#smart-tags}

Livefyre utiliza la tecnología de visión informática de Adobe Sensei para etiquetar automáticamente imágenes y vídeos que guarde o cargue en la biblioteca.

Las etiquetas inteligentes le permiten ahorrar una gran cantidad de tiempo, administrar, buscar y depurar contenido. Con las etiquetas inteligentes, puede:

* Buscar imágenes y vídeos guardados y cargados para obtener contenido preciso basado en la imagen y el contenido de vídeo, en lugar de solo texto
* Recopilar contenido en flujos en función de términos de búsqueda precisos que analicen la imagen o el vídeo, en lugar de solo texto

Al guardar o cargar una imagen o vídeo, Adobe Sensei revisa automáticamente el contenido y lo etiqueta con 135 000 clasificadores en tres categorías:

* Características (por ejemplo, gatos, perros, pirámides, monumentos)
* Categorías (por ejemplo, viajes, turismo, belleza)
* Propiedades estéticas (por ejemplo, calidad de imagen, reglas de la tercera)
* SFW/NSFW (esto le permite filtrar automáticamente las imágenes NSFW, lo que mejora la seguridad de sus flujos y de la biblioteca UGC

El algoritmo de clasificación de etiquetas inteligentes filtra el contenido mediante una puntuación de confianza de etiquetas inteligentes, cuán nuevo es el contenido y cuántas estrellas ha dado un usuario al contenido.

**Etiquetas inteligentes para vídeo**

Detalles de las funciones:

* Las etiquetas inteligentes se aplican a los formatos de vídeo MP4, .avi y .mov
* La duración máxima de los vídeos compatibles es de 60 segundos o 50 MB
* Las etiquetas inteligentes están disponibles en los archivos de Búsqueda social, Transmisiones y Vídeo cargado de la biblioteca

Tipos de etiquetas:

* Etiquetas de funciones: Funciona igual que las etiquetas de características para imágenes (por ejemplo, gatos, perros, pirámides, hitos).
* Etiquetas de acciones: Identifique las características que se producen en varios fotogramas en lugar de solo una. Son más eficaces para resumir el contenido de un vídeo.

Para obtener más información sobre las etiquetas inteligentes, consulte [Opciones de regla de flujo para todas las reglas de flujo](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
