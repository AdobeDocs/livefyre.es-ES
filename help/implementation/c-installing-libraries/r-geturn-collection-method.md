---
description: Este método devuelve el URN de esta colección. Debe ejecutar createOrUpdate() antes de ejecutar este método.
seo-description: Este método devuelve el URN de esta colección. Debe ejecutar createOrUpdate() antes de ejecutar este método.
seo-title: getUrn (método de recopilación)
solution: Experience Manager
title: getUrn (método de recopilación)
uuid: 2f4d7796-2ae5-4b74-a958-40825c6bff16
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getUrn (método de recopilación){#geturn-collection-method}

Este método devuelve el URN de esta colección. Debe ejecutar createOrUpdate() antes de ejecutar este método.

## Ejemplo de Java {#section_nyl_ycs_rz}

```
collection.getUrn(); 
```

Salida de muestra:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Ejemplo de NodeJS {#section_xkd_gds_rz}

```
collection.getUrn(); 
```

Salida de muestra:

```
<span class="str">"urn:livefyre:network=`example.fyre.co`:site=1:collection=1"</span>
```

## Ejemplo de PHP {#section_ghf_gds_rz}

```
$collection->getUrn(); 
```

Salida de muestra:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Ejemplo de Python {#section_dwg_gds_rz}

```
collection.urn() 
```

Salida de muestra:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Ejemplo de Ruby {#section_enh_gds_rz}

```
collection.urn
```

Salida de muestra:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

