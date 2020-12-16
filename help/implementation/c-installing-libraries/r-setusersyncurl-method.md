---
description: Informa a Livefyre de que actualice la URL de sincronización de usuarios de la red a la proporcionada. Devuelve un valor Boolean.
seo-description: Informa a Livefyre de que actualice la URL de sincronización de usuarios de la red a la proporcionada. Devuelve un valor Boolean.
seo-title: setUserSyncUrl (método de red)
solution: Experience Manager
title: setUserSyncUrl (método de red)
uuid: cd067e90-a2da-4e3d-8e60-7eabfd86fc7f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# setUserSyncUrl (método de red){#setusersyncurl-network-method}

Informa a Livefyre de que actualice la URL de sincronización de usuarios de la red a la proporcionada. Devuelve un valor Boolean.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| urlTemplate | Cadena | La URL para registrarse en Livefyre y sincronizar los ID de usuario. Requiere que &quot;`{id}`&quot; forme parte de la cadena URL proporcionada. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Salida de muestra:

```
true
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Salida de muestra:

```
true
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Salida de muestra:

```
true
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Salida de muestra:

```
True
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Salida de muestra:

```
True
```
