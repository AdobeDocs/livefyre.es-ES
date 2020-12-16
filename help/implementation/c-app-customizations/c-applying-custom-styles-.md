---
description: Para personalizar el contenido de estilo para los grupos de usuarios, primero debe agregar una etiqueta de usuario a la cuenta y después aplicar estilo al contenido mediante CSS.
seo-description: Para personalizar el contenido de estilo para los grupos de usuarios, primero debe agregar una etiqueta de usuario a la cuenta y después aplicar estilo al contenido mediante CSS.
seo-title: Aplicación de estilos personalizados
solution: Experience Manager
title: Aplicación de estilos personalizados
uuid: 0556aa2f-4fcd-4bde-abb5-479ec682f573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# Aplicación de estilos personalizados{#applying-custom-styles}

Para personalizar el contenido de estilo para los grupos de usuarios, primero debe agregar una etiqueta de usuario a la cuenta y después aplicar estilo al contenido mediante CSS.

Para cada etiqueta de usuario agregada mediante Studio o Ping para extracción, Livefyre creará dos clases CSS, ambas que se pueden utilizar para aplicar estilo al contenido del grupo.

Al convertir etiquetas de usuario en clases CSS:

* Livefyre crea dos clases: fyre-author-tag-***&lt;su_grupo>*** y fyre-tag-author-***&lt;su_grupo>***. Ambos se pueden utilizar para aplicar estilo al contenido.

* Los espacios incluidos en la etiqueta se convertirán en caracteres de subrayado. Por ejemplo: &quot;Usuario favorito&quot; se convertirá en usuario_favorito.
* Los caracteres Unicode incluidos en los nombres de grupo no se convertirán y aparecerán como Unicode en los nombres de clase. Por ejemplo: El grupo de usuarios &quot;modérateur&quot; se convertirá en &quot;fyre-comment-author-tag-modérateur&quot;.

Una vez creados los grupos de usuarios, utilice las clases CSS de Livefyre para aplicar estilo personalizado al contenido.

## Contenido de estilo para moderadores (y propietarios) {#section_vjv_2cv_xz}

* Utilice la clase CSS .fyre-moderator.

   >[!NOTE]
   >
   >Los propietarios, como también son moderadores, tendrán esta clase aplicada también a su contenido en el flujo.

* Cree una regla CSS para mostrar o aplicar estilo a un distintivo para el grupo:

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

Cree una regla CSS para mostrar o aplicar estilo a un distintivo para el grupo:

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

Utilice la clase CSS fyre-author-tag-***&lt;your_group>*** o fyre-tag-author-***&lt;your_group>** para aplicar estilo a la fuente y al fondo de cada elemento publicado desde una cuenta asociada a la etiqueta seleccionada.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

