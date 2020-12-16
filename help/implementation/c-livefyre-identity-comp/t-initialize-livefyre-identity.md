---
description: El paquete de autenticación Livefyre.js garantiza que todos los componentes sociales de la página puedan descubrir una única integración de autenticación.
seo-description: El paquete de autenticación Livefyre.js garantiza que todos los componentes sociales de la página puedan descubrir una única integración de autenticación.
seo-title: Inicializar la identidad de Livefyre
title: Inicializar la identidad de Livefyre
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Inicializar la identidad de Livefyre{#initialize-livefyre-identity}

El paquete de autenticación Livefyre.js garantiza que todos los componentes sociales de la página puedan descubrir una única integración de autenticación.

Livefyre proporciona un paquete `lfep-auth-delegate` que le hará un delegado de autenticación adecuado. Se debe proporcionar a la autenticación un objeto AuthDelegate que sepa cómo realizar acciones de autenticación, como el inicio de sesión y el cierre de sesión.

1. Añada Livefyre.js a su página web.
1. Para indicar a Auth que delegue estas acciones a la identidad de Livefyre, agregue lo siguiente:

   ```
   Livefyre.require([ 
     'livefyre-auth', 
     'identity' 
     ], function (auth, Identity) { 
       var identity = new Identity({ 
         app: "https://identity.livefyre.com/{networkName}.fyre.co" 
       }); 
    auth.delegate( identity ); 
    });
   ```
