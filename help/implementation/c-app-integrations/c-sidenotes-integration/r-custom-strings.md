---
description: 'null'
seo-description: 'null'
seo-title: Identifica cadenas personalizadas
title: Identifica cadenas personalizadas
uuid: 73745273-d3fb-4569-8910-d149fb37a7b4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 11%

---


# Identifica cadenas personalizadas{#sidenotes-custom-strings}

Las cadenas personalizadas se aplican a través de un objeto insertado en el constructor Sidenotes y anulan las cadenas predeterminadas utilizadas en la aplicación. Estos pueden utilizarse para personalizar cualquier parte del idioma de acuerdo con las especificaciones del estilo o idioma. Las cadenas se combinarán automáticamente con valores predeterminados.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Clave | Valor predeterminado |
|---|---|
| appName | Notas de identidad |
| commentModeratorTag | Mod |
| commentpendingTag | Pendiente |
| commentReadMoreLink | Más información... |
| commentReplyLink | Ver {número} respuestas |
| commentReplyLinkSing | Consulte la respuesta |
| commentVoteCount | votes |
| commentVoteCountSing | voto |
| editorMarcadorDePosición | ¿Qué piensas? |
| editorPostBtn | Publicar Sidenote |
| editorPostBtnMobile | Anuncio |
| editorPosting | Colocar un anuncio… |
| editorResponderBtn | Anunciar respuesta |
| editorReplyTitle | Escribir respuesta |
| editorTítulo | Escribir nota |
| emptyImageBlockTxt | ¿Qué piensas? |
| emptyTextBlockTxt | + |
| errorConnection | Oh-oh. No parece que tenga una buena conexión. |
| errorDuplicate | También nos gusta tu nota, pero no puedes publicarla dos veces. |
| errorGeneral | Se ha producido un error. Inténtelo de nuevo. |
| errorServer | Algo salió mal con nuestro servidor. ¿Intenta eso otra vez? |
| facebookShareCaption | Notas al margen de &quot;{title}&quot; |
| menuAuthSignedInMsg | Debe iniciar sesión en {action} |
| menuAuthSignInBtn | Iniciar sesión |
| menuBackBtn | Atrás |
| menuConfirmAccept | Sí, {action} |
| menuConfirmCancel | Cancelar |
| menuConfirmTitle | ¿Está seguro? |
| menuEtcOptionApprove | Aprobar |
| menuEtcOptionDelete | Eliminar |
| menuEtcOptionEdit | Editar  |
| menuEtcOptionFlag | Marcar |
| menuEtcOptionShare | Compartir |
| menuEtcPostedAt | Publicado el {date} |
| menuEtcTitle | Más |
| menuFlagOptionDisact | Rechazar |
| menuFlagOptionOffensive | Ofensivo |
| menuFlagOptionOffTopic | Desactivar tema |
| menuFlagOptionSpam | Correo no deseado |
| menuFlagTitle | Marcar como... |
| menuInfoCopyright | © Livefyre, Inc. 2014 |
| menuInfoHelp | Ayuda |
| menuInfoLivefyreLink | Visite Livefyre.com |
| menuReplyViewReply | Responder a conversación |
| menuReplyViewTitle | Detalles |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Copiar vínculo permanente |
| menuShareOptionLinkComplete | Copiado |
| menuShareOptionLinkFailed | Error al copiar |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | Compartir |
| notificationApproved | Aprobado |
| notificationDeleted | Eliminado |
| notificationFlagged | Marcado |
| permalinkBackBtn | Todas |
| permalinkTitle | Permalink |
| questionExplanation | Ahora puede leer y escribir comentarios directamente sobre oraciones, párrafos, imágenes y comillas.<br><br>Resalte el texto y haga clic en el icono &quot;Fycon-write&quot; o haga clic en el icono &quot;Fycon-action-vista&quot; al final de cada párrafo. |
| questionMockText | Lo que es &quot;conocido familiar&quot; no se conoce correctamente, sólo por la razón de que es &quot;familiar&quot;. |
| questionTitle | ¿Qué es un Sidenote? |
| queuedCommentsPlural | {number} nuevas notas |
| queuedCommentsSingular | 1 Nuevo Sidenote |
| queuedReplyPlural | {number} nuevas respuestas |
| queuedReplySingular | 1 Nueva respuesta |
| responseBtn | Responder |
| signInToPost | Iniciar sesión para escribir una nota de opinión |
| sliderCommentTally | of |
| sliderInviteRead | Leído |
| sliderInviteWrite | Escritura |
| sliderWriteText | ¿Qué piensas? Toque para escribir |
| threadCollapseBtn | Contraer |
| threadExpandBtnPlural | Expandir {número} respuestas |
| threadExpandBtnSingular | Expandir 1 respuesta |
| threadReplyBtn | Responder a conversación |
