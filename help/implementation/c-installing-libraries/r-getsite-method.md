---
description: Devuelve un nuevo objeto Site.
seo-description: Devuelve un nuevo objeto Site.
seo-title: Método de red getsite
solution: Experience Manager
title: Método de red getsite
uuid: 67 de 781 e -5240-4 be 5-9 e 93-c 614828 e 0 bb 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método de red getsite{#getsite-network-method}

Devuelve un nuevo objeto Site.
| Variable | Tipo | Descripción|
|— |— |— |
| Siteid | Cadena | El ID de Livefyre para el sitio Web o la aplicación a la que pertenece la colección. Por ejemplo: 303617. |
| Sitekey | String | El Clave secreta proporcionada por Livefyre para siteid. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

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

## Ejemplo Ruby {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

