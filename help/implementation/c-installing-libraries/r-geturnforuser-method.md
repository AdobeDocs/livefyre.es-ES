---
description: Este método devuelve el URN para el usuario de esta red.
title: getUrnForUser Network (método de red getUrnForUser)
exl-id: 272e724e-d09d-4d7d-9967-a229707ff47f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# getUrnForUser Network Method{#geturnforuser-network-method}

Este método devuelve el URN para el usuario de esta red.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| userID | Cadena | El userId que se va a usar en el URN. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Salida de ejemplo:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

Salida de ejemplo:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

Salida de ejemplo:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

Salida de ejemplo:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

Salida de ejemplo:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
