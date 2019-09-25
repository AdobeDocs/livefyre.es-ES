---
description: Cree una nueva colección creando un token collectionMeta que se pasa a Livefyre.
seo-description: Cree una nueva colección creando un token collectionMeta que se pasa a Livefyre.
seo-title: Creación de una colección con el token CollectionMeta
solution: Experience Manager
title: Creación de una colección con el token CollectionMeta
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Creación de una colección con el token CollectionMeta{#create-a-collection-using-the-collectionmeta-token}

Cree una nueva colección creando un token collectionMeta que se pasa a Livefyre.

1. Create the collectionMeta token.
1. Cree la suma de comprobación.

   La suma de comprobación es obligatoria si desea notificar a Livefyre cualquier cambio que haya realizado en la colección. Livefyre actualizará su colección solo si la suma de comprobación proporcionada es diferente a la suma de comprobación enviada anteriormente. Crear una suma de comprobación es como crear un `collectionMeta` token, pero en lugar de llamar `buildCollectionMetaToken` a `buildChecksum`.

Cree tokens de usuario para autenticarse en Livefyre.