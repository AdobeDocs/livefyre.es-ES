---
description: Devuelve un objeto de colección creado como tipo de chat. Ejecute crear_
  o_ update () desde el objeto Colección para completar el proceso de creación.
seo-description: Devuelve un objeto de colección creado como tipo de chat. Ejecute
  crear_ o_ update () desde el objeto Colección para completar el proceso de creación.
seo-title: Método del sitio de buildchatcollection
solution: Experience Manager
title: Método del sitio de buildchatcollection
uuid: 39 ee 32 d 0-29 c 9-47 a 8-a 458-a 3 cf 7 a 96 db 30
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método del sitio de buildchatcollection{#buildchatcollection-site-method}

Devuelve un objeto de colección creado como tipo de chat. Ejecute crear_ o_ update () desde el objeto Colección para completar el proceso de creación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| Articleid | Cadena | ID de artículo único que eligió identificar una colección dentro del sitio. |
| url | Cadena | La URL canónica canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Ejemplo Ruby {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
