---
description: Al implementar aplicaciones de Livefyre, el estilo de implementación
  depende del caso de uso. Esta página explica las funciones de las tres maneras de
  crear una aplicación.
seo-description: Al implementar aplicaciones de Livefyre, el estilo de implementación
  depende del caso de uso. Esta página explica las funciones de las tres maneras de
  crear una aplicación.
seo-title: Integraciones de aplicaciones CMS
solution: Experience Manager
title: Integraciones de aplicaciones CMS
uuid: 14 fd 7 e 36-0 e 50-4 ae 3-97 f 0-2 de 731 c 184 f 5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Integraciones de aplicaciones CMS{#cms-app-integrations}

Al implementar aplicaciones de Livefyre, el estilo de implementación depende del caso de uso. Esta página explica las funciones de las tres maneras de crear una aplicación.

La integración de Livefyre es indiferente a cualquier CMS, perfil de usuario y plataforma de autenticación. Implemente Livefyre de una o varias formas, según su uso y sus requisitos.

Puede utilizar la integración tradicional para crear componentes personalizados de AEM.

## Información general sobre el tipo de integración de aplicaciones CMS

| Tipo | Requisito de desarrollo | Funciones | Pros | Limitaciones |
|--- |--- |--- |--- |--- |
| App Designer | Muy bajo | Crear JS incrusta en Studio para agregarlo a páginas sin necesidad de un desarrollador <br>limitado y configuraciones disponibles </br>de uso: Páginas de uso único (cobertura de eventos, campañas, hubs) | Capacidad para poner una aplicación en marcha en un período de tiempo corto. <br>Las configuraciones pueden realizarlo un miembro no técnico. <br>Es fácil realizar cambios en la marcha | Debe crear una aplicación con Livefyre Studio primero <br>NO AUTOMATIZADO |
| Livefyre. js | Medio | Integre aplicaciones en el JavaScript del caso <br>de uso de páginas: Plantillas reutilizables (contenido editorial, revisiones de productos) | Utilice el conjunto completo de configuraciones y configuraciones <br>de la aplicación automatiza el proceso para crear instancias dinámicas de aplicaciones desde el CMS en sus páginas. | Need a developer up front. |
| API de SDK | Avanzado | Recupere el contenido de Livefyre para utilizarlo para aplicaciones personalizadas <br>Personalizar el front-end más allá de la oferta admitida en caso <br>de uso: Integraciones de datos/análisis y aplicaciones de front-end personalizadas | Potencia completa sobre el aspecto y la presentación de la aplicación | Requiere de desarrollo hacia arriba. <br>Nivel más alto de esfuerzo dev para implementar. |
