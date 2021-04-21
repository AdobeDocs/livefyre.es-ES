---
description: Tome los recuentos de anuncios y comentarios de ciertas colecciones para que se muestren en las páginas de índice.
title: Mostrar recuento de comentarios
exl-id: 03c911f0-1fdd-4d5c-9262-9ff7485b7b14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Mostrar recuento de comentarios{#display-comment-count}

Tome los recuentos de anuncios y comentarios de ciertas colecciones para que se muestren en las páginas de índice.

El `CommentCount.js` de Livefyre le permite recuperar los recuentos de contenido de las colecciones de su sitio. Aunque las aplicaciones mostrarán el recuento de comentarios de la colección actual, puede resultar útil tener estos recuentos sindicados en el sitio. Esta función es especialmente útil si no persiste contenido en la base de datos (o si la base de datos de CMS no está sincronizada con Livefyre).

1. Cargue JavaScript.

   Para utilizar `CommentCount.js`, primero incruste el archivo JavaScript en la sección `<head>` de la página o plantilla donde desee usarlo.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Enlace el elemento HTML.

   Una vez cargado el script, intentará encontrar otros elementos en la página con un nombre de clase `livefyre-commentcount`. Para cada uno de estos elementos, la secuencia de comandos buscará atributos HTML `data-lf-site-id` y `data-lf-article-id`, y los utilizará para recuperar contenido de Livefyre y actualizar cada elemento con el valor más reciente.

   Por ejemplo, se actualizaría el siguiente elemento:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >El código `CommentCount.js` comprueba si hay un valor numérico que actualizar con el recuento real. Asegúrese de incluir un valor numérico entre las etiquetas .

   **Ejemplo 1**  (uso de la URL como ID del artículo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Ejemplo 2**  (Uso de un sistema numerado como ID de artículo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configurar opciones.

   Para obtener más control sobre cómo se reemplazan los recuentos de contenido, llame a `LF.CommentCount()` y pase un objeto que contenga las opciones de configuración. Asegúrese de llamar a la función después de que todos los elementos que deben reemplazarse estén en el DOM. El mejor lugar para llamar a este método es en el pie de página, por lo que ocurre cuando se carga el DOM, pero antes de los eventos de documento y preparados para ventanas.

   Se permiten las siguientes opciones de configuración:

* **sustituto:** Función o Regex se usan para reemplazar el texto de cada recuento de contenido.

* **función:** se utiliza para reemplazar cada elemento. Los argumentos de la función son:

   **elemento:** El elemento HTML que se está actualizando.
   **count:** El recuento de contenido de este elemento.

* **regex:** se utiliza para determinar qué parte del texto del elemento debe reemplazarse por el recuento.

   **Ejemplo:**

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >Utilice el sustituto para personalizar o internacionalizar el mensaje de recuento de comentarios.
