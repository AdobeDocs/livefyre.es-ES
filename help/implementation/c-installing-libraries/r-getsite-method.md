---
description: Devuelve un nuevo objeto Site.
seo-description: Devuelve un nuevo objeto Site.
seo-title: getSite Network (método)
solution: Experience Manager
title: getSite Network (método)
uuid: 67de781e-5240-4be5-9e93-c614828e0bb5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---


# getSite Network Method{#getsite-network-method}

Devuelve un nuevo objeto Site.
|Variable|Tipo|Descripción|
|— |— |— |
|siteId|String|El ID proporcionado por Livefyre para el sitio web o la aplicación a la que pertenece la colección. Por ejemplo: 303617.  |
|siteKey|String|La clave secreta proporcionada por Livefyre para siteId.  |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

