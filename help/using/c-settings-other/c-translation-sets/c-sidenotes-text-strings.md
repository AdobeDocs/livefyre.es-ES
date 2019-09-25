---
description: Personalización de las cadenas de texto para Livefyre Sidenotes
seo-description: Personalización de las cadenas de texto para Livefyre Sidenotes
seo-title: Identifica cadenas de texto
solution: Experience Manager
title: Identifica cadenas de texto
uuid: a3735237-e55d-4bc0-b88d-8a323980ee09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Identifica cadenas de texto{#sidenotes-text-strings}

Personalización de las cadenas de texto para Livefyre Sidenotes

Esta página enumera y describe todas las cadenas disponibles para la personalización en las aplicaciones de Sidenotes. Para obtener información sobre las cadenas disponibles para las aplicaciones principales de Livefyre, consulte Personalizaciones de cadenas.

ImplementationAuthStream InfoAuthor / Content InfoAcciones de usuario Funciones de anuncioInterfaz de moderadorErrores

## Implementación {#section_wp2_ql4_xz}

Para implementar esta función, pase una asignación de objetos 1-1 de las cadenas que desee reemplazar al objeto de configuración de Javascript. Si no proporciona un campo, se utilizará el texto predeterminado.

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

## Información de flujo {#section_wpy_gl4_xz}

Cadenas disponibles para la información y visualización del flujo de contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Opciones del menú Información | menuInfoCopyright | © Livefyre, Inc. 2014 |
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
|  | datetimeMonths | Una matriz. Valor predeterminado =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionExplanation | Ahora puede leer y escribir comentarios directamente sobre oraciones, párrafos, imágenes y comillas.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Resalte el texto</span> y haga clic en el <span class="&rdquo;fycon-write&rdquo;"></span> icono o haga clic en el <span class="&rdquo;fycon-action-view&rdquo;"></span> icono al final de cada párrafo. |
|  | questionMockText | Lo que es "conocido familiar" no se conoce correctamente, sólo por la razón de que es "familiar". |
|  | questionTitle | ¿Qué es un Sidenote? |

## Acciones del usuario {#section_qxd_fl4_xz}

Cadenas disponibles para acciones de usuario: marcar, compartir y indicar que gusta el contenido existente.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Opciones del menú Respuesta | menuReplyViewTitle | Detalles |
|  | menuReplyViewReply | Responder a conversación |
| Opciones de menú Compartir | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Compartir |
| Opciones del menú Indicador | menuFlagOptionDisact | Rechazar |
|  | menuFlagOptionOffensive | Ofensivo |
|  | menuFlagOptionOffTopic | Desactivar tema |
|  | menuFlagOptionSpam | Correo no deseado |
|  | menuFlagTitle | Marcar como... |
|  | facebookShareCaption | Identifica las notas en "{title}" |
| Opciones de usuario móvil | sliderCommentTally | of |
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
| Opciones del menú Eliminar | menuConfirmAccept | Sí, {action} |
|  | menuConfirmCancel | Cancelar |
|  | menuConfirmTitle | ¿Está seguro? |
| Opciones de menú Etc | menuEtcOptionApprove | Aprobar |
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
| Mensajes de confirmación del menú Más | notificationApproved | Aprobado |
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

