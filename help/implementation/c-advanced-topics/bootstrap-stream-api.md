---
description: Utilice la API de flujo y Bootstrap con las aplicaciones de Livefyre.
seo-description: Utilice la API de flujo y Bootstrap con las aplicaciones de Livefyre.
seo-title: Uso de la API de flujo y Bootstrap con las aplicaciones de Livefyre
solution: Experience Manager
title: Visualización de los detalles de la cuenta
uuid: bace558f-ade8-49d6-abda-9ee754ce4ac0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---


# Usar la API de flujo y Bootstrap con las aplicaciones de Livefyre {#bootstrap-stream-api}

## API de Bootstrap {#bootstrap-api}

### ¿Cómo puedo recuperar contenido mayor que las 50 piezas más recientes? {#howcontentolder}

Bootstrap es todo contenido de una aplicación de Livefyre. Son los datos almacenados en caché, que suelen tener entre 12 y 20 minutos de antigüedad. Se distribuye en fragmentos de 50 piezas y se pagina para que pueda recuperar contenido de más de 50 piezas.

[Referencia de API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Solicitud de ejemplo](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

La solicitud de ejemplo anterior carga la página `init` que contiene la configuración de la colección y el único conjunto inicial de ~50 fragmentos de contenido más reciente. Para sondear contenido antiguo, debe cargar las páginas de arranque subsiguientes con `N` como número de página:

Solicitud: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Por ejemplo, una aplicación de ejemplo tiene 120 fragmentos de contenido. El contenido &quot;1&quot; es el contenido más antiguo y el contenido &quot;70&quot; es el contenido más reciente.

* `Init` cargará ~120-70 fragmentos de contenido en orden descendente:  [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` cargará ~ 1-50 fragmentos de contenido en orden ascendente:  [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` cargará entre 51 y 100 fragmentos de contenido en orden ascendente:  [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` cargará ~101-120 fragmentos de contenido en orden ascendente:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Haga clic aquí para ver el diagrama de flujo de la encuesta Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API de flujo {#stream-api}

¿Qué es la API de flujo?
El flujo es una encuesta larga que, por diseño, está pensada para permanecer abierta durante aproximadamente 30 segundos. La descripción de la técnica de sondeo largo se puede encontrar aquí: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Este extremo de sondeo largo transmite contenido nuevo (p. ej., un usuario publica un comentario), cambios en el estado del contenido (p. ej., el usuario elimina su comentario, me gusta) y cambios en la moderación del contenido (p. ej., el moderador aprueba un fragmento de contenido) a una aplicación de Livefyre.

La solicitud a la API de flujo debe ser de ~30 segundos (sondeo largo) con el tiempo de espera esperado después de 30 segundos cuando no hay ningún flujo de contenido nuevo.

Referencia de API: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Ejemplo de solicitud:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Tenga en cuenta: La `maxEventId` en una respuesta de API de flujo es el ID de Evento más alto de las actualizaciones en esta respuesta. Utilice este valor como parámetro de ruta `lastEventId` al generar la dirección URL de la siguiente solicitud de API de flujo para obtener actualizaciones que se produzcan después de todas las actualizaciones de esta respuesta.

El ejemplo siguiente se basa en una aplicación de comentarios:

El comentario &quot;Primer comentario&quot; se publicó primero. &quot;Segundo comentario&quot; se publicó después.

Primera respuesta de API de flujo de comentarios:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

El `maxEventId` de la respuesta es &quot;1520289700953369&quot;, que se utilizará como `lastEventId` para sondear el extremo y obtener actualizaciones (es decir, segundo comentario) después de todas las actualizaciones de esta respuesta.

Segunda respuesta de API de flujo de comentarios:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

El `maxEventID` &quot;1520289700953369&quot; de la respuesta debe utilizarse como `lastEventID` para generar la respuesta de la API de flujo para la siguiente actualización.