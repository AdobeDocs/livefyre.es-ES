---
description: Use la API de Bootstrap y flujo con aplicaciones de Livefyre.
title: Visualización de los detalles de la cuenta
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# Usar la API de Bootstrap y flujo con las aplicaciones de Livefyre {#bootstrap-stream-api}

## API del Bootstrap {#bootstrap-api}

### ¿Cómo puedo recuperar contenido anterior a las 50 piezas más recientes? {#howcontentolder}

Bootstrap es todo contenido de una aplicación de Livefyre. Son los datos en caché, normalmente de 12 a 20 minutos de antigüedad. Se entrega en trozos de 50 piezas y se pagina para que pueda recuperar contenido de más de 50 piezas.

[Referencia de API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Solicitud de ejemplo](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

La solicitud de ejemplo anterior carga la página `init` que contiene la configuración de la colección y el único conjunto inicial de ~50 fragmentos de contenido más reciente. Para sondear el contenido anterior, debe cargar las páginas de arranque subsiguientes con `N` como número de página:

Solicitud: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Por ejemplo, una aplicación de ejemplo tiene 120 fragmentos de contenido. El contenido &quot;1&quot; es la parte de contenido más antigua y el contenido &quot;70&quot; es la parte de contenido más reciente.

* `Init` cargará ~120-70 fragmentos de contenido en orden descendente:  [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` cargará ~ 1-50 fragmentos de contenido en orden ascendente:  [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` cargará ~ 51-100 fragmentos de contenido en orden ascendente:  [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` cargará ~101-120 fragmentos de contenido en orden ascendente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Haga clic aquí para ver el diagrama de flujo de la encuesta del Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API de flujo {#stream-api}

¿Qué es la API de flujo?
Stream es una encuesta larga que, por diseño, está pensada para permanecer abierta durante aproximadamente 30 segundos. La descripción de la técnica de sondeo largo se puede encontrar aquí: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Este extremo de sondeo prolongado transmite contenido nuevo (por ejemplo, un usuario publica un comentario), cambios en el estado del contenido (por ejemplo, el usuario elimina su comentario, &quot;Me gusta&quot;) y cambios de moderación en el contenido (por ejemplo, el moderador aprueba un fragmento de contenido) en una aplicación de Livefyre.

La solicitud a la API de flujo debe ser de ~30 segundos (sondeo largo) con el tiempo de espera esperado después de 30 segundos cuando no se transmita ningún contenido nuevo.

Referencia de API: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Solicitud de ejemplo:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Tenga en cuenta: El `maxEventId` en una respuesta de API de flujo es el ID de evento más alto de las actualizaciones en esta respuesta. Utilice este valor como parámetro de ruta `lastEventId` al crear la URL de la siguiente solicitud de API de flujo para obtener actualizaciones que se produzcan después de todas las actualizaciones de esta respuesta.

El ejemplo siguiente se basa en una aplicación de comentarios:

El comentario &quot;Primer comentario&quot; se publicó primero. &quot;Segundo comentario&quot; fue publicado después.

Primera respuesta de API de flujo de comentarios:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

El `maxEventId` en la respuesta es &quot;1520289700953369&quot; que se utilizará como `lastEventId` para sondear el punto final para obtener actualizaciones (es decir, el segundo comentario) que se produzcan después de todas las actualizaciones en esta respuesta.

Segunda respuesta de API de flujo de comentarios:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

A su vez, el `maxEventID` &quot;1520289700953369&quot; en la respuesta debe utilizarse como `lastEventID` para crear la respuesta de la API de flujo para la siguiente actualización.
