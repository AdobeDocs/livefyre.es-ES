---
description: null
seo-description: null
seo-title: Método del sitio de compildcollection
solution: Experience Manager
title: Método del sitio de compildcollection
uuid: 52 abc 42 a -9506-4492-b 219-f 2 e 05 eb 79 c 5 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método del sitio de compildcollection{#buildcollection-site-method}

| Variable | Tipo | Descripción |
|--- |--- |--- |
| type | Collectiontype | El tipo de la colección. |
| title | Cadena | Título de la colección. |
| Articleid | Cadena | ID de artículo único que eligió identificar una colección dentro del sitio. |
| url | Cadena | La URL canónica canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Ejemplo Ruby {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
