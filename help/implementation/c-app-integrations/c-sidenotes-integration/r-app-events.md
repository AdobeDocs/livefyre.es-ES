---
description: Puede escuchar eventos en una instancia de Sidenotes.
seo-description: Puede escuchar eventos en una instancia de Sidenotes.
seo-title: Eventos de la aplicación Sidenotes
solution: Experience Manager
title: Eventos de la aplicación Sidenotes
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Identifica los Eventos de la aplicación {#sidenotes-app-events}

Puede escuchar eventos en una instancia de Sidenotes.

Las llamadas de retorno se pueden registrar con el método `onmethod` y no se pueden registrar con el método `removeListener`. Existe un método `once` disponible para mayor comodidad si se debe llamar a la rellamada una sola vez y luego no se debe registrar.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Para obtener más información sobre los eventos de Livefyre, consulte la página Eventos de JavaScript en la sección Referencia.

| Clave | Descripción |
|--- |--- |
| sidenotes.initialized | Se activa cuando se crea una instancia de la aplicación, tiene datos y está en la página. |
| sidenotes.commentFlagged | Se activa cuando se marca un comentario. Los datos contienen: <br><ul><li>`targetId`:: ID del comentario que se marcó</li><li>`type`:: cadena de tipo de indicador  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Se activa cuando se publica un comentario. Los datos contienen: <br><ul><li> `authorId`:: ID del autor del comentario </li><li>`bodyHtml`:: cuerpo del comentario </li><li> `parent`:: id del elemento principal del comentario o nulo</li></ul> |
| `sidenotes.commentShared` | Se activa cuando se comparte un comentario. Los datos contienen: <br><ul><li>`targetId`:: ID del comentario que se compartió </li><li> `sharedToFacebook`:: si el comentario se compartió en Facebook </li><li>`sharedToTwitter`:: si el comentario se compartió en Twitter</li></ul> |
| `sidenotes.commentVoted` | Se activa cuando se ha votado un comentario. Los datos contienen: <br><ul><li>`targetId`:: ID del comentario sobre el que se votó </li><li> `targetAuthorId`:: ID del autor sobre el que se votó su comentario</li><li> `type`:: tipo de voto numérico: 0: &quot;clear&quot;, 1: &quot;voto en favor&quot; o 2: ‘voto negativo’</li></ul> |
| `sidenotes.userLoggedIn` | Se activa cuando un usuario inicia sesión. Los datos contienen: <br><ul><li>`avatar`:: dirección URL de avatar del usuario </li><li>`displayName`:: nombre para mostrar del usuario</li><li>`id`:: id del usuario</li><li> `isModerator`:: si el usuario es un moderador de la colección actual</li></ul> |
| `sidenotes.userLoggedOut` | Se activa cuando un usuario cierra la sesión |
