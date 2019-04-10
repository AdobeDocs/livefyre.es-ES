---
description: Devuelve un testigo autenticado autenticado de usuario para la red desde
  la que se llama.
seo-description: Devuelve un testigo autenticado autenticado de usuario para la red
  desde la que se llama.
seo-title: Método de red de builduserauthtoken
solution: Experience Manager
title: Método de red de builduserauthtoken
uuid: 8828 d 356-c 3 c 6-46 a 6-91 bf -83 bd 59 e 35050
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método de red de builduserauthtoken{#builduserauthtoken-network-method}

Devuelve un testigo autenticado autenticado de usuario para la red desde la que se llama.

| Variable | Tipo | Descripción |
|--- |--- |--- |
| Userid | Cadena | El ID de usuario del usuario al que pertenece este token. |
| Displayname | Cadena | Nombre para mostrar del usuario. |
| caduca | Doble | Cuando el token debe caducar en segundos. |

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Ejemplo Ruby {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
