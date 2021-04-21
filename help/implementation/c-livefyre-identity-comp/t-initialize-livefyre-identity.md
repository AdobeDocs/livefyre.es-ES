---
description: El paquete de autenticación de Livefyre.js garantiza que todos los componentes sociales de la página puedan descubrir una sola integración de autenticación.
title: Inicializar la identidad de Livefyre
exl-id: 9990d284-a21e-49fb-932c-62906b41484a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Inicializar la identidad de Livefyre{#initialize-livefyre-identity}

El paquete de autenticación de Livefyre.js garantiza que todos los componentes sociales de la página puedan descubrir una sola integración de autenticación.

Livefyre proporciona un paquete `lfep-auth-delegate` que hará que usted sea el delegado de autenticación adecuado. Se debe proporcionar a la autenticación un objeto AuthDelegate que sepa cómo realizar acciones de autenticación, como el inicio de sesión y el cierre de sesión.

1. Agregue Livefyre.js a su página web.
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
