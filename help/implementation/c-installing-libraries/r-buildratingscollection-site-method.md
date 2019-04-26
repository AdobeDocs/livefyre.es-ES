---
description: Devuelve un objeto de colección creado como tipo de clasificaciones.
  Ejecute crear_ o_ update () desde el objeto Colección para completar el proceso
  de creación.
seo-description: Devuelve un objeto de colección creado como tipo de clasificaciones.
  Ejecute crear_ o_ update () desde el objeto Colección para completar el proceso
  de creación.
seo-title: Método del sitio de recopilación de buildratingscollection
title: Método del sitio de recopilación de buildratingscollection
uuid: 5 eea 2 ba 3-48 e 1-4 cd 2-aa 73-ea 81788 af 1 df
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método del sitio de recopilación de buildratingscollection{#buildratingscollection-site-method}

Devuelve un objeto de colección creado como tipo de clasificaciones. Ejecute crear_ o_ update () desde el objeto Colección para completar el proceso de creación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| Articleid | Cadena | ID de artículo único que eligió identificar una colección dentro del sitio. |
| url | Cadena | La URL canónica canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildRatingsCollection(title, articleId, url); 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildRatingsCollection(title, articleId, url); 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

## Ejemplo Ruby {#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

