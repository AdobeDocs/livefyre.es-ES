---
description: En el caso de contenido de estilo personalizado para grupos de usuarios,
  primero debe agregar una etiqueta de usuario a la cuenta y, a continuación, aplicar
  estilo al contenido mediante CSS.
seo-description: En el caso de contenido de estilo personalizado para grupos de usuarios,
  primero debe agregar una etiqueta de usuario a la cuenta y, a continuación, aplicar
  estilo al contenido mediante CSS.
seo-title: Aplicación de estilos personalizados
solution: Experience Manager
title: Aplicación de estilos personalizados
uuid: 0556 aa 2 f -4 fcd -4 bde-abb 5-479 ec 682 f 573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Aplicación de estilos personalizados{#applying-custom-styles}

En el caso de contenido de estilo personalizado para grupos de usuarios, primero debe agregar una etiqueta de usuario a la cuenta y, a continuación, aplicar estilo al contenido mediante CSS.

Para cada etiqueta de usuario agregada a través de Studio o Ping para Extract, Livefyre creará dos clases CSS, las cuales pueden utilizarse para aplicar estilo al contenido del grupo.

Al convertir etiquetas de usuario en clases CSS:

* Livefyre crea dos clases: fyre-author-tag-*** < your_ group >*** y fyre-tag-author-*** < your_ group >***. Ambos pueden utilizarse para aplicar estilo al contenido.

* Todos los espacios incluidos en la etiqueta se convertirán en guiones bajos. Por ejemplo: ' Usuario favorito'se convertirá en favorito_ user.
* Los caracteres Unicode incluidos en los nombres de grupo no se convertirán y aparecerán como Unicode en los nombres de clase. Por ejemplo: El grupo de usuarios'modérateur'se convertirá en fyre-comment-author-tag-modérateur.

Una vez que se hayan creado los grupos de usuarios, utilice las clases CSS de Livefyre para aplicar estilo personalizado al contenido.

## Contenido de estilo para Moderadores (y Propietarios) {#section_vjv_2cv_xz}

* Use la clase CSS. fyre-moderator.

   >[!NOTE]
   >
   >Los propietarios, como también moderadores, tendrán esta clase aplicada a su contenido en el flujo.

* Cree una regla CSS para mostrar o aplicar estilo a un distintivo para el Grupo:

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## Contenido de estilo para grupos de usuarios {#section_ghn_s1v_xz}

Cree una regla CSS para mostrar o aplicar estilo a un distintivo para el Grupo:

```
<span class="fyre-comment-author-tag fyre-comment-author-tag-writer fyre-comment-plus" data-fyre-author-tag="staff">Staff Writer</span>
```

```
.livechat-comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag, .comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag { 
    display: inline-block !important; 
    background: #603url('/etc/designs/site/images/comments-icon-staff.8db5be91.png?1438807177') no-repeat left center !important; 
    padding-right: 3px !important; 
    padding-left: 20px !important; 
    text-transform: uppercase !important; 
    font-weight: bold !important; 
    font-size: 11px !important; 
    border-radius: 0 !important; 
    color: #ffffff !important; 
}
```

Utilice la clase CSS fyre-author-tag-*** < your_ group >*** o fyre-tag-author-*** < your_ group >*** para aplicar estilo a la fuente y al fondo de cada elemento publicado desde una cuenta asociada a la etiqueta seleccionada.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

