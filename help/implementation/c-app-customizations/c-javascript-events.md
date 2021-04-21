---
description: Los eventos disponibles para enlazar JavaScript para aplicaciones de conversación (por ejemplo, chats, blogs en directo, reseñas y notas).
title: Definiciones y ejemplos de eventos de JavaScript
exl-id: 5b865974-69aa-4d51-ac26-60f1d8a114fc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 11%

---

# Definiciones y ejemplos de eventos de JavaScript{#javascript-events-definitions-and-examples}

Los eventos disponibles para enlazar JavaScript para aplicaciones de conversación (por ejemplo, chats, blogs en directo, reseñas y notas).

Livefyre proporciona eventos de JavaScript para rastrear la actividad de los usuarios en sus aplicaciones de Livefyre. Por ejemplo, puede que desee actualizar la página cuando los usuarios quieran o compartan contenido en Twitter o Facebook, o cuando se publique contenido nuevo.

Livefyre también le permite agregar eventos a integraciones de análisis de terceros (Adobe Analytics JS, Google Analytics, Dynamic Tag Management, etc.) para rastrear eventos de aplicaciones. Para obtener más información, colabore con su administrador de integración de terceros para proporcionar los eventos correctos.

Para enlazar a estos eventos, añada el siguiente código a la página al crear una instancia de la aplicación en una página. Sustituya el nombre del evento por `{eventName}`:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('{eventName}', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

>[!NOTE]
>
>Los objetos de datos se proporcionan para todos los controladores de eventos. Los objetos de datos de ejemplo siguen cada evento.

## commentPosted {#section_qfr_51p_xz}

Un usuario publicó un comentario.

* Un elemento principal nulo es un comentario nuevo.
* El comentario principal de Ninguno es un comentario que se ha editado.
* Un número para el elemento principal es el ID principal de la respuesta.

```
data = { 
   authorId: "_u2012@livefyre.com" // The ID of the author of the comment  
   parent: "893549"  
      // The ID of the comment that this new comment is in reply to, else null 
   bodyHtml: "<p>42</>" // The HTML of the submitted Content 
   sharedToFacebook:true // Whether the comment was also posted to Facebook 
   sharedToTwitter:false // Whether the comment was also posted to Twitter 
   title: "demo title" // The title of the review (exists only for Reviews) 
   rating: [90] // Array of ratings for the review (exists only for Reviews) 
} 
```

## commentFlagged {#section_szy_s1p_xz}

Un usuario marcó un comentario.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

A un usuario le gustaba un comentario.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

Un usuario compartió un comentario del flujo. (Este evento no se activa cuando los usuarios comparten desde el editor de comentarios). Este evento se activa cuando se hace clic en el botón Compartir .

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdated {#section_qdq_f1p_xz}

El número total de comentarios visibles en esta conversación ha cambiado (ya sea incrementado o reducido).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

Un usuario ha iniciado sesión.

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## userLoggedOut {#section_tsg_5z4_xz}

Un usuario ha cerrado la sesión.

Los datos no están definidos.

## socialMention {#section_a1w_tz4_xz}

Un usuario incluyó un @mention en un comentario. Devuelve una matriz de lo siguiente:

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## commentFeedback

Un usuario moderador presentó un comentario. Devuelve una matriz de lo siguiente:

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

El flujo de comentarios se ha cargado y el conjunto inicial de contenido se ha recuperado del servidor y se ha mostrado al usuario.

Los datos no están definidos.

## showMore {#section_pqg_nz4_xz}

Un usuario hizo clic en el botón **[!UICONTROL Show More]**.

Los datos no están definidos.

## userFollowed {#section_xxw_jz4_xz}

Devuelve true cuando un usuario hace clic en el botón **[!UICONTROL Follow]** y false cuando se anuncia el contenido en la emisión.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnFollow {#section_wm1_gz4_xz}

Devuelve el valor verdadero cuando un usuario hace clic en el botón **Dejar de seguir** y falso cuando el contenido se anuncia en la emisión.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```
