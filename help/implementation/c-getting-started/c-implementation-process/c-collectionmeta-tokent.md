---
description: Cree un distintivo único en el servidor que identifica cada colección
  que cree.
seo-description: Cree un distintivo único en el servidor que identifica cada colección
  que cree.
seo-title: Collectionmeta Token
solution: Experience Manager
title: Collectionmeta Token
uuid: d 5 db 0 b 0 f -2807-4392-874 a -94 ac 3 c 1 e 7550
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Collectionmeta Token{#collectionmeta-token}

Cree un distintivo único en el servidor que identifica cada colección que cree.

Livefyre asigna un identificador único a cada colección que cree. Livefyre asigna un título, una dirección URL y otros parámetros, entre ellos:

## Collectionmeta Token Parameters

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| Networkname | Cadena (opcional) | El nombre de la red de Livefyre (disponible desde {! UICONTROL Studio > Settings > Integration Settings > Credentials]). Es opcional al utilizar la biblioteca para crear un token collectionmeta. |
| Networkkey | Cadena (opcional) | Clave secreta de la red específica (disponible desde Studio > Configuración > Ajustes de integración > Credenciales). Es opcional al utilizar la biblioteca para crear un token collectionmeta. |
| Siteid | Cadena (opcional) | ID del sitio (disponible desde [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Opcional al utilizar la biblioteca para crear un token collectionmeta. |
| Sitekey | Cadena (opcional) | La clave secreta del sitio (disponible desde {! UICONTROL Studio > Settings > Integration Settings > Credentials]). |
| Articleid | Cadena (opcional) | ID único de la colección. |
| title | Cadena (opcional) | Título que desea aplicar a la colección. Normalmente, esto corresponde al título de la página que muestra la aplicación. <br>Por ejemplo: «La integración es tan divertida! »» <br>Nota: La longitud máxima de caracteres para el título es de 255 caracteres. El campo de título no admite entidades HTML. Codifique caracteres especiales con UTF -8. |
| url | Cadena (opcional) | Dirección URL canónica que desea adjuntar a esta colección. Esta URL se utilizará para generar vínculos de vuelta a la aplicación desde contenido compartido en Facebook y Twitter, notificaciones por correo electrónico y Livefyre Studio. <br>Nota: Si realiza pruebas localmente, utilice un dominio de URL base válido (por ejemplo: válido: `https://customer.com`; invalid: `https://localhost:5995`). |
| tags | Cadena (opcional) | Lista separada por comas de frases o palabras clave únicas. Buscar colecciones por etiquetas mediante Studio. </br>Nota: Las etiquetas no pueden contener espacios. Utilice guiones bajos si desea que aparezca un espacio en la interfaz de usuario. |
| extensiones | JSON (opcional) | Conjunto de params con formato JSON para transmitir a la colección. |

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

## Nodejs {#section_kpk_44n_sz}

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

>[!NOTE] {important = "high"}
>
>Livefyre recibe el token collectionmeta que genera y determina la exclusividad combinando siteid (proporcionado por Livefyre) y articleid (cliente especificado).

