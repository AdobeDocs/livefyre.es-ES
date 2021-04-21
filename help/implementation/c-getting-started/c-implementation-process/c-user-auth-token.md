---
description: En esta sección se describe cómo generar el objeto JSON UserAuth que crea el token de autenticación de usuario necesario para iniciar sesión en las aplicaciones.
title: Token de autenticación de usuario
exl-id: 564144dd-6db4-447b-80ac-b743ecac833d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 2%

---

# Token de autenticación de usuario{#user-auth-token}

En esta sección se describe cómo generar el objeto JSON UserAuth que crea el token de autenticación de usuario necesario para iniciar sesión en las aplicaciones.

En esta sección se describe cómo generar el objeto JSON UserAuth que crea el token de autenticación de usuario necesario para iniciar sesión en las aplicaciones.

Para crear el token, utilice su biblioteca de idiomas preferida para pasar los siguientes parámetros:

| Parámetro | Tipo | Descripción |
|---|---|---|
| networkName | Cadena *requerida* | Nombre de la red Livefyre (proporcionada por Livefyre). |
| networkKey | Cadena *requerida* | La clave secreta para esta red específica (proporcionada por Livefyre). |
| userID | Cadena *requerida* | El ID del usuario que inicia sesión tal como está almacenado en el sistema de administración de usuarios (solo se permiten caracteres alfanuméricos, guiones, guiones bajos y puntos: [a-zA-Z0-9_-.]). **Nota:** El userId debe ser único. |
| caduca | Número entero *obligatorio* | Cuando el token debe caducar a partir de ahora (en segundos). **Nota:** Este valor también se puede pasar como flotante. El token web JSON producido almacenará este valor en tiempo UNIX epoch. |
| displayName | Cadena *requerida* | Texto para identificar a este usuario en la interfaz de usuario y en los comentarios. (Número máximo de caracteres: 50) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## NodeJS {#section_c42_mjz_1cb}

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
>Las claves de red no se comparten para las cuentas demosite de Livefyre. Recibirá una clave de red una vez Livefyre haya aprovisionado un entorno para usted. Esta clave debe mantenerse privada.
