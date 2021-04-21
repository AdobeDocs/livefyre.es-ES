---
description: Livefyre utiliza una interfaz PUSH para enviar información externa del sistema sobre los cambios en los permisos de usuario.
title: Anuncio de permisos de usuario en sistemas externos (opcional)
exl-id: 335c9ff2-e392-4310-aad2-7890c8e82eba
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 4%

---

# Anuncio de permisos de usuario en sistemas externos (opcional){#posting-user-permissions-to-external-systems-optional}

Livefyre utiliza una interfaz PUSH para enviar información externa del sistema sobre los cambios en los permisos de usuario.

## Tipos de usuarios en Livefyre Studio

| Tipo de usuario | Descripción |
|--- |--- |
| propietario | Este usuario es propietario y puede moderar el contenido y asignar nuevos moderadores. |
| admin | Este usuario es moderador y puede moderar contenido. |
| miembro | Este usuario está incluido en la lista de permitidos. El contenido publicado no pasa a través de filtros de correo no deseado o de profanidad y no requiere aprobación en flujos moderados previamente. |
| Ninguno | Este usuario es un usuario estándar y no tiene permisos especiales. |
| outcast | A este usuario se le ha prohibido participar en cualquier conversación. |

Para anunciar permisos de usuario en sistemas externos, debe registrar una dirección URL que reciba datos de permisos como solicitudes del POST.

Por ejemplo:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parámetro | Descripción |
|--- |--- |
| networkName | Su Livefyre ha proporcionado el nombre de red. |
| token | Token válido del sistema. |
| url | URL para registrar. |

La URL registrada debe aceptar las entradas de publicación con los siguientes datos como tipo de contenido: application/x-www-form-urlencoded.

| Parámetro | Descripción |
|--- |--- |
| jid | JID del usuario cuya afiliación ha cambiado. Un JID es una cadena del formulario `user_id@network`. |
| afiliación | Nombre de los permisos asignados, que debe ser uno de los siguientes:  `{admin | member | none | outcast | owner}` |

Para obtener información adicional sobre la actualización de la configuración de afiliación de usuario, consulte [Agregar referencia de API de afiliación de usuario](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
