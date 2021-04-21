---
description: Devuelve un nuevo objeto Site.
title: getSite Network (método de red)
exl-id: 88782da9-88c6-4e60-9a23-e46d68675d59
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '54'
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
