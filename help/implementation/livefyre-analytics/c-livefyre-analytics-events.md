---
description: null
seo-description: null
seo-title: Eventos de Analytics de Livefyre
solution: Experience Manager
title: Eventos de Analytics de Livefyre
uuid: 4 eb 5 a 196-ca 33-40 f 8-a 96 d-ed 46469223 de
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Eventos de Analytics de Livefyre {#livefyre-analytics-events}

## Definición del objeto de evento {#section_dh1_yhn_pdb}

El siguiente código define los campos del objeto de suceso que reciben el controlador de Analytics en una página.

```
{
  evars: {
    appId : string : URN ID of the app
    appType : string : Type of the app
    contentType : string : Type of the content that this event pertains to
    contextId : string : URN ID of the contextual item that this event pertains to
    environment : string : Environment that this app is using
    networkId : string : Network that this app is using
    publishedDate : number : Epoch time when the app was published
    userLoggedIn : boolean : If a user is logged in
  },
  generator: {
    env : string: Environment that this app is using
    id : string: URN ID of the app
    name : string: Name of the app
    networkId : string: Network that this app is using
    source : string: URN of the collection
    version : string: Semver version of the app
  },
  startTime : number: Epoch time when event was created
  type : string: Event type (Table 1)
}
```

## Eventos y evars de Livefyre Analytics {#section_u3k_tft_mcb}

Los siguientes eventos de Livefyre para asignar a eventos personalizados que se utilizan en los informes mediante el Administrador de grupos de informes. Para obtener más información acerca de los grupos de informes en Adobe Analytics, consulte [Administrador del grupo de informes](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html). Para obtener más información sobre cómo utilizar eventos de Livefyre con el Administrador de grupos de informes, consulte [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Eventos de Analytics de Livefyre

| Evento | Descripción |
|---|---|
| Init | Cuando se carga una página que incluye al menos una aplicación de Livefyre |
| Cargar | Cada vez que se carga una aplicación en una página independientemente de la vista del usuario |
| Ver | Cuando una aplicación entró en la ventanilla por primera vez. |
| Anuncio | Cada vez que un usuario publica un comentario o un fragmento de contenido, incluyendo el siguiente: anuncio de nivel superior, respuestas, revisiones, cargas de muro de medios |
| Publicado | Cuando un anuncio era exitoso. |
| Twitter_ Respuesta | Cada vez que un usuario responde en Twitter |
| Twitter_ Like | Donde se compartió el contenido con: Retweet |
| Livefyre_ Like | Cada vez que se utiliza la función de livefyre como |
| Livefyre_ Unlike | Cada vez que un usuario no le gusta un livefyre |
| Shareonpost | Cada vez que un usuario publica contenido y utiliza el uso compartido en la función de publicación |
| Sharebuttonclick | Cada vez que un usuario hace clic en el botón Compartir de un comentario |
| Sharetwitter | Cuando se hace clic en Compartir en Twitter |
| Sharefacebook | Cuando se hace clic en Compartir en Facebook |
| Shareurl | Cuando se selecciona o copia el área de texto Compartir con URL. |
| Expandreplies | Cuando un usuario hace clic en el vínculo + o Expandir para ver todas las respuestas en un anuncio de nivel superior |
| Collapsereplies | Cuando un usuario hace clic en el vínculo - o Contraer para ver todas las respuestas en un anuncio de nivel superior |
| Flagclick | Cada vez que un usuario abre el Modal modal |
| Flagole | Cuando un usuario marca el contenido como correo no deseado |
| Flagrechazar | Cuando un usuario marca el contenido como en desacuerdo |
| Flagofensiva | Cuando un usuario marca el contenido como ofensivo |
| Flagofftopic | Cuando un usuario marca el contenido como sin tema |
| Flagcancel | Cada vez que un usuario hace clic en X o «cancelar» al enviar un indicador |
| Followcollection | Cada vez que sigue una conversación ("Estoy interesado" en Revisiones) |
| Unfollowcollection | Cuando una conversación no sigue |
| Requestmore | Cada vez que un usuario cargó más contenido en una aplicación (debe ser también para velocity alta) |
| Modalview | Cada vez que un usuario hace clic para ver el contenido en un modal |
| Twitterretweetclick | Donde se compartió el contenido con: Retweet |
| Postbuttonclick | Cuando un usuario hace clic en la publicación ("¿Qué opina? ") button |
| Inicio de sesión | Cada vez que un usuario inició sesión |
| Cerrar sesión | Cada vez que un usuario ha cerrado sesión |

A continuación se muestra una lista de variables de conversión (evars) que proporciona Livefyre.

## Variables de conversión - evars

| Evento | Descripción |
|--- |--- |
| ID de red | ID de red/nombre en Livefyre |
| ID de la aplicación | La URN de la aplicación |
| ID de contexto | ID de contenido en Livefyre |
| Tipo de aplicación | Tipo de aplicación de Livefyre. Opciones: <br><ul><li>Blog activo  </li><li> Tarjeta de función</li><li>Carrusel</li><li>Chat </li><li>Comentarios</li><li>Tira de película</li><li>Mapa</li><li>Mosaico</li><li>Muro de medios</li><li>Tendencias</li><li>Upload Button</li></ul> |
| Tipo de contenido | Instagram, Twitter, Facebook, livefyre, YouTube, etc. |

## Más información {#section_b3d_4yl_pdb}

Para obtener más información sobre los temas analizados en esta página, consulte:

* [Administrador de grupos de informes](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [Reglas](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre. js](/help/implementation/c-livefyre.js.md)