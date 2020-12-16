---
description: Al implementar las aplicaciones de Livefyre, el estilo de implementación depende del caso de uso. En esta página se explican las características de las tres formas en que puede crear una aplicación.
seo-description: Al implementar las aplicaciones de Livefyre, el estilo de implementación depende del caso de uso. En esta página se explican las características de las tres formas en que puede crear una aplicación.
seo-title: Integraciones de aplicaciones de CMS
solution: Experience Manager
title: Integraciones de aplicaciones de CMS
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---


# Integraciones de aplicaciones de CMS{#cms-app-integrations}

Al implementar las aplicaciones de Livefyre, el estilo de implementación depende del caso de uso. En esta página se explican las características de las tres formas en que puede crear una aplicación.

La integración de Livefyre es independiente de cualquier plataforma de CMS y Perfil de usuarios y autenticación. Implemente Livefyre de una o varias maneras, según el caso de uso y los requisitos.

Puede utilizar la integración tradicional para crear componentes de AEM personalizados.

## Información general del tipo de integración de aplicaciones CMS

| Tipo | Requisito de desarrollo | Funciones | Pros | Limitaciones |
|--- |--- |--- |--- |--- |
| App Designer | Muy bajo | Cree incrustaciones de JS en Studio para agregarlas a páginas sin un <br>Diseño limitado y configuraciones disponibles </br>Caso de uso de desarrollador: Páginas de un solo uso (cobertura de evento, campañas, centros) | Capacidad para poner en marcha una aplicación en poco tiempo. <br>Las configuraciones las puede realizar un miembro no técnico. <br>Cambios sencillos sobre la marcha en las configuraciones | Debe crear una aplicación usando Livefyre Studio primero <br>No automatizado |
| Livefyre.js | Medio | Integrar aplicaciones en el JavaScript de las páginas <br>Caso de uso: Plantillas reutilizables (contenido editorial, revisiones de productos) | Utilice el grupo completo de personalizaciones y configuraciones de la aplicación <br>Automatiza el proceso para crear dinámicamente instancias de aplicaciones desde el CMS en las páginas | Se necesita un desarrollador por adelantado. |
| API de SDK | Advanced | Recupere el contenido de Livefyre para utilizarlo en aplicaciones personalizadas <br>Personalice el front-end más allá de la oferta admitida <br>Caso de uso: Integraciones de datos y análisis y aplicaciones de front-end personalizadas | Potencia total sobre el aspecto y la presentación de la aplicación | Requiere desarrollo por adelantado. <br>Mayor nivel de esfuerzo de desarrollo para implementar. |
