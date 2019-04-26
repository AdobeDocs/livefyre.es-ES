---
description: Informa a Livefyre de que actualice la URL de sincronización de usuario
  de la red con la proporcionada. Devuelve un valor booleano.
seo-description: Informa a Livefyre de que actualice la URL de sincronización de usuario
  de la red con la proporcionada. Devuelve un valor booleano.
seo-title: Método de red setusersyncurl
solution: Experience Manager
title: Método de red setusersyncurl
uuid: cd 067 e 90-a 2 da -4 e 3 d -8 e 60-7 eabfd 86 fc 7 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método de red setusersyncurl{#setusersyncurl-network-method}

Informa a Livefyre de que actualice la URL de sincronización de usuario de la red con la proporcionada. Devuelve un valor booleano.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| Urltemplate | Cadena | La URL para registrarse en Livefyre para sincronizar los ID de usuario. Requiere que «`{id}`» forme parte de la cadena URL proporcionada. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Salida de muestra:

```
true
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

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

## Ejemplo Ruby {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Salida de muestra:

```
True
```
