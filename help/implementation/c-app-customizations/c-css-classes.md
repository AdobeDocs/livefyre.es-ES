---
description: Utilice las clases CSS disponibles para personalizar la visualización de las aplicaciones.
seo-description: Utilice las clases CSS disponibles para personalizar la visualización de las aplicaciones.
seo-title: Clases CSS
solution: Experience Manager
title: Clases CSS
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Clases CSS{#css-classes}

Utilice las clases CSS disponibles para personalizar la visualización de las aplicaciones.

Disponible para chat, comentarios, Live Blog, críticas y notas de identidad.

Utilice CSS para personalizar las aplicaciones de Livefyre y así obtener una integración más completa con la página, ya que simplemente anula la CSS de la aplicación predeterminada con su propia hoja de estilo. Esta sección describe las personalizaciones de CSS disponibles.

* [CSS del editor](#c_css_classes/section_edx_prh_xz)
* [CSS de opciones de ordenación](#c_css_classes/section_btq_4rh_xz)
* [CSS de comentarios](#c_css_classes/section_mlv_nrh_xz)
* [CSS de comentarios destacados](#c_css_classes/section_m2v_mrh_xz)
* [CSS de comentarios archivados](#c_css_classes/section_bs5_lrh_xz)
* [CSS de notificador de comentarios](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS Clases](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## CSS del editor {#section_edx_prh_xz}

Utilice estas clases para cambiar la interfaz del editor de publicaciones.

| Clase | Descripción |
|---|---|
| .fyre-comment-count | Texto que muestra el número de comentarios. |
| .fyre-login-bar | Cuadro delimitador que contiene la barra de inicio de sesión y las opciones. |
| .fyre-live-container | Cuadro delimitador alrededor del número de personas que escuchan y sus avatares. |
| .fyre-editor | Cuadro delimitador alrededor de la barra de inicio de sesión .fyre, el contenedor de archivos .fyre y el área de texto donde los usuarios escriben sus comentarios. |
| .fyre-stream-sort | Cuadro delimitador alrededor de las opciones de ordenación. |

También puede editar estilos en la propia configuración de la aplicación, incluido el color de fondo del campo del editor y el color, el tamaño y la familia de la fuente del texto que aparece dentro del editor.

Para personalizar el editor de comentarios, agregue el objeto editorCss:{} a fyre.conv.load() e incluya el estilo que desee. Por ejemplo, para actualizar el editor con su CSS personalizada:

```
fyre.conv.load(networkConfig, [{ 
   siteId: LF_siteId, 
   el: 'livefyre', 
   articleId: LF_articleId, 
   collectionMeta: #CollectionMeta 
   editorCss: { 
      background: '#ccc', 
      color: 'red', 
      font: '30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif' 
   } 
}]);
```

## CSS de opciones de ordenación {#section_btq_4rh_xz}

| Clase | Descripción |
|---|---|
| .fyre-stream-sort | Las opciones de ordenación completas se div. |
| .fyre-stream-sort-newest | La opción "Más reciente". |
| .fyre-stream-sort-más antiguo | La opción "Más antiguo". |
| .fyre-stream-sort-bar | Barra separador entre las opciones. |
| .fyre-stream-sort-selected | La opción de ordenación seleccionada actualmente. |

Estructura HTML:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Oculte el carácter ‘|’ que separa las opciones de ordenación.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## CSS de comentarios {#section_mlv_nrh_xz}

| Clase | Descripción |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre creará una clase CSS en este formato para cada etiqueta de usuario agregada a través del estudio de Livefyre, sincronización [de perfiles](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Esta clase puede utilizarse para aplicar estilo al fondo de cualquier contenido publicado por cuentas de usuario, incluida esa etiqueta. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre creará una clase CSS en este formato para cada etiqueta de contenido agregada a través de Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Esta clase puede utilizarse para aplicar estilo a cualquier contenido al que haya agregado la etiqueta. |
| .fyre-comment-user | Cuadro delimitador que contiene la imagen del perfil de usuario. |
| .fyre-comment-username | El nombre de usuario. |
| .fyre-moderator | Cuadro delimitador del moderador. |
| .fyre-comment | Cuadro delimitador alrededor del texto o vínculo del comentario. |
| .fyre-comment-article | Cuadro delimitador para todo el contenido del comentario. |
| .fyre-comment-date | La etiqueta adjunta al elemento "tiempo transcurrido desde la publicación". |
| .fyre-comment-media | Cuadro delimitador alrededor del contenido multimedia. |
| .fyre-comment-actions | Cuadro delimitador alrededor de las acciones disponibles para realizar un comentario. |
| .fyre-comment-like | Cuadro delimitador alrededor del vínculo "Me gusta". |
| .fyre-comment-response | Cuadro delimitador alrededor del vínculo "Responder". |

## CSS de comentarios destacados {#section_m2v_mrh_xz}

>[!NOTE]
>
>Todas las clases CSS de comentarios también se pueden aplicar al contenido destacado.

| Clase | Descripción |
|---|---|
| .fyre-feature-content-wrapper | El div contenedor del lector. |
| .fyre-feature-header | Barra de título inicial. |
| .fyre-feature-header-icon | Icono de la secuencia del encabezado. |
| .fyre-feature-title | Texto del encabezado. |
| .fyre-feature-body | Div de contenedor para contenido destacado en el lector. |
| .fyre-feature-quote | Icono de comillas que comienza cada elemento de contenido. |

## CSS de comentarios archivados {#section_bs5_lrh_xz}

>[!NOTE]
>
>Todas las clases CSS de contenido también se pueden aplicar al contenido archivado.

| Clase | Descripción |
|---|---|
| .fyre-archive-stream-title | Texto "Del archivo". |
| .fyre-archive-stream-title-icon | El logotipo del encabezado "Desde el archivo". |

## CSS de notificador de comentarios {#section_dy4_krh_xz}

Estas clases permiten personalizar el notificador de comentarios de Livefyre.

| Clase | Descripción |
|---|---|
| .fyre-notification | El div del elemento de lista (contenido nuevo y de archivo). |
| .fyre-notificfier | El contenedor del contenido del notificador. |
| .fyre-notificfier-archive | El contenedor de todo el contenido nuevo que no sea el más reciente. |
| .fyre-notificfier-avatar | Imagen del avatar. |
| .fyre-notificfier-avatar-container | El div contenedor del avatar del usuario. Permite definir la posición. |
| .fyre-notificfier-avatar-shading | Sombreado para el avatar div. |
| .fyre-notificfier-banner | Contenedor del contenido de vista previa del notificador, que muestra el avatar del usuario y un fragmento de contenido del último elemento publicado. |
| .fyre-notificfier-base | El contenedor de la parte de información del notificador, que enumera el número de comentarios nuevos, el rótulo del notificador y el botón de cierre. |
| .fyre-notificfier-base-close | El div contenedor del botón de cierre (x) del notificador. |
| .fyre-notificfier-base-Shadow | Sombreado de la base del notificador. |
| .fyre-notificfier-caption | Texto que se muestra para el notificador. "Nuevos comentarios" de forma predeterminada. |
| .fyre-notificfier-close | Botón que cierra el notificador. |
| .fyre-notificfier-container | El contenedor del notificador incluye tanto la pancarta como la base. |
| .fyre-notificfier-counter | El contenedor del número que aparece en el Notificador. |
| .fyre-notificfier-list | Contenedor del contenido más reciente. |
| .fyre-notificfier-message | Los primeros ~30 caracteres del contenido mostrado. |
| .fyre-notificfier-message-container | El div contenedor del mensaje de encabezado. |
