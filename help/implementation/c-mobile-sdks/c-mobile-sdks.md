---
description: Agregue Livefyre a sus aplicaciones móviles nativas.
title: SDK para móvil
exl-id: e05001a4-6199-4d98-a661-123e031b657b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 4%

---

# SDK para móvil{#mobile-sdks}

Agregue Livefyre a sus aplicaciones móviles nativas.

Hay varias opciones disponibles para implementaciones móviles, según el grado de personalización que planifique realizar:

* Aplicaciones web móviles
* SDK para Android o iOS de Livefyre
* API HTTP

## Aplicaciones web móviles {#section_t2k_vpb_11b}

Los clientes que abren una página web en un dispositivo móvil obtienen automáticamente un flujo de contenido de Livefyre optimizado para dispositivos móviles, incluido el estilo para adaptarse al tamaño de pantalla reducido y las modificaciones para gestionar eventos táctiles.

>[!NOTE]
>
>Cuando se utiliza una aplicación Livefyre en una WebView de Android, el parámetro Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) debe establecerse en true. Si localStorage no está habilitado, Livefyre no podrá iniciar sesión en la aplicación Livefyre.

Para optimizar para dispositivos móviles, Livefyre limita los comentarios, los blogs en directo y la aplicación de chat establecidos para incluir:

* Anuncio
* Editar 
* Marcar
* Me gusta
* Responder
* Recuento de oyentes
* Recuento de comentarios
* Moderación pendiente en línea
* Sobremesas
* Comentarios principales
* Subprocesos en caliente
* Comentarios de cola

En las aplicaciones web móviles, al hacer clic en el nombre de un autor, se abre la información de la tarjeta de visita en una página nueva.

## SDK de Android o iOS de Livefyre {#section_zdz_spb_11b}

Livefyre también proporciona dos SDK para móviles: un SDK para iOS y un SDK para Android. Estos SDK son envolventes alrededor de nuestros extremos HTTP, creados para proporcionar un método más sencillo de enviar y recibir datos. No se proporciona ninguna interfaz con estos SDK, lo que permite una buena flexibilidad en la forma en que se muestra y utiliza el contenido en la aplicación móvil.

Los SDK para Android e iOS admiten las siguientes funciones para Comentarios, Blogs en directo y Chat:

| Funciones de iOS: | Funciones de Android: |
|--- |--- |
| <ul><li> Anuncio </li><li>Editar  </li><li>Marcar </li><li>Me gusta </li><li>Responder </li><li>Subprocesos en caliente</li></ul> | <ul><li>Anuncio </li><li>Editar  </li><li>Me gusta </li><li>Responder </li><li>Subprocesos en caliente</li></ul> |

## API HTTP {#section_yqb_qpb_11b}

Las API HTTP son el grupo de puntos finales que le permite crear conversaciones y contenido en la plataforma Livefyre. También alimenta todos los flujos de Livefyre fuera de la caja. Aunque esta solución requiere más tiempo de desarrollo por parte de su equipo de ingeniería, proporciona buena flexibilidad al utilizar el grupo de productos Livefyre y permite la integración nativa con dispositivos móviles.

>[!IMPORTANT]
>
>**No** cree tokens de autenticación de usuarios dentro del cliente móvil, ya que esto requeriría que expusiera la clave de red secreta de Livefyre dentro de una aplicación no segura. Para obtener una solución más sólida y segura, consulte la sección Tokens de autenticación de usuario .
