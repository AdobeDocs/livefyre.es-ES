---
description: La biblioteca principal de Livefyre utilizada para impulsar Livefyre en su sitio.
title: Livefyre.js
exl-id: 82083dc0-3b4a-467c-bad7-dbf242ab5bbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Livefyre.js {#livefyre-js}

La biblioteca principal de Livefyre utilizada para impulsar Livefyre en su sitio.

`Livefyre.js` es la biblioteca principal que puede instalar en cada página web habilitada para Livefyre. Define el objeto `window.Livefyre` global y un único método público, `Livefyre.require`, que puede utilizarse para cargar otras bibliotecas JavaScript de Livefyre que ayuden a [Incrustar aplicaciones de Livefyre](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [Integrar su proveedor de autenticación con Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) y más.

## Agregar al sitio {#section_cst_twg_xz}

Agregue la siguiente etiqueta `<script>` a su página web o plantilla de sitio web. Si es posible, agréguelo a la sección `<head>` del documento HTML para que se cargue rápidamente.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Este script incrustará un archivo muy pequeño (~1 Kb) llamado el scout Livefyre.js que posteriormente cargará la última versión de Livefyre.js a través del protocolo con el que se ha accedido a su página web (HTTP o HTTPS).

## Livefyre.required {#section_ipq_hwg_xz}

`Livefyre.require` es un cargador de módulos JavaScript personalizado como  [curl.](https://github.com/cujojs/curl) jsor  [RequireJS](https://requirejs.org/). Se puede utilizar para cargar la mayoría de los paquetes publicados por Livefyre y presenta una cómoda e intuitiva ruta de integración.

Los paquetes a los que se puede acceder mediante `Livefyre.require` reciben versiones mediante [Semantic Versioning](https://semver.org/). Los paquetes pueden ser necesarios en una versión específica o en una serie de versiones, de modo que su página web pueda beneficiarse automáticamente de las nuevas funciones de corrección de errores. Esto le proporciona flexibilidad para integrar Livefyre en su sitio. Hay tres niveles de anclaje de versión que puede usar con `Livefyre.require`.

* **package-name#1:** Anclar a la versión v1 principal. Obtendrá todas las actualizaciones nuevas que mantengan una API compatible con versiones anteriores. Anclar a una versión principal para recibir correcciones de errores y mejoras menores en las funciones de esa versión.
* **package-name#1.1:** Anclar a la versión menor v1.1. Obtendrá todas las correcciones de errores a esta versión menor. Livefyre Engineering siempre golpeará la versión menor de un paquete si su comportamiento predeterminado o su ámbito funcional cambian de forma que pueda provocar un comportamiento nuevo e inesperado en su página web. Anclar a una versión menor si desea recibir correcciones de errores automatizadas, pero sin funcionalidad adicional o cambios en el comportamiento predeterminado.
* **package-name#1.1.1:** Anclar a la versión v1.1.1 del parche. El comportamiento de esta incrustación nunca cambiará, aunque haya correcciones de errores. Anclar a una versión de parche si tiene personalizaciones CSS extensas para su sitio que dependen de la estructura de marcado de un paquete que puede cambiar, o si tiene otras razones para preferir que la versión de Livefyre que está ejecutando no cambiará de ninguna manera.

Una integración de ejemplo con `Livefyre.require` podría tener este aspecto:

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

¿Qué paquetes JavaScript de Livefyre están disponibles a través de `Livefyre.require`? Siempre puede encontrar una lista actualizada de los paquetes compatibles y sus últimas versiones aquí: [packages.html](https://cdn.livefyre.com/packages.html).

## Prueba de versiones anteriores al lanzamiento de paquetes {#section_pgm_dpg_xz}

A veces, es posible que desee probar una versión próxima de un paquete de Livefyre para asegurarse de que funcione en su sitio web o para probar la aceptación de una función que se esté desarrollando a petición suya. Además de incluir un rango de versiones semánticas, se puede especificar el entorno UAT de prelanzamiento.

Por ejemplo, lo siguiente requeriría el lanzamiento de UAT de `fyre.conv`, las aplicaciones Comentarios, Blogs en Directo y Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
