---
description: Respuestas a las preguntas más frecuentes sobre las solicitudes de privacidad preparadas para el RGPD.
seo-description: Respuestas a las preguntas más frecuentes sobre las solicitudes de privacidad preparadas para el RGPD.
seo-title: Preguntas más frecuentes sobre la solicitud de privacidad
solution: Experience Manager
title: Preguntas más frecuentes sobre la solicitud de privacidad
uuid: 0cd6f0d2-504d-46e9-ac46-070536cda086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 1%

---


# Preguntas más frecuentes sobre la solicitud de privacidad{#privacy-request-faqs}

Respuestas a las preguntas más frecuentes sobre las solicitudes de privacidad preparadas para el RGPD.

* **¿Cómo pueden los visitantes del sitio exclusión el seguimiento en un sitio que utiliza aplicaciones de Livefyre?** Cuando exclusión un visitante del sitio, la implementación del cliente debe indicar a Livefyre que el usuario ha exclusión antes de crear una instancia de una aplicación. Livefyre ha creado una manera de hacerlo con la opción JavaScript, `userPrivacyOptOut`. Para obtener más información sobre cómo utilizar `userPrivacyOptOut`, consulte [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Cuando el indicador `userPrivacyOptOut` se establece en true, las aplicaciones de la página no transmitirán datos a los servidores Livefyre mediante cookies u otro método. Livefyre no actualizará el almacenamiento local con datos que se puedan usar para rastrear visitantes del sitio. Si una fuente no admite un proxy, Livefyre muestra una máscara en el contenido a menos que un usuario haga clic en el vídeo y apruebe el seguimiento potencial de esa fuente.

   Si utiliza la identidad de Livefyre, los usuarios pueden elegir eliminar su perfil o crear un informe de los datos rastreados para su cuenta de usuario.

* **¿Cómo evito recopilar contenido futuro de un visitante del sitio que ha exclusión?** Se utiliza  `userPrivacyOptOut` con  `livefyre.js` en una página web que utiliza aplicaciones de Livefyre. Para obtener más información sobre `userPrivacyOptOut`, consulte [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **¿Cómo genero un informe y elimino los datos de los usuarios de la aplicación o de los propietarios de cuentas sociales?** [Solicitudes de privacidad ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para generar un informe y eliminar datos de usuario de las aplicaciones.

* **¿Cómo elimino todo el contenido de un visitante?** Livefyre no mantiene la información persistente sobre los visitantes del sitio, excepto en forma de cookies para identificarlos de forma única para las características de Livefyre. Livecount es un recuento transitorio y en tiempo real de visitantes en el sitio. No se conserva ningún historial después de que el visitante abandone o borre las cookies.

   Cree [Solicitudes de privacidad](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para eliminar la cuenta. Livefyre elimina o hace que el perfil del usuario y los registros asociados sean anónimos.

* **¿Cómo elimino contenido para un usuario registrado?** Cree una  [solicitud de ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) privacidad para eliminar la cuenta. El perfil del usuario y los registros asociados se destruirán por completo.

   >[!NOTE]
   >
   >No se puede deshacer esta acción.

* **¿Cómo se produce un informe de los datos rastreados por un empleado actual o anterior?** [Vista de un ](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) informe de privacidad para generar un informe de los datos rastreados para una cuenta de usuario.

* **¿Es compatible el flujo social de Livefyre?** Cuando un usuario elimina una publicación o un tweet de su red social, en un plazo de 24 horas el contenido también se elimina de todas las fuentes de Livefyre. Esto se aplica a Twitter y Facebook.

