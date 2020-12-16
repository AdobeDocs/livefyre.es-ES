---
description: Devuelve un objeto Collection creado como un tipo de blog. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.
seo-description: Devuelve un objeto Collection creado como un tipo de blog. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.
seo-title: buildBlogCollection (método del sitio)
solution: Experience Manager
title: buildBlogCollection (método del sitio)
uuid: 6a5ec6b9-bc32-467a-abe6-a57c6defe067
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# buildBlogCollection (método del sitio){#buildblogcollection-site-method}

Devuelve un objeto Collection creado como un tipo de blog. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| articleId | Cadena | ID única del artículo que eligió para identificar una colección dentro del sitio. |
| url | Cadena | Dirección URL absoluta canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildBlogCollection(title, articleId, url); 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildBlogCollection(title, articleId, url); 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

