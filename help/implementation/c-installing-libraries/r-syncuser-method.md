---
description: Informa a Livefyre para extraer la información del usuario de una URL de sincronización de usuario establecida anteriormente. Devuelve un valor Boolean.
seo-description: Informa a Livefyre para extraer la información del usuario de una URL de sincronización de usuario establecida anteriormente. Devuelve un valor Boolean.
seo-title: syncUser Network (método)
solution: Experience Manager
title: syncUser Network (método)
uuid: 2affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# syncUser Network Method{#syncuser-network-method}

Informa a Livefyre para extraer la información del usuario de una URL de sincronización de usuario establecida anteriormente. Devuelve un valor Boolean.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| userID | Cadena | ID de usuario que se va a sincronizar con Livefyre. Debe tener una URL de sincronización de usuario establecida con Livefyre antes de llamar a este método. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Salida de muestra:

```
true
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

Salida de muestra:

```
true
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

Salida de muestra:

```
true
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

Salida de muestra:

```
True
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Salida de muestra:

```
True
```
