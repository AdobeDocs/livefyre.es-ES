---
description: Automatizar el proceso mediante las API de funciones
seo-description: Automatizar el proceso mediante las API de funciones
seo-title: API de funciones
title: API de funciones
uuid: eac3a156-0b60-4ffa-8b6f-e451eb03da77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# API de funciones{#feature-apis}

Automatizar el proceso mediante las API de funciones

Utilice las API de funciones para automatizar el proceso mediante el cual se presenta el contenido. Por ejemplo, al crear un blog en directo o una aplicación de comentarios, incluya todo el contenido publicado por un moderador seleccionado para dirigir la conversación y establecer la coherencia dentro del flujo.

Livefyre ofrece tanto API de funciones como de funciones.

## Función {#section_jpw_nqw_xz}

**Recurso**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

&#x200B; Introduzca el token de usuario del moderador seleccionado.

**Datos de anuncio**

```
{value: <number>} 
```

El valor se utilizará para ordenar el contenido destacado, de mayor a menor (10 aparecerá antes de 1 en la lista de contenido destacado). El valor predeterminado de este valor es **ahora** en el tiempo de la época, por lo que los comentarios de las funciones generalmente se clasifican de más reciente a más antiguo.

**Respuesta de ejemplo**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>El campo de datos aún no se está utilizando.

## Desfunción {#section_knh_mqw_xz}

**Recurso**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Introduzca el token de usuario del moderador seleccionado.

**Respuesta de ejemplo**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>El campo de datos aún no se está utilizando.

