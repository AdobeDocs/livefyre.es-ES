---
description: Utilice Bootstrap y la API de flujo con aplicaciones de Livefyre.
seo-description: Utilice Bootstrap y la API de flujo con aplicaciones de Livefyre.
seo-title: Uso de Bootstrap y API de flujo con aplicaciones de Livefyre
solution: Experience Manager
title: Visualización de detalles de la cuenta
uuid: bace 558 f-ade 8-49 d 6-abda -9 ee 754 ce 4 ac 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Uso de Bootstrap y API de flujo con aplicaciones de Livefyre {#bootstrap-stream-api}

## API de Bootstrap {#bootstrap-api}

### ¿Cómo puedo recuperar contenido anterior a las 50 unidades más recientes? {#howcontentolder}

Bootstrap es todo el contenido de una aplicación de Livefyre. Son los datos almacenados en caché, normalmente de 12 a 20 minutos. Se entrega en bloques de 50 partes y se pagina para poder recuperar contenido que supere los 50 lados.

[Referencia de API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Solicitud de ejemplo](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

La solicitud de ejemplo anterior carga la `init` página que contiene Configuración de colección y el único conjunto inicial de ~ 50 fragmentos de contenido más reciente. Para sondear contenido anterior, debe cargar las siguientes páginas de bootstrap con `N` el número de página:

Solicitud: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Por ejemplo, una aplicación de ejemplo tiene 120 unidades de contenido. El contenido "1" es la parte más antigua de contenido y el contenido "70" es la parte más reciente de contenido.

* `Init` cargarán ~ 120-70 fragmentos de contenido en orden descendente: [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` cargará ~ 1-50 fragmentos de contenido en orden ascendente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` cargará ~ 51-100 unidades de contenido en orden ascendente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` cargará ~ 101-120 unidades de contenido en orden ascendente:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Haga clic aquí para ver el Diagrama de flujo de encuesta de Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API de flujo {#stream-api}

¿Qué es la API de flujo?
El flujo es una encuesta larga que por diseño está pensada para permanecer abierta durante 30 segundos aproximadamente. Aquí puede encontrar la descripción sobre la técnica de sondeo largo: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Este extremo de sondeo largo transmite contenido nuevo (p. ej., un usuario publica un comentario), cambios en el estado del contenido (p. ej., elimina su comentario, cantidad de "Me gusta") y cambios de moderación en contenido (p. ej., aprobador aprueba un fragmento de contenido) a una aplicación de Livefyre.

La solicitud de API de flujo debe ser de ~ 30 segundos (sondeo largo) con el tiempo de espera esperado después de 30 segundos cuando no hay flujos de contenido nuevos en.

Referencia de API: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Ejemplo de solicitud:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Nota: La `maxEventId` respuesta de una API de flujo es el ID de evento más alto de las actualizaciones en esta respuesta. Utilice este valor como `lastEventId` parámetro de ruta cuando cree la URL de la siguiente solicitud de Flujo de flujo para obtener actualizaciones después de todas las actualizaciones en esta respuesta.

El ejemplo siguiente se basa en una aplicación de comentarios:

El comentario "Primer comentario" se publicó primero. Se publicó "Segundo comentario" después.

Respuesta de la API de flujo de comentarios del primer comentario:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

El `maxEventId` en la respuesta es "1520289700953369", que se utilizará para `lastEventId` sondear el punto final para obtener actualizaciones (p. ej. Segundo comentario) que se produce después de todas las actualizaciones de esta respuesta.

Respuesta de la segunda API de flujo de comentarios:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

El `maxEventID` "1520289700953369" de la respuesta debe usarse a su vez como `lastEventID` para crear la respuesta de la API de flujo para la siguiente actualización.