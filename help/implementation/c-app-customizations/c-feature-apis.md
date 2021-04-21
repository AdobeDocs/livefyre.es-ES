---
description: Automatice el proceso mediante las API de funciones
title: API de funciones
exl-id: 765e47fe-a406-44e6-b4fb-b2e85fc83c01
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# API de funciones{#feature-apis}

Automatice el proceso mediante las API de funciones

Utilice las API de funciones para automatizar el proceso mediante el cual se muestra el contenido. Por ejemplo, al crear un blog en directo o una aplicación de comentarios, personalice todo el contenido publicado por un moderador seleccionado para dirigir la conversación y establecer la coherencia dentro del flujo.

Livefyre ofrece tanto API de funciones como de función.

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

El valor se utilizará para ordenar el contenido destacado, de mayor a menor (10 aparecerá antes de 1 en la lista de contenido destacado). El valor predeterminado es **now** en el tiempo de época, por lo que los comentarios destacados se clasificarán normalmente de más reciente a más antiguo.

**Respuesta de ejemplo**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>El campo de datos aún no está en uso.

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
>El campo de datos aún no está en uso.
