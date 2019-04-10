---
description: Esta sección describe cómo generar el objeto JSON userauth que crea el
  testigo Autenticación de usuario necesario para registrar a los usuarios en sus
  aplicaciones.
seo-description: Esta sección describe cómo generar el objeto JSON userauth que crea
  el testigo Autenticación de usuario necesario para registrar a los usuarios en sus
  aplicaciones.
seo-title: Testigo de autenticación de usuario
solution: Experience Manager
title: Testigo de autenticación de usuario
uuid: 6483 debd -453 c -4780-b 19 c -1 d 8041693617
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Testigo de autenticación de usuario{#user-auth-token}

Esta sección describe cómo generar el objeto JSON userauth que crea el testigo Autenticación de usuario necesario para registrar a los usuarios en sus aplicaciones.

Esta sección describe cómo generar el objeto JSON userauth que crea el testigo Autenticación de usuario necesario para registrar a los usuarios en sus aplicaciones.

Para crear el token, utilice su biblioteca de idioma preferida para pasar los parámetros siguientes:

| Parámetro | Tipo | Descripción |
|---|---|---|
| Networkname | Cadena *requerida* | Nombre de la red de Livefyre (proporcionado por Livefyre). |
| Networkkey | Cadena *requerida* | Clave secreta de esta red específica (proporcionada por Livefyre). |
| Userid | Cadena *requerida* | El ID del usuario que inicia sesión como se almacena en su sistema de administración de usuarios (solo se permiten los caracteres alfanuméricos, guión, guión bajo y puntos): [a-zA-Z 0-9_-.]). **Nota:** El ID de usuario debe ser único. |
| caduca | *Se requiere entero* | Cuando el token debe caducar desde ahora (en segundos). **Nota:** Este valor también se puede pasar como flotante. El token web JSON producido almacenará este valor en tiempo epoch UNIX. |
| Displayname | Cadena *requerida* | Texto para identificar a este usuario en la interfaz de usuario y en los comentarios. (Número máximo de caracteres: 50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## Nodejs {#section_c42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

## PHP {#section_d42_mjz_1cb}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

## Python {#section_e42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

## Ruby {#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>Las claves de red no se comparten para cuentas de demositio de Livefyre. Recibirá una clave de red una vez que Livefyre haya aprovisionado un entorno. Esta clave debe ser privada.

