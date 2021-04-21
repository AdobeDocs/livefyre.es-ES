---
description: Puede iniciar sesión de un usuario a través de la consola durante la integración y la prueba para depurar la autorización.
title: Depuración del delegado de autenticación
exl-id: fa1c17fa-5aba-4f4c-9217-5823af30af61
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Depuración del delegado de autenticación{#debugging-auth-delegate}

Puede iniciar sesión de un usuario a través de la consola durante la integración y la prueba para depurar la autorización.

Inicie sesión de un usuario a través de la consola utilizando el siguiente `auth.authenticate` (token) y pase un token de usuario de Livefyre para autenticar a los usuarios en la página.

También puede modificar el ejemplo mostrado arriba y agregar el siguiente fragmento en línea en su JavaScript para iniciar sesión rápidamente en Livefyre (requiere una referencia a auth).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```
