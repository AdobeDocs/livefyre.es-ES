---
description: Instagram ha cambiado el número de solicitudes que cualquier empresa que utilice la API de Instagram, incluido Livefyre, puede realizar de 5000 solicitudes por hora por token a 200 solicitudes por hora por token. Esto se conoce como limitación de velocidad.
title: Limitación de la tasa de instagram
exl-id: b13db09b-fb5a-4711-a566-d0976172e35e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Solución de problemas: Límites en el contenido de Instagram {#instagram-rate-limiting}

Instagram ha cambiado el número de solicitudes que cualquier empresa que utilice la API de Instagram, incluido Livefyre, puede realizar de 5000 solicitudes por hora por token a 200 solicitudes por hora por token. Esto se conoce como *limitación de velocidad*.

Un token es lo mismo que una cuenta de Instagram.

Puede encontrarse con un error que limita su capacidad de buscar u obtener contenido de Instagram porque:

* Están usando una cuenta para más de un flujo
* Tienen un gran número de emisiones de Instagram
* Puede estar usando hashtags de gran volumen (por ejemplo, `#cats` o `#beach`)

Para reducir el impacto de la limitación de velocidad de Instagram:

* Conecte varias cuentas de Instagram a la red. Para obtener información sobre cómo agregar cuentas de Instagram a la red, consulte [Acerca de las cuentas de Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)
Desactivar las emisiones de Instagram que no utilice
Asegúrese de que los flujos estén dirigidos con las palabras clave correctas y utilice filtros de etiquetas inteligentes para que las consultas sean más precisas. Para obtener información sobre cómo utilizar los filtros de etiquetas inteligentes, consulte [Etiquetas inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md)
Minimice las veces que varias personas utilizan la misma cuenta de Instagram en una red para depurar contenido de Instagram.
