---
description: Personalización de las cadenas de texto para Livefyre Reviews.
seo-description: Personalización de las cadenas de texto para Livefyre Reviews.
seo-title: Revisar cadenas de texto
solution: Experience Manager
title: Revisar cadenas de texto
uuid: 86251e49-bc73-4eec-9f9b-b4b0a5b42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Revisar cadenas de texto{#review-text-strings}

Personalización de las cadenas de texto para Livefyre Reviews.

Esta página enumera y describe las cadenas disponibles para la personalización en las aplicaciones de revisión. Las cadenas que se muestran aquí se suman a las cadenas predeterminadas de las aplicaciones principales de Livefyre y se anulan, enumeradas en Personalizaciones de cadenas. En los casos en que se muestran duplicados, las cadenas que aparecen en estas tablas son las predeterminadas para las aplicaciones de críticas.

ImplementaciónRevisar / Interfaz de clasificaciónInformación de flujoAutor / Información de contenido Acciones de usuario Funciones de anuncioErrores

## Implementación {#section-vsy-1k4-xz}

Para implementar esta función, pase una asignación de objetos 1-1 de las cadenas que desee reemplazar al objeto de configuración de Javascript. Si no se proporciona un campo, se utilizará el texto predeterminado.

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

## Interfaz de revisión y clasificación {#section_iyv_zj4_xz}

Cadenas disponibles para la interfaz de usuario Revisar y clasificar.

| Elemento | Clave | Texto predeterminado |
|--- |--- |--- |
| Botones | editReviewBtn | Editar revisión |
|  | reviewBtn | [Escribir revisión](https://d.pr/i/QscA) |
|  | reseñasCerradas | [Reseñas cerradas](https://d.pr/i/zr7M) |
|  | showReviewBtn | [Mostrar revisión](https://d.pr/i/onxU) |
|  | seguir | Me interesa |
|  | shareText | Acabo de escribir una reseña. ¡Echa un vistazo! |
| Sugerencias de herramientas de clasificación | ratingValues | Una matriz. Predeterminado = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Nota: Los valores de la matriz deben duplicarse para asignar el mismo nombre a la mitad izquierda y a la derecha de cada estrella. |
| Subpartes de clasificación | ratingSubpartPlaceholder | Una matriz. Valor predeterminado = `[]` |
|  | ratingSubpartTitles | Una matriz. Valor predeterminado = `[]` |
|  | reviewStreamTitle | En blanco de forma predeterminada. Título de la sección de resumen del examen. |
| Misc | averageRating | [Clasificación promedio de usuarios](https://d.pr/i/QscA) |
|  | breakHeader | [Desglose de clasificación](https://d.pr/i/QscA) |
|  | útil | %s de %s encontró útil |
|  | helpPlural | %s de %s encontró útil |
|  | outOf | / |
|  | ratingType | star |

## Información de flujo {#section_wmv_yj4_xz}

Cadenas disponibles para la información y visualización del flujo de contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Clasificación |  sortBy | En blanco de forma predeterminada. |
|  | sortHighestRated | [Clasificación más alta](https://d.pr/i/huTd) |
|  | sortLowestRated | [Clasificación más baja](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Más útil](https://d.pr/i/huTd) |
| Misc de flujo. | showMore | Mostrar más |
| Velocidad de flujo alta | newComment | Nueva revisión |
|  | newComments | Nuevas revisiones |
| Recuentos de escucha | listenerCount | persona que escucha |
|  | listenerCountPlural | personas escuchando |
| Recuentos de comentarios | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Recuentos de notificaciones de comentarios | commentNotifier | Nueva revisión |
|  | commentNotifierPlural | Nuevas revisiones |

## Información de autor/contenido {#section_osx_xj4_xz}

Las cadenas están disponibles para la información de contenido individual y de autor.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Grupo de trabajo de subprocesos | reviewContentNotFoundMsg | [Esta revisión ya no está visible](https://d.pr/i/svXs) |
|  | backToComments | Volver a las revisiones |

## Acciones del usuario {#section_tlx_wj4_xz}

Cadenas disponibles para acciones de usuario: marcar, compartir y marcar el contenido existente como útil.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Pie de comentario | wasReviewHelpful | [¿Útil?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | ¿Útil? |
|  | ownWasReviewHelpful | [Encontrado útil.](https://d.pr/i/Q0mA) |
|  | reviewWasHelpful | [Sí](https://d.pr/i/Q0mA) |
|  | helpDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotHelpful | [No ](https://d.pr/i/Q0mA) |
| Modo de voto | voteTitle | ¿Fue útil esta revisión? |
|  | voteDownvote | No |
|  | voteReplyTitle | ¿Fue útil esta respuesta? |
|  | voteTitle | ¿Este comentario fue útil? |
|  | voteUpvote | Sí |
| Indicador modal | flagTitle | Marcar la revisión de %s |
|  | flagSuccessMsg | Se ha marcado la revisión. |
| Marcar móvil | flagConfirmationMessage | ¿Marcar la revisión de %s como %s? |
| Mención modal | sayDefaultText | ¡Te mencioné en una reseña de Livefyre! |
| Compartir modal | shareTitle | Compartir revisión |

## Funciones de anuncio {#section_yl1_wj4_xz}

Cadenas disponibles para los usuarios que publican revisiones.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Editor | bodyPlaceholder | Escribir revisión... |
|  | postEditButton | Editar  |
|  | postEditCancelButton | Cancelar |
|  | postAsButton | Anunciar revisión como... |
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
|  | errorAuthError | No está autorizado para publicar una revisión de esta conversación |
|  | errorCommentsNotAllowed | Las revisiones no se pueden publicar en este momento |
|  | errorDislikeOwnComment | No puede desagradar su propia revisión |
|  | errorDuplicate | Por mucho que le guste la revisión, no se le permite publicarla dos veces. |
|  | errorEditDuplicate | Debe cambiar el cuerpo de la revisión cuando la edite. |
|  | errorEditNotAllowed | No tiene permiso para editar reseñas de esta conversación. |
|  | errorEditTimeExceeded | El período de edición de la revisión ha caducado. |
|  | errorEmpty | Parece que está intentando publicar una revisión vacía. |
|  | errorEmptyTitle | Parece que está intentando publicar un título vacío |
|  | errorFieldRating | clasificación por estrellas |
|  | errorFieldReview | revisión |
|  | errorFieldTitle | title |
|  | errorMaxChars | Lo sentimos, tu revisión es demasiado larga. Edite e inténtelo nuevamente. |
|  | errorMissingFields | Escriba un |
|  | errorRatingEmpty | No se puede enviar una clasificación vacía |
|  | errorRatingNotSet | Todas las clasificaciones deben configurarse |
|  | errorRatingNotvalid | La clasificación debe ser un objeto |
|  | errorShowMore | Error al cargar más revisiones. |
|  | errorTitleMaxChars | Lo siento, tu título es demasiado largo. Edite e inténtelo nuevamente. |
|  | errorVoteOwnComment | No puede votar por su propia revisión |

