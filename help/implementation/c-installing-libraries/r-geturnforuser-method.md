---
description: Este método devuelve el URN del usuario de esta red.
seo-description: Este método devuelve el URN del usuario de esta red.
seo-title: getUrnForUser (método de red)
solution: Experience Manager
title: getUrnForUser (método de red)
uuid: b70b8b0f-2b3a-4a1d-90d0-93a97a137ad4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getUrnForUser (método de red){#geturnforuser-network-method}

Este método devuelve el URN del usuario de esta red.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| userID | Cadena | UserId que se usará en la URN. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Salida de muestra:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

Salida de muestra:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

Salida de muestra:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

Salida de muestra:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

Salida de muestra:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
