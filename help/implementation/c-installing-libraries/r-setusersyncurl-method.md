---
description: Informa a Livefyre de que actualice la URL de sincronización de usuarios de la red a la que se proporciona. Devuelve un valor Boolean.
title: Método de red setUserSyncUrl
exl-id: 8124ac0f-013f-4943-a33c-6cf8fe696f95
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# setUserSyncUrl (método de red){#setusersyncurl-network-method}

Informa a Livefyre de que actualice la URL de sincronización de usuarios de la red a la que se proporciona. Devuelve un valor Boolean.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| urlTemplate | Cadena | La URL para registrarse en Livefyre y sincronizar los ID de usuario. Requiere que &quot;`{id}`&quot; forme parte de la cadena de URL proporcionada. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Salida de ejemplo:

```
true
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Salida de ejemplo:

```
true
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Salida de ejemplo:

```
true
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Salida de ejemplo:

```
True
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Salida de ejemplo:

```
True
```
