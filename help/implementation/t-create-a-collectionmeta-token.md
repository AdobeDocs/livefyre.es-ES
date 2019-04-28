---
description: Cree una colección nueva creando un distintivo collectionmeta que se pase a Livefyre.
seo-description: Cree una colección nueva creando un distintivo collectionmeta que se pase a Livefyre.
seo-title: Crear una colección con collectionmeta Token
solution: Experience Manager
title: Crear una colección con collectionmeta Token
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Crear una colección con collectionmeta Token{#create-a-collection-using-the-collectionmeta-token}

Cree una colección nueva creando un distintivo collectionmeta que se pase a Livefyre.

1. Cree el token collectionmeta.
1. Cree la suma de comprobación.

   La suma de verificación es obligatoria si desea notificar a Livefyre los cambios realizados en la colección. Livefyre actualizará su colección solo si la suma de comprobación proporcionada es diferente a la suma de comprobación enviada anteriormente. Crear una suma de comprobación es como crear `collectionMeta` un token, en lugar de llamar `buildCollectionMetaToken` a llamar `buildChecksum`.

Cree tokens de usuario para autenticarse en Livefyre.