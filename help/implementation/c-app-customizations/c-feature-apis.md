---
description: Automatización del proceso mediante las API de características
seo-description: Automatización del proceso mediante las API de características
seo-title: API de funciones
title: API de funciones
uuid: eac 3 a 156-0 b 60-4 ffa -8 b 6 f-e 451 eb 03 da 77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# API de funciones{#feature-apis}

Automatización del proceso mediante las API de características

Utilice las API de funciones para automatizar el proceso por el que se muestra el contenido. Por ejemplo, al crear una aplicación de comentarios o blogs en directo, incluya todo el contenido publicado por un moderador seleccionado para dirigir la conversación y establecer coherencia dentro del flujo.

Livefyre ofrece las API de funciones y no funciones.

## Función {#section_jpw_nqw_xz}

**Recurso**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

Introduzca el token de usuario para el moderador seleccionado.

**Datos de anuncio**

```
{value: <number>} 
```

El valor se utilizará para ordenar el contenido destacado, mayor a menor (10 aparecerá antes de 1 en la lista de contenido destacado). Este valor toma **ahora** el valor predeterminado en tiempo de época, por lo que los comentarios destacados normalmente se ordenarán de nuevo a más antiguos.

**Respuesta de ejemplo**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>El campo de datos aún no está en uso.

## No funcionalidades {#section_knh_mqw_xz}

**Recurso**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Introduzca el token de usuario para el moderador seleccionado.

**Respuesta de ejemplo**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>El campo de datos aún no está en uso.

