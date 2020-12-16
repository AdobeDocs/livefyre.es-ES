---
description: Una guía para crear tokens de metadatos y autenticación.
seo-description: Una guía para crear tokens de metadatos y autenticación.
seo-title: Generar tokens del lado del servidor
solution: Experience Manager
title: Generar tokens del lado del servidor
uuid: 8313f26e-5ceb-414e-a61a-480bb7a8ba66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# Generar tokens del lado del servidor{#build-server-side-tokens}

Una guía para crear tokens de metadatos y autenticación.

La creación de los tokens que Livefyre utiliza para validar solicitudes garantiza que solo usted puede realizar actualizaciones en su red de Livefyre.

## CollectionMeta Token

Aprenda a crear un token para crear conversaciones nuevas y mostrar las existentes.

## Autentificador

Aprenda a crear un token para autenticar usuarios, un paso necesario en el proceso de integración si no utiliza Janrain Capture para la administración de usuarios.

## Token de autenticación de usuario {#section_l5l_hwt_bbb}

En esta sección se describe cómo generar el objeto JSON UserAuth que crea el autentificador de autenticación de usuario necesario para iniciar sesión en las aplicaciones.

Para crear el token, utilice la biblioteca de idioma que prefiera para pasar los siguientes parámetros:

| Parámetro | Tipo | Descripción |
|---|---|---|
| networkName | Cadena *requerida* | Nombre de la red Livefyre (proporcionada por Livefyre). |
| networkKey | Cadena *requerida* | Clave secreta para esta red específica (proporcionada por Livefyre). |
| userID | Cadena *requerida* | ID del usuario que inicia sesión como almacenado en el sistema de administración de usuarios (solo se permiten caracteres alfanuméricos, guiones, guiones bajos y puntos: `[a-zA-Z0-9_-.]`). **Nota:** El userId debe ser único. |
| expires | Número entero *requerido* | El token debe caducar a partir de ahora (en segundos). **Nota:** Este valor también se puede pasar como flotante. El token web de JSON generado almacenará este valor en tiempo de época de UNIX. |
| displayName | Cadena *requerida* | Texto para identificar a este usuario en la interfaz de usuario y en los comentarios. (Número máximo de caracteres: 50) |

