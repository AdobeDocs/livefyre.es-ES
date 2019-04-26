---
description: Crear un objeto de red.
seo-description: Crear un objeto de red.
seo-title: Métodos de clase de red
solution: Experience Manager
title: Métodos de clase de red
uuid: 4130 beda-dd 09-49 ae-aafb-f 6 b 956 e 30 b 51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Métodos de clase de red{#network-class-methods}

Crear un objeto de red.

Una vez creado un objeto de red, el resto de la página asumirá que tiene un objeto de red creado en la sesión.

## Objeto de red

| Parámetro | Tipo | Descripción |
|---|---|---|
| *`network`* | Cadena | Su red de Livefyre. Por ejemplo: «`labs.fyre.co`». |
| *`networkKey`* | Cadena | Clave secreta proporcionada por Livefyre para la red. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## Nodejs {#section_nyk_dzs_kbb}

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
