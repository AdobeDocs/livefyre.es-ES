---
description: 'null'
seo-description: 'null'
seo-title: Eventos de análisis de Livefyre
solution: Experience Manager
title: Eventos de análisis de Livefyre
uuid: 4eb5a196-ca33-40f8-a96d-ed46469223de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Eventos de análisis de Livefyre {#livefyre-analytics-events}

## Definición de objeto de evento {#section_dh1_yhn_pdb}

El código siguiente define los campos del objeto de evento que recibe el controlador de análisis en una página.

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

## eVars y eventos de análisis de Livefyre {#section_u3k_tft_mcb}

Los siguientes eventos de Livefyre que se asignarán a los eventos personalizados que se utilizarán en los informes mediante el Administrador del grupo de informes. Para obtener más información sobre los grupos de informes en Adobe Analytics, consulte Administrador [de grupos](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)de informes. Para obtener más información sobre cómo utilizar los eventos de Livefyre con el Administrador de grupos de informes, consulte [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Eventos de análisis de Livefyre

| Evento | Descripción |
|---|---|
| Init | Cuando se carga una página que incluye al menos una aplicación de Livefyre |
| Load | Cada vez que se carga una aplicación en una página independientemente de la vista del usuario |
| Ver | Cuando una aplicación entró en la ventanilla por primera vez. |
| Anuncio | Cada vez que un usuario publica un comentario o un contenido que incluye: anuncios de nivel superior, respuestas, reseñas, cargas de muro de medios |
| Publicado | Cuando una publicación se ha realizado correctamente. |
| Twitter_Reply | Cada vez que un usuario respondió en Twitter |
| Twitter_Like | Dónde se compartió el contenido: Retweet |
| Livefyre_Like | Cada vez que se utiliza una función "Me gusta" en una aplicación |
| Livefyre_Different | Cada vez que a un usuario no le gusta una película |
| ShareOnPost | Cada vez que un usuario publica contenido y utiliza la función Compartir en la publicación |
| ShareButtonClick | Cada vez que un usuario hace clic en el botón Compartir de un comentario |
| ShareTwitter | Cuando se hace clic en Compartir en Twitter |
| ShareFacebook | Cuando se hace clic en Compartir en Facebook |
| ShareURL | Cuando se selecciona o copia el área de texto Compartir con URL. |
| ExpandirRespuestas | Cuando un usuario hace clic en el vínculo + o Expandir para ver todas las respuestas en un anuncio de nivel superior |
| Contraer respuestas | Cuando un usuario hace clic en el vínculo - o Contraer para ver todas las respuestas en un anuncio de nivel superior |
| FlagClick | Cada vez que un usuario abre el Modelo de marca |
| MarcarCorreoNoDeseado | Cuando un usuario marca contenido como correo no deseado |
| FlagDisaccept | Cuando un usuario marca el contenido como no conforme |
| Bandera ofensiva | Cuando un usuario marca el contenido como ofensivo |
| FlagOffTopic | Cuando un usuario marca el contenido como tema no relacionado |
| FlagCancel | Cada vez que un usuario hace clic en X o en "cancelar" al enviar un indicador |
| FollowCollection | Cada vez que se sigue una conversación ("Estoy interesado" en críticas) |
| UnfollowCollection | Cuando se deja de seguir una conversación |
| RequestMore | Cada vez que un usuario carga más contenido en una aplicación (debe ser a alta velocidad también) |
| ModalView | Cada vez que un usuario hace clic para ver el contenido en un modal |
| TwitterRetweetClick | Dónde se compartió el contenido: Retweet |
| PostButtonClick | Cuando un usuario hace clic en la publicación ("¿Qué tiene en mente?") button |
| Inicio de sesión | Cada vez que un usuario inicia sesión |
| Cerrar sesión | Cada vez que un usuario cierra la sesión |

A continuación se muestra una lista de variables de conversión (eVars) que proporciona Livefyre.

## Variables de conversión - eVars

| Evento | Descripción |
|--- |--- |
| ID de red | ID/nombre de red en Livefyre |
| ID de la aplicación | La URL de la aplicación |
| ID de contexto | ID de contenido en Livefyre |
| Tipo de aplicación | Tipo de aplicación de Livefyre. Opciones: <br><ul><li>Blog en vivo  </li><li> Tarjeta de función</li><li>Carrusel</li><li>Conversación </li><li>Comentarios</li><li>Tira de película</li><li>Mapa</li><li>Mosaico</li><li>Muro de los medios</li><li>Tendencias</li><li>Upload Button</li></ul> |
| Tipo de contenido | Instagram, Twitter, Facebook, LiveFyre, YouTube, etc. |

## Más información {#section_b3d_4yl_pdb}

Para obtener más información sobre los temas tratados en esta página, consulte:

* [Report Suite](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[ManagerDTM](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [Reglas](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)