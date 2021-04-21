---
description: Personalización de las cadenas de texto para notas de Livefyre
title: Notas de cadena de texto
exl-id: 132a7c8d-10e1-419c-9d79-a40553e70785
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 12%

---

# Identifica cadenas de texto{#sidenotes-text-strings}

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
|  | datetimeMonths | Una matriz. Valor predeterminado =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
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
