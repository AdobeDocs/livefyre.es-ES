---
title: Eventos de análisis de Livefyre
description: Eventos de análisis de Livefyre
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 5%

---

# Eventos de análisis de Livefyre

## Definición de objeto de evento {#section_dh1_yhn_pdb}

El siguiente código define los campos del objeto de evento que recibe el controlador de análisis en una página.

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

Los siguientes eventos de Livefyre para asignarlos a eventos personalizados y utilizarlos en informes mediante el Administrador del grupo de informes. Para obtener más información sobre los grupos de informes en Adobe Analytics, consulte [Administrador del grupo de informes](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en). Para obtener más información sobre cómo usar eventos de Livefyre con el Administrador de grupos de informes, consulte [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Eventos de análisis de Livefyre

| Evento | Descripción |
|---|---|
| Init | Cuando se carga una página que incluye al menos una aplicación de Livefyre |
| Load | Cada vez que se carga una aplicación en una página, independientemente de la vista del usuario |
| Ver | Cuando una aplicación entró en la ventanilla móvil por primera vez. |
| Anuncio | Cada vez que un usuario publica un comentario o un fragmento de contenido, como por ejemplo: anuncios de nivel superior, respuestas, reseñas, cargas de muro de medios |
| Publicado | Cuando una publicación se ha realizado correctamente. |
| Twitter_Reply | Cada vez que un usuario responde en Twitter |
| Twitter_Like | Dónde se compartió el contenido en: Retweet |
| Livefyre_Like | Cada vez que se utiliza la función &quot;Me gusta&quot; del ciclo vital en una aplicación |
| Livefyre_A | Cada vez que un usuario desgusta una función de livefyre como |
| ShareOnPost | Cada vez que un usuario publica contenido y utiliza la función Compartir en la publicación |
| ShareButtonClick | Cada vez que un usuario hace clic en el botón Compartir de un comentario |
| ShareTwitter | Cuando se hace clic en Compartir en Twitter |
| ShareFacebook | Cuando se hace clic en Compartir en Facebook |
| ShareURL | Cuando se selecciona o copia Compartir en el área de texto de la URL. |
| ExpandirRespuestas | Cuando un usuario hace clic en el vínculo + o Expandir para ver todas las respuestas en un anuncio de nivel superior |
| Contraer respuestas | Cuando un usuario hace clic en el vínculo - o Contraer para ver todas las respuestas en un anuncio de nivel superior |
| FlagClick | Cada vez que un usuario abre el modal de la marca |
| FlagSpam | Cuando un usuario marca el contenido como correo no deseado |
| Marcar como no conforme | Cuando un usuario marca el contenido como en desacuerdo |
| Bandera ofensiva | Cuando un usuario marca el contenido como ofensivo |
| FlagOffTopic | Cuando un usuario marca el contenido como tema fuera de línea |
| FlagCancel | Cada vez que un usuario hace clic en X o &quot;cancelar&quot; al enviar una marca |
| FollowCollection | Cada vez que se sigue una conversación (&quot;Estoy interesado&quot; en las reseñas) |
| UnseguirCollection | Cuando se deja de seguir una conversación |
| RequestMore | Cada vez que un usuario carga más contenido en una aplicación (también debe ser a una velocidad alta) |
| Vista modal | Cada vez que un usuario hace clic para ver el contenido en un modal |
| TwitterRetweetClick | Dónde se compartió el contenido en: Retweet |
| PostButtonClick | Cuando un usuario hace clic en la publicación (&quot;¿Qué te pasa por la cabeza?&quot;) botón |
| Inicio de sesión | Cada vez que un usuario inicia sesión |
| Cerrar sesión | Cada vez que un usuario cierra la sesión |

La siguiente es una lista de variables de conversión (eVars) que proporciona Livefyre.

## Variables de conversión - eVars

| Evento | Descripción |
|--- |--- |
| ID de red | ID/nombre de red en Livefyre |
| ID de la aplicación | La URL de la aplicación |
| ID de contexto | ID de contenido en Livefyre |
| Tipo de aplicación | Tipo de aplicación de Livefyre. Opciones: <br><ul><li>Blog en directo  </li><li> Tarjeta de características</li><li>Carrusel</li><li>Conversación </li><li>Comentarios</li><li>Tira de película</li><li>Mapa</li><li>Mosaic</li><li>Muro de los medios</li><li>Tendencias</li><li>Upload Button</li></ul> |
| Tipo de contenido | Instagram, Twitter, Facebook, LiveFile, YouTube, etc. |

## Más información {#section_b3d_4yl_pdb}

Para obtener más información sobre los temas tratados en esta página, consulte:

* [Administrador del grupo de informes](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)
* [Etiquetas](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
