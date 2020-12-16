---
description: Livefyre utiliza una interfaz PUSH para enviar información externa del sistema sobre los cambios en los permisos de usuario.
seo-description: Livefyre utiliza una interfaz PUSH para enviar información externa del sistema sobre los cambios en los permisos de usuario.
seo-title: Registro de permisos de usuario en sistemas externos (opcional)
solution: Experience Manager
title: Registro de permisos de usuario en sistemas externos (opcional)
uuid: 9c18b20d-3b93-4666-b7de-1ec60318cf88
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---


# Registro de permisos de usuario en sistemas externos (opcional){#posting-user-permissions-to-external-systems-optional}

Livefyre utiliza una interfaz PUSH para enviar información externa del sistema sobre los cambios en los permisos de usuario.

## Tipos de usuarios en Livefyre Studio

| Tipo de usuario | Descripción |
|--- |--- |
| propietario | Este usuario es propietario y puede moderar contenido y asignar nuevos moderadores. |
| admin | Este usuario es un moderador y puede moderar contenido. |
| miembro | Este usuario está permitido. El contenido publicado no pasa a través de filtros de contenido no deseado o de contenido no deseado y no requiere aprobación en flujos moderados previamente. |
| Ninguno | Este usuario es un usuario estándar y no tiene permisos especiales. |
| outcast | A este usuario se le ha prohibido participar en cualquier conversación. |

Para publicar permisos de usuario en sistemas externos, debe registrar una URL que reciba datos de permisos como solicitudes de POST.

Por ejemplo:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parámetro | Descripción |
|--- |--- |
| networkName | El nombre de red proporcionado por Livefyre. |
| token | Distintivo válido del sistema. |
| url | URL para registrarse. |

La dirección URL registrada debe aceptar POST con los siguientes datos como tipo de contenido: application/x-www-form-urlencoded.

| Parámetro | Descripción |
|--- |--- |
| jid | JID del usuario cuya afiliación ha cambiado. Un JID es una cadena del formulario `user_id@network`. |
| afiliación | Nombre de los permisos asignados, que debe ser uno de los siguientes:  `{admin | member | none | outcast | owner}` |

Para obtener información adicional sobre la actualización de la configuración de afiliación de usuario, consulte la [Referencia de la API de Añadir afiliación de usuario](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
