---
description: Agregue el indicador userprivacyoptout a la página para permitir que
  un visitante del sitio desactive este seguimiento.
seo-description: Agregue el indicador userprivacyoptout a la página para permitir
  que un visitante del sitio desactive este seguimiento.
seo-title: Userprivacyoptout
title: Userprivacyoptout
uuid: a 043 c 50 e -0 a 02-4 c 83-bbce -54 b 9 b 51316 a 5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacyoptout{#userprivacyoptout}

Agregue `userPrivacyOptOut` el indicador a la página para permitir que un visitante del sitio desactive este seguimiento.

Livefyre proporciona eventos de JavaScript para rastrear la actividad de los usuarios en sus aplicaciones de Livefyre.

Si incrusta aplicaciones de Livefyre y un visitante no aprueba el seguimiento, puede configurar de forma dinámica Livefyre para deshabilitar la funcionalidad a fin de garantizar la privacidad del visitante.

Cuando se configure, Livefyre:

* Deshabilitar la compatibilidad de autenticación en Aplicaciones.
* Deshabilitar la generación de Livecount y eventos
* Eliminar las cookies existentes creadas por cualquier aplicación que se encuentre en la página
* Medios proxy con imágenes de dominios de terceros para impedir que terceros creen cookies
* Habilitar la pulsación de máscara de vídeo para vídeos de terceros que requieran un clic adicional para ver

## Configurar una página para la exclusión

Las integraciones que incorporan aplicaciones de Livefyre pueden configurar Livefyre cuando un visitante del sitio no ha concedido el consentimiento mediante una sola variable JavaScript.

Instrucciones:

1. Agregue `userPrivacyOptOut` el indicador a la página antes del `Livefyre.js` JavaScript:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Add `Livefyre.js` to the page anywhere after `userPrivacyOptOut`.

   Las aplicaciones de Livefyre crean una instancia con la configuración de privacidad elevada.

   >[!NOTE]
   >
   >No cambie el valor de `userPrivacyOptOut` una vez que se hayan cargado las aplicaciones de Livefyre.

Asegúrese de que el flujo de trabajo de consentimiento establezca el `userPrivacyOptOut` valor true si un visitante del sitio elige desactivar la opción.
