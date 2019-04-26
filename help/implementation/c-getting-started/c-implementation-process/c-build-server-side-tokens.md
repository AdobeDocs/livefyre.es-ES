---
description: Guía para crear collectionmeta y tokens de autenticación.
seo-description: Guía para crear collectionmeta y tokens de autenticación.
seo-title: Generar tokens de servidor
solution: Experience Manager
title: Generar tokens de servidor
uuid: 8313 f 26 e -5 ceb -414 e-a 61 a -480 bb 7 a 8 ba 66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Generar tokens de servidor{#build-server-side-tokens}

Guía para crear collectionmeta y tokens de autenticación.

La creación de los tokens que Livefyre utiliza para validar solicitudes garantiza que solo usted pueda realizar actualizaciones en su red de Livefyre.

## Collectionmeta Token

Aprenda a crear un token para crear nuevas conversaciones y mostrarlas.

## Autentificador de autenticación

Aprenda a crear un token para autenticar usuarios, un paso necesario en el proceso de integración si no utiliza Jashcapture Capture para la administración de usuarios.

## Testigo de autenticación de usuario {#section_l5l_hwt_bbb}

Esta sección describe cómo generar el objeto JSON userauth que crea el testigo Autenticación de usuario necesario para registrar a los usuarios en sus aplicaciones.

Para crear el token, utilice su biblioteca de idioma preferida para pasar los parámetros siguientes:

| Parámetro | Tipo | Descripción |
|---|---|---|
| Networkname | Cadena *requerida* | Nombre de la red de Livefyre (proporcionado por Livefyre). |
| Networkkey | Cadena *requerida* | Clave secreta de esta red específica (proporcionada por Livefyre). |
| Userid | Cadena *requerida* | El ID del usuario que inicia sesión como se almacena en su sistema de administración de usuarios (solo se permiten los caracteres alfanuméricos, guión, guión bajo y puntos): `[a-zA-Z0-9_-.]`). **Nota:** El ID de usuario debe ser único. |
| caduca | *Se requiere entero* | Cuando el token debe caducar desde ahora (en segundos). **Nota:** Este valor también se puede pasar como flotante. El token web JSON producido almacenará este valor en tiempo epoch UNIX. |
| Displayname | Cadena *requerida* | Texto para identificar a este usuario en la interfaz de usuario y en los comentarios. (Número máximo de caracteres: 50.) |

