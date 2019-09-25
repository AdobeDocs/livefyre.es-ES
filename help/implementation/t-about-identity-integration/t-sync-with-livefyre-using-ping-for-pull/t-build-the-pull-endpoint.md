---
description: Genere el extremo de extracción para recibir y responder a las solicitudes de acceso al sistema de identidad de usuario.
seo-description: Genere el extremo de extracción para recibir y responder a las solicitudes de acceso al sistema de identidad de usuario.
seo-title: Generar el extremo de extracción
solution: Experience Manager
title: Generar el extremo de extracción
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Generar el extremo de extracción{#build-the-pull-endpoint}

Genere el extremo de extracción para recibir y responder a las solicitudes de acceso al sistema de identidad de usuario.

1. Cree un extremo HTTPS que reciba solicitudes de Livefyre y responda con un objeto JSON que contenga los datos de usuario más recientes.

   >[!NOTE]
   >
   >Este extremo debe ser accesible. También se recomienda encarecidamente que tanto las solicitudes como las respuestas se envíen a través del protocolo HTTPS.

1. Registre el Extremo con Studio.
