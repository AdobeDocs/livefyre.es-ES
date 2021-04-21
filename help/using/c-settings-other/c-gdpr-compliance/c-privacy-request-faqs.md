---
description: Respuestas a las preguntas más frecuentes sobre las solicitudes de privacidad listas para RGPD.
title: Preguntas frecuentes sobre solicitudes de privacidad
exl-id: 6d0add45-589a-46d0-b15a-63a7599aad73
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 1%

---

# Preguntas frecuentes sobre solicitudes de privacidad{#privacy-request-faqs}

Respuestas a las preguntas más frecuentes sobre las solicitudes de privacidad listas para RGPD.

* **¿Cómo pueden los visitantes del sitio impedir el seguimiento en un sitio que usa aplicaciones de Livefyre?** Cuando el visitante de un sitio decide excluirse, la implementación del cliente debe indicar a Livefyre que el usuario ha excluido antes de crear una instancia de una aplicación. Livefyre ha creado una forma de hacerlo con la opción JavaScript, `userPrivacyOptOut`. Para obtener más información sobre cómo utilizar `userPrivacyOptOut`, consulte [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Cuando el indicador `userPrivacyOptOut` se establece en true, ninguna aplicación de la página transmitirá datos a los servidores de Livefyre mediante cookies u otro método. Livefyre no actualizará el almacenamiento local con datos que se puedan usar para realizar el seguimiento de los visitantes del sitio. Si una fuente no admite un proxy, Livefyre muestra una máscara en el contenido a menos que un usuario haga clic en el vídeo y apruebe el seguimiento potencial de dicha fuente.

   Si utiliza la identidad de Livefyre, los usuarios pueden optar por eliminar su perfil o crear un informe de datos rastreados para su cuenta de usuario.

* **¿Cómo evito recopilar contenido futuro de un visitante del sitio que ha excluido?** Use  `userPrivacyOptOut` con  `livefyre.js` en una página web que use aplicaciones de Livefyre. Para obtener más información sobre `userPrivacyOptOut`, consulte [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **¿Cómo genero un informe y elimino los datos de los usuarios de la aplicación o los propietarios de cuentas sociales?** [Solicitudes de privacidad ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para generar un informe y eliminar datos de usuario de aplicaciones.

* **¿Cómo elimino todo el contenido de un visitante?** Livefyre no mantiene la información persistente sobre los visitantes del sitio, excepto en forma de cookies para identificarlos de forma única para las características de Livefyre. Livecount es un recuento transitorio y en tiempo real de visitantes en el sitio. No se conserva ningún historial después de que el visitante abandone o borre las cookies.

   Cree [Solicitudes de privacidad](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para eliminar la cuenta. Livefyre elimina o hace que el perfil de usuario y los registros asociados sean anónimos.

* **¿Cómo elimino contenido para un usuario registrado?** Cree una solicitud de  [privacidad ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para eliminar la cuenta. El perfil de usuario y los registros asociados se destruirán completamente.

   >[!NOTE]
   >
   >No se puede deshacer esta acción.

* **¿Cómo se produce un informe de datos rastreados por un empleado actual o anterior?** [Vea un ](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) informe de privacidad para generar un informe de los datos rastreados en una cuenta de usuario.

* **¿Es compatible el flujo social de Livefyre?** Cuando un usuario elimina un anuncio o tweet de su red social, en un plazo de 24 horas el contenido también se elimina de todas las fuentes de Livefyre. Esto se aplica a Twitter y Facebook.
