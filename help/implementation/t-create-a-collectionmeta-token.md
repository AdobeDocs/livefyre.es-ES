---
description: Cree una nueva colección creando un token collectionMeta que se pase a Livefyre.
title: Creación de una colección mediante el token CollectionMeta
exl-id: d2dafc90-de21-4998-8e85-83f970524329
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Crear una colección utilizando el token de CollectionMeta{#create-a-collection-using-the-collectionmeta-token}

Cree una nueva colección creando un token collectionMeta que se pase a Livefyre.

1. Cree el token collectionMeta .
1. Cree la suma de comprobación.

   La suma de comprobación es obligatoria si desea notificar a Livefyre cualquier cambio que haya realizado en su colección. Livefyre actualizará su colección solo si la suma de comprobación proporcionada es diferente a la suma de comprobación enviada anteriormente. Crear una suma de comprobación es como crear un token `collectionMeta` pero en lugar de llamar a `buildCollectionMetaToken` llama a `buildChecksum`.

Cree tokens de usuario para autenticarse en Livefyre.
