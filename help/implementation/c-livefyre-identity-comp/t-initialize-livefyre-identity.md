---
description: El paquete de autenticación de Livefyre. js garantiza que todos los componentes sociales de la página puedan descubrir una única integración de autenticación.
seo-description: El paquete de autenticación de Livefyre. js garantiza que todos los componentes sociales de la página puedan descubrir una única integración de autenticación.
seo-title: Inicializar identidad de Livefyre
title: Inicializar identidad de Livefyre
uuid: 9365 d 827-2734-4 a 84-bfe 7-9 be 573 b 2 b 03 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Inicializar identidad de Livefyre{#initialize-livefyre-identity}

El paquete de autenticación de Livefyre. js garantiza que todos los componentes sociales de la página puedan descubrir una única integración de autenticación.

Livefyre proporciona `lfep-auth-delegate` un paquete que le enviará un delegado de autenticación adecuado. Se debe proporcionar un objeto authdelegate que sepa cómo realizar acciones de autenticación, como iniciar sesión y cerrar sesión.

1. Agregue Livefyre. js a su página web.
1. Para indicar a Auth que delege estas acciones en la identidad de Livefyre, agregue lo siguiente:

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
