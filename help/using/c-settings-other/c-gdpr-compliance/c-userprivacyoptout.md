---
description: Agregue el indicador userPrivacyOptOut a la página para permitir que un visitante del sitio se excluya de este seguimiento.
title: userPrivacyOptOut
exl-id: 1e935e69-60af-4151-905c-93a1cccbeb49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# userPrivacyOptOut{#userprivacyoptout}

Agregue el indicador `userPrivacyOptOut` a la página para permitir que un visitante del sitio se excluya de este seguimiento.

Livefyre proporciona eventos de JavaScript para rastrear la actividad de los usuarios en sus aplicaciones de Livefyre.

Si incrusta aplicaciones de Livefyre y un visitante no da su consentimiento para realizar el seguimiento, puede configurar Livefyre de forma dinámica para deshabilitar la funcionalidad y garantizar la privacidad del visitante.

Cuando esté configurado, Livefyre:

* Deshabilite la compatibilidad con la autenticación en las aplicaciones.
* Desactivar Livecount y la generación de eventos
* Elimine las cookies existentes creadas por cualquier aplicación que se encuentre en la página
* Medios proxy con imágenes de dominios de terceros para evitar que terceros creen cookies
* Habilitar clics de máscara de vídeo para vídeos de terceros que requieran un clic adicional para ver

## Configurar una página para la exclusión

Las integraciones que incrustan aplicaciones de Livefyre pueden configurar Livefyre cuando el visitante de un sitio no ha concedido el consentimiento mediante una sola variable de JavaScript.

Instrucciones:

1. Agregue el indicador `userPrivacyOptOut` a la página antes del JavaScript `Livefyre.js`:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Agregue `Livefyre.js` a la página en cualquier lugar después de `userPrivacyOptOut`.

   Las aplicaciones de Livefyre crean instancias con la configuración de privacidad elevada.

   >[!NOTE]
   >
   >No cambie el valor de `userPrivacyOptOut` una vez que las aplicaciones de Livefyre se hayan cargado.

Asegúrese de que el flujo de trabajo de consentimiento establezca `userPrivacyOptOut` en true si el visitante del sitio decide excluirse.
