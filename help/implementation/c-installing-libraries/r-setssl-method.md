---
description: Establece SSL para que las llamadas de API estén activadas o desactivadas.
seo-description: Establece SSL para que las llamadas de API estén activadas o desactivadas.
seo-title: Setssl Network Method
solution: Experience Manager
title: Setssl Network Method
uuid: 8 d 989 e 63-c 859-456 a -99 ca -8 d 87933913 ba
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Setssl Network Method{#setssl-network-method}

Establece SSL para que las llamadas de API estén activadas o desactivadas.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| ssl | Booleano | El valor predeterminado es true. si desea SSL en, false en caso contrario. <br><ul><li>Verdadero - SSL </li><li>Falso - SSL DESACTIVADO</li></ul> |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Ejemplo Ruby {#section_enh_gds_rz}

```
network.ssl = false 
```
