---
description: Agregue una etiqueta de usuario a una cuenta para agregar un usuario a un grupo.
title: Agregar usuarios a grupos
exl-id: 6e799c77-e815-40c2-ae06-bbd076df9fe7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# Agregar usuarios a grupos{#adding-users-to-groups}

Agregue una etiqueta de usuario a una cuenta para agregar un usuario a un grupo.

Las etiquetas de usuario se pueden implementar tanto para los sistemas de perfil propietarios como empresariales, y se pueden agregar a las cuentas por varios medios:

* La creación de propietarios y moderadores mediante Studio asigna la etiqueta de usuario &quot;Moderador&quot; a la cuenta.
* Al crear grupos de usuarios y agregarles usuarios a través de Studio, se aplican automáticamente etiquetas de usuario con el nombre del grupo a los usuarios seleccionados.
* Las etiquetas de usuario también se pueden aplicar directamente a las cuentas mediante la llamada [Añadir etiqueta de usuario HTTP](https://api.livefyre.com/docs#add-user-tag) o Ping para extracción.

>[!NOTE]
>
>Ambos métodos de API, la llamada HTTP Agregar etiqueta de usuario y el método Ping para extracción, sobrescribirán cualquier etiqueta previamente asignada a la cuenta por otros medios. Por lo tanto, seleccione un método y utilícelo de forma consistente durante todo el proceso.

## Agregar un usuario a un grupo desde la página Usuarios de Studio {#section_qgq_nbw_xz}

* Haga clic en **[!UICONTROL Add Group]** o en la etiqueta de grupo debajo de cualquier nombre de usuario para abrir el menú de grupos.
* Desplácese por la lista y busque el grupo al que desea agregar el usuario. Puede introducir un nombre de grupo en el cuadro **[!UICONTROL Search]** de la parte superior de la lista desplegable.
* Haga clic en la casilla de verificación situada junto a los grupos a los que se debe agregar el usuario y vuelva a la visita.

El perfil del usuario mostrará el nombre del grupo (si el usuario está solo en un grupo) o el número de grupos a los que pertenece el usuario.

## Agregar un usuario a un grupo mediante la llamada Agregar etiqueta de usuario {#section_kn3_gbw_xz}

Pase la LFToken del usuario y el nombre de la etiqueta seleccionada con la solicitud del POST

Por ejemplo:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Para obtener más información, consulte Referencia de API > [Agregar etiqueta de usuario](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Agregar un usuario a un grupo mediante Ping para extracción {#section_kyj_11w_xz}

Utilice la matriz de etiquetas para asignar usuarios a grupos de usuarios. (Las etiquetas pueden incluir entre 1 y 63 caracteres alfanuméricos y de guion bajo).

Por ejemplo:

```
"tags": ["moderator", "brand_advocate"],
```

## Agregar un usuario a un grupo mediante Perfiles remotos {#section_uyn_scv_xz}

Agregue etiquetas de usuario al Perfil remoto, que se usan para sincronizar datos de usuario entre el sistema de perfiles personalizado y Livefyre, para usuarios específicos.
