---
description: Puede crear reglas de flujo que extraigan contenido de Correo electrónico.
seo-description: Puede crear reglas de flujo que extraigan contenido de Correo electrónico.
seo-title: Reglas de correo electrónico
solution: Experience Manager
title: Reglas de correo electrónico
uuid: 3 cd 27 d 28-b 7 c 0-4 cbc-bae 3-e 2 ef 7 beacba 9
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Reglas de correo electrónico{#email-rules}

Puede crear reglas de flujo que extraigan contenido de Correo electrónico.

Creación de flujos basados en correo electrónico permite publicar contenido directamente en una aplicación o carpeta por correo electrónico.

Utilice esta función para permitir que los colaboradores anuncien directamente en sus aplicaciones o en la biblioteca de recursos desde sus equipos o dispositivos móviles.

Una vez creada la regla, cualquier mensaje de correo electrónico que contenga una imagen o un archivo de vídeo enviado a la dirección de correo electrónico enumerada se publicará directamente en la biblioteca de recursos o aplicaciones, según se especifica. Los correos electrónicos enviados con varios archivos adjuntos anunciarán todos los archivos en la ubicación adecuada. Los correos electrónicos enviados a la dirección que contenga sólo texto no harán nada.

Una vez enviados, los campos del mensaje de correo electrónico se utilizarán para rellenar los siguientes elementos para el fragmento de contenido:

* **[!UICONTROL From:]** Se utiliza como autor del contenido, si existe la cuenta de usuario. Si no existe ninguna cuenta para el remitente, el autor aparece como anónimo.
* **[!UICONTROL Subject:]** Se utiliza para el título del contenido.
* **[!UICONTROL Body:]** Se utiliza para rellenar los detalles del contenido en Studio.
* **[!UICONTROL Attachments:]** Los archivos multimedia deben adjuntarse o se ignorará el correo electrónico. Entre los tipos de archivos compatibles se incluyen 3 GP, ASF, AVI, DV, GIF, JPG, MOV, MP 4, MPEG, MPG, PNG, QT y WMV. El total de todos los archivos adjuntos debe tener por debajo de 25 MB.

Para obtener más opciones de reglas de flujo para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
