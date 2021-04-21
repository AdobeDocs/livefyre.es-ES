---
description: Para el contenido de estilo personalizado de los grupos de usuarios, primero debe agregar una etiqueta de usuario a la cuenta y después aplicar un estilo al contenido mediante CSS.
title: Aplicación de estilos personalizados
exl-id: 54692525-32ce-487a-b3c3-da1261b58da1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Aplicar estilos personalizados{#applying-custom-styles}

Para el contenido de estilo personalizado de los grupos de usuarios, primero debe agregar una etiqueta de usuario a la cuenta y después aplicar un estilo al contenido mediante CSS.

Para cada etiqueta de usuario agregada a través de Studio o Ping para extracción, Livefyre creará dos clases CSS, las cuales pueden utilizarse para aplicar estilo al contenido del grupo.

Al convertir Etiquetas de usuario en clases CSS:

* Livefyre crea dos clases: fyre-author-tag-***&lt;your_group>*** y fyre-tag-author-***&lt;your_group>***. Ambos pueden utilizarse para aplicar estilo al contenido.

* Los espacios incluidos en la etiqueta se convertirán en guiones bajos. Por ejemplo: &quot;Usuario favorito&quot; se convertirá en usuario_favorito.
* Los caracteres Unicode incluidos en los nombres de grupo no se convertirán y aparecerán como Unicode en los nombres de clase. Por ejemplo: El grupo de usuarios &quot;modérateur&quot; se convertirá en &quot;fyre-comment-author-tag-modérateur&quot;.

Una vez creados los grupos de usuarios, utilice las clases CSS de Livefyre para aplicar estilo personalizado al contenido.

## Contenido de estilo para moderadores (y propietarios) {#section_vjv_2cv_xz}

* Utilice la clase CSS .fyre-moderator.

   >[!NOTE]
   >
   >Los propietarios, como también son moderadores, tendrán esta clase aplicada a su contenido en el flujo también.

* Cree una regla CSS para mostrar o aplicar estilo a un distintivo del grupo:

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

Cree una regla CSS para mostrar o aplicar estilo a un distintivo del grupo:

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

Utilice la clase CSS fyre-author-tag-***&lt;your_group>*** o fyre-tag-author-****&lt;your_group>** para aplicar estilo a la fuente y el fondo de cada elemento publicado desde una cuenta asociada a la etiqueta seleccionada.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```
