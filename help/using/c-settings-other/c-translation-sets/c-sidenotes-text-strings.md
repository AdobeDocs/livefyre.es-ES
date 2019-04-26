---
description: Personalización de cadenas de texto para Livefyre Sidenotes
seo-description: Personalización de cadenas de texto para Livefyre Sidenotes
seo-title: Cadenas de texto Sidenotes
solution: Experience Manager
title: Cadenas de texto Sidenotes
uuid: a 3735237-e 55 d -4 bc 0-b 88 d -8 a 323980 ee 09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Cadenas de texto Sidenotes{#sidenotes-text-strings}

Personalización de cadenas de texto para Livefyre Sidenotes

Esta página enumera y describe todas las cadenas disponibles para la personalización en las aplicaciones Sidenotes. Para obtener información sobre las cadenas disponibles para las aplicaciones principales de Livefyre, consulte Personalizaciones de cadenas.

Información del flujo de autenticación de implementación
Autor/Información
del contenido Acciones
de usuario de acciones Post Post Errores Interfaz
del moderador

## Implementación {#section_wp2_ql4_xz}

Para implementar esta función, pase una asignación de objeto 1-1 de las cadenas que desee sobrescribir al objeto de configuración Javascript. Si no proporciona un campo, se utilizará el texto predeterminado.

Ejemplo:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Autenticación {#section_pqf_3l4_xz}

Cadenas disponibles para el proceso de autenticación y desde los menús de usuario autenticados.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Cadenas de menú de autenticación | Menuauthsigninbtn | Iniciar sesión |
|  | Menuauthsignedemplsg | Debe iniciar sesión en {action} |
|  | Menuusereditprofile | Editar perfil |
|  | Menuuseradmin | Consola de administración |
|  | Menuuserlogout | Cerrar sesión |
|  | Menuuserbackbtn | Todos |

## Información del flujo {#section_wpy_gl4_xz}

Cadenas disponibles para la información de flujo de contenido y visualización.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Opciones del menú Información | Menuinfocopyright | © Livefyre, Inc. 2014 |
|  | Menuinfohelp | Ayuda |
|  | Menuinfolivefyrelink | Visite Livefyre.com |

## Información de autor/contenido {#section_dhb_gl4_xz}

Listas disponibles para la información de contenido y de autor individual.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | Commentatortag commentModeratorTag | Mod |
|  | Commentpendingtag | Pendiente |
|  | Commentreadmorelink | Más información |
|  | Commentreplylink | Consulte {número} respuestas |
|  | Commentreplylinksing | Consulte respuesta |
|  | Commentvotecount | votos |
|  | Commentvotecountsing | votar |
|  | Datetimeminuteprefix | m |
|  | Datetimemonths | Una matriz. Default =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | Explicación de preguntas | Ahora puede leer y escribir comentarios directamente sobre las frases, párrafos, imágenes y comillas.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Resalte el texto</span> y haga clic en <span class="&rdquo;fycon-write&rdquo;"></span> el icono o haga clic en el <span class="&rdquo;fycon-action-view&rdquo;"></span> icono al final de cada párrafo. |
|  | Questionmocktext | Lo que se conoce «familiarmente» no es conocido, simplemente por el motivo de que es «familiar». |
|  | Questiontitle | ¿Qué es un Sidenote? |

## Acciones del usuario {#section_qxd_fl4_xz}

Cadenas disponibles para las acciones del usuario: marcar, compartir y indicar que gusta contenido existente.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Opciones del menú Responder | Menurepliesviewtitle | Detalles |
|  | Menurepliesviewreply | Responder a la conversación |
| Opciones del menú Compartir | Menushareoptionfacebook | Facebook |
|  | Menushareoptiontwitter | Twitter |
|  | Menusharetitle | Compartir |
| Opciones del menú Indicador | Menuflagoptiondisagree | Rechazar |
|  | Menuflagoptionoffensive | Ofensiva |
|  | Menuflagoptionofftopic | Tema desactivado |
|  | Menuflagoptionspam | Correo no deseado |
|  | Menuflagtitle | Marcar como… |
|  | Facebooksharecaption | Sidenotes en «{title}» |
| Opciones de usuario móvil | Slidercommenttally | de |
|  | Sliderinviteread | Leer |
|  | Sliderinvitewrite | Escribir |
|  | Sliderloading | Cargando… |
|  | Sliderwritetext | ¿Qué piensa? Toque para escribir. |

## Funciones de anuncio {#section_xzf_2l4_xz}

Cadenas disponibles para los usuarios que envían contenido.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | Editoreditbtn | Guardar |
|  | Editoreditposting | Guardando… |
|  | Editoreditreplytitle | Editar respuesta |
|  | Editoredittitle | Editar Sidenote |
|  | Editorplaceholder | ¿Qué piensa? |
|  | Editorpostbtn | Post Sidenote |
|  | Editorpostbtnmobile | Anuncio |
|  | Editorpost | Publicando… |
|  | Editorreplybtn | Publicar respuesta |
|  | Editorreplytitle | Escribir respuesta |
|  | Editortitle | Escribir sidenote |
|  | Emptyimageblocktxt | ¿Qué piensa? |
|  | Emptytextblocktxt | + |
|  | Replybtn | Responder |
|  | Threadreplybtn | Responder a la conversación |
| Opciones de menú Eliminar | Menuconfirmaccept | Sí, {action} |
|  | Menuconfirmcancel | Cancelar |
|  | Menuconfirmtitle | ¿Está seguro? |
| Opciones de menú, etc. | Menuetcoptionapprove | Aprobar |
|  | Menuetcoptiondelete | Eliminar |
|  | Menuetcoptionedit | Editar |
|  | Menuetcoptionflag | Indicador |
|  | Menuetcoptionshare | Compartir |
|  | Menuetcpostedat | Publicado el {date} |
|  | Menuetctitle | Más |

## Interfaz del moderador {#section_o5f_dl4_xz}

Cadenas disponibles para la interfaz de moderador autenticada por el usuario.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
| Mensajes de confirmación del menú Más | Notificationapproved | Aprobado |
|  | Notificationdeleted | Eliminado |
|  | Notificationmarcado | Marcado |

## Errores {#section_gtk_cl4_xz}

Cadenas disponibles para mensajes de error generales.

| Elemento | Clave | Texto predeterminado |
|---|---|---|
|  | Errorconnection | Uh-oh. Parece que no tiene una buena conexión. |
|  | Errorduplicate | También nos gusta su nota, pero no puede anunciarla dos veces. |
|  | Errorgeneral | Se ha producido un error. Inténtelo de nuevo. |
|  | Errorserver | Algo salió mal con nuestro servidor. ¿Inténtelo de nuevo? |

