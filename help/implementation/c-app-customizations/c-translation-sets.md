---
description: Los conjuntos de traducción permiten especificar un idioma alternativo para las aplicaciones.
seo-description: Los conjuntos de traducción permiten especificar un idioma alternativo para las aplicaciones.
seo-title: Conjuntos de traducción
solution: Experience Manager
title: Conjuntos de traducción
uuid: 8ba66a61-5520-482a-bc0b-e4f6b57f1744
translation-type: tm+mt
source-git-commit: 366b7248c2f3b6994fa10419599e66fa1c8e5e48
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 7%

---


# Conjuntos de traducción {#translation-sets}

Los conjuntos de traducción permiten especificar un idioma alternativo para las aplicaciones.

<!-- 
c_translation_sets.dita
-->

Utilice la configuración de traducción para localizar aplicaciones en varios idiomas o para especificar texto alternativo para varias aplicaciones desde una ubicación en Studio. Por ejemplo, puede asegurarse de que todos los sitios en español utilicen el idioma español para todos los campos de la aplicación. También puede modificar el texto para que todos los campos coincidan con la voz y la presentación de su sitio o red.

Puede especificar la configuración de traducción para todas las aplicaciones, excepto Storify 2. Para obtener más información sobre los campos que puede localizar, consulte [Localizar cadenas](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Comentarios, Live Blog y Chat comparten el mismo conjunto de cadenas dentro de un conjunto de traducciones.

Especifique un conjunto de traducción para una red, sitio, aplicación o mediante una API.

Los conjuntos de traducción en diferentes niveles se anulan entre sí siguiendo este patrón:

* El conjunto de traducción de API anula todos los conjuntos de traducción en cualquier nivel (aplicación, red y sitio)
* El conjunto de traducción de aplicaciones anula los conjuntos de traducción a nivel de red y de sitio.
* Los conjuntos de traducción a nivel de sitio anulan los conjuntos de traducción a nivel de red.

## Revisar cadenas de texto {#c-review-text-strings}

Personalización de las cadenas de texto para Livefyre Reviews.

Esta página lista y describe las cadenas disponibles para la personalización en las aplicaciones de revisión. Las cadenas que se muestran aquí se suman a las cadenas predeterminadas de las aplicaciones principales de Livefyre y se anulan, enumeradas en Personalizaciones de cadenas. Donde se muestran los duplicados, las cadenas que aparecen en estas tablas son las predeterminadas para las aplicaciones de críticas.

* Implementación
* Interfaz de revisión y clasificación
* Información de flujo
* Información de autor/contenido
* Acciones del usuario
* Funciones de anuncio
* Errores

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

## Interfaz de clasificación/revisión {#section_iyv_zj4_xz}

Cadenas disponibles para la interfaz de usuario Revisar y clasificar.

| Elemento | Clave | Texto predeterminado |
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Botones |  |  |
|  | editReviewBtn | Editar revisión |
|  | reviewBtn | Escribir revisión |
|  | reseñasCerradas | Reseñas cerradas |
|  | showReviewBtn | Mostrar revisión |
|  | seguir | Me interesa |
|  | shareText | Acabo de escribir una reseña. ¡Echa un vistazo! |
| Sugerencias de herramientas de clasificación |  |  |
|  | ratingValues | Una matriz. Predeterminado = [‘Pobre’, ‘Pobre’, ‘Justo’, ‘Justo’, ‘Promedio’, ‘Promedio’, ‘Bueno’, ‘Excelente’, ‘Excelente’]; |
|  |  | Nota: Los valores de la matriz deben duplicarse para asignar el mismo nombre a la mitad izquierda y a la derecha de cada estrella. |
| Subpartes de clasificación |  |  |
|  | ratingSubpartPlaceholder | Una matriz. Valor predeterminado = [] |
|  | ratingSubpartTitles | Una matriz. Valor predeterminado = [] |
|  | reviewStreamTitle | En blanco de forma predeterminada. Título de la sección de resumen del examen. |
| Misc |  |  |
|  | averageRating | Clasificación promedio de usuarios |
|  | breakHeader | Desglose de clasificación |
|  | útil | %s de %s encontró útil |
|  | helpPlural | %s de %s encontró útil |
|  | outOf | / |
|  | ratingType | star |

## Información de flujo {#section_wmv_yj4_xz}

Cadenas disponibles para la información y visualización del flujo de contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Clasificación* |  |  |
|  | sortBy | *En blanco de forma predeterminada.* |
|  | sortHighestRated | [Clasificación más alta](https://d.pr/i/huTd) |
|  | sortLowestRated | [Clasificación más baja](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Más útil](https://d.pr/i/huTd) |
| *Misc de flujo.* |  |  |
|  | showMore | Mostrar más |
| *Velocidad de flujo alta* |  |  |
|  | newComment | Nueva revisión |
|  | newComments | Nuevas revisiones |
| *Recuentos de escucha* |  |  |
|  | listenerCount | persona que escucha |
|  | listenerCountPlural | personas escuchando |
| *Recuentos de comentarios* |  |  |
|  | commentCountLabel | LiveReviews |
|  | commentCountLabelPlural | LiveReviews |
| *Recuentos de notificaciones de comentarios* |  |  |
|  | commentNotifier | Nueva revisión |
|  | commentNotifierPlural | Nuevas revisiones |

## Información de autor/contenido {#section_osx_xj4_xz}

Las cadenas están disponibles para la información de contenido individual y de autor.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Grupo de trabajo de subprocesos* |  |  |
|  | reviewContentNotFoundMsg | [Esta revisión ya no está visible](https://d.pr/i/svXs) |
|  | backToComments | Volver a las revisiones |

## Acciones del usuario {#section_tlx_wj4_xz}

Cadenas disponibles para acciones de usuario: marcar, compartir y marcar el contenido existente como útil.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Pie de comentario* |  |  |
|  | wasReviewHelpful | [¿Útil?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | ¿Útil? |
|  | ownWasReviewHelpful | [Encontrado útil.](https://d.pr/i/Q0mA) |
|  | reviewWasHelpful | [Sí](https://d.pr/i/Q0mA) |
|  | helpDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotHelpful | [No ](https://d.pr/i/Q0mA) |
| *Modo de voto* |  |  |
|  | voteTitle | ¿Fue útil esta revisión? |
|  | voteDownvote | No |
|  | voteReplyTitle | ¿Fue útil esta respuesta? |
|  | voteTitle | ¿Este comentario fue útil? |
|  | voteUpvote | Sí |
| *Indicador modal* |  |  |
|  | flagTitle | Marcar la revisión de %s |
|  | flagSuccessMsg | Se ha marcado la revisión. |
| *Marcar móvil* |  |  |
|  | flagConfirmationMessage | ¿Marcar la revisión de %s como %s? |
| *Mención modal* |  |  |
|  | sayDefaultText | ¡Te mencioné en una reseña de Livefyre! |
| *Compartir modal* |  |  |
|  | shareTitle | Compartir revisión |

## Funciones de anuncio {#section_yl1_wj4_xz}

Cadenas disponibles para los usuarios que publican revisiones.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Editor* |  |  |
|  | bodyPlaceholder | Escribir revisión... |
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
| Errores |  |  |
|  | errorAlreadyPosted | Solo puede publicar una revisión. |
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
|  | errorMaxChars | Lo sentimos, tu revisión es demasiado larga. Edite e inténtelo de nuevo. |
|  | errorMissingFields | Escriba un |
|  | errorRatingEmpty | No se puede enviar una clasificación vacía |
|  | errorRatingNotSet | Todas las clasificaciones deben configurarse |
|  | errorRatingNotvalid | La clasificación debe ser un objeto |
|  | errorShowMore | Se produjo un error al cargar más revisiones. |
|  | errorTitleMaxChars | Lo siento, tu título es demasiado largo. Edite e inténtelo de nuevo. |
|  | errorVoteOwnComment | No puede votar por su propia revisión |

## Identifica cadenas de texto {#c_sidenotes_text_strings}

Personalización de las cadenas de texto para Livefyre Sidenotes

<!-- 

c_sidenotes_text_strings.dita

 -->

Esta página lista y describe todas las cadenas disponibles para la personalización en las aplicaciones de Sidenotes. Para obtener información sobre las cadenas disponibles para las aplicaciones principales de Livefyre, consulte Personalizaciones de cadenas.

* Implementación
* Auth
* Información de flujo
* Información de autor/contenido
* Acciones del usuario
* Funciones de anuncio
* Interfaz del moderador
* Errores

## Implementación {#section_wp2_ql4_xz}

Para implementar esta función, pase una asignación de objetos 1-1 de las cadenas que desee reemplazar al objeto de configuración de Javascript. Si no se proporciona un campo, se utilizará el texto predeterminado.

Ejemplo:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Autenticación {#section_pqf_3l4_xz}

Cadenas disponibles para el proceso de autenticación y en los menús de usuario autenticados.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Cadenas de menú de autenticación* |  |  |
|  | menuAuthSignInBtn | Iniciar sesión |
|  | menuAuthSignedInMsg | Debe iniciar sesión en {action} |
|  | menuUserEditProfile | Editar perfil |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Cerrar sesión |
|  | menuUserBackBtn | Todas |

## Información de flujo {#section_wpy_gl4_xz}

Cadenas disponibles para la información y visualización del flujo de contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Opciones del menú Información* |  |  |
|  | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Ayuda |
|  | menuInfoLivefyreLink | Visite Livefyre.com |

## Información de autor/contenido {#section_dhb_gl4_xz}

Las cadenas están disponibles para la información de contenido individual y de autor.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentpendingTag | Pendiente |
|  | commentReadMoreLink | Más información... |
|  | commentReplyLink | Ver {número} respuestas |
|  | commentReplyLinkSing | Consulte la respuesta |
|  | commentVoteCount | votes |
|  | commentVoteCountSing | voto |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | *Una matriz. Predeterminado = *[ ‘enero’, ‘febrero’, ‘marzo’, ‘abril’, ‘mayo’, ‘junio’, ‘julio’, ‘agosto’, ‘septiembre’, ‘octubre’, ‘noviembre’, ‘diciembre’ ] |
|  | questionExplanation | Ahora puede leer y escribir comentarios directamente sobre oraciones, párrafos, imágenes y comillas. <br>Resalte el texto y haga clic en el icono o haga clic en el icono al final de cada párrafo. |
|  | questionMockText | Lo que es &quot;conocido familiar&quot; no se conoce correctamente, sólo por la razón de que es &quot;familiar&quot;. |
|  | questionTitle | ¿Qué es un Sidenote? |

## Acciones del usuario {#section_qxd_fl4_xz}

Cadenas disponibles para acciones de usuario: marcar, compartir y indicar que gusta el contenido existente.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Opciones del menú Respuesta* |  |  |
|  | menuReplyViewTitle | Detalles |
|  | menuReplyViewReply | Responder a conversación |
| *Opciones de menú Compartir* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Compartir |
| *Opciones del menú Indicador* |  |  |
|  | menuFlagOptionDisact | Rechazar |
|  | menuFlagOptionOffensive | Ofensivo |
|  | menuFlagOptionOffTopic | Desactivar tema |
|  | menuFlagOptionSpam | Correo no deseado |
|  | menuFlagTitle | Marcar como... |
|  | facebookShareCaption | Identifica las notas en &quot;{title}&quot; |
| *Opciones de usuario móvil* |  |  |
|  | sliderCommentTally | of |
|  | sliderInviteRead | Leído |
|  | sliderInviteWrite | Escritura |
|  | sliderLoading | Cargando… |
|  | sliderWriteText | ¿Qué piensas? Toque para escribir. |

## Funciones de anuncio {#section_xzf_2l4_xz}

Cadenas disponibles para los usuarios que publican contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | editorEditBtn | Guardar |
|  | editorEditPosting | Guardando... |
|  | editorEditReplyTitle | Editar respuesta |
|  | editorEditTitle | Editar Sidenote |
|  | editorMarcadorDePosición | ¿Qué piensas? |
|  | editorPostBtn | Publicar Sidenote |
|  | editorPostBtnMobile | Anuncio |
|  | editorPosting | Colocar un anuncio… |
|  | editorResponderBtn | Anunciar respuesta |
|  | editorReplyTitle | Escribir respuesta |
|  | editorTítulo | Escribir Sidenote |
|  | emptyImageBlockTxt | ¿Qué piensas? |
|  | emptyTextBlockTxt | + |
|  | responseBtn | Responder |
|  | threadReplyBtn | Responder a conversación |
| *Opciones del menú Eliminar* |  |  |
|  | menuConfirmAccept | Sí, {action} |
|  | menuConfirmCancel | Cancelar |
|  | menuConfirmTitle | ¿Está seguro? |
| *Opciones de menú Etc* |  |  |
|  | menuEtcOptionApprove | Aprobar |
|  | menuEtcOptionDelete | Eliminar |
|  | menuEtcOptionEdit | Editar  |
|  | menuEtcOptionFlag | Marcar |
|  | menuEtcOptionShare | Compartir |
|  | menuEtcPostedAt | Publicado el {date} |
|  | menuEtcTitle | Más |

## Interfaz del moderador {#section_o5f_dl4_xz}

Cadenas disponibles para la interfaz del moderador autenticado por el usuario.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Mensajes de confirmación del menú Más* |  |  |
|  | notificationApproved | Aprobado |
|  | notificationDeleted | Eliminado |
|  | notificationFlagged | Marcado |

## Errores {#section_gtk_cl4_xz}

Cadenas disponibles para mensajes de error generales.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | errorConnection | Oh-oh. No parece que tenga una buena conexión. |
|  | errorDuplicate | También nos gusta tu nota, pero no puedes publicarla dos veces. |
|  | errorGeneral | Se ha producido un error. Inténtelo de nuevo. |
|  | errorServer | Algo salió mal con nuestro servidor. ¿Intenta eso otra vez? |
