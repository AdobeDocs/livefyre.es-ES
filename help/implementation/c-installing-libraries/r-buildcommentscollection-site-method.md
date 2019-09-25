---
description: Devuelve un objeto Collection creado como un tipo Comments. Ejecute createOrUpdate() desde el objeto Collection para completar el proceso de compilación.
seo-description: Devuelve un objeto Collection creado como un tipo Comments. Ejecute createOrUpdate() desde el objeto Collection para completar el proceso de compilación.
seo-title: buildCommentsCollection (método de sitio)
solution: Experience Manager
title: buildCommentsCollection (método de sitio)
uuid: 0e5c062e-960d-4ab0-ba32-0965731a1571
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildCommentsCollection (método de sitio){#buildcommentscollection-site-method}

Devuelve un objeto Collection creado como un tipo Comments. Ejecute createOrUpdate() desde el objeto Collection para completar el proceso de compilación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| articleId | Cadena | ID única del artículo que eligió para identificar una colección dentro del sitio. |
| url | Cadena | Dirección URL absoluta canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

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

## Ejemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
