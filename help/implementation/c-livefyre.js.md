---
description: La biblioteca principal de Livefyre utilizada para poder completar Livefyre
  en su sitio.
seo-description: La biblioteca principal de Livefyre utilizada para poder completar
  Livefyre en su sitio.
seo-title: Livefyre. js
solution: Experience Manager
title: Livefyre. js
uuid: 7 b 3 eca 57-d 5 e 8-416 d-badf-a 9 c 51 d 10 dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre. js {#livefyre-js}

La biblioteca principal de Livefyre utilizada para poder completar Livefyre en su sitio.

`Livefyre.js` es la biblioteca principal que puede instalar en todas las páginas web de Livefyre habilitada. Define el objeto global `window.Livefyre` y un único método público, `Livefyre.require`que se puede utilizar para cargar otras bibliotecas JavaScript de Livefyre que ayudan a [incrustar aplicaciones de Livefyre](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [integrar su proveedor de autenticación con Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) y mucho más.

## Agregar al sitio {#section_cst_twg_xz}

Agregue `<script>` la siguiente etiqueta a la plantilla web o a la plantilla del sitio web. Si es posible, añádalo a `<head>` la sección del documento HTML para que se cargue rápidamente.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Esta secuencia de comandos incrustará un archivo muy pequeño (~ 1 Kb) denominado Scoefyre. js que posteriormente cargará la última versión de Livefyre. js sobre el protocolo con el que se haya accedido a su página web (HTTP o HTTPS).

## Livefyre. require {#section_ipq_hwg_xz}

`Livefyre.require` es un cargador de módulos JavaScript personalizado como [curl. js](https://github.com/cujojs/curl) o [requirejs](https://requirejs.org/). Puede utilizarse para cargar la mayoría de los paquetes publicados por Livefyre y ofrecer una ruta de integración práctica e intuitiva.

Los paquetes accesibles se `Livefyre.require` muestran con versiones [semánticas](https://semver.org/). Los paquetes pueden ser necesarios en una versión específica o en una serie de versiones, de modo que su página web pueda beneficiarse automáticamente de las nuevas funciones de corrección de errores. Esto le proporciona flexibilidad al integrar Livefyre en su sitio. Existen tres niveles de fijación de versiones con `Livefyre.require`los que puede utilizar.

* **package-name # 1:** Anclar a la versión principal v 1. Obtendrá todas las actualizaciones nuevas que mantienen una API retrocompatible. Anclar a una versión principal para recibir correcciones de errores y mejoras menores de funciones para esa versión.
* **package-name # 1.1:** Pin to minor version v 1.1. Obtendrá todos los errores en esta versión secundaria. El departamento de ingeniería de Livefyre colocará siempre la versión secundaria de un paquete si su comportamiento predeterminado o su alcance funcional cambia de manera que pudiera provocar un comportamiento nuevo inesperado en la página web. Fije a una versión secundaria si desea recibir correcciones de errores automatizadas, pero no funcionalidades adicionales ni cambios en el comportamiento predeterminado.
* **package-name # 1.1.1:** Anclar a la versión 1.1.1 de parche. El comportamiento de este incrustado nunca cambiará, aunque haya correcciones. Fije en una versión de parche si tiene amplias personalizaciones CSS para su sitio que dependen de la estructura de marcado del paquete que pueda cambiar, o si tiene otras razones para preferir que la versión de Livefyre que está ejecutando no cambie de ningún modo.

Una integración de ejemplo podría `Livefyre.require` verse así:

```
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
  
<!-- Then load up all the desired Livefyre packages and Do Stuff in the callback --> 
<script> 
Livefyre.require([ 
    'lfawesome#1', 
    'lfsuperawesome#2.1.2' 
], function (LFAwesome, LFSuperAwesome) { 
    var greatness = new LFAwesome(); 
    // etc.. 
}); 
</script>
```

## Paquetes disponibles {#section_ygd_dwg_xz}

¿Dónde se encuentran disponibles los paquetes de JavaScript de Livefyre `Livefyre.require`? Siempre puede encontrar una lista actualizada de los paquetes admitidos y las versiones más recientes aquí: [packages.html](https://cdn.livefyre.com/packages.html).

## Prueba de versiones preliminares de paquetes {#section_pgm_dpg_xz}

A veces, es posible que desee probar una versión próxima de un paquete de Livefyre para asegurarse de que funcionará en su sitio web o en la aceptación de una función que esté desarrollándose a petición suya. Además de incluir un intervalo de versión semántica, se puede especificar el entorno UAT de la versión preliminar.

Por ejemplo: lo siguiente requeriría la versión UAT de `fyre.conv`las aplicaciones de chat, de comentarios y Live Blog.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
