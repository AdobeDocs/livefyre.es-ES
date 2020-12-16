---
description: En esta sección se describe cómo generar el objeto JSON UserAuth que crea el autentificador de autenticación de usuario necesario para iniciar sesión en las aplicaciones.
seo-description: En esta sección se describe cómo generar el objeto JSON UserAuth que crea el autentificador de autenticación de usuario necesario para iniciar sesión en las aplicaciones.
seo-title: Autentificador de usuario
solution: Experience Manager
title: Autentificador de usuario
uuid: 6483debd-453c-4780-b19c-1d8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 2%

---


# Token de autenticación de usuario{#user-auth-token}

En esta sección se describe cómo generar el objeto JSON UserAuth que crea el autentificador de autenticación de usuario necesario para iniciar sesión en las aplicaciones.

En esta sección se describe cómo generar el objeto JSON UserAuth que crea el autentificador de autenticación de usuario necesario para iniciar sesión en las aplicaciones.

Para crear el token, utilice la biblioteca de idioma que prefiera para pasar los siguientes parámetros:

| Parámetro | Tipo | Descripción |
|---|---|---|
| networkName | Cadena *requerida* | Nombre de la red Livefyre (proporcionada por Livefyre). |
| networkKey | Cadena *requerida* | Clave secreta para esta red específica (proporcionada por Livefyre). |
| userID | Cadena *requerida* | ID del usuario que inicia sesión como almacenado en el sistema de administración de usuarios (solo se permiten caracteres alfanuméricos, guiones, guiones bajos y puntos: [a-zA-Z0-9_-.]). **Nota:** El userId debe ser único. |
| expires | Número entero *requerido* | El token debe caducar a partir de ahora (en segundos). **Nota:** Este valor también se puede pasar como flotante. El token web de JSON generado almacenará este valor en tiempo de época de UNIX. |
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
>Las claves de red no se comparten para las cuentas de Livefyre demosite. Recibirá una clave de red una vez Livefyre haya suministrado un entorno. Esta clave debe mantenerse privada.

