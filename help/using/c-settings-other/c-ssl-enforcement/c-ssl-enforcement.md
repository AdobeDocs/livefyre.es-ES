---
description: 'null'
seo-description: 'null'
seo-title: Aplicación de SSL
solution: Experience Manager
title: Aplicación de SSL
uuid: e64af8c2-3ab6-4034-b385-0e552d828c6e
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 2%

---


# Aplicación de SSL{#ssl-enforcement}

Para garantizar que los datos permanezcan seguros, se está dejando de utilizar HTTP en favor de HTTPS. Adobe Livefyre deshabilitará por completo todos los cifrados HTTP y SSL/TLS inseguros para fines de agosto de 2018. Se trata de un estándar de Adobe diseñado para proteger la privacidad de usted y de sus usuarios.

## ¿Quién se ve afectado? {#section_jf2_4yz_kcb}

Esto podría afectar a los clientes de Livefyre que:

* Llamadas de servidor a servidor desde su CRM, CMS, WordPress u otro cliente.
* Integraciones móviles (aplicaciones de Android e iOS)
* Aplicaciones personalizadas o código personalizado

## ¿Qué es necesario hacer?{#section_unv_dc5_kcb}

1. Todos los clientes de Livefyre deben comunicarse con todas las API mediante HTTPS para todo el tráfico, incluidos:

   * Integraciones de servidor a servidor (CRM, CMS, WordPress, etc.)
   * Integraciones móviles (aplicaciones de Android e iOS)
   * Aplicaciones personalizadas (SDK de Streamhub o directamente codificadas).

1. Servidor a servidor y los clientes HTTP móviles deben admitir TLS 1.2
1. Cambie los nombres de host de `{*}.<network>.fyre.co` a `<network>.{*}.fyre.co`. Por ejemplo, el nombre de host `example.network.fyre.co` cambia a `network.`example.fyre.co&quot;. Por ejemplo:

   * `bootstrap.<network_name>.fyre.co` a `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` a `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` a `<network_name>.admin.fyre.co`

## ¿Cómo sé si hice los cambios? {#section_sqk_5d5_kcb}

Puede que ya utilice HTTPS, pero Livefyre recomienda que compruebe el doble, especialmente si tiene:

* Llamadas de servidor a servidor desde el CMS o CRM.
* Código personalizado o utilice SDK para aplicaciones personalizadas en JavaScript o Mobile.
* Si su integración tiene más de un año.
* Si la tecnología de la pila es anterior a un año.

Aunque ya utilice HTTPS, debe comprobar que sus clientes de API admiten TLS 1.2.

## ¿Cómo puedo verificar que mis clientes API admitan TLS 1.2? {#section_nd1_j25_kcb}

Una persona que trabaje en el desarrollo del sitio puede:

* Identifique el software cliente.
* Identifique la versión.
* Lea la documentación para asegurarse de que el cliente de API admite TLS 1.2.
* Active el modo de depuración, si es necesario.

## Compatibilidad con Java para TLS 1.2 {#section_lwn_rwk_ycb}

Las JVM de oracle y OpenJDK para Java 8 y versiones posteriores están configuradas para utilizar TLS 1.2, de forma predeterminada, en todas las conexiones SSL. No es necesario que realice ninguna acción adicional si utiliza Java 8 o posterior.

Los usuarios de Java 7 o versiones anteriores deben consultar la documentación pública sobre cómo habilitar TLS 1.2.

## ¿Por qué necesito cambiar mis nombres de host? {#section_d5q_p25_kcb}

Livefyre no tiene certificados SSL en dominios `{*}.<network>.fyre.co`. Al cambiar la dirección URL a HTTPS, se rompe la aplicación.

## ¿Tengo que actualizar a la última versión de los SDK de Livefyre? {#section_dw5_s25_kcb}

No. En su lugar, puede aplicar parches al código. Para parchear el código, modifique algunas cadenas estáticas y vuelva a compilar el código. Si el cliente HTTP no está actualizado, deberá actualizarlo también o usar uno diferente.

## ¿Cuánto tiempo llevará esto? {#section_lgd_v25_kcb}

El tiempo que esto tarda depende de la configuración. Si tiene una implementación sencilla, la confirmación debería tardar poco tiempo. Si tiene muchas personalizaciones, deberá probar e implementar código actualizado en sus servidores o nuevas aplicaciones en App Store. Para obtener los mejores resultados, le recomendamos que realice una auditoría inicial del trabajo para que pueda planificar cualquier trabajo a largo plazo.

## ¿Cuál es el plazo para completar este trabajo? {#section_kgk_w25_kcb}

Livefyre desactivará el puerto 80 (HTTP) a nuestros servicios a finales de agosto de 2018 y solo admitirá conexiones a 443 (HTTPS). Los exploradores y otros clientes que intenten utilizar HTTP no funcionarán.

## ¿Cuándo necesito terminar este trabajo? {#section_rvb_x25_kcb}

Todos los clientes deben utilizar HTTPS para finales de julio de 2018. Si no puede cumplir este plazo, póngase en contacto con nuestro equipo en prioritysupport@livefyre.com.
