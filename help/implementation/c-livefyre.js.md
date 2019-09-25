---
description: Biblioteca principal de Livefyre que se utiliza para alimentar a Livefyre en su sitio.
seo-description: Biblioteca principal de Livefyre que se utiliza para alimentar a Livefyre en su sitio.
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre.js {#livefyre-js}

Biblioteca principal de Livefyre que se utiliza para alimentar a Livefyre en su sitio.

`Livefyre.js` es la biblioteca principal que puede instalar en todas las páginas web habilitadas para Livefyre. Define el `window.Livefyre` objeto global y un único método público, `Livefyre.require`, que puede utilizarse para cargar otras bibliotecas JavaScript de Livefyre que ayudan a [incrustar aplicaciones](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)de Livefyre, [integrando su proveedor de autenticación con Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) y más.

## Agregar al sitio {#section_cst_twg_xz}

Agregue la siguiente `<script>` etiqueta a la página web o plantilla de sitio web. Si es posible, agréguelo a la `<head>` sección del documento HTML para que se cargue rápidamente.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Esta secuencia de comandos incorporará un archivo muy pequeño (~1 Kb), denominado Livefyre.js scout, que posteriormente cargará la última versión de Livefyre.js a través del protocolo con el que se ha accedido a su página web (HTTP o HTTPS).

## Livefyre.required {#section_ipq_hwg_xz}

`Livefyre.require` es un cargador de módulos JavaScript personalizado como [curl.js](https://github.com/cujojs/curl) o [RequireJS](https://requirejs.org/). Se puede utilizar para cargar la mayoría de los paquetes publicados por Livefyre y presenta una conveniente e intuitiva ruta de integración.

Los paquetes a los que se puede acceder a través de `Livefyre.require` la versión tienen versiones [semánticas](https://semver.org/). Los paquetes pueden ser necesarios en una versión específica o en una serie de versiones, de modo que su página web se puede beneficiar automáticamente de las nuevas funciones de corrección de errores. Esto le proporciona flexibilidad al integrar Livefyre en su sitio. Existen tres niveles de fijación de versiones que puede utilizar con `Livefyre.require`.

* **** package-name #1: Anclar a la versión principal v1. Obtendrá todas las actualizaciones nuevas que mantengan una API compatible con versiones anteriores. Anclar a una versión principal para recibir correcciones de errores y mejoras menores de funciones para esa versión.
* **** package-name#1.1: Anclar a la versión secundaria v1.1. Obtendrá todas las correcciones de errores de esta versión secundaria. El departamento de ingeniería de Livefyre siempre superará la versión secundaria de un paquete si su comportamiento predeterminado o su ámbito funcional cambian de forma que pueda provocar un comportamiento nuevo e inesperado en su página web. Anclar a una versión secundaria si desea recibir correcciones de errores automatizadas, pero sin funcionalidad adicional ni cambios en el comportamiento predeterminado.
* **** package-name#1.1.1: Anclar a la versión de parche v1.1.1. El comportamiento de esta incrustación nunca cambiará, incluso si hay correcciones de errores. Anclar a una versión de parche si tiene personalizaciones CSS extensas para su sitio que dependen de la estructura de marcado de un paquete que puede cambiar o si tiene otras razones para preferir que la versión de Livefyre que está ejecutando no cambiará en modo alguno.

Un ejemplo de integración que utiliza `Livefyre.require` podría tener este aspecto:

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

¿Se pregunta a través de qué paquetes JavaScript de Livefyre se encuentra disponible `Livefyre.require`? Siempre puede encontrar una lista actualizada de los paquetes admitidos y sus últimas versiones aquí: [packages.html](https://cdn.livefyre.com/packages.html).

## Prueba de las versiones preliminares de los paquetes {#section_pgm_dpg_xz}

A veces puede que desee probar una versión próxima de un paquete de Livefyre para asegurarse de que funcionará en su sitio web o para probar la aceptación de una función que se esté desarrollando a petición suya. Además de incluir un rango de versiones semánticas, se puede especificar el entorno de evaluación de UAT.

Por ejemplo, lo siguiente requeriría la publicación de `fyre.conv`la UAT, las aplicaciones Comments, Live Blog y Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
