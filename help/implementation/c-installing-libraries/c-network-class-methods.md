---
description: Cree un objeto Network .
title: Métodos de clase de red
exl-id: 5a011120-05d0-4768-9038-6a312e8c5dd1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 14%

---

# Métodos de clase de red{#network-class-methods}

Cree un objeto Network .

Una vez creado un objeto de red, el resto de la página supondrá que tiene un objeto de red creado como instancia en la sesión.

## Objeto de red

| Parámetro | Tipo | Descripción |
|---|---|---|
| *`network`* | Cadena | Su red Livefyre. Por ejemplo: “`labs.fyre.co`”. |
| *`networkKey`* | Cadena | La clave secreta proporcionada por Livefyre para la red. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## NodeJS {#section_nyk_dzs_kbb}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork(network, networkKey); 
```

## PHP {#section_oyk_dzs_kbb}

```
use Livefyre\Livefyre; 
  
$network = Livefyre::getNetwork(network, networkKey); 
```

## Python {#section_pyk_dzs_kbb}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network(network, networkKey) 
```

## Ruby {#section_qyk_dzs_kbb}

```
require 'livefyre' 
  
network = Livefyre.get_network(network, networkKey) 
```
