---
description: Ponga el contenido de la comunidad a disposición de los rastreadores de motores de búsqueda.
seo-description: Ponga el contenido de la comunidad a disposición de los rastreadores de motores de búsqueda.
seo-title: Bootstrap HTML
solution: Experience Manager
title: Bootstrap HTML
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Bootstrap HTML

Ponga el contenido de la comunidad a disposición de los rastreadores de motores de búsqueda.

Para obtener una lista completa de los extremos disponibles, consulte la sección Referencia [de la](https://api.livefyre.com/docs) API de Livefyre.

Las aplicaciones de Livefyre requieren que ejecute JavaScript en la página para mostrar el contenido de las colecciones. Dado que la mayoría de los rastreadores de motores de búsqueda no pueden ejecutar JavaScript, no pueden ver el contenido que anuncia su comunidad. Utilice la API HTML de Bootstrap para agregar fragmentos de este contenido en los que se puede buscar a la respuesta HTTP inicial de la página, lo que permite que el contenido y las palabras clave mejoren la optimización del motor de búsqueda.

>[!NOTE]
>
>Esta API solo está disponible para los tipos Comentarios y Live Blog Collection.

## Integración

La API HTML de Bootstrap de Livefyre devolverá un fragmento HTML del contenido del usuario, que puede incluirse en la respuesta HTTP de la página. Los rastreadores de motores de búsqueda podrán leer esta respuesta sin ejecutar ningún JavaScript. Una vez que la página esté activa en el navegador del usuario, el fragmento HTML se reemplazará por la utilidad completa e interactiva y el usuario podrá publicar contenido.

Para implementar la API HTML de Bootstrap:

1. Realice una solicitud de API de servidor a servidor en el extremo HTML de Bootstrap documentado a continuación.

   >[!NOTE]
   >
   >Si intenta capturar el HTML de Bootstrap para una conversación que aún no existe (es decir, si todavía no ha incrustado la aplicación o creado la colección), recibirá un 200, pero con contenido que tiene un aspecto similar a: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Si su devolución no incluye contenido con un "404", guárdelo en una cadena. Puede almacenar en caché esta respuesta para usarla posteriormente a fin de evitar solicitar la API HTML de Bootstrap en cada carga de página.
1. Inserte la cadena HTML de Bootstrap en la página web donde desee que aparezca el contenido.
1. Proporcione la página web al explorador (o al buscador del motor de búsqueda).

## Recurso

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parámetros

* **networkName** El nombre de red proporcionado por Livefyre. Por ejemplo: *laboratorios* en `labs.fyre.co`.
* **siteId** El ID del sitio de la colección.
* **b64articleId** El ID del artículo de la colección con la codificación base64url.

## Ejemplo

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Respuesta

```
https://gist.github.com/ec5c2457322faf9cf515 
```
