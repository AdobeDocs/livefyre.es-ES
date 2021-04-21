---
description: Los conjuntos de traducciones permiten especificar un idioma alternativo para las aplicaciones.
title: Conjuntos de traducción
exl-id: 1de99602-b97e-42e9-8450-39abd4ba2f9b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 7%

---

# Conjuntos de traducciones{#translation-sets}

Los conjuntos de traducciones permiten especificar un idioma alternativo para las aplicaciones.

Utilice la configuración de traducción para localizar aplicaciones en varios idiomas o para especificar texto alternativo para varias aplicaciones desde una ubicación en Studio. Por ejemplo, puede asegurarse de que todos los sitios en español utilicen español para todos los campos de la aplicación. También puede modificar el texto para que todos los campos coincidan con la voz y la presentación de su sitio o red.

Puede especificar la configuración de traducción para todas las aplicaciones, excepto Storify 2. Para obtener más información sobre los campos que puede localizar, consulte [Localize Strings](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md#c-localize-strings).

Comentarios, blogs en directo y chat comparten el mismo conjunto de cadenas dentro de un conjunto de traducciones.

Especifique un conjunto de traducción para una red, sitio, aplicación o mediante una API.

Los conjuntos de traducción en diferentes niveles se anulan entre sí siguiendo este patrón:

El conjunto de traducción de API anula todos los conjuntos de traducción a cualquier nivel (aplicación, red y sitio)
El conjunto de traducción de aplicaciones anula los conjuntos de traducción a nivel de red y a nivel de sitio.
Los conjuntos de traducción a nivel de sitio anulan los conjuntos de traducción a nivel de red.

## Revisar cadenas de texto {#c_review_text_strings}

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
|  | reviewBtn | Escribir revisión |
|  | reviewClosed | Reseñas cerradas |
|  | showReviewBtn | Mostrar revisión |
|  | seguir | Estoy interesado |
|  | shareText | Acabo de escribir una reseña. ¡Echa un vistazo! |
| Sugerencias de herramientas de clasificación | ratingValues | Una matriz. Default = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Nota: Los valores de la matriz deben duplicarse para asignar el mismo nombre tanto a la izquierda como a la derecha de cada estrella. |
| Subpartes de clasificación | ratingSubpartPlaceholder | Una matriz. Valor predeterminado = [] |
|  | ratingSubpartTitles | Una matriz. Valor predeterminado = [] |
|  | reviewStreamTitle | En blanco de forma predeterminada. Título de la sección resumen del examen. |
| Misc | averageRating | Puntuación media del usuario |
|  | breakHeader | Desglose de clasificación |
|  | útil | %s de %s encontrado útil |
|  | helpPlural | %s de %s encontrado útil |
|  | outOf | / |
|  | ratingType | star |

## Información de emisión {#section_wmv_yj4_xz}

Cadenas disponibles para la visualización e información del flujo de contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Clasificación | sortBy | *En blanco de forma predeterminada.* |
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

## Muestra las cadenas de texto {#c_sidenotes_text_strings}

Personalización de las cadenas de texto para notas de Livefyre

Esta página enumera y describe todas las cadenas disponibles para la personalización en las aplicaciones de Notas . Para obtener información sobre las cadenas disponibles para las aplicaciones principales de Livefyre, consulte Personalizaciones de cadenas.

Implementación
Auth
Información de flujo
Información de autor/contenido
Acciones del usuario
Funciones de publicación
Interfaz del moderador
Errores

## Implementación {#section_wp2_ql4_xz}

Para implementar esta función, pase una asignación de objeto 1-1 de las cadenas que desee reemplazar al objeto de configuración de Javascript. Si no proporciona un campo, se utilizará el texto predeterminado.

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
| Cadenas de menú de autenticación | menuAuthSignInBtn | Iniciar sesión |
|  | menuAuthSignedInMsg | Debe iniciar sesión en {action} |
|  | menuUserEditProfile | Editar perfil |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Cerrar sesión |
|  | menuUserBackBtn | Todas |

## Información de emisión {#section_wpy_gl4_xz}

Cadenas disponibles para la visualización e información del flujo de contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Opciones del menú Información | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Ayuda |
|  | menuInfoLivefyreLink | Visite Livefyre.com |

## Información de autor/contenido {#section_dhb_gl4_xz}

Cadenas disponibles para la información de contenido individual y de autor.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentPendingTag | Pendiente |
|  | commentReadMoreLink | Más información... |
|  | commentReplyLink | Ver {número} respuestas |
|  | commentReplyLinkSing | Consulte respuesta |
|  | commentVoteCount | vote |
|  | commentVoteCountSing | voto |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | Una matriz. Predeterminado =[ &quot;Enero&quot;, &quot;Febrero&quot;, &quot;Marzo&quot;, &quot;Abril&quot;, &quot;Mayo&quot;, &quot;Junio&quot;, &quot;Julio&quot;, &quot;Agosto&quot;, &quot;Septiembre&quot;, &quot;Octubre&quot;, &quot;Noviembre&quot;, &quot;Diciembre&quot; ] |
|  | questionExplanation | Ahora puede leer y escribir comentarios directamente sobre oraciones, párrafos, imágenes y comillas.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Resalte el </span> texto y haga clic en el  <span class="&rdquo;fycon-write&rdquo;"></span> icono o haga clic en el  <span class="&rdquo;fycon-action-view&rdquo;"></span> icono situado al final de cada párrafo. |
|  | questionMockText | Lo que es &quot;conocido&quot; no se conoce adecuadamente, simplemente por ser &quot;familiar&quot;. |
|  | questionTitle | ¿Qué es un Sidenote? |

## Acciones del usuario {#section_qxd_fl4_xz}

Cadenas disponibles para acciones del usuario: marcar, compartir y indicar que gusta el contenido existente.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Opciones del menú Respuesta | menuReplyViewTitle | Detalles |
|  | menuReplyViewReply | Responder a conversación |
| Opciones de menú Compartir | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Compartir |
| Opciones del menú Indicador | menuFlagOptionDisaccept | Desacuerdo |
|  | menuFlagOptionOffensive | Ofensivo |
|  | menuFlagOptionOffTopic | Desactivar tema |
|  | menuFlagOptionSpam | Correo no deseado |
|  | menuFlagTitle | Marcar como... |
|  | facebookShareCaption | Notas sobre &quot;{title}&quot; |
| Opciones de usuario móviles | sliderCommentTally | of |
|  | sliderInviteRead | Leído |
|  | sliderInviteWrite | Escritura |
|  | sliderLoading | Cargando… |
|  | sliderWriteText | ¿Qué piensas? Toque para escribir. |

## Funciones de publicación {#section_xzf_2l4_xz}

Cadenas disponibles para los usuarios que publican contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | editorEditBtn | Guardar |
|  | editorEditPosting | Guardando... |
|  | editorEditReplyTitle | Editar respuesta |
|  | editorEditTitle | Editar nota |
|  | editorMarcador de posición | ¿Qué piensas? |
|  | editorPostBtn | Publicar Sidenote |
|  | editorPostBtnMobile | Anuncio |
|  | editorPosting | Colocar un anuncio… |
|  | editorReplyBtn | Anunciar respuesta |
|  | editorReplyTitle | Escribir respuesta |
|  | editorTitle | Escribir Sidenote |
|  | emptyImageBlockText | ¿Qué piensas? |
|  | emptyTextBlockText | + |
|  | replyBtn | Responder |
|  | threadReplyBtn | Responder a conversación |
| Opciones del menú Eliminar | menuConfirmAccept | Sí, {action} |
|  | menuConfirmCancel | Cancelar |
|  | menuConfirmTitle | ¿Está seguro? |
| Opciones de menú Etc | menuEtcOptionApprove | Aprobar |
|  | menuEtcOptionDelete | Eliminar |
|  | menuEtcOptionEdit | Editar  |
|  | menuEtcOptionFlag | Marcar |
|  | menuEtcOptionShare | Compartir |
|  | menuEtcPostedAt | Publicado el {fecha} |
|  | menuEtcTitle | Más |

## Interfaz de moderador {#section_o5f_dl4_xz}

Cadenas disponibles para la interfaz de moderador autenticada por el usuario.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Mensajes de confirmación del menú Más | notificationApproved | Aprobado |
|  | notificationDeleted | Eliminado |
|  | notificationFlagged | Marcado |

## Errores {#section_gtk_cl4_xz}

Cadenas disponibles para mensajes de error generales.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | errorConnection | Oh-oh. Parece que no tiene una buena conexión. |
|  | errorDuplicate | También nos gusta tu nota, pero no puedes publicarla dos veces. |
|  | errorGeneral | Se ha producido un error. Inténtelo de nuevo. |
|  | errorServer | Algo salió mal con nuestro servidor. ¿Intenta eso otra vez? |
