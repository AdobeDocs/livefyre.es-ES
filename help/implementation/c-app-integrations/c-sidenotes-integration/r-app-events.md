---
description: Puede escuchar eventos en una instancia de Sidenotes.
seo-description: Puede escuchar eventos en una instancia de Sidenotes.
seo-title: Eventos de aplicación Sidenotes
solution: Experience Manager
title: Eventos de aplicación Sidenotes
uuid: afca 4 b 03-c 370-41 ca-aa 12-45 bc 357517 ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Eventos de aplicación Sidenotes {#sidenotes-app-events}

Puede escuchar eventos en una instancia de Sidenotes.

Las llamadas de retorno se pueden registrar `onmethod` con `removeListener` el método y sin registrarse. Si la llamada de retorno debe llamarse una sola vez y, a continuación, no se registra, hay `once` un método disponible.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Para obtener más información sobre los eventos de Livefyre, consulte la página Eventos de JavaScript en la sección Referencia.

| Clave | Descripción |
|--- |--- |
| sidenotes. initialized | Se activa cuando se crea una instancia de la aplicación, tiene datos y se encuentra en la página. |
| sidenotes. commentflag COMMENTFLAGGED | Se activa cuando se marca un comentario. Los datos contienen: <br><ul><li>`targetId`: id del comentario marcado</li><li>`type`: cadena de tipo de indicador `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Se activa cuando se publica un comentario. Los datos contienen: <br><ul><li> `authorId`: id del autor del comentario </li><li>`bodyHtml`: cuerpo del comentario </li><li> `parent`: id del comentario principal del comentario o nulo</li></ul> |
| `sidenotes.commentShared` | Se activa cuando se comparte un comentario. Los datos contienen: <br><ul><li>`targetId`: id del comentario que se compartió </li><li> `sharedToFacebook`: si el comentario se compartió con Facebook </li><li>`sharedToTwitter`: si el comentario se compartió con Twitter</li></ul> |
| `sidenotes.commentVoted` | Se activa cuando se votó un comentario. Los datos contienen: <br><ul><li>`targetId`: id del comentario que se votó en </li><li> `targetAuthorId`: id del autor cuyo comentario se votó en</li><li> `type`: tipo de voto numérico: 0: ' clear ', 1: ' upvote'o 2: ' downvote '</li></ul> |
| `sidenotes.userLoggedIn` | Se activa cuando un usuario inicia sesión. Los datos contienen: <br><ul><li>`avatar`: URL de avatar para el usuario </li><li>`displayName`: nombre para mostrar del usuario</li><li>`id`: id del usuario</li><li> `isModerator`: si el usuario es moderador de la colección actual</li></ul> |
| `sidenotes.userLoggedOut` | Se activa cuando un usuario cierra sesión |
