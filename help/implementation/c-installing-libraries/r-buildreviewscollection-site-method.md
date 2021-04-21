---
description: Devuelve un objeto Collection creado como instancia de tipo Reviews. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.
title: Método del sitio buildReviewsCollection
exl-id: 581ad24c-d115-4ffb-93eb-936c2da6e3fa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# Método del sitio buildReviewsCollection{#buildreviewscollection-site-method}

Devuelve un objeto Collection creado como instancia de tipo Reviews. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| articleId | Cadena | ID de artículo único que eligió para identificar una colección dentro del sitio. |
| url | Cadena | La URL absoluta canónica de esta colección. |


## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildReviewsCollection(title, articleId, url); 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildReviewsCollection(title, articleId, url); 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```
