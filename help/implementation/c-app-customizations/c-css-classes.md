---
description: Utilice las clases CSS disponibles para personalizar la visualización de las aplicaciones.
title: Clases CSS
exl-id: 605f2c47-13f7-4535-90b1-c53cbf548534
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 1%

---

# Clases CSS{#css-classes}

Utilice las clases CSS disponibles para personalizar la visualización de las aplicaciones.

Disponible para chat, comentarios, blogs en directo, reseñas y notas.

Utilice CSS para personalizar sus aplicaciones de Livefyre y lograr una integración más completa con su página, simplemente anulando el CSS de aplicación predeterminado con su propia hoja de estilo. En esta sección se describen las personalizaciones de CSS disponibles.

* [Editor CSS](#c_css_classes/section_edx_prh_xz)
* [Opciones de ordenación CSS](#c_css_classes/section_btq_4rh_xz)
* [CSS de comentario](#c_css_classes/section_mlv_nrh_xz)
* [CSS de comentarios destacados](#c_css_classes/section_m2v_mrh_xz)
* [Comentarios archivados CSS](#c_css_classes/section_bs5_lrh_xz)
* [Notificador de comentarios CSS](#c_css_classes/section_dy4_krh_xz)
* [Almacenar clases CSS](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editor CSS {#section_edx_prh_xz}

Utilice estas clases para cambiar la interfaz del editor de publicaciones.

| Clase | Descripción |
|---|---|
| .fyre-comment-count | Texto que muestra el número de comentarios. |
| .file-login-bar | El cuadro delimitador que contiene la barra de inicio de sesión y las opciones. |
| .file-live-container | Cuadro delimitador alrededor del número de personas que escuchan y sus avatares. |
| .fyre-editor | Cuadro delimitador alrededor de la barra de inicio de sesión .fyre, contenedor .fyre-live y el área de texto donde los usuarios escriben sus comentarios. |
| .file-stream-sort | Cuadro delimitador alrededor de las opciones de clasificación. |

También puede editar estilos en la propia configuración de la aplicación, incluido el color de fondo del campo del editor y el color, el tamaño y la familia de la fuente del texto que aparece dentro del editor.

Para personalizar el editor de comentarios, añada el objeto editorCss:{} a file.conv.load() e incluya el estilo que desee. Por ejemplo, para actualizar el editor con su CSS personalizada:

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

## Opciones de ordenación CSS {#section_btq_4rh_xz}

| Clase | Descripción |
|---|---|
| .file-stream-sort | Las opciones de ordenación completas div. |
| .fyre-stream-sort-newest | La opción &quot;Más reciente&quot;. |
| .file-stream-sort-más antiguo | La opción &quot;Oldest&quot;. |
| .file-stream-sort-bar | Barra separador entre las opciones. |
| .file-stream-sort-selected | La opción de ordenación seleccionada actualmente. |

Estructura HTML:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Oculte el signo &quot;|&quot; que separa las opciones de ordenación.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## CSS de comentario {#section_mlv_nrh_xz}

| Clase | Descripción |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre creará una clase CSS en este formato para cada etiqueta de usuario agregada a través del estudio de Livefyre, [Sincronización de perfiles](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Esta clase se puede usar para aplicar estilo al fondo de cualquier contenido publicado por cuentas de usuario, incluida esa etiqueta. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre creará una clase CSS en este formato para cada etiqueta de contenido agregada a través de Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Esta clase se puede utilizar para aplicar estilo a cualquier contenido al que haya añadido la etiqueta. |
| .fyre-comment-user | Cuadro delimitador que contiene la imagen del perfil del usuario. |
| .fyre-comment-username | El nombre de usuario. |
| .file-moderator | Cuadro delimitador del moderador. |
| .fyre-comment | Cuadro delimitador alrededor del texto/vínculo del comentario. |
| .fyre-comment-article | Cuadro delimitador para todo el contenido del comentario. |
| .fyre-comment-date | La etiqueta adjunta al elemento &quot;Tiempo desde la publicación&quot;. |
| .fyre-comment-media | Cuadro delimitador alrededor del contenido multimedia. |
| .fyre-comment-actions | Cuadro delimitador alrededor de las acciones disponibles para realizar en un comentario. |
| .fyre-comment-like | Cuadro delimitador alrededor del vínculo &quot;Me gusta&quot;. |
| .fyre-comment-reply | Cuadro delimitador alrededor del vínculo &quot;Responder&quot;. |

## Comentarios destacados CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>Todas las clases de comentarios CSS también se pueden aplicar a Contenido destacado.

| Clase | Descripción |
|---|---|
| .fyre-featured-content-wrapper | El div contenedor para el lector. |
| .fyre-featured | La barra de título inicial. |
| .fyre-featured-header-icon | El icono de la canilla del encabezado. |
| .fyre-featured-title | Texto del encabezado. |
| .fyre-featured-body | El div contenedor para contenido destacado en el lector. |
| .fyre-featured-entrecomillar | Icono de comillas que inicia cada elemento de contenido. |

## Comentarios archivados CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>Todas las clases CSS de contenido también se pueden aplicar a contenido archivado.

| Clase | Descripción |
|---|---|
| .file-archive-stream-title | El texto &quot;Desde el archivo&quot;. |
| .file-archive-stream-title-icon | El logotipo del encabezado &quot;Desde el archivo&quot;. |

## Notificador de comentarios CSS {#section_dy4_krh_xz}

Estas clases permiten personalizar el notificador de comentarios de Livefyre.

| Clase | Descripción |
|---|---|
| .fyre-notification | El div para el elemento de la lista (tanto contenido nuevo como contenido de archivo). |
| .fyre-notificfier | El envoltorio del contenido del notificador. |
| .fyre-notificfier-archive | El envoltorio de todo el contenido nuevo que no sea la publicación más reciente. |
| .fyre-notificfier-avatar | La imagen del avatar. |
| .fyre-notificfier-avatar-container | El div contenedor para el avatar del usuario. Permite definir el posicionamiento. |
| .fyre-notificfier-avatar-shading | Sombreado para el avatar div. |
| .fyre-notificfier-banner | El contenedor del contenido de vista previa del notificador, que muestra el avatar del usuario y un fragmento de contenido para el elemento que se publicó más recientemente. |
| .fyre-notificfier-base | El contenedor de la parte de información del notificador, que enumera el número de comentarios nuevos, el rótulo del notificador y el botón de cierre. |
| .fyre-notificfier-base-close | El div contenedor para el botón de cierre (x) del notificador. |
| .fyre-notificfier-base-Shadow | Sombreado de la base del notificador. |
| .fyre-notificfier-caption | Texto mostrado para el notificador. &quot;Nuevos comentarios&quot; de forma predeterminada. |
| .fyre-notificfier-close | Botón que cierra el notificador. |
| .fyre-notificfier-container | El contenedor del notificador, incluye el banner y la base. |
| .fyre-notificfier-counter | El contenedor del número que aparece en el Notificador. |
| .fyre-notificfier-list | Contenedor del contenido más reciente. |
| .fyre-notificfier-message | Los primeros ~30 caracteres del contenido mostrado. |
| .fyre-notificfier-message-container | El div contenedor del mensaje del encabezado. |
