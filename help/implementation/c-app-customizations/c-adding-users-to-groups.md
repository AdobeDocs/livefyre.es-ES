---
description: Agregue una etiqueta de usuario a una cuenta para agregar un usuario a un grupo.
seo-description: Agregue una etiqueta de usuario a una cuenta para agregar un usuario a un grupo.
seo-title: Adición de usuarios a grupos
solution: Experience Manager
title: Adición de usuarios a grupos
uuid: 3633f2df-8d60-4cdd-b9a2-3807218c74a0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Adding Users to Groups{#adding-users-to-groups}

Agregue una etiqueta de usuario a una cuenta para agregar un usuario a un grupo.

Las etiquetas de usuario pueden implementarse para los sistemas de perfil privado y empresarial y pueden agregarse a las cuentas por varios medios:

* La creación de propietarios y moderadores mediante Studio asigna la etiqueta de usuario "Moderador" a la cuenta.
* Al crear grupos de usuarios y agregarles usuarios a través de Studio, se aplican automáticamente etiquetas de usuario con el nombre del grupo a los usuarios seleccionados.
* Las etiquetas de usuario también se pueden aplicar directamente a las cuentas mediante la llamada [Agregar etiqueta de usuario HTTP](https://api.livefyre.com/docs#add-user-tag) o Ping para extracción.

>[!NOTE]
>
>Ambos métodos de API, la llamada HTTP Agregar etiqueta de usuario y el método Ping para extracción, sobrescribirán cualquier etiqueta asignada anteriormente a la cuenta por otros medios. Por lo tanto, seleccione un método y utilícelo de forma consistente a lo largo del proceso.

## Agregar un usuario a un grupo desde la página Usuarios de Studio {#section_qgq_nbw_xz}

* Haga clic en **[!UICONTROL Add Group]** o en la etiqueta de grupo debajo de cualquier nombre de usuario para abrir el menú de grupos.
* Desplácese por la lista y busque el grupo al que desee agregar el usuario. Puede introducir un nombre de grupo en el **[!UICONTROL Search]** cuadro de la parte superior del menú desplegable.
* Haga clic en la casilla de verificación situada junto a los grupos a los que se debe agregar el usuario y vuelva a la visita.

El perfil del usuario mostrará el nombre del grupo (si el usuario solo está en un grupo) o el número de grupos al que pertenece el usuario.

## Agregar un usuario a un grupo mediante la llamada Agregar etiqueta de usuario {#section_kn3_gbw_xz}

Pase el LFToken del usuario y el nombre de la etiqueta seleccionada junto con la solicitud POST

Por ejemplo:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Para obtener más información, consulte Referencia de API &gt; [Agregar etiqueta](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post)de usuario.

## Agregar un usuario a un grupo mediante ping para extracción {#section_kyj_11w_xz}

Utilice la matriz de etiquetas para asignar usuarios a grupos de usuarios. (Las etiquetas pueden incluir entre 1 y 63 caracteres alfanuméricos y de subrayado).

Por ejemplo:

```
"tags": ["moderator", "brand_advocate"],
```

## Agregar un usuario a un grupo mediante perfiles remotos {#section_uyn_scv_xz}

Agregue etiquetas de usuario al perfil remoto, que se utilizan para sincronizar datos de usuario entre el sistema de perfiles personalizado y Livefyre, para usuarios específicos.
