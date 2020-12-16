---
description: Devuelve un objeto Collection creado como tipo de chat. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.
seo-description: Devuelve un objeto Collection creado como tipo de chat. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.
seo-title: buildChatCollection (método de sitio)
solution: Experience Manager
title: buildChatCollection (método de sitio)
uuid: 39ee32d0-29c9-47a8-a458-a3cf7a96db30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# buildChatCollection (método del sitio){#buildchatcollection-site-method}

Devuelve un objeto Collection creado como tipo de chat. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| articleId | Cadena | ID única del artículo que eligió para identificar una colección dentro del sitio. |
| url | Cadena | Dirección URL absoluta canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

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

## Ejemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
