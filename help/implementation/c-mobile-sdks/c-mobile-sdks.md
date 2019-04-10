---
description: Agregue Livefyre a sus aplicaciones móviles nativas.
seo-description: Agregue Livefyre a sus aplicaciones móviles nativas.
seo-title: SDK para móviles
solution: Experience Manager
title: SDK para móviles
uuid: 84 c 7 ca 1 c -3401-492 a-bfa 5-62 b 996947 a 44
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# SDK para móviles{#mobile-sdks}

Agregue Livefyre a sus aplicaciones móviles nativas.

Existen varias opciones disponibles para implementaciones móviles, según el alcance de la personalización que tenga pensado realizar:

* Aplicaciones web móviles
* SDK de Livefyre o iOS para iOS
* API HTTP

## Aplicaciones web móviles {#section_t2k_vpb_11b}

Los clientes que abren una página web en un dispositivo móvil obtienen automáticamente un flujo de contenido de Livefyre optimizado para dispositivos móviles, incluido el estilo para adaptarse al tamaño de pantalla reducido y las modificaciones para gestionar eventos táctiles.

>[!NOTE]
>
>Al utilizar una aplicación de Livefyre en Android webview, el parámetro [Websettings. setdomstorageenabled de Android](https://developer.android.com/reference/android/webkit/WebSettings.html) debe definirse como true. Si localstorage no está habilitado, Livefyre no podrá iniciar sesión en la aplicación de Livefyre.

Para optimizar para dispositivos móviles, Livefyre limita las funciones de los comentarios, el blog directo y la aplicación de chat para incluir:

* Anuncio
* Editar
* Indicador
* Me gusta
* Responder
* Recuento de oyentes
* Recuento de comentarios
* Moderación pendiente en línea
* Hovercards
* Comentarios principales
* Hilos interactivos
* Comentarios en cola

En aplicaciones web móviles, al hacer clic en el nombre de un autor se abre información de la tarjeta en una página nueva.

## SDK de Android Android o SDK para iOS {#section_zdz_spb_11b}

Livefyre también proporciona dos SDK para móviles: un SDK para iOS y un SDK para Android. Estos SDK son contenedores alrededor de nuestros terminales HTTP, creados con el fin de proporcionar un método más sencillo para enviar y recibir datos. No se proporciona ninguna interfaz con estos SDK, lo que permite una mayor flexibilidad en la forma en que se muestra y se utiliza el contenido dentro de la aplicación móvil.

Los SDK de Android y iOS admiten las siguientes funciones para Comentarios, Blog directo y Chat:

| Funciones de iOS: | Funciones de Android: |
|--- |--- |
| <ul><li> Anuncio </li><li>Editar </li><li>Indicador </li><li>Me gusta </li><li>Responder </li><li>Hilos interactivos</li></ul> | <ul><li>Anuncio </li><li>Editar </li><li>Me gusta </li><li>Responder </li><li>Hilos interactivos</li></ul> |

## API HTTP {#section_yqb_qpb_11b}

Las API de HTTP son el grupo de puntos finales que le permite crear conversaciones y contenido en la plataforma de Livefyre. También alimenta todos los flujos de Livefyre. Aunque esta solución requiere más tiempo de desarrollo de su equipo de ingeniería, proporciona mayor flexibilidad al utilizar el grupo de productos de Livefyre y permite una integración móvil nativa.

>[!IMPORTANT]
>
>**No** cree tokens de autenticación de usuario dentro del cliente móvil, ya que esto requiere que exponga su clave de red secreta de Livefyre en una aplicación no segura. Para obtener una solución más segura y segura, consulte la sección Autentificadores de autenticación de usuarios.

