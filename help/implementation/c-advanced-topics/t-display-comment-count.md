---
description: Tome los recuentos de publicaciones y comentarios para que determinadas colecciones se muestren en las páginas de índice.
seo-description: Tome los recuentos de publicaciones y comentarios para que determinadas colecciones se muestren en las páginas de índice.
seo-title: Mostrar recuento de comentarios
solution: Experience Manager
title: Mostrar recuento de comentarios
uuid: 0 f 39 b 25 e -11 e 0-4945-be 71-55 fb 4798 b 6 c 7
translation-type: tm+mt
source-git-commit: c287e7a880f956f0444af746adee682571fe5a72

---


# Mostrar recuento de comentarios{#display-comment-count}

Tome los recuentos de publicaciones y comentarios para que determinadas colecciones se muestren en las páginas de índice.

Livefyre le `CommentCount.js` permite recuperar los recuentos de contenido de las colecciones del sitio. Aunque las aplicaciones mostrarán el recuento de comentarios de la colección actual, tener estos recuentos sindicados en el sitio puede resultar útil. Esta función es especialmente útil si no persiste en su base de datos (o si la base de datos CMS no se sincroniza con Livefyre).

1. Cargue el JavaScript.

   Para usarlo `CommentCount.js`, primero incruste el archivo JavaScript en `<head>` la sección de la página o plantilla donde desee utilizarla.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Enlace el elemento HTML.

   Una vez cargada la secuencia de comandos, intentará encontrar otros elementos en la página con un nombre de clase de `livefyre-commentcount`. Para cada uno de estos elementos, la secuencia de comandos buscará `data-lf-site-id` y los atributos `data-lf-article-id` HTML, y usarán estos elementos para recuperar contenido de Livefyre y actualizar cada elemento con el valor más reciente.

   Por ejemplo, se actualizará el siguiente elemento:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {important = &quot;high&quot;}
   >
   >`CommentCount.js` El código comprueba si hay un valor numérico que actualizar con el recuento real. Asegúrese de incluir un valor numérico entre las etiquetas.

   **Ejemplo 1** (Uso de la URL como ID del artículo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Ejemplo 2** (Uso de un sistema numerado como ID del artículo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configurar opciones.

   Para obtener más control sobre cómo se reemplazan los recuentos de contenido, realice una llamada `LF.CommentCount()` y pase un objeto que contenga las opciones de configuración. Asegúrese de llamar a la función después de que todos los elementos que deban reemplazarse estén en DOM. El mejor lugar para llamar a este método es en el pie de página, por lo que se produce cuando se carga el DOM, pero antes de los eventos ready de documento y ventana.

   Se permiten las siguientes opciones de configuración:

* **replacer:** Función o Regex utilizada para reemplazar el texto de cada recuento de contenido.

* **function:** Se utiliza para hacer el reemplazo en cada elemento. Los argumentos de la función son:

   **element:** Elemento HTML que se está actualizando.
   **count:** Recuento de contenido de este elemento.

* **regex:** Se utiliza para determinar qué parte del texto del elemento debe reemplazarse por el recuento.

   **Ejemplo**:

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
   >Utilice el replacer para personalizar o internacionalizar el mensaje de recuento de comentarios.
