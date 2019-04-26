---
description: null
seo-description: null
seo-title: Cumplimiento de SSL
solution: Experience Manager
title: Cumplimiento de SSL
uuid: e 64 af 8 c 2-3 ab 6-4034-b 385-0 e 552 d 828 c 6 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Cumplimiento de SSL{#ssl-enforcement}

Para garantizar que sus datos sigan siendo seguros, estamos desaprobando HTTP en favor de HTTPS. Adobe Livefyre deshabilitará todos los ciphers SSL/TLS no seguros para finales de agosto de 2018. Adobe Standard se ha diseñado para proteger su privacidad y sus usuarios.

## ¿Quién ve esto? {#section_jf2_4yz_kcb}

Esto podría afectar a los clientes de Livefyre que tengan:

* Llamadas servidor a servidor desde su CRM, CMS, Wordpress u otro cliente.
* Integraciones móviles (aplicaciones Android e iOS)
* Aplicaciones personalizadas o código personalizado

## ¿Qué debo hacer? {#section_unv_dc5_kcb}

1. Todos los clientes de Livefyre deben comunicarse con todas las API a través de HTTPS para todo el tráfico, incluso:

   * Server to Server Integrations (CRM, CMS, Wordpress, etc.)
   * Integraciones móviles (aplicaciones Android e iOS)
   * Aplicaciones personalizadas (SDK de Streamhub o codificadas directamente).

1. Los clientes de servidor a servidor y HTTP móvil deben admitir TLS 1.2
1. Cambiar los nombres de host `{*}.<network>.fyre.co` a `<network>.{*}.fyre.co`. Por ejemplo, el nombre de host `example.network.fyre.co` cambia a `network.`example. fyre. co «. Por ejemplo:

   * `bootstrap.<network_name>.fyre.co` to `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` to `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` to `<network_name>.admin.fyre.co`

## ¿Cómo sé si realizé los cambios? {#section_sqk_5d5_kcb}

Ya puede utilizar HTTPS, pero Livefyre recomienda comprobar doble, especialmente si tiene:

* Llamadas servidor a servidor desde CMS o CRM.
* Código personalizado o utilice SDK para aplicaciones personalizadas en Javascript o Móvil.
* Si la integración tiene más de un año,
* Si la tecnología de la pila es anterior a un año.

Aunque ya utilice HTTPS, debe verificar que los clientes de API admitan TLS 1.2.

## ¿Cómo puedo verificar que mis clientes de API admitan TLS 1.2? {#section_nd1_j25_kcb}

Una persona que trabaja en el desarrollo de su sitio puede:

* Identifique el software del cliente.
* Identifique la versión.
* Lea documentación para asegurarse de que el cliente API admite TLS 1.2.
* Active el modo de depuración, si es necesario.

## Compatibilidad de Java para TLS 1.2 {#section_lwn_rwk_ycb}

Los JVMS de Oracle y openjdk para Java 8 y versiones posteriores se configuran para utilizar de forma predeterminada TLS 1.2 para todas las conexiones SSL. No necesita realizar ninguna acción adicional si utiliza Java 8 o posterior.

Los usuarios de Java 7 o anteriores deben consultar documentación pública sobre cómo habilitar TLS 1.2.

## ¿Por qué necesito cambiar mis nombres de host? {#section_d5q_p25_kcb}

Livefyre no tiene certificados SSL en `{*}.<network>.fyre.co` los dominios. Si se cambia la URL a HTTPS, se interrumpe la aplicación.

## ¿Tengo que actualizar a la versión más reciente de los SDK de Livefyre? {#section_dw5_s25_kcb}

No. En su lugar, puede parche el código. Para filtrar el código, modifique algunas cadenas estáticas y vuelva a compilar el código. Si el cliente HTTP está obsoleto, tendrá que actualizarlo también o utilizar otro diferente.

## ¿Cuánto tiempo llevará esto? {#section_lgd_v25_kcb}

La cantidad de tiempo que esto tarda depende de la configuración. Si tiene una implementación sencilla, debe tardar poco tiempo en confirmarse. Si tiene muchas personalizaciones, deberá probar e implementar el código actualizado en sus servidores o nuevas aplicaciones en tiendas de aplicaciones. Para obtener los mejores resultados, le recomendamos que realice una auditoría inicial del trabajo para que pueda planificar cualquier trabajo a más largo plazo.

## ¿Cuál es la cronología para completar este trabajo? {#section_kgk_w25_kcb}

Livefyre deshabilitará el puerto 80 (HTTP) a nuestros servicios finales de agosto de 2018 y solo admitirá conexiones a 443 (HTTPS). Los navegadores y otros clientes que intentan utilizar HTTP producirán errores.

## ¿Cuándo debo finalizar este trabajo? {#section_rvb_x25_kcb}

Todos los clientes deben utilizar HTTPS para finales de julio de 2018. Si no puede cumplir este plazo, póngase en contacto con nuestro equipo en prioritysupport@livefyre.com.
