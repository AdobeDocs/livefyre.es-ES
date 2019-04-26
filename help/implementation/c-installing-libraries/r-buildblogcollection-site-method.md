---
description: Devuelve un objeto de colección creado como tipo de blog. Ejecute crear_
  o_ update () desde el objeto Colección para completar el proceso de creación.
seo-description: Devuelve un objeto de colección creado como tipo de blog. Ejecute
  crear_ o_ update () desde el objeto Colección para completar el proceso de creación.
seo-title: Método del sitio de buildblogcollection
solution: Experience Manager
title: Método del sitio de buildblogcollection
uuid: 6 a 5 ec 6 b 9-bc 32-467 a-abe 6-a 57 c 6 defe 067
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método del sitio de buildblogcollection{#buildblogcollection-site-method}

Devuelve un objeto de colección creado como tipo de blog. Ejecute crear_ o_ update () desde el objeto Colección para completar el proceso de creación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| Articleid | Cadena | ID de artículo único que eligió identificar una colección dentro del sitio. |
| url | Cadena | La URL canónica canónica de esta colección. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

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

## Ejemplo Ruby {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

