---
description: Devuelve un objeto Collection creado como un tipo de clasificación. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.
seo-description: Devuelve un objeto Collection creado como un tipo de clasificación. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.
seo-title: buildRatingsCollection (método de sitio)
title: buildRatingsCollection (método de sitio)
uuid: 5eea2ba3-48e1-4cd2-aa73-ea81788af1df
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildRatingsCollection (método de sitio){#buildratingscollection-site-method}

Devuelve un objeto Collection creado como un tipo de clasificación. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| articleId | Cadena | ID única del artículo que eligió para identificar una colección dentro del sitio. |
| url | Cadena | Dirección URL absoluta canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

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

## Ejemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

