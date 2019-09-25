---
description: Agregue el indicador userPrivacyOptOut a la página para permitir que un visitante del sitio pueda desactivar este seguimiento.
seo-description: Agregue el indicador userPrivacyOptOut a la página para permitir que un visitante del sitio pueda desactivar este seguimiento.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyOptOut{#userprivacyoptout}

Agregue el `userPrivacyOptOut` indicador a la página para permitir a un visitante del sitio desactivar este seguimiento.

Livefyre proporciona eventos de JavaScript para rastrear la actividad de los usuarios en sus aplicaciones de Livefyre.

Si incrusta las aplicaciones de Livefyre y un visitante no consiente en realizar el seguimiento, puede configurar de forma dinámica Livefyre para deshabilitar la funcionalidad y garantizar la privacidad del visitante.

Cuando se configura, Livefyre:

* Deshabilite la compatibilidad con la autenticación en las aplicaciones.
* Deshabilitar Livecount y generación de eventos
* Eliminar las cookies existentes creadas por cualquier aplicación que se encuentre en la página
* Medios proxy con imágenes de dominios de terceros para evitar que terceros creen cookies
* Activar pulsaciones de máscara de vídeo para vídeos de terceros que requieran un clic adicional para ver

## Configurar una página para la exclusión

Las integraciones que incrustan aplicaciones de Livefyre pueden configurar Livefyre cuando un visitante del sitio no ha concedido el consentimiento mediante una sola variable de JavaScript.

Instrucciones:

1. Agregue el `userPrivacyOptOut` indicador a la página antes del `Livefyre.js` JavaScript:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Agregue `Livefyre.js` a la página en cualquier lugar después de `userPrivacyOptOut`.

   Las aplicaciones de Livefyre crean instancias con la configuración de privacidad elevada.

   >[!NOTE]
   >
   >No cambie el valor de una `userPrivacyOptOut` vez cargadas las aplicaciones de Livefyre.

Asegúrese de que el flujo de trabajo de consentimiento establezca el valor `userPrivacyOptOut` en true si un visitante del sitio decide desactivar la opción.
