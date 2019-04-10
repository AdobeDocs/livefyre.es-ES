---
description: Inserte Publicidades en el flujo de comentarios.
seo-description: Inserte Publicidades en el flujo de comentarios.
seo-title: Publicidades en comentarios
solution: Experience Manager
title: Publicidades en comentarios
uuid: f 8 d 6372 f -4468-4884-a 384-116180 b 4 c 748
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Publicidades en comentarios{#ads-in-comments}

Inserte Publicidades en el flujo de comentarios.

## Publicidades en comentarios {#topic_CDD2ACF16AED4DE782725EE90089C04E}

Inserte Publicidades en el flujo de comentarios.

La función Publicidades de Livefyre en Comentarios permite inyectar publicidades en el flujo de comentarios, definir la frecuencia con la que aparecerán las publicidades en el flujo y crear delegados sincrónicos y delegados de inyección de publicidad asincrónicos.

Livefyre proporciona el contenedor a través del cual puede insertar una publicidad mediante el proveedor de la solución de administración de publicidad.

Para insertar una publicidad, pase dos valores de Livefyre:

* Frecuencia en la que el anuncio debe insertarse en el flujo de comentarios
* Función que proporciona la publicidad adecuada.

>[!NOTE]
>
>Las publicidades solo se procesarán cuando la colocación de la publicidad esté en la ventanilla móvil. Las publicidades solo se mostrarán después de los comentarios principales (no dentro de los hilos) y los usuarios no podrán comentar estas publicidades. Esta API no permite especificar el tamaño del elemento en el que se colocarán las publicidades.

## de CRM{#concept_C99029E618EC49779E3117D2C303E4F1}

Para utilizar esta función, cree un elemento div en la página en la que se colocarán las publicidades y luego pase el HTML de su proveedor de publicidad.

Livefyre proporciona dos tipos de colocación de publicidad: sincrónica y asincrónico. Ambos tipos cargan las publicidades únicamente cuando el usuario desplaza la página de manera que la posición de la publicidad se vea. Ambos también requieren que se devuelva un elemento DOM (iframe o div).

Para obtener la publicidad, se realizan llamadas de método sincrónico a un repositorio local, mientras que llamadas asincrónicas a un servicio externo.

### Sincrónica

Para crear una colocación sincrónica, incluya la publicidad en el delegado y devuelva el elemento de publicidad mismo. Las llamadas de método sincrónico a un repositorio local, permitiéndole gestionar su propia generación de publicidades.

### Asincrónico

El método asincrónico requiere que el elemento se inserte en el DOM antes de llamar al proveedor de publicidad. A continuación, su proveedor determina qué publicidad se enviará y la devuelve.

Para implementar publicidades asincrónicas, cree un delegado que devuelva un elemento en el que se coloque el anuncio y una llamada de retorno que realice la colocación del anuncio. El elemento devuelto en el delegado debe tener un identificador único para que la publicidad se dirija a target. La rellamada insertará la publicidad en el elemento proporcionado por la ID única.

>[!NOTE]
>
>Según el proveedor de publicidad, la llamada de retorno se comportará de forma diferente.

Cuando se carga la página, Publicidades en Comentarios abrirá el delegado, insertará el elemento y luego llamará a la rellamada que actualiza el elemento (previamente definido) con la publicidad.

## Parámetros {#concept_D7E27B0C21EF405C8EB826083DBB53EC}

Los parámetros siguientes están disponibles para utilizarse con esta llamada.

Para el objeto ad:

* **delay:****(opcional) entero** : establece el número de comentarios tras los cuales se mostrará la primera publicidad. El valor predeterminado es 10.
* **frecuencia: (opcional) entero** : establece el número de comentarios tras los cuales se mostrará cada anuncio posterior. Por ejemplo: Introduzca 2 para mostrar un anuncio como tercer comentario. El valor predeterminado es 10.
* **delegate:*****función requerida*** : la función llamada para inyectar publicidades en el flujo de comentarios.

El objeto delegado admite invocaciones de publicidad sincrónicas y asíncronas. El parámetro que se proporciona a la función delegada, data, contendrá:

* **title:****cadena** : el título de la colección.
* **etiquetas:****array** : Lista de etiquetas asociadas con la colección.
* **id:****cadena** : identificador del artículo de la colección.
* **url:****cadena** : la URL de la colección.
* **Networkid:****cadena** : ID de red de la colección.
* **Siteid:****int** : ID del sitio de la colección.

Estos elementos se pasan a través del objeto convconfig en nuestro ejemplo y se explican con más detalle en la [sección](/help/implementation/c-app-integrations/c-comments-integration/c-comments-integration.md#section_656AAC97903F485084650269A6C7EBCE) Introducción.

### Sincrónica

El delegado devuelve un objeto que contiene:

* **element:*****required* DOM element** - El elemento que contiene la publicidad que se va a insertar en la aplicación.

**Asincrónico**: El delegado devuelve un objeto que contiene: El delegado devuelve un objeto que contiene dos propiedades: elemento y rellamada:

* **element:*****required* DOM element** - El elemento que contiene la publicidad que se va a insertar en la aplicación.
* **rellamada:*****función requerida*** : la rellamada que manejará la inserción de la publicidad en el elemento DOM anterior.

Para `Conv` el objeto, puede pasar una cadena para denotar el título de la sección de publicidad:

* **cadenas:****(opcional)** : se utiliza para personalizar el texto del encabezado de las publicidades. ' Patrocinado'de forma predeterminada.

## Ejemplo sincrónico {#concept_E733E4431D9948638B8102ADE398735F}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```

## Ejemplo asincrónico {#concept_16B798C7EB20423DAA53ACCC71540051}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  function insertSlot(slotName) { 
    var adElem = document.createElement("img"); 
    var ad = "https://your-ad-here.com/great-ad-image.image"; 
    adElem.setAttribute("src", ad); 
    document.getElementById(slotName).appendChild(adElem); 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem, 
              callback: function() { 
                insertSlot(elem.id); 
              } 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```
