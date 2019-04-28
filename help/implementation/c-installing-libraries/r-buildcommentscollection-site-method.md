---
description: Devuelve un objeto de colección creado como tipo de comentarios. Ejecute createorupdate () desde el objeto Colección para completar el proceso de creación.
seo-description: Devuelve un objeto de colección creado como tipo de comentarios. Ejecute createorupdate () desde el objeto Colección para completar el proceso de creación.
seo-title: Generocomentarios del sitio de recopilación
solution: Experience Manager
title: Generocomentarios del sitio de recopilación
uuid: 0 e 5 c 062 e -960 d -4 ab 0-ba 32-0965731 a 1571
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Generocomentarios del sitio de recopilación{#buildcommentscollection-site-method}

Devuelve un objeto de colección creado como tipo de comentarios. Ejecute createorupdate () desde el objeto Colección para completar el proceso de creación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| Articleid | Cadena | ID de artículo único que eligió identificar una colección dentro del sitio. |
| url | Cadena | La URL canónica canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Ejemplo Ruby {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
