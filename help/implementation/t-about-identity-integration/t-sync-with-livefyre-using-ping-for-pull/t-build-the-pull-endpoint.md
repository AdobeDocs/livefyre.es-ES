---
description: Cree el extremo de extracción para recibir y responder a las solicitudes
  de acceso a su sistema de identidad de usuario.
seo-description: Cree el extremo de extracción para recibir y responder a las solicitudes
  de acceso a su sistema de identidad de usuario.
seo-title: Generar el extremo de extracción
solution: Experience Manager
title: Generar el extremo de extracción
uuid: 1703152 f-aaa 7-4 a 88-aa 33-d 9 f 8957 ad 42 b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Generar el extremo de extracción{#build-the-pull-endpoint}

Cree el extremo de extracción para recibir y responder a las solicitudes de acceso a su sistema de identidad de usuario.

1. Cree un extremo HTTPS que reciba solicitudes de Livefyre y responda con un objeto JSON que contenga los datos de usuario más recientes.

   >[!NOTE]
   >
   >Este extremo debe ser accesible. También se recomienda enfáticamente que las solicitudes y respuestas se envíen a través del protocolo HTTPS.

1. Registre el extremo con Studio.
