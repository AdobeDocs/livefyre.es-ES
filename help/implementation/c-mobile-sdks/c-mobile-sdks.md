---
description: Agregue Livefyre a sus aplicaciones móviles nativas.
seo-description: Agregue Livefyre a sus aplicaciones móviles nativas.
seo-title: SDK para móvil
solution: Experience Manager
title: SDK para móvil
uuid: 84c7ca1c-3401-492a-bfa5-62b996947a44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK para móvil{#mobile-sdks}

Agregue Livefyre a sus aplicaciones móviles nativas.

Existen varias opciones disponibles para implementaciones móviles, según el grado de personalización que tenga pensado realizar:

* Aplicaciones web móviles
* SDK para Android o iOS de Livefyre
* API HTTP

## Aplicaciones web móviles {#section_t2k_vpb_11b}

Los clientes que abren una página web en un dispositivo móvil obtienen automáticamente un flujo de contenido de Livefyre optimizado para dispositivos móviles, incluido el estilo para adaptarse al tamaño de pantalla reducido y las modificaciones para gestionar eventos táctiles.

>[!NOTE]
>
>Al utilizar una aplicación Livefyre en una vista web de Android, el parámetro [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) de Android debe establecerse en true. Si localStorage no está habilitado, Livefyre no podrá iniciar sesión en la aplicación Livefyre.

Para optimizar para dispositivos móviles, Livefyre limita el conjunto de funciones Comentarios, Blogs en vivo y Aplicación de chat para incluir:

* Anuncio
* Editar 
* Marcar
* Me gusta
* Responder
* Recuento de escucha
* Recuento de comentarios
* Moderación pendiente en línea
* Hovercards
* Comentarios principales
* Subprocesos en caliente
* Comentarios de cola

En Aplicaciones web móviles, al hacer clic en el nombre de un autor se abre la información de la tarjeta de visita en una página nueva.

## Livefyre Android SDK o iOS SDK {#section_zdz_spb_11b}

Livefyre también proporciona dos SDK para móviles: un SDK para iOS y un SDK para Android. Estos SDK son envolventes alrededor de nuestros extremos HTTP, creados para proporcionar un método más sencillo de enviar y recibir datos. No se proporciona ninguna interfaz con estos SDK, lo que permite una mayor flexibilidad en la forma en que se muestra y se utiliza el contenido en la aplicación móvil.

Los SDK para Android e iOS admiten las siguientes funciones para Comentarios, Blog en directo y Chat:

| Funciones de iOS: | Funciones de Android: |
|--- |--- |
| <ul><li> Anuncio </li><li>Editar  </li><li>Marcar </li><li>Me gusta </li><li>Responder </li><li>Subprocesos en caliente</li></ul> | <ul><li>Anuncio </li><li>Editar  </li><li>Me gusta </li><li>Responder </li><li>Subprocesos en caliente</li></ul> |

## API HTTP {#section_yqb_qpb_11b}

Las API HTTP son el grupo de extremos que le permite crear conversaciones y contenido en la plataforma Livefyre. También alimenta a todos los Livefyre de los flujos de caja. Aunque esta solución requiere más tiempo de desarrollo por parte de su equipo de ingeniería, proporciona mayor flexibilidad al utilizar el grupo de productos Livefyre y permite la integración nativa con dispositivos móviles.

>[!IMPORTANT]
>
>**No cree** tokens de autenticación de usuarios en el cliente móvil, ya que esto requeriría que exponga la clave de red secreta de Livefyre en una aplicación no segura. Para obtener una solución más sólida y segura, consulte la sección Tokens de autenticación de usuario.

