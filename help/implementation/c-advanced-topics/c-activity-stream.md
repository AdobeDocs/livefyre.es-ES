---
description: Descubra cómo monitorizar y almacenar el contenido generado por el usuario que fluye a través del sistema Livefyre.
title: Flujo de actividad
exl-id: 4a552034-96e4-4f1c-9965-3495992005f1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 1%

---

# Flujo de actividad {#activity-stream}

Descubra cómo monitorizar y almacenar el contenido generado por el usuario que fluye a través del sistema Livefyre.

Utilice la API de flujo de actividad para consumir los datos generados por el usuario que fluyen a través del sistema Livefyre de su red o sitio. Por ejemplo: utilice los datos de esta API para actualizar los índices de búsqueda según las clasificaciones o para administrar los distintivos de los usuarios en un sistema de terceros basado en su actividad.

API de flujo de actividad:

Para obtener una lista completa de los extremos disponibles, consulte la sección Referencia de la API de Livefyre .

## Recursos {#section_aql_n4l_b1b}

Hay dos extremos, uno para el entorno de ensayo y otro para la producción.

### Ensayo

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Producción

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### Parámetros

* **recurso:** ** cadenaUna dirección URL del objeto para el que solicita datos de actividad.

* **since:** ** integerUn entero de 64 bits que representa el ID del último evento que recibió. Especifique &quot;0&quot; si no tiene datos anteriores.

## Cadenas URN {#section_skl_q4l_b1b}

Ejemplos:

* **urn:livefyre:** `example.fyre.co` el flujo de actividad de  `example.fyre.co`.
* **urn:livefyre:** `example.fyre.co:site=54321` flujo de actividad del sitio 54321 bajo la  `example.fyre.co` red.

## Directivas de token {#section_nwh_c5j_11b}

