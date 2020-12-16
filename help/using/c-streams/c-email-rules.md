---
description: Puede crear reglas de flujo que extraigan contenido del correo electrónico.
seo-description: Puede crear reglas de flujo que extraigan contenido del correo electrónico.
seo-title: reglas de correo electrónico
solution: Experience Manager
title: reglas de correo electrónico
uuid: 3cd27d28-b7c0-4cbc-bae3-e2ef7beacba9
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# reglas de correo electrónico{#email-rules}

Puede crear reglas de flujo que extraigan contenido del correo electrónico.

La creación de flujos basados en correo electrónico le permite anunciar contenido directamente en una aplicación o carpeta por correo electrónico.

Utilice esta función para permitir que los colaboradores publiquen directamente en las aplicaciones o en la biblioteca de recursos desde su ordenador o dispositivo móvil.

Una vez creada la regla, cualquier correo electrónico que contenga una imagen o un archivo de vídeo enviado a la dirección de correo electrónico de la lista se publicará directamente en la aplicación o biblioteca de recursos, según se especifique. Los correos electrónicos enviados con varios archivos adjuntos anunciarán todos los archivos en la ubicación adecuada. Los mensajes de correo electrónico enviados a la dirección de la lista que contenga solo texto no harán nada.

Una vez enviados, los campos del correo electrónico se utilizarán para rellenar los siguientes elementos para el contenido:

* **[!UICONTROL From:]** Se utiliza como autor del contenido, si existe la cuenta de usuario. Si no existe ninguna cuenta para el remitente, el autor se muestra como anónimo.
* **[!UICONTROL Subject:]** Se utiliza para el título del contenido.
* **[!UICONTROL Body:]** Se utiliza para rellenar los detalles de contenido en Studio.
* **[!UICONTROL Attachments:]** Los archivos multimedia deben adjuntarse o se omitirá el correo electrónico. Los tipos de archivo admitidos son 3GP, ASF, AVI, DV, GIF, JPG, MOV, MP4, MPEG, MPG, PNG, QT y WMV. El total de todos los archivos adjuntos debe ser inferior a 25 MB.

Para obtener opciones de regla de flujo adicionales para todas las reglas de flujo, consulte [Opciones de regla de flujo para todas las reglas de flujo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
