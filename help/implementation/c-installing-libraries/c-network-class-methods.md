---
description: Cree un objeto Network.
seo-description: Cree un objeto Network.
seo-title: Métodos de clase de red
solution: Experience Manager
title: Métodos de clase de red
uuid: 4130beda-dd09-49ae-aafb-f6b956e30b51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 13%

---


# Métodos de clase de red{#network-class-methods}

Cree un objeto Network.

Una vez creado un objeto de red, el resto de la página supondrá que tiene un objeto de red con instancias en la sesión.

## Objeto de red

| Parámetro | Tipo | Descripción |
|---|---|---|
| *`network`* | Cadena | Tu red Livefyre. Por ejemplo: “`labs.fyre.co`”. |
| *`networkKey`* | Cadena | Clave secreta proporcionada por Livefyre para la red. |

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
