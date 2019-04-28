---
description: Notas de la versión de la versión del 15 de noviembre de 2018.
seo-description: Notas de la versión de la versión del 15 de noviembre de 2018.
seo-title: Notas de la versión
solution: Experience Manager
title: Notas de la versión
uuid: 34 e 64943-dea 6-46 ac -9 fcc -8 febeab 6 aa 42
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# Notas de la versión{#release-notes}

Notas de la versión de la versión del 15 de noviembre de 2018.

## Nuevas características {#section_syx_mdt_wcb}

Se han publicado las siguientes funciones nuevas en la versión de producción de esta versión:

* **Actualizaciones en la búsqueda y el flujo de Instagram.** Puede utilizar una *cuenta empresarial de Instagram* para:

   * Realice una búsqueda social de Instagram por usuario (el usuario debe ser una cuenta empresarial de Instagram).

   * Crear flujos Instagram desde una cuenta de usuario concreta de Instagram (la cuenta también debe ser una cuenta comercial), incluido su propio.

   * Solicite derechos para recursos desde Instagram mediante un flujo de trabajo parcialmente automatizado.

   * Para obtener información sobre el tipo de cuentas de Instagram que necesita para configurar y solicitar derechos de Instagram, consulte [Acerca de las cuentas de Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Supervisión automática de las respuestas de solicitud de derechos de uso para las búsquedas basadas en cuentas comerciales.** Solo para búsquedas basadas en cuentas comerciales—Se encuentra disponible la capacidad de monitorear automáticamente las respuestas a las solicitudes de derechos y actualizar el historial de actividades en Livefyre.

Para obtener más información sobre cómo solicitar derechos de cuentas de Instagram, consulte [Envío manual de derechos de Instagram](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) y [Envío de una solicitud de derechos de Instagram parcialmente automatizada](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Integración de Adobe Target.** Integración añadida con Adobe Target permitiéndole compartir aplicaciones de Livefyre directamente en la biblioteca de ofertas de Adobe Target. Para obtener más información sobre el uso de Livefyre con Adobe Target, consulte [la documentación de Target](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html).

## Problemas {#section_ehw_ndt_wcb}

En esta versión se resolvieron los problemas de las tablas siguientes.

### Versión de producción

| Tipo de problema | Componente | Versión de la versión |
|--- |--- |--- |
| Problema | Appservice: Identidad de Livefyre | Se ha corregido un problema en el cual hacer clic [en UICONTROL Restablecer a predeterminado] no restablecía el logotipo en Login Modal en Studio &gt; Settings Settings &gt; Livefyre Identity con la imagen predeterminada. |
| Problema | Biblioteca | Se ha corregido un problema por el que un vídeo cargado a la biblioteca y luego visto en detalle de recurso no se mostraba correctamente. |
| Problema | Flujos | Se ha corregido un problema que impedía que los productos se mostraran en una regla de flujo. |
| Problema | Flujos | Se corrigió un problema en el cual las etiquetas de productos no estaban disponibles para una regla de flujo. |
| Mejora | Studio | Se corrigió un problema en el cual el ID de producto no se mostraba en Livefyre Studio. |
| Problema | Estudio: Modq | Se corrigió un problema en el cual el contenido eliminado aún se mostraba en modq después de eliminarlo. |

### Versión de UAT

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Problema | Componente Social: Carrusel | Se corrigió un problema en el cual el vínculo Compartir no respondía y copió la URL como se espera en IE 11 y Mozilla Firefox. |