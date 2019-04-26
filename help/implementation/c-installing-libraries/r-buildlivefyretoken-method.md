---
description: Devuelve un testigo de Livefyre válido cifrado que se puede utilizar
  para interactuar con otra API de Livefyre para la red desde la que se llama.
seo-description: Devuelve un testigo de Livefyre válido cifrado que se puede utilizar
  para interactuar con otra API de Livefyre para la red desde la que se llama.
seo-title: Método de red de buildlivefyretoken
solution: Experience Manager
title: Método de red de buildlivefyretoken
uuid: 7 c 72 a 05 f -669 b -4 df 3-8117-aa 4 af 2 f 7 a 179
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método de red de buildlivefyretoken{#buildlivefyretoken-network-method}

Devuelve un testigo de Livefyre válido cifrado que se puede utilizar para interactuar con otra API de Livefyre para la red desde la que se llama.

Devuelve un testigo de Livefyre válido cifrado que se puede utilizar para interactuar con otra API de Livefyre para la red desde la que se llama.

De forma predeterminada, este token está configurado para caducar en 24 horas desde el momento de su creación.

## Ejemplo de Java {#section_nyl_ycs_rz}

```
network.buildLivefyreToken(); 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Ejemplo de nodejs {#section_xkd_gds_rz}

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

## Ejemplo Ruby {#section_enh_gds_rz}

```
network.build_livefyre_token() 
```

Salida de muestra:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

