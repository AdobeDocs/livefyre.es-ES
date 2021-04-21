---
description: Informa a Livefyre para extraer información de usuario de una URL de sincronización de usuarios establecida anteriormente. Devuelve un valor Boolean.
title: syncUser Network (método de red syncUser)
exl-id: a21ff487-2ab1-4788-b455-84941f03a98f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

---

# syncUser Network Method{#syncuser-network-method}

Informa a Livefyre para extraer información de usuario de una URL de sincronización de usuarios establecida anteriormente. Devuelve un valor Boolean.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| userID | Cadena | El ID de usuario que se va a sincronizar con Livefyre. Debe tener una URL de sincronización de usuarios configurada con Livefyre antes de llamar a este método. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Salida de ejemplo:

```
true
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

Salida de ejemplo:

```
true
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

Salida de ejemplo:

```
true
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

Salida de ejemplo:

```
True
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Salida de ejemplo:

```
True
```
