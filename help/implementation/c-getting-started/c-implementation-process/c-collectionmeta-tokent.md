---
description: Cree un token único en el servidor que identifique cada colección que cree.
title: CollectionMeta Token
exl-id: 52edfe75-5ce6-40c9-9afe-c34a3812f1e7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 3%

---

# CollectionMeta Token{#collectionmeta-token}

Cree un token único en el servidor que identifique cada colección que cree.

Livefyre asigna un identificador único a cada colección que cree. Livefyre asigna un título, una dirección URL y otros parámetros, entre ellos:

## Parámetros de collectionMeta Token

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| networkName | Cadena (opcional) | El nombre de la red de Livefyre (disponible en [!UICONTROL Studio] > [!UICONTROL Settings] > [!UICONTROL Integration Settings] > [!UICONTROL Credentials] ). Esto es opcional al usar la biblioteca para crear un token collectionMeta. |
| networkKey | Cadena (opcional) | La clave secreta para la red específica (disponible en Studio > Settings > Integration Settings > Credentials ). Esto es opcional al usar la biblioteca para crear un token collectionMeta. |
| siteId | Cadena (opcional) | El ID del sitio (disponible desde [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Opcional al usar la biblioteca para crear un token collectionMeta. |
| siteKey | Cadena (opcional) | La clave secreta del sitio (disponible en [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). |
| articleId | Cadena (opcional) | Un ID único para la colección. |
| title | Cadena (opcional) | El título que desea aplicar a la colección. Normalmente, corresponde al título de la página que muestra la aplicación. <br>Por ejemplo: &quot;¡La integración es tan divertida!&quot; <br>Nota: La longitud máxima de caracteres del título es de 255 caracteres. El campo de título no admite entidades HTML. Codifique caracteres especiales utilizando UTF-8. |
| url | Cadena (opcional) | La URL absoluta canónica que desea adjuntar a esta colección. Esta URL se utilizará para generar vínculos a la aplicación a partir de contenido compartido en Facebook y Twitter, notificaciones por correo electrónico y Livefyre Studio. <br>Nota: Si realiza la prueba localmente, utilice un dominio de URL base válido (por ejemplo: válido:  `https://customer.com`; no válido:  `https://localhost:5995`). |
| etiquetas | Cadena (opcional) | Una lista separada por comas de palabras clave o expresiones únicas. Buscar colecciones por etiquetas usando Studio.  </br>Nota: Las etiquetas no pueden contener espacios. Utilice guiones bajos si desea que aparezca un espacio en la interfaz de usuario. |
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
>Livefyre recibe el token collectionMeta que usted genera y determina la exclusividad combinando siteId (proporcionado por Livefyre) y articleId (especificado por el cliente).
