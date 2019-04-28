---
description: Respuestas a preguntas más frecuentes sobre solicitudes de privacidad para RDPD.
seo-description: Respuestas a preguntas más frecuentes sobre solicitudes de privacidad para RDPD.
seo-title: Preguntas frecuentes sobre solicitud de privacidad
solution: Experience Manager
title: Preguntas frecuentes sobre solicitud de privacidad
uuid: 0 cd 6 f 0 d 2-504 d -46 e 9-ac 46-070536 cda 086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Preguntas frecuentes sobre solicitud de privacidad{#privacy-request-faqs}

Respuestas a preguntas más frecuentes sobre solicitudes de privacidad para RDPD.

* **¿Cómo pueden desactivar los visitantes el seguimiento en un sitio que utiliza aplicaciones de Livefyre?** Cuando un visitante del sitio opta por una renuncia, la implementación del cliente debe indicar a Livefyre que el usuario ha optado por la desactivación de una aplicación. Livefyre has created a way to do this with the JavaScript option, `userPrivacyOptOut`. Para obtener más información sobre cómo utilizar `userPrivacyOptOut`, consulte [userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Cuando `userPrivacyOptOut` el indicador se establece en true, cualquier aplicación de la página no transmitirá datos a los servidores de Livefyre mediante cookies u otro método. Luego, Livefyre no actualizará el almacenamiento local con datos que podrían utilizarse para rastrear a los visitantes del sitio. Si un origen no admite un proxy, Livefyre muestra una máscara en el contenido a menos que un usuario haga clic en el vídeo y apruebe el seguimiento potencial de ese origen.

   Si utiliza la identidad de Livefyre, los usuarios pueden eliminar su perfil o crear un informe de los datos rastreados para su cuenta de usuario.

* **¿Cómo evito la recopilación de contenido futuro de un visitante del sitio que no haya optado por la exclusión?** Utilice `userPrivacyOptOut` en `livefyre.js` una página web que utilice aplicaciones de Livefyre. Para obtener más información, `userPrivacyOptOut`consulte [userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **¿Cómo genero un informe y elimino los datos de los usuarios de la aplicación o los propietarios de cuentas sociales?**[Solicitudes de privacidad](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para generar un informe y eliminar datos de usuarios de Aplicaciones.

* **¿Cómo elimino todo el contenido de un visitante?** Livefyre no mantiene información persistente sobre los visitantes del sitio, excepto en forma de cookies para identificarlas de forma única para las funciones Livecount. Livecount es un recuento temporal y temporal de los visitantes del sitio. No se mantiene ningún historial después de que el visitante abandone o borre las cookies.

   Cree una [solicitud de privacidad](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para eliminar la cuenta. Livefyre elimina o hace que el perfil de usuario y los registros asociados sean anónimos.

* **¿Cómo elimino contenido de un usuario registrado?** Cree una [solicitud](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) de privacidad para eliminar la cuenta. El perfil de usuario y los registros asociados se destruirán completamente.

   >[!NOTE]
   >
   >Esta acción no se puede deshacer.

* **¿Cómo se produce un informe de los datos rastreados por un empleado actual o antiguo?**[Vea un informe de privacidad](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) para generar un informe de los datos rastreados para una cuenta de usuario.

* **¿Es compatible el flujo social de Livefyre?** Cuando un usuario elimina una publicación o tweet de su red social, en las 24 horas el contenido también se elimina de todas las fuentes de Livefyre. Esto se aplica a Twitter y Facebook.

