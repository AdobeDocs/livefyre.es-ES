---
description: Los conjuntos de traducción permiten especificar idioma alternativo para
  aplicaciones.
seo-description: Los conjuntos de traducción permiten especificar idioma alternativo
  para aplicaciones.
seo-title: Conjuntos de traducción
solution: Experience Manager
title: Conjuntos de traducción
uuid: 8 ba 66 a 61-5520-482 a-bc 0 b-e 4 f 6 b 57 f 1744
translation-type: tm+mt
source-git-commit: 366b7248c2f3b6994fa10419599e66fa1c8e5e48

---


# Conjuntos de traducción {#translation-sets}

Los conjuntos de traducción permiten especificar idioma alternativo para aplicaciones.

<!-- 
c_translation_sets.dita
-->

Utilice la configuración de traducción para localizar aplicaciones en varios idiomas o para especificar texto alternativo para varias aplicaciones desde una ubicación en Studio. Por ejemplo, puede asegurarse de que todos los sitios en español utilicen el idioma español para todos los campos de la aplicación. También puede modificar el texto para que todos los campos coincidan con la voz y la presentación del sitio o la red.

Puede especificar la configuración de traducción para todas las aplicaciones, excepto Storify 2. Para obtener más información sobre los campos que puede localizar, consulte [Localización de cadenas](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Los comentarios, Live Blog y chat comparten el mismo conjunto de cadenas dentro de un conjunto de traducción.

Especifique un conjunto de traducción para una red, un sitio, una aplicación o una API.

Los conjuntos de traducción en distintos niveles anulan los unos a los otros siguiendo este patrón:

* La configuración de traducción de API anula cualquier conjunto de traducción en cualquier nivel (aplicación, red y sitio)
* La traducción de la aplicación anula conjuntos de traducción a nivel de red y de sitio.
* Los conjuntos de traducción a nivel de sitio anulan los conjuntos de traducción a nivel de red.

## Revisar cadenas de texto {#c-review-text-strings}

Personalización de cadenas de texto para revisiones de Livefyre.

Esta página enumera y describe las cadenas disponibles para la personalización en Aplicaciones de revisión. Las cadenas enumeradas aquí son además de las cadenas predeterminadas de las aplicaciones principales de Livefyre, enumeradas en Personalizaciones de cadenas. Cuando se enumeran duplicados, las cadenas enumeradas en estas tablas son el valor predeterminado para las aplicaciones de revisión.

* Implementación
* Interfaz de revisión/clasificación
* Información del flujo
* Información de autor/contenido
* Acciones del usuario
* Funciones de anuncio
* Errores

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
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Botones |  |  |
|  | Editreviewbtn | Editar revisión |
|  | Reviewbtn | Escribir revisión |
|  | Reviewsclosed | Revisiones cerradas |
|  | Showreviewbtn | Mostrar revisión |
|  | seguir | Estoy interesado |
|  | Sharetext | Acabo de escribir una reseña. ¡Descárguelo! |
| Información sobre herramientas de clasificación |  |  |
|  | Ratingvalues | Una matriz. Predeterminado =[' Deficiente ',' Deficiente ',' Justo ',' Justo ',' Promedio ',' Promedio ',' Bueno ',' Buena ',' Excelente ',' Excelente ']; |
|  |  | Nota: Los valores de la matriz deben duplicarse para asignar a la izquierda y a la derecha de cada estrella el mismo nombre. |
| Subsecciones de clasificación |  |  |
|  | Ratingsubpartplaceholders | Una matriz. Default =[] |
|  | Ratingsubparttitles | Una matriz. Default =[] |
|  | Reviewstreamtitle | En blanco de forma predeterminada. Título de la sección resumen de la revisión. |
| Misc |  |  |
|  | Averagerating | Clasificación promedio de usuario |
|  | Breakdownheader | Desglose de clasificación |
|  | serviciales | Se encontraron % s de % s útiles |
|  | Helpfulplural | Se encontraron % s de % s útiles |
|  | Outof | / |
|  | Ratingtype | estrella |

## Información del flujo {#section_wmv_yj4_xz}

Cadenas disponibles para la información de flujo de contenido y visualización.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Ordenar* |  |  |
|  | Sortby | *En blanco de forma predeterminada.* |
|  | Sorthighestrated | [Clasificación más alta](https://d.pr/i/huTd) |
|  | Sortlowestrated | [Clasificación más baja](https://d.pr/i/huTd) |
|  | Sortmosthelpful | [Más serviciales](https://d.pr/i/huTd) |
| *Stream misc.* |  |  |
|  | Showmore | Mostrar más |
| *Velocidad alta de flujo* |  |  |
|  | Newcomment | Nueva revisión |
|  | Newcomments | Nuevas revisiones |
| *Recuento de detectores* |  |  |
|  | Listenercount | persona que escucha |
|  | Listenercountplural | personas que escucha |
| *Recuento de comentarios* |  |  |
|  | Commentcountlabel | Livereviews |
|  | Commentcountlabelplural | Livereviews |
| *Recuento de notificadores de comentarios* |  |  |
|  | Commentnotificfier | Nueva revisión |
|  | Commentnotificfierplural | Nuevas revisiones |

## Información de autor/contenido {#section_osx_xj4_xz}

Listas disponibles para la información de contenido y de autor individual.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Grupo de trabajo de debate* |  |  |
|  | Reviewscontentnotfoundmsg | [Esta revisión ya no está visible](https://d.pr/i/svXs) |
|  | Backtocomments | Regresar a Críticas |

## Acciones del usuario {#section_tlx_wj4_xz}

Cadenas disponibles para las acciones del usuario: marcar, compartir y marcar el contenido existente como útil.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Pie de página de comentario* |  |  |
|  | Wasreviewhelpful | [¿Resulta útil?](https://d.pr/i/Q0mA) |
|  | Wasreviewhelpfulmobile | ¿Resulta útil? |
|  | Ownwasreviewhelpful | [Se ha encontrado una utilidad.](https://d.pr/i/Q0mA) |
|  | Reviewwashelpful | [Sí](https://d.pr/i/Q0mA) |
|  | Helpfuldivider | [& amp; vert;](https://d.pr/i/Q0mA) |
|  | Reviewwasnothelpful | [No](https://d.pr/i/Q0mA) |
| *Votar modal* |  |  |
|  | Votetitle | ¿Es útil esta revisión? |
|  | Votedownvote | No |
|  | Votereplytitle | ¿Es útil esta respuesta? |
|  | Votetitle | ¿Es útil este comentario? |
|  | Voteupvote | Sí |
| *Modal, modal* |  |  |
|  | Flagtitle | Revisión del indicador % s |
|  | Flagsuccessmsg | Se marcó la revisión. |
| *Marcar móvil* |  |  |
|  | Flagconfirmationmessage | ¿Marcar la revisión % s como % s? |
| *Menciones modales* |  |  |
|  | Mentiondefaulttext | ¡Lo mencioné en una revisión de Livefyre! |
| *Compartir modal* |  |  |
|  | Sharetitle | Compartir revisión |

## Funciones de anuncio {#section_yl1_wj4_xz}

Cadenas disponibles para los usuarios que publican revisiones.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Editor* |  |  |
|  | Bodyplaceholder | Escribir revisión… |
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
| Errores |  |  |
|  | Erroralreadyposted | Solo puede publicar una revisión. |
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

## Cadenas de texto Sidenotes {#c_sidenotes_text_strings}

Personalización de cadenas de texto para Livefyre Sidenotes

<!-- 

c_sidenotes_text_strings.dita

 -->

Esta página enumera y describe todas las cadenas disponibles para la personalización en las aplicaciones Sidenotes. Para obtener información sobre las cadenas disponibles para las aplicaciones principales de Livefyre, consulte Personalizaciones de cadenas.

* Implementación
* Auth
* Información del flujo
* Información de autor/contenido
* Acciones del usuario
* Funciones de anuncio
* Interfaz del moderador
* Errores

## Implementación {#section_wp2_ql4_xz}

Para implementar esta función, pase una asignación de objeto 1-1 de las cadenas que desee sobrescribir al objeto de configuración Javascript. Si no proporciona un campo, se utilizará el texto predeterminado.

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

Cadenas disponibles para el proceso de autenticación y desde los menús de usuario autenticados.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Cadenas de menú de autenticación* |  |  |
|  | Menuauthsigninbtn | Iniciar sesión |
|  | Menuauthsignedemplsg | Debe iniciar sesión en {action} |
|  | Menuusereditprofile | Editar perfil |
|  | Menuuseradmin | Consola de administración |
|  | Menuuserlogout | Cerrar sesión |
|  | Menuuserbackbtn | Todos |

## Información del flujo {#section_wpy_gl4_xz}

Cadenas disponibles para la información de flujo de contenido y visualización.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Opciones del menú Información* |  |  |
|  | Menuinfocopyright | © Livefyre, Inc. 2014 |
|  | Menuinfohelp | Ayuda |
|  | Menuinfolivefyrelink | Visite Livefyre.com |

## Información de autor/contenido {#section_dhb_gl4_xz}

Listas disponibles para la información de contenido y de autor individual.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | Commentatortag commentModeratorTag | Mod |
|  | Commentpendingtag | Pendiente |
|  | Commentreadmorelink | Más información |
|  | Commentreplylink | Consulte {número} respuestas |
|  | Commentreplylinksing | Consulte respuesta |
|  | Commentvotecount | votos |
|  | Commentvotecountsing | votar |
|  | Datetimeminuteprefix | m |
|  | Datetimemonths | * Una matriz. Predeterminado = *[ ' Enero ',' Febrero ',' Marzo ',' Abril ',' Mayo ',' Junio ',' Julio ',' Agosto ',' Septiembre ',' Octubre ',' Noviembre ',' Diciembre ',' Diciembre ',' Diciembre ',' Diciembre ', ] |
|  | Explicación de preguntas | Ahora puede leer y escribir comentarios directamente sobre las frases, párrafos, imágenes y comillas. <br>Resalte el texto y haga clic en el icono o haga clic en el icono al final de cada párrafo. |
|  | Questionmocktext | Lo que se conoce «familiarmente» no es conocido, simplemente por el motivo de que es «familiar». |
|  | Questiontitle | ¿Qué es un Sidenote? |

## Acciones del usuario {#section_qxd_fl4_xz}

Cadenas disponibles para las acciones del usuario: marcar, compartir y indicar que gusta contenido existente.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Opciones del menú Responder* |  |  |
|  | Menurepliesviewtitle | Detalles |
|  | Menurepliesviewreply | Responder a la conversación |
| *Opciones del menú Compartir* |  |  |
|  | Menushareoptionfacebook | Facebook |
|  | Menushareoptiontwitter | Twitter |
|  | Menusharetitle | Compartir |
| *Opciones del menú Indicador* |  |  |
|  | Menuflagoptiondisagree | Rechazar |
|  | Menuflagoptionoffensive | Ofensiva |
|  | Menuflagoptionofftopic | Tema desactivado |
|  | Menuflagoptionspam | Correo no deseado |
|  | Menuflagtitle | Marcar como… |
|  | Facebooksharecaption | Sidenotes en «{title}» |
| *Opciones de usuario móvil* |  |  |
|  | Slidercommenttally | de |
|  | Sliderinviteread | Leer |
|  | Sliderinvitewrite | Escribir |
|  | Sliderloading | Cargando… |
|  | Sliderwritetext | ¿Qué piensa? Toque para escribir. |

## Funciones de anuncio {#section_xzf_2l4_xz}

Cadenas disponibles para los usuarios que envían contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | Editoreditbtn | Guardar |
|  | Editoreditposting | Guardando… |
|  | Editoreditreplytitle | Editar respuesta |
|  | Editoredittitle | Editar Sidenote |
|  | Editorplaceholder | ¿Qué piensa? |
|  | Editorpostbtn | Post Sidenote |
|  | Editorpostbtnmobile | Anuncio |
|  | Editorpost | Publicando… |
|  | Editorreplybtn | Publicar respuesta |
|  | Editorreplytitle | Escribir respuesta |
|  | Editortitle | Escribir sidenote |
|  | Emptyimageblocktxt | ¿Qué piensa? |
|  | Emptytextblocktxt | + |
|  | Replybtn | Responder |
|  | Threadreplybtn | Responder a la conversación |
| *Opciones de menú Eliminar* |  |  |
|  | Menuconfirmaccept | Sí, {action} |
|  | Menuconfirmcancel | Cancelar |
|  | Menuconfirmtitle | ¿Está seguro? |
| *Opciones de menú, etc.* |  |  |
|  | Menuetcoptionapprove | Aprobar |
|  | Menuetcoptiondelete | Eliminar |
|  | Menuetcoptionedit | Editar |
|  | Menuetcoptionflag | Indicador |
|  | Menuetcoptionshare | Compartir |
|  | Menuetcpostedat | Publicado el {date} |
|  | Menuetctitle | Más |

## Interfaz del moderador {#section_o5f_dl4_xz}

Cadenas disponibles para la interfaz de moderador autenticada por el usuario.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| *Mensajes de confirmación del menú Más* |  |  |
|  | Notificationapproved | Aprobado |
|  | Notificationdeleted | Eliminado |
|  | Notificationmarcado | Marcado |

## Errores {#section_gtk_cl4_xz}

Cadenas disponibles para mensajes de error generales.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | Errorconnection | Uh-oh. Parece que no tiene una buena conexión. |
|  | Errorduplicate | También nos gusta su nota, pero no puede anunciarla dos veces. |
|  | Errorgeneral | Se ha producido un error. Inténtelo de nuevo. |
|  | Errorserver | Algo salió mal con nuestro servidor. ¿Inténtelo de nuevo? |
