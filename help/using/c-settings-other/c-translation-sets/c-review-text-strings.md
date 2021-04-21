---
description: Personalización de las cadenas de texto para revisiones de Livefyre.
title: Revisar cadenas de texto
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 5%

---

# Revisar cadenas de texto{#review-text-strings}

Personalización de las cadenas de texto para revisiones de Livefyre.

Esta página enumera y describe las cadenas disponibles para la personalización en las aplicaciones de revisión. Las cadenas enumeradas aquí se suman a y anulan para las cadenas predeterminadas de las aplicaciones principales de Livefyre, que se enumeran en Personalizaciones de cadenas. Cuando se muestran duplicados, las cadenas enumeradas en estas tablas son las predeterminadas para las aplicaciones de Reseñas.

Implementación
Interfaz de revisión/clasificación
Información de flujo
Información de autor/contenido
Acciones del usuario
Funciones de publicación
Errores

## Implementación {#section-vsy-1k4-xz}

Para implementar esta función, pase una asignación de objeto 1-1 de las cadenas que desee reemplazar al objeto de configuración de Javascript. Si no proporciona un campo, se utilizará el texto predeterminado.

Ejemplo:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" }; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Revisar / Interfaz de Clasificación {#section_iyv_zj4_xz}

Cadenas disponibles para la interfaz de usuario de Revisión y Clasificación.

| Elemento | Clave | Texto predeterminado |
|--- |--- |--- |
| Botones | editReviewBtn | Editar revisión |
|  | reviewBtn | [Escribir revisión](https://d.pr/i/QscA) |
|  | reviewClosed | [Reseñas cerradas](https://d.pr/i/zr7M) |
|  | showReviewBtn | [Mostrar revisión](https://d.pr/i/onxU) |
|  | seguir | Estoy interesado |
|  | shareText | Acabo de escribir una reseña. ¡Echa un vistazo! |
| Sugerencias de herramientas de clasificación | ratingValues | Una matriz. Default = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Nota: Los valores de la matriz deben duplicarse para asignar el mismo nombre tanto a la izquierda como a la derecha de cada estrella. |
| Subpartes de clasificación | ratingSubpartPlaceholder | Una matriz. Valor predeterminado = `[]` |
|  | ratingSubpartTitles | Una matriz. Valor predeterminado = `[]` |
|  | reviewStreamTitle | En blanco de forma predeterminada. Título de la sección resumen del examen. |
| Misc | averageRating | [Puntuación media del usuario](https://d.pr/i/QscA) |
|  | breakHeader | [Desglose de clasificación](https://d.pr/i/QscA) |
|  | útil | %s de %s encontrado útil |
|  | helpPlural | %s de %s encontrado útil |
|  | outOf | / |
|  | ratingType | star |

## Información de emisión {#section_wmv_yj4_xz}

Cadenas disponibles para la visualización e información del flujo de contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Clasificación | sortBy | En blanco de forma predeterminada. |
|  | sortHighestRated | [Clasificación más alta](https://d.pr/i/huTd) |
|  | sortLowestRated | [Clasificación más baja](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Más útil](https://d.pr/i/huTd) |
| Flujo misc. | showMore | Mostrar más |
| Flujo a gran velocidad | newComment | Nueva revisión |
|  | newComments | Nuevas revisiones |
| Recuentos de oyentes | listenerCount | escucha de persona |
|  | listenerCountPlural | personas escuchando |
| Recuentos de comentarios | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Recuentos del notificador de comentarios | commentNotifier | Nueva revisión |
|  | commentNotifierPlural | Nuevas revisiones |

## Información de autor/contenido {#section_osx_xj4_xz}

Cadenas disponibles para la información de contenido individual y de autor.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Desglose de subprocesos | reviewContentNotFoundMsg | [Esta revisión ya no es visible](https://d.pr/i/svXs) |
|  | backToComments | Volver a las revisiones |

## Acciones del usuario {#section_tlx_wj4_xz}

Cadenas disponibles para acciones del usuario: marcar, compartir y marcar el contenido existente como útil.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Pie de comentario | wasReviewHelpful | [¿Útil?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | ¿Útil? |
|  | ownDidReviewHelpful | [Encontré útil.](https://d.pr/i/Q0mA) |
|  | reviewDidHelpful | [Sí](https://d.pr/i/Q0mA) |
|  | helpDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewDidNotHelpful | [No ](https://d.pr/i/Q0mA) |
| Modo de voto | voteTitle | ¿Fue útil esta revisión? |
|  | voteDownvote | No |
|  | voteReplyTitle | ¿Fue útil esta respuesta? |
|  | voteTitle | ¿Fue útil este comentario? |
|  | voteUpvote | Sí |
| Modo de marca | flagTitle | Marcar la revisión de %s |
|  | flagSuccessMsg | La revisión se ha marcado. |
| Marcar como móvil | flagConfirmationMessage | ¿Marcar la revisión de %s como %s? |
| Modo de mención | mentionDefaultText | ¡Te mencioné en una reseña de Livefyre! |
| Compartir modal | shareTitle | Compartir revisión |

## Funciones de publicación {#section_yl1_wj4_xz}

Cadenas disponibles para los usuarios que publican revisiones.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Editor | bodyPlaceholder | Escribir revisión... |
|  | postEditButton | Editar  |
|  | postEditCancelButton | Cancelar |
|  | postAsButton | Revisión posterior como... |
|  | postButton | Revisión posterior |
|  | postReplyAsButton | Publicar como... |
|  | postReplyButton | Anuncio |
|  | shareButton | Compartir |
|  | titlePlaceholder | Título… |

## Errores {#section_jbc_vj4_xz}

Cadenas disponibles para mensajes de error generales.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Errores | errorAlreadyPosted | Solo puede publicar una revisión. |
|  | errorAuthError | No está autorizado a publicar una revisión en esta conversación |
|  | errorCommentsNotAllowed | Las revisiones no se pueden publicar en este momento |
|  | errorDislikeOwnComment | No puede desagradar su propia revisión |
|  | errorDuplicate | Por más que le guste su reseña, no se le permite publicarla dos veces. |
|  | errorEditDuplicate | Debe cambiar el cuerpo de la revisión cuando la edite. |
|  | errorEditNotAllowed | No se le permite editar revisiones en esta conversación. |
|  | errorEditTimeExceeded | Lo sentimos, el período de edición de la revisión ha expirado. |
|  | errorEmpty | Parece que está intentando publicar una revisión vacía. |
|  | errorEmptyTitle | Parece que está intentando publicar un título vacío |
|  | errorFieldRating | clasificación por estrellas |
|  | errorFieldReview | review |
|  | errorFieldTitle | title |
|  | errorMaxChars | Lo siento, tu revisión es demasiado larga. Edite e inténtelo de nuevo. |
|  | errorMissingFields | Escriba un |
|  | errorRatingEmpty | No se puede enviar una clasificación vacía |
|  | errorRatingNotSet | Todas las clasificaciones deben estar configuradas |
|  | errorRatingNotValid | La clasificación debe ser un objeto |
|  | errorShowMore | Error al cargar más revisiones. |
|  | errorTitleMaxChars | Lo siento, tu título es demasiado largo. Edite e inténtelo de nuevo. |
|  | errorVoteOwnComment | No puede votar por su propia revisión |
