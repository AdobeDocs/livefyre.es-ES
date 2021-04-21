---
description: Puede escuchar eventos en una instancia de Sidenotes.
title: Identifica eventos de aplicación
exl-id: e341ca76-002d-425c-8d1a-35c3253fb254
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Identifica eventos de aplicación {#sidenotes-app-events}

Puede escuchar eventos en una instancia de Sidenotes.

Las devoluciones de llamadas se pueden registrar con `onmethod` y no estar registradas con el método `removeListener` . Hay disponible un método `once` para mayor comodidad si se va a llamar a la rellamada solo una vez y después no se va a registrar.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Para obtener más información sobre los eventos de Livefyre, consulte la página Eventos de JavaScript en la sección Referencia .

| Clave | Descripción |
|--- |--- |
| sidenotes.initialized | Se activa cuando se crea una instancia de la aplicación, tiene datos y está en la página. |
| sidenotes.commentFlagged | Se activa cuando se marca un comentario. Los datos contienen: <br><ul><li>`targetId`: id del comentario marcado</li><li>`type`: cadena de tipo indicador  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Se activa cuando se ha publicado un comentario. Los datos contienen: <br><ul><li> `authorId`: id del autor del comentario </li><li>`bodyHtml`: cuerpo del comentario </li><li> `parent`: id del elemento principal del comentario o nulo</li></ul> |
| `sidenotes.commentShared` | Se activa cuando se comparte un comentario. Los datos contienen: <br><ul><li>`targetId`: id del comentario que se compartió </li><li> `sharedToFacebook`: si el comentario se compartió con Facebook </li><li>`sharedToTwitter`: si el comentario se compartió con Twitter</li></ul> |
| `sidenotes.commentVoted` | Se activa cuando se ha votado un comentario. Los datos contienen: <br><ul><li>`targetId`: id del comentario sobre el que se votó </li><li> `targetAuthorId`: identificación del autor cuyo comentario fue votado</li><li> `type`: tipo de voto numérico: 0: &quot;clear&quot;, 1: &quot;votación inicial&quot;, o 2: &quot;downvote&quot;</li></ul> |
| `sidenotes.userLoggedIn` | Se activa cuando un usuario inicia sesión. Los datos contienen: <br><ul><li>`avatar`: url de avatar para el usuario </li><li>`displayName`: nombre para mostrar del usuario</li><li>`id`: id del usuario</li><li> `isModerator`: si el usuario es moderador de la colección actual</li></ul> |
| `sidenotes.userLoggedOut` | Se activa cuando un usuario cierra la sesión |