La API de flujo de actividad utiliza un token del portador de OAuth para la autenticación. Los tokens del portador forman parte de la especificación OAuth 2.0 y se describen oficialmente [aquí](https://tools.ietf.org/html/rfc6750#section-1.2).

Un token contiene varias cosas:

* Quién creó el token.
* A quién se le dio un token.
* Momento en el que ya no es válido.
* Lo que estamos operando.
* Una lista de permisos que se han concedido.

### Pasos

Los pasos para crear un token de portador de OAuth incluyen:

* Cree un mapa/diccionario que contenga el emisor, la audiencia, el asunto, la caducidad y el ámbito.
* Utilice la biblioteca JWT, con su secreto, para codificar un token JWT.
* Añadir &quot;Autenticación: Portador&quot; a su petición HTTP.

El siguiente ejemplo de código muestra los pasos anteriores en Python:

```
import time 
import jwt 
  
# network data goes here: 
network = "timeout-0.fyre.co" 
network_secret = "...replaceme..." 
  
# api URN 
api_urn = "urn:livefyre:api:core=GetActivityStream" 
  
# expires in 10 seconds 
expiration = int(time.time() + 10) 
  
network_urn = "urn:livefyre:" + network 
  
data = dict(iss=network_urn, aud=network_urn, sub=network_urn, scope=api_urn, exp=expiration) 
  
token = jwt.encode(data, key=network_secret)
```

Donde las claves del token al portador se definen de la siguiente manera:

* **iss** *(Emitido)*  Una entidad con la autoridad para generar tokens. Puede ser Livefyre, un sitio o una red. (Para que una nota llegue tarde a la escuela, es su padre).
* **aud** *(Audiencia)* Persona para la que se generó este token. Si está creando el token usted mismo, es el sitio o la red.
* **** *(Asunto)* El asunto para el que se deben conceder permisos. Por ejemplo, si está operando en una colección, el asunto debe ser el identificador de la colección. (En la nota del ejemplo escolar, eres tú.)
* **exp** *(Caducidad)* Un punto en el tiempo en el que el token ya no es válido.
* **ámbito** *(Ámbito)* Es una lista de los permisos otorgados en el asunto. Un ejemplo es &quot;tarde para la escuela&quot;. El nombre de una API es otro ejemplo.

## Ejemplo {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## Respuesta {#section_gs2_stj_11b}

```
{ 
"code": 200,  
"data": { 
  "annotations": {},  
  "authors": {  
      /** "a set of every author who generated activity within this window" */ 
      "_up1770425@livefyre.com": { 
        "avatar": "https://gravatar.com/avatar/68c789597150d3e941769a5c0a0c4249/?s=50&d=https://avatars-qa.fyre.co/a/anon/50.jpg",  
        "displayName": "ross_pfahler",   
        "id": "_up1770425@livefyre.com",  
        "profileUrl": "https://www.qa-ext.livefyre.com/profile/1770425/",  
        "tags": [],  
        "type": 1 
      },  
  ... 
  },  
  "collections": {  
      /** "a set of every collection for which an activity was generated" */ 
      "2486601": { 
        "articleIdentifier": "75",  
        "id": "2486601",  
        "site": "290596",  
        "title": "Live Blog",  
        "url": "https://orangesaregreat.com/..." 
      }, 
  ... 
  },  
  /** "the maximum event ID for this window" */ 
  "maxEventId": 1383508243715211, 
  "states": {  
      /** "a set of messages (comments, reviews, etc) for which activity  
           was generated in this window, represents the compiled 
           'state' of the object including visible actions on that object 
           (up-votes, likes, and etc.)" */ 
      "3ad6480eb00c4895b29b7a972380f489@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "annotations": { 
                "rating": [ 90 ], /** "this object is a Rating (4.5)" */ 
                "vote": [ 
                    { 
                      "author": "_up1792695@livefyre.com",  
                      "collectionId": "2486685",  
                      "value": 1 
                    } 
                ] 
              },  
              "attachments": [  
              /** "a list of oembeds; the body of this Rating included  
                  this Youtube video" */ 
                { 
                  "author_name": "mauricio890",  
                  "author_url": "https://www.youtube.com/user/mauricio890",  
                  "height": 480,  
                  "html": "<iframe width=\"854\" height=\"480\" src=\"https://www.youtube.com/embed/pmMAw5a7POU?autoplay=1&feature=oembed\" frameborder=\"0\" allowfullscreen></iframe>",  
                  "link": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "provider_name": "YouTube",  
                  "provider_url": "https://www.youtube.com/",  
                  "thumbnail_height": 360,  
                  "thumbnail_url": "https://i1.ytimg.com/vi/pmMAw5a7POU/hqdefault.jpg",  
                  "thumbnail_width": 480,  
                  "title": "Napoleon Dynamite dance scene",  
                  "type": "video",  
                  "url": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "version": "1.0",  
                  "width": 854 
                } 
              ],  
              // "who authored the content" 
              "authorId": "_up1793160@livefyre.com",  
              "bodyHtml": "<p><strong>Pros:</strong>Boom</p><p><strong>Cons:</strong>Goes</p><p><strong>Description:</strong>The dynamite:</p><p><a href=\"https://www.youtube.com/watch?v=pmMAw5a7POU\" target=\"_blank\" rel=\"nofollow\">https://www.youtube.com/watch?v=pmMAw5a7POU</a><br/></p>",  
              // "UNIX timestamp" 
              "createdAt": 1383257354,  
              "id": "3ad6480eb00c4895b29b7a972380f489@livefyre.com",  
              // "non-empty only if this were a reply" 
              "parentId": "", 
              // "UNIX timestamp"  
              "updatedAt": 1383257356  
          },  
          // "the event ID of this state." 
          "event": 1383369320554187,  
          "lastVis": 3,  
          "source": 0,  
          "type": 0,  
          // "Object visibility: 0 = deleted, 1 = everyone, 2 = bozo,  
          // 3 = owner + admins (e.g. premod)" 
          "vis": 1  
      },  
      "5943789": { 
          "collectionId": "2486688",  
          "content": { 
            "annotations": { 
                // "posted by a moderator" 
                "moderator": true  
            },  
            "authorId": "_up1792872@livefyre.com",  
            "bodyHtml": "<p>This is a regular comment from a moderator</p>",  
            "createdAt": 1383372338,  
            "id": "5943789",  
            "parentId": "",  
            "updatedAt": 1383372338 
          },  
          "event": 1383372338732492,  
          "lastVis": 0,  
          "source": 5,  
          "type": 0,  
          "vis": 1 
      },  
      "863c616a2c0c44239feed0914c282d7c@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "id": "863c616a2c0c44239feed0914c282d7c@livefyre.com" 
          },  
          "event": 1383371303805767,  
          "lastVis": 1,  
          "source": 0,  
          "type": 0,  
          "vis": 0 // "0 = deleted; this object was removed" 
      },  
  ... 
},  
"meta": { 
  // "this describes position in the stream" 
  "cursor": {  
    // "maximum number of objects returned in a single call through this API" 
    "limit": 50,  
    // "the final position in the stream, and from where data should be requested" 
    "next": 1383508243715211, 
    // "the initial position (the 'since' parameter value in this request)" 
    "self": 0  
  } 
},  
"status": "ok" 
} 
```

Una respuesta con nuevos datos desde la última solicitud:

```
{ 
    "code": 200,  
    "data": { 
        "annotations": {},  
        "authors": {},  
        "collections": {},  
        "maxEventId": -1,  
        "states": {} 
    },  
    "meta": { 
        "cursor": { 
            "limit": 50, 
            /** "indicates there is no data beyond 1383508243715211" */  
            "next": null, 
            "self": 1383508243715211 
        } 
    },  
    "status": "ok" 
}
```

## Notas {#section_hj3_crj_11b}

* Una llamada correcta a la API devolverá un código de estado HTTP 200. Todos los demás códigos de estado deben considerarse errores.
* Si no es nulo, use el valor de `data.meta.cursor.next` como parámetro `since` de la siguiente solicitud.
* Si el valor de `data.meta.cursor.next` es nulo, significa que no hay datos nuevos que consumir. Debe volver a solicitar más adelante con el mismo valor `since` para ver si han llegado nuevos datos.
* Como práctica, debe solicitar inmediatamente más datos si el valor `data.meta.cursor.next` no es nulo.
* Aproximadamente dos horas de datos recientes están disponibles a través de esta API en producción.
* Debe configurar sus procesos para sondear este extremo con frecuencia en cronjob para evitar que falten datos. Un intervalo de cinco minutos debería ser perfectamente adecuado para la mayoría de las implementaciones.
