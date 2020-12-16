---
description: Devuelve un token de Livefyre válido cifrado que puede utilizarse para interactuar con otras API de Livefyre para la red desde la que se llama.
seo-description: Devuelve un token de Livefyre válido cifrado que puede utilizarse para interactuar con otras API de Livefyre para la red desde la que se llama.
seo-title: buildLivefyreToken Network (método)
solution: Experience Manager
title: buildLivefyreToken Network (método)
uuid: 7c72a05f-669b-4df3-8117-aa4af2f7a179
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# buildLivefyreToken Network (método){#buildlivefyretoken-network-method}

Devuelve un token de Livefyre válido cifrado que puede utilizarse para interactuar con otras API de Livefyre para la red desde la que se llama.

Devuelve un token de Livefyre válido cifrado que puede utilizarse para interactuar con otras API de Livefyre para la red desde la que se llama.

De forma predeterminada, este token está configurado para caducar en 24 horas desde el momento de su creación.

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.buildLivefyreToken(); 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
network.buildLivefyreToken(); 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
network.buildLivefyreToken(); 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
network.build_livefyre_token() 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
network.build_livefyre_token() 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

