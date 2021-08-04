---
description: Notas de la versión de la versión del 15 de noviembre de 2018.
title: Notas de la versión
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
source-git-commit: beb224fdccf68c98fc3eff62b0867f22fa52902b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 6%

---

# Notas de la versión{#release-notes}

Notas de la versión de la versión del 15 de noviembre de 2018.

## Nuevas características {#section_syx_mdt_wcb}

En la versión de producción de esta versión se lanzaron las siguientes funciones nuevas:

* **Actualizaciones de la búsqueda y el flujo de Instagram.** Puede utilizar una cuenta comercial de  *Instagram* para:

   * Realice una búsqueda social de Instagram por usuario (el usuario debe ser también una cuenta comercial de Instagram).

   * Cree emisiones de Instagram a partir de una cuenta de usuario específica de Instagram (la cuenta también debe ser una cuenta comercial), incluida la suya propia.

   * Solicite derechos para los recursos desde Instagram mediante un flujo de trabajo parcialmente automatizado.

   * Para obtener información sobre el tipo de cuentas de Instagram que debe configurar y solicitar derechos de Instagram, consulte [Acerca de las cuentas de Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Supervisión automática de las respuestas de solicitudes de derechos de uso para búsquedas basadas en cuentas comerciales.** Solo para búsquedas basadas en cuentas empresariales: está disponible la capacidad de supervisar automáticamente las respuestas a solicitudes de derechos y actualizar el historial de actividades en Livefyre.

Para obtener más información sobre cómo solicitar derechos para cuentas de Instagram, consulte [Enviar solicitud de derechos de Instagram manualmente](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) y [Enviar una solicitud de derechos de Instagram parcialmente automatizada](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Integración con Adobe Target.** Se ha agregado integración con Adobe Target que le permite compartir aplicaciones de Livefyre directamente con la biblioteca de ofertas de Adobe Target. Para obtener más información sobre el uso de Livefyre con Adobe Target, consulte [Documentación de Target](https://experienceleague.adobe.com/docs/livefyre/using/library/livefyre-target.html).

## Problemas {#section_ehw_ndt_wcb}

Los problemas de las tablas siguientes se resolvieron en esta versión.

### Versión de producción

| Tipo de incidencia | Componente | Nota de la versión |
|--- |--- |--- |
| Problema | AppService: Identidad de Livefyre | Se ha corregido un problema en el cual al hacer clic en [!UICONTROL Reset to Default] no se restablecía el logotipo en el modo de inicio de sesión en Studio > Configuración de integración > Identidad de Livefyre a la imagen predeterminada. |
| Problema | Biblioteca | Se ha corregido un problema por el cual un vídeo cargado en la biblioteca y luego visualizado en detalle de recursos no se mostraba correctamente. |
| Problema | Transmisiones | Se ha corregido un problema que impedía que los productos se mostraran en una regla de flujo. |
| Problema | Transmisiones | Se ha corregido un problema en el cual las etiquetas de producto no estaban disponibles para una regla de flujo. |
| Mejora | Studio | Se ha corregido un problema por el cual el ID del producto no se mostraba en Livefyre Studio. |
| Problema | Estudio: ModQ | Se ha corregido un problema por el cual el contenido eliminado seguía mostrándose en ModQ después de eliminarse. |

### Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Problema | Componente social: Carrusel | Se ha corregido un problema en el cual el vínculo Compartir no respondía y copiaba la URL como se esperaba en IE11 y Mozilla Firefox. |
