---
description: Agregue una etiqueta de usuario a una cuenta para agregar un usuario
  a un grupo.
seo-description: Agregue una etiqueta de usuario a una cuenta para agregar un usuario
  a un grupo.
seo-title: Adición de usuarios a grupos
solution: Experience Manager
title: Adición de usuarios a grupos
uuid: 3633 f 2 df -8 d 60-4 cdd-b 9 a 2-3807218 c 74 a 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Adición de usuarios a grupos{#adding-users-to-groups}

Agregue una etiqueta de usuario a una cuenta para agregar un usuario a un grupo.

Las etiquetas de usuario pueden implementarse tanto para sistemas de perfil de propiedad como de empresas, y pueden agregarse a las cuentas por varios medios:

* Crear propietarios y moderadores a través de Studio asigna la etiqueta de usuario'Moderador'a la cuenta.
* Crear grupos de usuarios y agregar usuarios a través de Studio, aplica automáticamente Etiquetas de usuario con el nombre del grupo a los usuarios seleccionados.
* Las etiquetas de usuario también se pueden aplicar directamente a cuentas mediante [la llamada Agregar etiqueta de](https://api.livefyre.com/docs#add-user-tag) usuario HTTP o Ping para extraer.

>[!NOTE]
>
>Tanto los métodos API como la llamada HTTP Agregar etiqueta de usuario y el método Ping para extracción sobrescribirán las etiquetas asignadas anteriormente a la cuenta a través de otros medios. Por lo tanto, seleccione un método y utilícelo de forma coherente durante todo el proceso.

## Agregar un usuario a un grupo desde la página Usuarios en Studio {#section_qgq_nbw_xz}

* Haga clic **[!UICONTROL Add Group]** o en la etiqueta de grupo debajo de cualquier nombre de usuario para abrir el menú de grupos.
* Desplácese por la lista y busque el grupo al que desee agregar el usuario. Puede introducir un nombre de grupo en **[!UICONTROL Search]** el cuadro situado en la parte superior de la lista desplegable.
* Haga clic en la casilla junto a los grupos a los que debe agregarse el usuario y vuelva a la visita.

El perfil del usuario mostrará el nombre del grupo (si el usuario está sólo en un grupo) o el número de grupos a los que pertenece el usuario.

## Agregar un usuario a un grupo mediante la llamada Agregar etiqueta de usuario {#section_kn3_gbw_xz}

Pasar el lftoken del usuario y el nombre de etiqueta seleccionado con la solicitud POST

Por ejemplo:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Para obtener más información, consulte Referencia de API > [Agregar etiqueta de usuario](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Agregar un usuario a un grupo mediante Ping para extracción {#section_kyj_11w_xz}

Utilice la matriz de etiquetas para asignar usuarios a grupos de usuarios. (Las etiquetas pueden incluir caracteres alfanuméricos y de guiones bajos de 1 a 63).

Por ejemplo:

```
"tags": ["moderator", "brand_advocate"],
```

## Agregar un usuario a un grupo mediante perfiles remotos {#section_uyn_scv_xz}

Agregue etiquetas de usuario al perfil remoto, utilizado para sincronizar los datos de usuario entre el sistema de perfiles personalizado y Livefyre para los usuarios específicos.
