---
title: Aplicación SSL
description: Aplicación SSL
exl-id: 033e15d9-84f6-42d5-8457-04263dcbd11c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 2%

---

# Aplicación SSL{#ssl-enforcement}

Para garantizar que los datos sigan siendo seguros, se ha eliminado HTTP en favor de HTTPS. Adobe Livefyre deshabilitará por completo todos los cifrados HTTP y SSL/TLS inseguros a finales de agosto de 2018. Se trata de un estándar de Adobe diseñado para proteger la privacidad de usted y de sus usuarios.

## ¿A quién afecta? {#section_jf2_4yz_kcb}

Esto podría afectar a los clientes de Livefyre que:

* Llamadas de servidor a servidor desde su CRM, CMS, WordPress u otro cliente.
* Integraciones móviles (aplicaciones de Android e iOS)
* Aplicaciones personalizadas o código personalizado

## ¿Qué es necesario hacer?{#section_unv_dc5_kcb}

1. Todos los clientes de Livefyre deben comunicarse con todas las API a través de HTTPS para todo el tráfico, lo que incluye:

   * Integraciones de servidor a servidor (CRM, CMS, WordPress, etc.)
   * Integraciones móviles (aplicaciones de Android e iOS)
   * Aplicaciones personalizadas (SDK de Streamhub o código directo).

1. Servidor a servidor y los clientes HTTP móviles deben admitir TLS 1.2
1. Cambie los nombres de host de `{*}.<network>.fyre.co` a `<network>.{*}.fyre.co`. Por ejemplo, el nombre de host `example.network.fyre.co` cambia a `network.`example.fyre.co&quot;. Por ejemplo:

   * `bootstrap.<network_name>.fyre.co` a `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` a `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` a `<network_name>.admin.fyre.co`

## ¿Cómo sé si hice los cambios? {#section_sqk_5d5_kcb}

Puede que ya utilice HTTPS, pero Livefyre recomienda realizar una doble comprobación, especialmente si tiene:

* Llamadas de servidor a servidor desde su CMS o CRM.
* Código personalizado o utilice SDK para aplicaciones personalizadas en Javascript o Mobile.
* Si la integración tiene más de un año.
* Si la tecnología de la pila es mayor de un año.

Aunque ya utilice HTTPS, debe verificar que sus clientes de API sean compatibles con TLS 1.2.

## ¿Cómo puedo verificar que mis clientes de API admiten TLS 1.2? {#section_nd1_j25_kcb}

Una persona que trabaje en el desarrollo del sitio puede:

* Identifique el software cliente.
* Identifique la versión.
* Lea la documentación para asegurarse de que el cliente de API es compatible con TLS 1.2.
* Active el modo de depuración si es necesario.

## Compatibilidad de Java con TLS 1.2 {#section_lwn_rwk_ycb}

Las JVM de oracle y OpenJDK para Java 8 y versiones posteriores están configuradas para utilizar TLS 1.2, de forma predeterminada, para todas las conexiones SSL. No es necesario que realice ninguna acción adicional si utiliza Java 8 o posterior.

Los usuarios de Java 7 o versiones anteriores deben consultar la documentación pública sobre cómo habilitar TLS 1.2.

## ¿Por qué necesito cambiar mis nombres de host? {#section_d5q_p25_kcb}

Livefyre no tiene certificados SSL en dominios `{*}.<network>.fyre.co`. Simplemente cambiar la URL a HTTPS rompe la aplicación.

## ¿Tengo que actualizar a la última versión de los SDK de Livefyre? {#section_dw5_s25_kcb}

No. En su lugar, puede aplicar un parche al código. Para parchear el código, debe modificar algunas cadenas estáticas y reconstruir el código. Si el cliente HTTP está desactualizado, también deberá actualizarlo o utilizar uno diferente.

## ¿Cuánto tiempo llevará esto? {#section_lgd_v25_kcb}

El tiempo que tarda en hacerlo depende de la configuración. Si tiene una implementación sencilla, debería tardar poco tiempo en confirmarse. Si tiene muchas personalizaciones, deberá probar e implementar código actualizado en los servidores o en las nuevas aplicaciones en App Stores. Para obtener los mejores resultados, le recomendamos que realice una auditoría inicial del trabajo para poder planificar cualquier trabajo a largo plazo.

## ¿Cuál es el calendario para completar este trabajo? {#section_kgk_w25_kcb}

Livefyre deshabilitará el puerto 80 (HTTP) a nuestros servicios a finales de agosto de 2018 y solo admitirá conexiones al 443 (HTTPS). Los navegadores y otros clientes que intenten utilizar HTTP fallarán.

## ¿Cuándo necesito terminar este trabajo? {#section_rvb_x25_kcb}

Todos los clientes deben utilizar HTTPS para finales de julio de 2018. Si no puede cumplir esta fecha límite, póngase en contacto con nuestro equipo a prioritysupport@livefyre.com.
