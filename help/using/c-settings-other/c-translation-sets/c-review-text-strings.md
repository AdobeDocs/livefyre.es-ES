---
description: Personalización de cadenas de texto para revisiones de Livefyre.
seo-description: Personalización de cadenas de texto para revisiones de Livefyre.
seo-title: Revisar cadenas de texto
solution: Experience Manager
title: Revisar cadenas de texto
uuid: 86251 e 49-bc 73-4 eec -9 f 9 b-b 4 b 0 a 5 b 42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Revisar cadenas de texto{#review-text-strings}

Personalización de cadenas de texto para revisiones de Livefyre.

Esta página enumera y describe las cadenas disponibles para la personalización en Aplicaciones de revisión. Las cadenas enumeradas aquí son además de las cadenas predeterminadas de las aplicaciones principales de Livefyre, enumeradas en Personalizaciones de cadenas. Cuando se enumeran duplicados, las cadenas enumeradas en estas tablas son el valor predeterminado para las aplicaciones de revisión.

Errores de autor de la información
del flujo de la interfaz
de clasificación/revisión de implementación/Información
del contenido Acciones
de post Post

## Implementación {#section-vsy-1k4-xz}

Para implementar esta función, pase una asignación de objeto 1-1 de las cadenas que desee sobrescribir al objeto de configuración Javascript. Si no se proporciona un campo, se utilizará el texto predeterminado.

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

## Interfaz de revisión/clasificación {#section_iyv_zj4_xz}

Cadenas disponibles para la interfaz de usuario de revisión y clasificación.

| Elemento | Clave | Texto predeterminado |
|--- |--- |--- |
| Botones | Editreviewbtn | Editar revisión |
|  | Reviewbtn | [Escribir revisión](https://d.pr/i/QscA) |
|  | Reviewsclosed | [Revisiones cerradas](https://d.pr/i/zr7M) |
|  | Showreviewbtn | [Mostrar revisión](https://d.pr/i/onxU) |
|  | seguir | Estoy interesado |
|  | Sharetext | Acabo de escribir una reseña. ¡Descárguelo! |
| Información sobre herramientas de clasificación | Ratingvalues | Una matriz. Default = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Nota: Los valores de la matriz deben duplicarse para asignar a la izquierda y a la derecha de cada estrella el mismo nombre. |
| Subsecciones de clasificación | Ratingsubpartplaceholders | Una matriz. Default = `[]` |
|  | Ratingsubparttitles | Una matriz. Default = `[]` |
|  | Reviewstreamtitle | En blanco de forma predeterminada. Título de la sección resumen de la revisión. |
| Misc | Averagerating | [Clasificación promedio de usuario](https://d.pr/i/QscA) |
|  | Breakdownheader | [Desglose de clasificación](https://d.pr/i/QscA) |
|  | serviciales | Se encontraron % s de % s útiles |
|  | Helpfulplural | Se encontraron % s de % s útiles |
|  | Outof | / |
|  | Ratingtype | estrella |

## Información del flujo {#section_wmv_yj4_xz}

Cadenas disponibles para la información de flujo de contenido y visualización.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Ordenar | Sortby | En blanco de forma predeterminada. |
|  | Sorthighestrated | [Clasificación más alta](https://d.pr/i/huTd) |
|  | Sortlowestrated | [Clasificación más baja](https://d.pr/i/huTd) |
|  | Sortmosthelpful | [Más serviciales](https://d.pr/i/huTd) |
| Stream misc. | Showmore | Mostrar más |
| Velocidad alta de flujo | Newcomment | Nueva revisión |
|  | Newcomments | Nuevas revisiones |
| Recuento de detectores | Listenercount | persona que escucha |
|  | Listenercountplural | personas que escucha |
| Recuento de comentarios | Commentcountlabel | Livereviews<strong> | </strong>% s |
|  | Commentcountlabelplural | Livereviews<strong> | </strong>% s |
| Recuento de notificadores de comentarios | Commentnotificfier | Nueva revisión |
|  | Commentnotificfierplural | Nuevas revisiones |

## Información de autor/contenido {#section_osx_xj4_xz}

Listas disponibles para la información de contenido y de autor individual.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Grupo de trabajo de debate | Reviewscontentnotfoundmsg | [Esta revisión ya no está visible](https://d.pr/i/svXs) |
|  | Backtocomments | Regresar a Críticas |

## Acciones del usuario {#section_tlx_wj4_xz}

Cadenas disponibles para las acciones del usuario: marcar, compartir y marcar el contenido existente como útil.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Pie de página de comentario | Wasreviewhelpful | [¿Resulta útil?](https://d.pr/i/Q0mA) |
|  | Wasreviewhelpfulmobile | ¿Resulta útil? |
|  | Ownwasreviewhelpful | [Se ha encontrado una utilidad.](https://d.pr/i/Q0mA) |
|  | Reviewwashelpful | [Sí](https://d.pr/i/Q0mA) |
|  | Helpfuldivider | [& amp; vert;](https://d.pr/i/Q0mA) |
|  | Reviewwasnothelpful | [No](https://d.pr/i/Q0mA) |
| Votar modal | Votetitle | ¿Es útil esta revisión? |
|  | Votedownvote | No |
|  | Votereplytitle | ¿Es útil esta respuesta? |
|  | Votetitle | ¿Es útil este comentario? |
|  | Voteupvote | Sí |
| Modal, modal | Flagtitle | Revisión del indicador % s |
|  | Flagsuccessmsg | Se marcó la revisión. |
| Marcar móvil | Flagconfirmationmessage | ¿Marcar la revisión % s como % s? |
| Menciones modales | Mentiondefaulttext | ¡Lo mencioné en una revisión de Livefyre! |
| Compartir modal | Sharetitle | Compartir revisión |

## Funciones de anuncio {#section_yl1_wj4_xz}

Cadenas disponibles para los usuarios que publican revisiones.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Editor | Bodyplaceholder | Escribir revisión… |
|  | Posteditbutton | Editar |
|  | Posteditcancelbutton | Cancelar |
|  | Postasbutton | Publicar revisión como… |
|  | Postbutton | Revisión posterior |
|  | Postreplyasbutton | Anunciar como… |
|  | Postreplybutton | Anuncio |
|  | Sharebutton | Compartir |
|  | Titleplaceholder | Título… |

## Errores {#section_jbc_vj4_xz}

Cadenas disponibles para mensajes de error generales.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Errores | Erroralreadyposted | Solo puede publicar una revisión. |
|  | Errorautherror | No está autorizado a publicar una revisión en esta conversación |
|  | Errorcommentsnotallowed | Las revisiones no se pueden publicar en este momento |
|  | Errordisputowncomment | No puede disgustar su propia revisión |
|  | Errorduplicate | Al igual que le gusta la revisión, no tiene permiso para anunciarla dos veces. |
|  | Erroreditduplicate | Debe cambiar el cuerpo de la revisión cuando lo edite. |
|  | Erroreditnotallowed | No está autorizado a editar las revisiones de esta conversación. |
|  | Erroredittimeexceeded | Lo lamentamos, el período de edición de la revisión ha caducado. |
|  | Errorempty | Parece que está intentando publicar una revisión vacía. |
|  | Erroremptytitle | Parece que está intentando anunciar un título vacío |
|  | Errorfieldrating | clasificación de estrella |
|  | Errorfieldreview | revisar |
|  | Errorfieldtitle | title |
|  | Errormaxchars | La reseña es demasiado larga. Edite e inténtelo de nuevo. |
|  | Errormissingfields | Escriba un |
|  | Errorratingempty | No se puede enviar una clasificación vacía |
|  | Errorratingnotset | Se deben configurar todas las clasificaciones |
|  | Errorratingnotvalid | La clasificación debe ser un objeto |
|  | Errorshowmore | Se produjo un error al cargar más críticas. |
|  | Errortitlemaxchars | Su título es demasiado largo. Edite e inténtelo de nuevo. |
|  | Errorvoteowncomment | No puede votar por su propia revisión |

