---
description: Notas de la versión de la versión del 15 de noviembre de 2018.
seo-description: Notas de la versión de la versión del 15 de noviembre de 2018.
seo-title: Notas de la versión
solution: Experience Manager
title: Notas de la versión
uuid: 34e64943-dea6-46ac-9fcc-8febeab6aa42
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# Notas de la versión{#release-notes}

Notas de la versión de la versión del 15 de noviembre de 2018.

## Nuevas funciones {#section_syx_mdt_wcb}

En la versión de producción de esta versión se lanzaron las siguientes nuevas funciones:

* **Actualizaciones de la búsqueda y el flujo de Instagram.** Puede usar una cuenta *comercial de* Instagram para:

   * Realice una búsqueda social en Instagram por usuario (el usuario también debe ser una cuenta comercial de Instagram).

   * Cree flujos de Instagram a partir de una cuenta de usuario de Instagram específica (la cuenta también debe ser una cuenta comercial), incluida la suya propia.

   * Solicite derechos para los recursos desde Instagram mediante un flujo de trabajo parcialmente automatizado.

   * Para obtener información sobre el tipo de cuentas de Instagram que necesita configurar y solicitar derechos de Instagram, consulte [Acerca de las cuentas](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)de Instagram.

* **Supervisión automática de las respuestas de solicitudes de derechos de uso para búsquedas basadas en cuentas comerciales.** Solo para búsquedas basadas en cuentas comerciales: está disponible la capacidad de supervisar automáticamente las respuestas a solicitudes de derechos y actualizar el historial de actividades en Livefyre.

Para obtener más información sobre cómo solicitar derechos para cuentas de Instagram, consulte [Enviar una solicitud de derechos de Instagram manualmente](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) y [Enviar una solicitud](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)de derechos de Instagram parcialmente automatizada.

* **Integración con Adobe Target.** Se ha añadido una integración con Adobe Target que le permite compartir aplicaciones de Livefyre directamente en la biblioteca de ofertas de Adobe Target. Para obtener más información sobre el uso de Livefyre con Adobe Target, consulte la documentación [de Target](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html).

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

### Versión de producción

| Tipo de incidencia | Componente | Nota de versión |
|--- |--- |--- |
| Problema | AppService:Identidad de Livefyre | Se corrigió un problema en el cual hacer clic en [! UICONTROL Restablecer como predeterminado] no restableció el logotipo en Modo de inicio de sesión en Estudio &gt; Ajustes de integración &gt; Identidad de Livefyre a la imagen predeterminada. |
| Problema | Biblioteca | Se corrigió un problema en el cual un vídeo cargado en la biblioteca y visualizado posteriormente con los detalles del recurso no se mostraba correctamente. |
| Problema | Flujos | Se ha corregido un problema que impedía que los productos se mostraran en una regla de flujo. |
| Problema | Flujos | Se corrigió un problema en el cual las etiquetas de producto no estaban disponibles para una regla de flujo. |
| Mejora | Studio | Se corrigió un problema en el cual el ID de producto no se mostraba en Livefyre Studio. |
| Problema | Estudio:ModQ | Se corrigió un problema en el cual el contenido eliminado seguía mostrándose en ModQ después de eliminarse. |

### Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Problema | Componente social:Carrusel | Se corrigió un problema en el cual el vínculo Compartir no respondía y copiaba la URL como se esperaba en IE11 y Mozilla Firefox. |