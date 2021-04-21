---
description: Una guía para crear tokens de colección Meta y autenticación.
title: Generar tokens del lado del servidor
exl-id: f709b79e-9236-443e-b862-c7d281815d91
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---

# Generar tokens del lado del servidor{#build-server-side-tokens}

Una guía para crear tokens de colección Meta y autenticación.

La creación de los tokens que utiliza Livefyre para validar las solicitudes garantiza que solo usted pueda realizar actualizaciones en su red de Livefyre.

## CollectionMeta Token

Aprenda a crear un token para crear conversaciones nuevas y mostrar las existentes.

## Token de autenticación

Obtenga información sobre cómo crear un token para autenticar usuarios, un paso necesario en el proceso de integración si no utiliza Janrain Capture para la administración de usuarios.

## Token de autenticación de usuario {#section_l5l_hwt_bbb}

En esta sección se describe cómo generar el objeto JSON UserAuth que crea el token de autenticación de usuario necesario para iniciar sesión en las aplicaciones.

Para crear el token, utilice su biblioteca de idiomas preferida para pasar los siguientes parámetros:

| Parámetro | Tipo | Descripción |
|---|---|---|
| networkName | Cadena *requerida* | Nombre de la red Livefyre (proporcionada por Livefyre). |
| networkKey | Cadena *requerida* | La clave secreta para esta red específica (proporcionada por Livefyre). |
| userID | Cadena *requerida* | El ID del usuario que inicia sesión tal como está almacenado en el sistema de administración de usuarios (solo se permiten caracteres alfanuméricos, guiones, guiones bajos y puntos: `[a-zA-Z0-9_-.]`). **Nota:** El userId debe ser único. |
| caduca | Número entero *obligatorio* | Cuando el token debe caducar a partir de ahora (en segundos). **Nota:** Este valor también se puede pasar como flotante. El token web JSON producido almacenará este valor en tiempo UNIX epoch. |
| displayName | Cadena *requerida* | Texto para identificar a este usuario en la interfaz de usuario y en los comentarios. (Número máximo de caracteres: 50) |
