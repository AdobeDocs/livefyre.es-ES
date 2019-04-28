---
description: Informa a Livefyre de que extrae información de usuario de una URL de sincronización de usuarios establecida anteriormente. Devuelve un valor booleano.
seo-description: Informa a Livefyre de que extrae información de usuario de una URL de sincronización de usuarios establecida anteriormente. Devuelve un valor booleano.
seo-title: Método de red syncuser
solution: Experience Manager
title: Método de red syncuser
uuid: 2 affb 03 d -3907-4 b 01-9 a 64-02 ba 1 b 06 da 14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método de red syncuser{#syncuser-network-method}

Informa a Livefyre de que extrae información de usuario de una URL de sincronización de usuarios establecida anteriormente. Devuelve un valor booleano.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| Userid | Cadena | ID de usuario para sincronizar con Livefyre. Debe tener una URL de sincronización de usuario establecida con Livefyre antes de llamar a este método. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Salida de muestra:

```
true
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

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

## Ejemplo Ruby {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Salida de muestra:

```
True
```
