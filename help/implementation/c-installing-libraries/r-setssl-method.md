---
description: Establece SSL para que las llamadas a la API estén activadas o desactivadas.
title: Método de red setSSL
exl-id: 5682b84a-0b4d-479b-af40-60d2c6c38155
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# setSSL Network Method{#setssl-network-method}

Establece SSL para que las llamadas a la API estén activadas o desactivadas.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| ssl | Booleano | El valor predeterminado es true. si desea activar SSL, false en caso contrario. <br><ul><li>True: SSL activado </li><li>False: SSL desactivado</li></ul> |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

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

## Ejemplo de Ruby {#section_enh_gds_rz}

```
network.ssl = false 
```
