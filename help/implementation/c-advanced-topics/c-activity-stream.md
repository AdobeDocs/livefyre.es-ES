---
description: Aprenda cómo monitorear y almacenar el contenido generado por el usuario a través del sistema de Livefyre.
seo-description: Aprenda cómo monitorear y almacenar el contenido generado por el usuario a través del sistema de Livefyre.
seo-title: Flujo de actividad
solution: Experience Manager
title: Flujo de actividad
uuid: f 40 deec 1-58 ab -41 c 9-aac 4-d 2 d 8 c 9192 bb 9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Flujo de actividad {#activity-stream}

Aprenda cómo monitorear y almacenar el contenido generado por el usuario a través del sistema de Livefyre.

Utilice la API de flujo de actividad para consumir datos generados por el usuario a través del sistema de Livefyre en su red o sitio. Por ejemplo: utilizar datos de esta API para actualizar los índices de búsqueda según las clasificaciones, o para administrar las insignias de los usuarios en un sistema de terceros basado en su actividad.

API de flujo de actividad:

Para obtener una lista completa de los puntos finales disponibles, consulte la sección Referencia de la API de Livefyre.

## Recursos {#section_aql_n4l_b1b}

Existen dos puntos finales, uno para el entorno de ensayo y otro para producción.

### Ensayo

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Producción

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### Parámetros

* **recurso:***cadena* Una URN del objeto para el que está solicitando datos de actividad.

* **desde:***integer* Un entero de 64 bits que representa el ID del último evento recibido. Especifique «0» si no tiene datos anteriores.

## Cadenas URN {#section_skl_q4l_b1b}

Ejemplos:

* **urn: livefyre:**`example.fyre.co` Flujo de actividad para `example.fyre.co`.
* **urn: livefyre:**`example.fyre.co:site=54321` Flujo de actividad del sitio 54321 debajo de `example.fyre.co` la red.

## Políticas de tokens {#section_nwh_c5j_11b}

La API de flujo de actividad utiliza un testigo de portada oauth para la autenticación. Los tokens del portador forman parte de la especificación oauth 2.0 y se describen oficialmente [aquí](https://tools.ietf.org/html/rfc6750#section-1.2).

Un token contiene varias cosas:

* Quién creó el token.
* A quién se le ha concedido un token.
* Una hora en la que ya no es válida.
* Lo que estamos trabajando.
* Lista de permisos que se han concedido.

### Pasos

Entre los pasos para crear un token de portador oauth se incluyen:

* Cree un mapa o diccionario que contenga el emisor, audiencia, asunto, caducidad y alcance.
* Utilice la biblioteca JWT, con su secreto, para codificar un token JWT.
* Agregar «Autenticación: Portador» a su solicitud HTTP.

El ejemplo de código siguiente muestra los pasos anteriores en Python:

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

Donde las claves de tokens del portador se definen de la siguiente manera:

* **iss** *(Issuer)* Una entidad con la autoridad para generar tokens. Puede ser Livefyre, un sitio o una red. (Para que una nota sea posterior al colegio, es su principal).
* **aud** *(Audiencia)* La persona para la que se generó este token. Si está creando el token usted mismo es el sitio o la red.
* **sub** *(Asunto)* El asunto para el que se van a conceder los permisos. Por ejemplo, si está trabajando en una colección, el sujeto debe ser el identificador de la colección. (En la nota del ejemplo de la escuela, es usted.)
* **exp** *(Caducidad)* Un punto en el que el token ya no es válido.
* **ámbito** *(Ámbito)* Es una lista de los permisos concedidos en el asunto. «Tarde para la escuela» es un ejemplo. El nombre de una API es otro ejemplo.

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

* Una llamada correcta a la API generará un código de estado HTTP 200. Todos los demás códigos de estado deben considerarse errores.
* Si es nulo, utilice el valor como `data.meta.cursor.next``since` parámetro de la siguiente solicitud.
* Si el valor de `data.meta.cursor.next` es nulo, significa que no hay datos nuevos que consumir. Debe volver a solicitar más tarde con el mismo `since` valor para ver si han llegado nuevos datos.
* Como cuestión de práctica, debe solicitar inmediatamente más datos si `data.meta.cursor.next` el valor no es nulo.
* Se dispone de aproximadamente dos horas de datos recientes a través de esta API en producción.
* Debe configurar los procesos para sondear este punto final con frecuencia en cronjob a fin de evitar que falte datos. Un intervalo de cinco minutos debería ser perfectamente adecuado para la mayoría de las implementaciones.
