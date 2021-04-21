---
title: Notas de cadena personalizadas
description: Notas de cadena personalizadas
exl-id: b5e2c18b-5b98-45ff-aa89-dd92a02949a9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 10%

---

# Muestra las cadenas personalizadas{#sidenotes-custom-strings}

Las cadenas personalizadas se aplican a través de un objeto insertado en el constructor Sidenotes y anulan las cadenas predeterminadas utilizadas a través de la aplicación. Pueden utilizarse para personalizar cualquier parte del idioma para adaptarlo a sus especificaciones de estilo o idioma. Las cadenas se fusionarán automáticamente con los valores predeterminados.

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
| appName | Notas |
| commentModeratorTag | Mod |
| commentPendingTag | Pendiente |
| commentReadMoreLink | Más información... |
| commentReplyLink | Ver {número} respuestas |
| commentReplyLinkSing | Consulte respuesta |
| commentVoteCount | vote |
| commentVoteCountSing | voto |
| editorMarcador de posición | ¿Qué piensas? |
| editorPostBtn | Publicar Sidenote |
| editorPostBtnMobile | Anuncio |
| editorPosting | Colocar un anuncio… |
| editorReplyBtn | Anunciar respuesta |
| editorReplyTitle | Escribir respuesta |
| editorTitle | Escribir nota |
| emptyImageBlockText | ¿Qué piensas? |
| emptyTextBlockText | + |
| errorConnection | Oh-oh. Parece que no tiene una buena conexión. |
| errorDuplicate | También nos gusta tu nota, pero no puedes publicarla dos veces. |
| errorGeneral | Se ha producido un error. Inténtelo de nuevo. |
| errorServer | Algo salió mal con nuestro servidor. ¿Intenta eso otra vez? |
| facebookShareCaption | Notas laterales sobre &quot;{title}&quot; |
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
| menuEtcPostedAt | Publicado el {fecha} |
| menuEtcTitle | Más |
| menuFlagOptionDisaccept | Desacuerdo |
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
| menuShareOptionLinkFailed | Error en la copia |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | Compartir |
| notificationApproved | Aprobado |
| notificationDeleted | Eliminado |
| notificationFlagged | Marcado |
| permalinkBackBtn | Todas |
| permalinkTitle | Permalink |
| questionExplanation | Ahora puede leer y escribir comentarios directamente sobre oraciones, párrafos, imágenes y comillas.<br><br>Resalte el texto y haga clic en el icono &quot;Fycon-write&quot; o haga clic en el icono &quot;Fycon-action-view&quot; al final de cada párrafo. |
| questionMockText | Lo que es &quot;conocido&quot; no se conoce adecuadamente, simplemente por ser &quot;familiar&quot;. |
| questionTitle | ¿Qué es un Sidenote? |
| queuedCommentsPlural | {número} nuevas notas |
| queuedCommentsSingular | 1 Nuevo guión |
| queuedReplyPlural | {número} nuevas respuestas |
| queuedReplySingular | 1 Nueva respuesta |
| replyBtn | Responder |
| signInToPost | Iniciar sesión para escribir una nota secundaria |
| sliderCommentTally | of |
| sliderInviteRead | Leído |
| sliderInviteWrite | Escritura |
| sliderWriteText | ¿Qué piensas? Toque para escribir |
| threadCollapseBtn | Contraer |
| threadExpandBtnPlural | Expandir {número} respuestas |
| threadExpandBtnSingular | Expandir 1 respuesta |
| threadReplyBtn | Responder a conversación |
