---
description: Conozca las convenciones de Livefyre y cómo organiza Livefyre el contenido.
seo-description: Conozca las convenciones de Livefyre y cómo organiza Livefyre el
  contenido.
seo-title: Arquitectura
solution: Experience Manager
title: Arquitectura
uuid: 94358 e 6 c -954 a -4 a 52-9 bb 2-d 800 b 2933130
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Arquitectura{#architecture}

Conozca las convenciones de Livefyre y cómo organiza Livefyre el contenido.

Esta sección proporciona información general sobre la arquitectura de red de Livefyre.

## Información general de redes y sitios

Livefyre organiza usuarios y contenido por red y sitio. Cada red puede tener una o varias cuentas de usuario asociadas con ella, y cada red puede incluir uno o varios sitios de Livefyre. Un sitio de Livefyre es una agrupación arbitraria de colecciones. Una colección se asigna a un ID de artículo en su CMS.

## Explicación de las redes {#section_hqt_4m4_xz}

Los clientes con varios dominios pueden compartir cuentas de usuario en todos los dominios, con una sola red de Livefyre. Los clientes que deseen mantener cuentas de usuario independientes para dominios distintos requerirán redes de Livefyre independientes.

Las opciones de configuración pueden aplicarse a sitios, redes y colecciones (denominados conversaciones en la ilustración anterior).

>[!NOTE]
>
>Algunas opciones de configuración solo están disponibles a nivel de red (como las preferencias de notificación por correo electrónico, correo electrónico de dirección y logotipos personalizados de correo electrónico). Si desea que estos ajustes sean diferentes para cada dominio, debe utilizar varias redes.

## Explicación de sitios {#section_vjw_nm4_xz}

Un sitio es una agrupación arbitraria de artículos. La agrupación es útil ya que permite asignar moderadores diferentes a diferentes grupos de contenido. Los moderadores y propietarios pueden estar configurados para moderar contenido y configurar los ajustes de administración en la red o en el nivel del sitio. Si desea que algunos moderadores vean ciertas colecciones, estas colecciones pueden configurarse como un sitio de Livefyre independiente.

>[!NOTE]
>
>No hay límite en el número de sitios que puede tener en su red personalizada.

## Diagrama de secuencia de aplicaciones {#section_mw2_lm4_xz}

Ya sea que quiera implementar la función personalizada con los puntos finales de Livefyre o simplemente necesitar depurar un problema, ayuda a comprender cómo funciona el flujo de respuesta o solicitud de la aplicación de Livefyre.

![](assets/appsequencediagram.png)

1. Cuando el cliente llegue al sitio, cree una instancia de la aplicación de Livefyre con el ID del sitio y el ID del artículo.
1. Si desea autenticar al usuario (valioso para la evaluación del tráfico, así como la protección del sitio), envíe a Livefyre la información del sitio y el testigo Perfil de usuario.
1. Envíe Livefyre ID del sitio y ID del artículo para inicializar la aplicación.

   Livefyre devuelve el contenido inicial.

   Envíe este contenido a la página y muestre la aplicación.

1. Para actualizar el contenido mostrado en la página, envíe a Livefyre el último ID de evento desde su página. Si hay contenido nuevo disponible, se devolverá.

   Vuelva a cargar la página con contenido nuevo y repita el proceso indefinidamente.

1. Si permite que los usuarios anuncien contenido nuevo, desencadenan un evento cuando se publica contenido nuevo en su sitio para publicar el contenido en Livefyre. Livefyre devolverá un flujo actualizado, que puede utilizar para actualizar el sitio.
