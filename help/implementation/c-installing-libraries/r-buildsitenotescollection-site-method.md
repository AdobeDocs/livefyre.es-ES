---
description: Devuelve un objeto Collection creado como un tipo Sidenotes. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.
seo-description: Devuelve un objeto Collection creado como un tipo Sidenotes. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.
seo-title: buildSitenotesCollection (método de sitio)
solution: Experience Manager
title: buildSitenotesCollection (método de sitio)
uuid: 2bfbc032-4c0c-48d2-8ce6-02460b38bd6c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# buildSitenotesCollection (método del sitio){#buildsitenotescollection-site-method}

Devuelve un objeto Collection creado como un tipo Sidenotes. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| articleId | Cadena | ID única del artículo que eligió para identificar una colección dentro del sitio. |
| url | Cadena | Dirección URL absoluta canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildSidenotesCollection(title, articleId, url); 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```
