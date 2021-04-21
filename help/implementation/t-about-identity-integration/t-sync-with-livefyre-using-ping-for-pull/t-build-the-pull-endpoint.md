---
description: Cree el punto final de extracción para recibir y responder a las solicitudes de acceso a su sistema de identidad de usuario.
title: Generar el extremo de extracción
exl-id: cc66365b-0d5f-4a0b-954f-ee014e75d4a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# Generar el extremo de extracción{#build-the-pull-endpoint}

Cree el punto final de extracción para recibir y responder a las solicitudes de acceso a su sistema de identidad de usuario.

1. Cree un extremo HTTPS que reciba solicitudes de Livefyre y responda con un objeto JSON que contenga los datos de usuario más recientes.

   >[!NOTE]
   >
   >Se debe poder acceder a este extremo. También se recomienda encarecidamente que tanto las solicitudes como las respuestas se envíen a través del protocolo HTTPS.

1. Registre el extremo con Studio.
