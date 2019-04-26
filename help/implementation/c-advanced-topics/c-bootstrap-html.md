---
description: Hacer que el contenido de la comunidad esté disponible para los rastreadores
  de motores de búsqueda.
seo-description: Hacer que el contenido de la comunidad esté disponible para los rastreadores
  de motores de búsqueda.
seo-title: HTML de Bootstrap
solution: Experience Manager
title: HTML de Bootstrap
uuid: 137 e 4382-4 e 7 b -4124-9 d 35-1 d 872 a 497 bc 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# HTML de Bootstrap

Hacer que el contenido de la comunidad esté disponible para los rastreadores de motores de búsqueda.

Para obtener una lista completa de los puntos finales disponibles, consulte la sección Referencia [de la API](https://api.livefyre.com/docs) de Livefyre.

Las aplicaciones de Livefyre requieren que ejecute JavaScript en la página para mostrar contenido de sus colecciones. Debido a que la mayoría de los rastreadores de motores de búsqueda no puede ejecutar JavaScript, no pueden ver el contenido que las publicaciones de la comunidad. Utilice la API de HTML de Bootstrap para agregar fragmentos que pueden buscar de este contenido a la respuesta HTTP inicial de su página, permitiendo que el contenido y las palabras clave mejoren la optimización de los motores de búsqueda.

>[!NOTE]
>
>Esta API solo está disponible para los tipos de comentarios y recopilación de blogs en directo.

## de CRM

La API HTML de Bootstrap HTML devolverá un fragmento HTML de su contenido de usuario, que puede incluirse en la respuesta HTTP de la página. Esta respuesta será legible por los rastreadores de motores de búsqueda sin ejecutar JavaScript. Una vez que la página esté activa en el navegador de un usuario, el fragmento HTML será reemplazado por la utilidad completa, interactiva y el usuario podrá publicar contenido.

Para implementar la API de HTML de Bootstrap:

1. Realice una solicitud de servidor a API de servidor al extremo HTML de Bootstrap que se documentó a continuación.

   >[!NOTE]
   >
   >Si intenta capturar el HTML de Bootstrap para una conversación que aún no existe (es decir, si aún no ha incrustado la aplicación o crea la colección), recibirá un 200, pero con contenido similar a: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Si el retorno no incluye contenido con un «404», guárdelo en una cadena. Puede almacenar en caché esta respuesta para usarla posteriormente para evitar solicitar la API de HTML de Bootstrap en cada página.
1. Inserte la cadena HTML de Bootstrap en la página web donde desee que aparezca el contenido.
1. Proporcione su página web al navegador (o buscador de motores de búsqueda).

## Recurso

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parámetros

* **Networkname** Su Livefyre ha proporcionado el nombre de la red. Por ejemplo: *labs* in `labs.fyre.co`.
* **Siteid** El ID del sitio de la colección.
* **b 64 articleid** El ID del artículo de la colección con la codificación de URL base 64.

## Ejemplo

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Respuesta

```
https://gist.github.com/ec5c2457322faf9cf515 
```
