---
description: Establece SSL para que las llamadas de API estén activadas o desactivadas.
seo-description: Establece SSL para que las llamadas de API estén activadas o desactivadas.
seo-title: setSSL Network (método)
solution: Experience Manager
title: setSSL Network (método)
uuid: 8d989e63-c859-456a-99ca-8d87933913ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setSSL Network (método){#setssl-network-method}

Establece SSL para que las llamadas de API estén activadas o desactivadas.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| ssl | Booleano | El valor predeterminado es true. si desea activar SSL, false en caso contrario. <br><ul><li>True: SSL activado </li><li>Falso - SSL desactivado</li></ul> |

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
