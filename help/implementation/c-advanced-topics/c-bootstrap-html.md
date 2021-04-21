---
description: Poner el contenido de la comunidad a disposición de los rastreadores de motores de búsqueda.
title: HTML de Bootstrap
exl-id: 22ab4f2d-f433-4805-b0dd-16d4531e425d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---

# HTML de Bootstrap

Poner el contenido de la comunidad a disposición de los rastreadores de motores de búsqueda.

Para obtener una lista completa de los puntos finales disponibles, consulte la sección [Referencia de API](https://api.livefyre.com/docs) de Livefyre.

Las aplicaciones de Livefyre requieren que ejecute JavaScript en la página para mostrar contenido para sus colecciones. Debido a que la mayoría de los rastreadores de motores de búsqueda no pueden ejecutar JavaScript, no pueden ver el contenido que publica su comunidad. Utilice la API HTML de Bootstrap para añadir fragmentos de este contenido que se puedan buscar a la respuesta HTTP inicial de la página, lo que permite que el contenido y las palabras clave mejoren la optimización de los motores de búsqueda.

>[!NOTE]
>
>Esta API solo está disponible para los tipos Comentarios y Colección de blogs en directo.

## Integración

La API HTML Bootstrap de Livefyre devolverá un fragmento HTML del contenido del usuario, que puede incluirse en la respuesta HTTP de la página. Los rastreadores de motores de búsqueda podrán leer esta respuesta sin ejecutar JavaScript. Una vez que la página está activa en el explorador de un usuario, el fragmento HTML se sustituye por el widget completo e interactivo y el usuario puede publicar contenido.

Para implementar la API HTML del Bootstrap:

1. Realice una solicitud de API de servidor a servidor al extremo HTML del Bootstrap documentado a continuación.

   >[!NOTE]
   >
   >Si está intentando obtener el HTML Bootstrap para una conversación que aún no existe (es decir, si todavía tiene que incrustar la aplicación o crear la colección), recibirá un 200, pero con contenido que tiene un aspecto similar al siguiente: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Si la devolución no incluye contenido con un &quot;404&quot; en él, guárdelo en una cadena. Puede almacenar en caché esta respuesta para usarla más adelante a fin de evitar solicitar la API HTML de Bootstrap en cada carga de página.
1. Inserte la cadena HTML Bootstrap en la página web donde desee que aparezca el contenido.
1. Entregue la página web al navegador (o al buscador del motor de búsqueda).

## Recurso

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parámetros

* **** networkNameSu Livefyre proporcionó un nombre de red. Por ejemplo: *labs* en `labs.fyre.co`.
* **** siteIdEl ID del sitio de la colección.
* **b64** articleId El ID del artículo de la colección utilizando la codificación base64url.

## Ejemplo

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Respuesta

```
https://gist.github.com/ec5c2457322faf9cf515 
```
