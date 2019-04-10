---
description: null
seo-description: null
seo-title: Sidenotes Custom Strings
title: Sidenotes Custom Strings
uuid: 73745273-d 3 fb -4569-8910-d 149 fb 37 a 7 b 4
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sidenotes Custom Strings{#sidenotes-custom-strings}

Las cadenas personalizadas se aplican a través de un objeto insertado en el constructor Sidenotes y anulan las cadenas predeterminadas utilizadas a través de la aplicación. Pueden utilizarse para personalizar cualquier parte del idioma que se ajuste a las especificaciones de estilo o idioma. Las cadenas se combinarán automáticamente con valores predeterminados.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Clave | Predeterminado |
|---|---|
| Appname | Sidenotes |
| Commentatortag commentModeratorTag | Mod |
| Commentpendingtag | Pendiente |
| Commentreadmorelink | Más información |
| Commentreplylink | Consulte {número} respuestas |
| Commentreplylinksing | Consulte respuesta |
| Commentvotecount | votos |
| Commentvotecountsing | votar |
| Editorplaceholder | ¿Qué piensa? |
| Editorpostbtn | Post Sidenote |
| Editorpostbtnmobile | Anuncio |
| Editorpost | Publicando… |
| Editorreplybtn | Publicar respuesta |
| Editorreplytitle | Escribir respuesta |
| Editortitle | Escribir nota |
| Emptyimageblocktxt | ¿Qué piensa? |
| Emptytextblocktxt | + |
| Errorconnection | Uh-oh. Parece que no tiene una buena conexión. |
| Errorduplicate | También nos gusta su nota, pero no puede anunciarla dos veces. |
| Errorgeneral | Se ha producido un error. Inténtelo de nuevo. |
| Errorserver | Algo salió mal con nuestro servidor. ¿Inténtelo de nuevo? |
| Facebooksharecaption | Sidenotes en «{title}» |
| Menuauthsignedemplsg | Debe iniciar sesión en {action} |
| Menuauthsigninbtn | Iniciar sesión |
| Menubackbtn | Atrás |
| Menuconfirmaccept | Sí, {action} |
| Menuconfirmcancel | Cancelar |
| Menuconfirmtitle | ¿Está seguro? |
| Menuetcoptionapprove | Aprobar |
| Menuetcoptiondelete | Eliminar |
| Menuetcoptionedit | Editar |
| Menuetcoptionflag | Indicador |
| Menuetcoptionshare | Compartir |
| Menuetcpostedat | Publicado el {date} |
| Menuetctitle | Más |
| Menuflagoptiondisagree | Rechazar |
| Menuflagoptionoffensive | Ofensiva |
| Menuflagoptionofftopic | Tema desactivado |
| Menuflagoptionspam | Correo no deseado |
| Menuflagtitle | Marcar como… |
| Menuinfocopyright | © Livefyre, Inc. 2014 |
| Menuinfohelp | Ayuda |
| Menuinfolivefyrelink | Visite Livefyre.com |
| Menurepliesviewreply | Responder a la conversación |
| Menurepliesviewtitle | Detalles |
| Menushareoptionfacebook | Facebook |
| Menushareoptionlink | Copiar permalink |
| Menushareoptionlinkcomplete | Copiado |
| Menushareoptionlinkfailed | Error al copiar |
| Menushareoptiontwitter | Twitter |
| Menusharetitle | Compartir |
| Notificationapproved | Aprobado |
| Notificationdeleted | Eliminado |
| Notificationmarcado | Marcado |
| Permalinkbackbtn | Todos |
| Permalinktitle | Permalink |
| Explicación de preguntas | Ahora puede leer y escribir comentarios directamente sobre las frases, párrafos, imágenes y comillas.<br><br>Resalte el texto y haga clic en el icono "fycon-write" o haga clic en el icono "fycon-action-view" al final de cada párrafo. |
| Questionmocktext | Lo que se conoce «familiarmente» no es conocido, simplemente por el motivo de que es «familiar». |
| Questiontitle | ¿Qué es un Sidenote? |
| Queuedcommentsplural | {número} Nuevo sidenotes |
| Queuedcommentsunique | 1 Nuevo Sidenote |
| Queuedrepliesplural | {número} Nuevas respuestas |
| Queuedrepliesunique | 1 Nueva respuesta |
| Replybtn | Responder |
| Signintopost | Iniciar sesión para escribir un sidenote |
| Slidercommenttally | de |
| Sliderinviteread | Leer |
| Sliderinvitewrite | Escribir |
| Sliderwritetext | ¿Qué piensa? Tocar para escribir |
| Threadcollapsebtn | Contraer |
| Threadexpandbtnplural | Expandir {número} respuestas |
| Threadexpandbtnsingular | Expandir 1 respuesta |
| Threadreplybtn | Responder a la conversación |
