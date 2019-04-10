---
description: Devuelve un objeto de colección creado como tipo de críticas. Ejecute
  crear_ o_ update () desde el objeto Colección para completar el proceso de creación.
seo-description: Devuelve un objeto de colección creado como tipo de críticas. Ejecute
  crear_ o_ update () desde el objeto Colección para completar el proceso de creación.
seo-title: Método del sitio de recopilación de DPS
solution: Experience Manager
title: Método del sitio de recopilación de DPS
uuid: 88 af 4 c 68-57 de -4 ae 9-9394-550 c 94 ede 48 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método del sitio de recopilación de DPS{#buildreviewscollection-site-method}

Devuelve un objeto de colección creado como tipo de críticas. Ejecute crear_ o_ update () desde el objeto Colección para completar el proceso de creación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| Articleid | Cadena | ID de artículo único que eligió identificar una colección dentro del sitio. |
| url | Cadena | La URL canónica canónica de esta colección. |


## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

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

## Ejemplo Ruby {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

