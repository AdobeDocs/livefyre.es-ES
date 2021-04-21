---
description: Conozca las convenciones de Livefyre y cómo organiza el contenido Livefyre.
title: Arquitectura
exl-id: d4fe12d1-117a-4aae-90ff-e9ebdd6c5bac
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Arquitectura{#architecture}

Conozca las convenciones de Livefyre y cómo organiza el contenido Livefyre.

Esta sección proporciona información general sobre la arquitectura de red de Livefyre.

## Información general sobre redes y sitios

Livefyre organiza los usuarios y el contenido por red y sitio. Cada red puede tener una o más cuentas de usuario asociadas, y cada red puede incluir uno o más sitios de Livefyre. Un sitio Livefyre es una agrupación arbitraria de Colecciones. Una colección se asigna a un ID de artículo en el CMS.

## Explicación de las redes {#section_hqt_4m4_xz}

Los clientes con varios dominios pueden compartir cuentas de usuario en todos los dominios mediante una sola red de Livefyre. Los clientes que deseen mantener cuentas de usuario independientes para distintos dominios necesitarán redes de Livefyre independientes.

Los ajustes de configuración se pueden aplicar a sitios, redes y colecciones (lo que se conoce como conversación en la ilustración anterior).

>[!NOTE]
>
>Algunos ajustes solo están disponibles en el nivel de red (como las preferencias de notificación de correo electrónico, el correo electrónico de la dirección y los logotipos personalizados de correo electrónico). Si desea que esta configuración sea diferente para cada dominio, debe utilizar varias redes.

## Explicación de los sitios {#section_vjw_nm4_xz}

Un sitio es una agrupación arbitraria de artículos. La agrupación es útil, ya que le permite asignar diferentes moderadores a diferentes grupos de contenido. Los moderadores y propietarios pueden configurarse para moderar el contenido y configurar la configuración de administración a nivel de red o de sitio. Si desea que algunos moderadores solo vean ciertas colecciones, estas colecciones pueden configurarse como un sitio separado de Livefyre.

>[!NOTE]
>
>No hay límite en el número de sitios que puede tener en su red personalizada.

## Diagrama de secuencia de aplicaciones {#section_mw2_lm4_xz}

Ya sea que esté buscando implementar una función personalizada con los puntos finales proporcionados por Livefyre o simplemente necesite depurar un problema, ayuda a comprender cómo funciona el flujo de respuestas/solicitudes de aplicaciones de Livefyre.

![](assets/appsequencediagram.png)

1. Cuando el cliente visite el sitio web, cree una instancia de la aplicación Livefyre con el ID del sitio y el ID del artículo.
1. Si desea autenticar al usuario (valioso para la evaluación del tráfico, así como para la protección del sitio), envíe a Livefyre la información del sitio y el token de perfil de usuario.
1. Envíe a Livefyre el ID del sitio y el ID del artículo para inicializar la aplicación.

   Livefyre devuelve el contenido inicial.

   Envíe este contenido a la página y muestre la aplicación.

1. Para actualizar el contenido mostrado en la página, envíe a Livefyre el ID de evento más reciente de su página. Si hay contenido nuevo disponible, se devuelve.

   Vuelva a cargar la página con contenido nuevo y repita el proceso indefinidamente.

1. Si permite que los usuarios anuncien contenido nuevo, establezca un déclencheur en un evento cuando se publique contenido nuevo en el sitio para publicarlo en Livefyre. Livefyre devolverá un flujo actualizado, que puede utilizar para actualizar su sitio.
