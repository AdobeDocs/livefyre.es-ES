---
description: Livefyre utiliza una interfaz PUSH para enviar información del sistema
  externo sobre los cambios a los permisos de usuario.
seo-description: Livefyre utiliza una interfaz PUSH para enviar información del sistema
  externo sobre los cambios a los permisos de usuario.
seo-title: Publicar permisos de usuario en sistemas externos (opcional)
solution: Experience Manager
title: Publicar permisos de usuario en sistemas externos (opcional)
uuid: 9 c 18 b 20 d -3 b 93-4666-b 7 de -1 ec 60318 cf 88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Publicar permisos de usuario en sistemas externos (opcional){#posting-user-permissions-to-external-systems-optional}

Livefyre utiliza una interfaz PUSH para enviar información del sistema externo sobre los cambios a los permisos de usuario.

## Tipos de usuarios en Livefyre Studio

| Tipo de usuario | Descripción |
|--- |--- |
| propietario | Este usuario es propietario y puede moderar contenido y asignar nuevos moderadores. |
| administrador | Este usuario es moderador y puede moderar contenido. |
| miembro | Este usuario está en la lista blanca. El contenido publicado no pasa por filtros de correo no deseado o de perfil, y no requiere aprobación en flujos previamente moderados. |
| none | Este usuario es un usuario estándar y no tiene permisos especiales. |
| outcast | Se ha prohibido a este usuario participar en cualquier conversación. |

Para publicar permisos de usuario en sistemas externos, debe registrar una URL que reciba datos de permisos como solicitudes POST.

Por ejemplo:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parámetro | Descripción |
|--- |--- |
| Networkname | Su Livefyre ha proporcionado el nombre de la red. |
| token | Token válido del sistema. |
| url | URL para registrarse. |

La URL registrada debe aceptar POST con los siguientes datos como tipo de contenido: application/x-www-form-urlencoded.

| Parámetro | Descripción |
|--- |--- |
| jid | JID del usuario cuya afiliación se ha cambiado. Un JID es una cadena del formulario `user_id@network`. |
| afiliación | Nombre de los permisos asignados, que deben ser uno de los siguientes: `{admin | member | none | outcast | owner}` |

Para obtener más información sobre la actualización de la configuración de afiliación de usuario, consulte [la Referencia de la API de afiliación de usuario](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
