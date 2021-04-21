---
description: Devuelve un objeto Collection creado como instancia de tipo Blog. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.
title: Método del sitio buildBlogCollection
exl-id: 93565eff-dc4e-4868-9d75-50f16ddb4fa4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# Método del sitio buildBlogCollection{#buildblogcollection-site-method}

Devuelve un objeto Collection creado como instancia de tipo Blog. Ejecute create_or_update() desde el objeto Collection para completar el proceso de compilación.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| title | Cadena | Título de la colección. |
| articleId | Cadena | ID de artículo único que eligió para identificar una colección dentro del sitio. |
| url | Cadena | La URL absoluta canónica de esta colección. |

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
