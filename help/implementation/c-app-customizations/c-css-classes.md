---
description: Utilice las clases CSS disponibles para personalizar la visualización
  de sus aplicaciones.
seo-description: Utilice las clases CSS disponibles para personalizar la visualización
  de sus aplicaciones.
seo-title: Clases CSS
solution: Experience Manager
title: Clases CSS
uuid: 8714 e 7 e 5-3858-458 f-a 464-de 87 fd 2 f 0 ff 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Clases CSS{#css-classes}

Utilice las clases CSS disponibles para personalizar la visualización de sus aplicaciones.

Disponible para chat, comentarios, blogs en directo, revisiones y Sidenotes.

Use CSS para personalizar las aplicaciones de Livefyre para una integración más completa con su página, anulando simplemente la CSS predeterminada de la aplicación con su propia hoja de estilo. Esta sección describe las personalizaciones CSS disponibles.

* [CSS Editor](#c_css_classes/section_edx_prh_xz)
* [Ordenar opciones CSS](#c_css_classes/section_btq_4rh_xz)
* [CSS de comentarios](#c_css_classes/section_mlv_nrh_xz)
* [CSS de comentarios destacados](#c_css_classes/section_m2v_mrh_xz)
* [CSS de comentarios archivados](#c_css_classes/section_bs5_lrh_xz)
* [CSS de notificador de comentarios](#c_css_classes/section_dy4_krh_xz)
* [Clases de Storify CSS](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## CSS Editor {#section_edx_prh_xz}

Utilice estas clases para cambiar la interfaz del editor de anuncios.

| Clase | Descripción |
|---|---|
| . fyre-comment-count | Texto que muestra el número de comentarios. |
| . fyre-login-bar | Cuadro delimitador que contiene la barra de inicio de sesión y las opciones. |
| . fyre-live-container | Cuadro delimitador alrededor del número de personas que escucha y sus avatares. |
| . fyre-editor | Cuadro delimitador alrededor de la barra. fyre-login-bar. fyre-live-container y el área de texto donde los usuarios escriben sus comentarios. |
| . fyre-stream-sort | Cuadro delimitador alrededor de las opciones de clasificación. |

También puede editar estilos en la configuración de la aplicación, incluido el color de fondo del campo del editor, el color de fuente, el tamaño y la familia del texto que aparece dentro del editor.

Para personalizar el editor de comentarios, agregue editorcss: {} a fyre. conv. load () e incluir el estilo deseado. Por ejemplo, para actualizar el editor con su CSS personalizada:

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

## Ordenar opciones CSS {#section_btq_4rh_xz}

| Clase | Descripción |
|---|---|
| . fyre-stream-sort | El div de opciones de ordenación completo. |
| . fyre-stream-sort-más reciente | La opción «Más reciente». |
| . fyre-stream-sort-older | La opción «Más antiguos». |
| . fyre-stream-sort-bar | Barra separadora entre las opciones. |
| . fyre-stream-sort-selected | La opción de clasificación seleccionada actualmente. |

Estructura HTML:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Ocultar el|' separar las opciones de clasificación.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## CSS de comentarios {#section_mlv_nrh_xz}

| Clase | Descripción |
|---|---|
| . fyre-comment-author-tag- *`custom tag name`* | Livefyre creará una clase CSS en este formato para cada etiqueta de usuario agregada mediante el estudio de Livefyre, Sincronización [de perfil](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Esta clase puede utilizarse para aplicar estilo al fondo de cualquier contenido publicado por cuentas de usuario, incluida la etiqueta. |
| . fyre-tag-content-icon- *`tag name`* | Livefyre creará una clase CSS en este formato para cada etiqueta de contenido agregada a través de Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Esta clase puede utilizarse para aplicar estilo a cualquier contenido al que agregue la etiqueta. |
| . fyre-comment-user | Cuadro delimitador que contiene la imagen del perfil de usuario. |
| . fyre-comment-username | El nombre de usuario. |
| . fyre-moderator | Cuadro delimitador del moderador. |
| . fyre-comment | Cuadro delimitador alrededor del texto o vínculo del comentario. |
| . fyre-comment-article | Cuadro delimitador para todo el contenido del comentario. |
| . fyre-comment-date | Etiqueta adjunta al elemento «hora desde que se publicó». |
| . fyre-comment-media | Cuadro delimitador alrededor del contenido multimedia. |
| . fyre-comment-actions | Cuadro delimitador alrededor de las acciones disponibles para realizar en un comentario. |
| . fyre-comment | Cuadro delimitador alrededor del vínculo "Me gusta". |
| . fyre-comment-answer | Cuadro delimitador alrededor del vínculo «Responder». |

## CSS de comentarios destacados {#section_m2v_mrh_xz}

>[!NOTE]
>
>Todas las clases CSS de comentarios también pueden aplicarse al contenido destacado.

| Clase | Descripción |
|---|---|
| . fyre-featured-content-wrapper | El div contenedor del lector. |
| . fyre-featured-header | Barra de título inicial. |
| . fyre-featured-header-icon | Icono de margen del encabezado. |
| . fyre-featured-title | El texto del encabezado. |
| . fyre-legacy | El div contenedor del contenido destacado del lector. |
| . fyre-featured-quote | Icono de cita que comienza cada elemento de contenido. |

## CSS de comentarios archivados {#section_bs5_lrh_xz}

>[!NOTE]
>
>Todas las clases CSS de contenido también pueden aplicarse al contenido archivado.

| Clase | Descripción |
|---|---|
| . fyre-archive-stream-title | El texto «Desde el archivo». |
| . fyre-archive-stream-title-icon | Logotipo del encabezado «Desde el archivo». |

## CSS de notificador de comentarios {#section_dy4_krh_xz}

Estas clases permiten personalizar el Notificador de comentarios de Livefyre.

| Clase | Descripción |
|---|---|
| . fyre | El div del elemento de lista (nuevo y archivado). |
| . fyre-notificfier | El envoltorio para el contenido del notificador. |
| . fyre-notificfier-archive | El envoltorio para todo el contenido nuevo que no sea el más reciente. |
| . fyre-notificfier-avatar | La imagen para el avatar. |
| . fyre-notificfier-avatar-container | El div contenedor para el avatar del usuario. Permite definir la posición. |
| . fyre-notificfier-avatar-sombreado | Sombreado del div avatar. |
| . fyre-notificfier-banner | Contenedor del contenido de vista previa del notificador, que muestra el avatar del usuario y un fragmento de contenido del último elemento publicado. |
| . fyre-notificfier-base | Contenedor de la parte de información del Notificador, que indica el número de nuevos comentarios, el rótulo del Notificador y el botón de cierre. |
| . fyre-notificfier-base-close | El div contenedor del botón de cierre (x) para el notificador. |
| . fyre-notificfier-base-shadow | Sombreado de la base de notificación. |
| . fyre-notificfier-caption | Texto mostrado para el notificador. ' Nuevos comentarios'de forma predeterminada. |
| . fyre-notificfier-close | Botón que cierra el notificador. |
| . fyre-notificfier-container | El contenedor del Notificador incluye tanto la pancarta como la base. |
| . fyre-notificfier-counter | El contenedor del número enumerado en el Notificador. |
| . fyre-notificfier-list | Contenedor del contenido más reciente. |
| . fyre-notificfier-message | Los primeros ~ 30 caracteres del contenido mostrado. |
| . fyre-notificfier-message-container | El div contenedor para el mensaje de encabezado. |
