---
title: Método del sitio buildCollection
description: Método del sitio buildCollection
exl-id: d5c9a2fb-2d30-44f4-8ebf-24b0ec7babee
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 15%

---

# Método del sitio buildCollection{#buildcollection-site-method}

| Variable | Tipo | Descripción |
|--- |--- |--- |
| type | CollectionType | Tipo de colección. |
| title | Cadena | Título de la colección. |
| articleId | Cadena | ID de artículo único que eligió para identificar una colección dentro del sitio. |
| url | Cadena | La URL absoluta canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

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

## Ejemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
