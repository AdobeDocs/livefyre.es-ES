---
description: Añada el indicador userPrivacyOptOut a la página para permitir que un visitante del sitio exclusión este seguimiento.
seo-description: Añada el indicador userPrivacyOptOut a la página para permitir que un visitante del sitio exclusión este seguimiento.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# userPrivacyOptOut{#userprivacyoptout}

Añada el indicador `userPrivacyOptOut` a la página para permitir que un visitante del sitio exclusión este seguimiento.

Livefyre proporciona eventos de JavaScript para rastrear la actividad de los usuarios en sus aplicaciones de Livefyre.

Si incrusta aplicaciones de Livefyre y un visitante no consiente en realizar el seguimiento, puede configurar de forma dinámica Livefyre para deshabilitar la funcionalidad y garantizar la privacidad del visitante.

Cuando se configura, Livefyre:

* Deshabilite la compatibilidad con la autenticación en las aplicaciones.
* Deshabilitar Livecount y la generación de eventos
* Elimine las cookies existentes creadas por cualquier aplicación que se encuentre en la página
* Medios proxy con imágenes de dominios de terceros para evitar que terceros creen cookies
* Activar pulsaciones de máscara de vídeo para vídeos de terceros que requieran un clic adicional en la vista

## Configurar una página para la exclusión

Las integraciones que incrustan aplicaciones de Livefyre pueden configurar Livefyre cuando un visitante del sitio no ha concedido el consentimiento mediante una sola variable de JavaScript.

Instrucciones:

1. Añada el indicador `userPrivacyOptOut` a la página antes del JavaScript `Livefyre.js`:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Añada `Livefyre.js` a la página en cualquier lugar después de `userPrivacyOptOut`.

   Las aplicaciones de Livefyre crean instancias con la configuración de privacidad elevada.

   >[!NOTE]
   >
   >No cambie el valor de `userPrivacyOptOut` una vez cargadas las aplicaciones de Livefyre.

Asegúrese de que el flujo de trabajo de consentimiento establezca `userPrivacyOptOut` en true si un visitante del sitio decide exclusión.
