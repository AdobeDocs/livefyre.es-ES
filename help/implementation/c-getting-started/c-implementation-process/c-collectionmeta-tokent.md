---
description: Cree un token único en el servidor que identifique cada colección que cree.
seo-description: Cree un token único en el servidor que identifique cada colección que cree.
seo-title: CollectionMeta Token
solution: Experience Manager
title: CollectionMeta Token
uuid: d5db0b0f-2807-4392-874a-94ac3c1e7550
translation-type: tm+mt
source-git-commit: acba83da6abd919062025322beeced500a3db662
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 2%

---


# CollectionMeta Token{#collectionmeta-token}

Cree un token único en el servidor que identifique cada colección que cree.

Livefyre asigna un identificador único a cada colección que cree. Livefyre asigna un título, una dirección URL y otros parámetros, incluidos:

## Parámetros de collectionMeta Token

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| networkName | Cadena (opcional) | El nombre de la red Livefyre (disponible en {!UICONTROL Studio > Configuración > Ajustes de integración > Credenciales]). Esto es opcional cuando se utiliza la biblioteca para crear un token collectionMeta. |
| networkKey | Cadena (opcional) | Clave secreta para la red específica (disponible en Studio > Configuración > Configuración de integración > Credenciales ). Esto es opcional cuando se utiliza la biblioteca para crear un token collectionMeta. |
| siteId | Cadena (opcional) | ID del sitio (disponible en [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Opcional cuando se utiliza la biblioteca para crear un token collectionMeta. |
| siteKey | Cadena (opcional) | Clave secreta para el sitio (disponible en {!UICONTROL Studio > Configuración > Configuración de integración > Credenciales]). |
| articleId | Cadena (opcional) | Un ID exclusivo para la colección. |
| title | Cadena (opcional) | Título que desea aplicar a la colección. Normalmente, esto corresponde al título de la página que muestra la aplicación. <br>Por ejemplo: &quot;¡La integración es tan divertida!&quot; <br>Nota:  La longitud máxima de caracteres del título es de 255 caracteres. El campo de título no admite entidades HTML. Codifique caracteres especiales con UTF-8. |
| url | Cadena (opcional) | Dirección URL absoluta canónica que desea adjuntar a esta colección. Esta URL se utilizará para generar vínculos de regreso a la aplicación a partir de contenido compartido en Facebook y Twitter, notificaciones por correo electrónico y Livefyre Studio. <br>Nota:  Si realiza pruebas localmente, utilice un dominio de URL base válido (por ejemplo: válido: `https://customer.com`; no válido: `https://localhost:5995`). |
| etiquetas | Cadena (opcional) | lista separada por comas de palabras clave o frases únicas. Buscar colecciones por etiquetas mediante Studio.  </br>Nota:  Las etiquetas no pueden contener espacios. Utilice caracteres de subrayado si desea que aparezca un espacio en la interfaz de usuario. |
| extensiones | JSON (opcional) | Conjunto de parámetros con formato JSON para pasarlos a la colección. |

## Java {#section_orz_m4n_sz}

```
import com.livefyre.Livefyre; 
import com.livefyre.core.Network; 
import com.livefyre.core.Site; 
import com.livefyre.core.Collection; 
  
Network network = Livefyre.getNetwork("networkName", "networkKey"); 
Site site = network.getSite("siteId", "siteKey"); 
Collection collection = site.buildCommentsCollection("title", "articleId", "https://www.example.com"); 
collection.getData().setTags("tags"); 
  
String collectionMetaToken = collection.buildCollectionMetaToken();
```

## NodeJS {#section_kpk_44n_sz}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork('networkName', 'networkKey'); 
var site = network.getSite('siteId', 'siteKey'); 
var collection = site.buildCommentsCollection('title', 'articleId', 'https://www.example.com'); 
collection.data.tags = 'tags'; 
  
var collectionMetaToken = collection.buildCollectionMetaToken(); 
```

## PHP {#section_zmd_zbj_tz}

```
$network = Livefyre::getNetwork("networkName", "networkKey"); 
$site = $network->getSite("siteId", "siteKey"); 
$collection = $site->buildCommentsCollection("title", "articleId", "https://www.example.com"); 
$collection->getData()->setTags("tags"); 
  
$collectionMetaToken = $collection->buildCollectionMetaToken();
```

## Python {#section_rdm_prj_tz}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token()
```

## Ruby {#section_l5n_qrj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```

>[!NOTE]
>
>Livefyre recibe el token collectionMeta que crea y determina la exclusividad combinando siteId (Livefyre proporcionado) y articleId (cliente especificado).
