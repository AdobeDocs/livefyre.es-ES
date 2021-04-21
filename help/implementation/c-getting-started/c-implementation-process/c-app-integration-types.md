---
description: Al implementar aplicaciones de Livefyre, el estilo de implementación depende de su caso de uso. En esta página se explican las funciones de las tres formas de crear una aplicación.
title: Integraciones de aplicaciones CMS
exl-id: 7590e247-87cc-470e-bab6-e61a19221dbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# Integraciones de aplicaciones CMS{#cms-app-integrations}

Al implementar aplicaciones de Livefyre, el estilo de implementación depende de su caso de uso. En esta página se explican las funciones de las tres formas de crear una aplicación.

La integración de Livefyre no es compatible con ninguna plataforma CMS y de perfil de usuario y autenticación. Implemente Livefyre de una o varias formas, según su caso de uso y sus requisitos.

Puede utilizar la integración tradicional para crear componentes de AEM personalizados.

## Información general sobre el tipo de integración de aplicaciones CMS

| Tipo | Requisito de desarrollo | Funciones | Pros | Limitaciones |
|--- |--- |--- |--- |--- |
| Diseñador de aplicaciones | Muy bajo | Cree incrustaciones de JS en Studio para agregarlas a páginas sin un desarrollador <br>Estilo limitado y configuraciones disponibles </br>Caso de uso: Páginas de un solo uso (cobertura de eventos, campañas, centros) | Capacidad para poner en marcha una aplicación en un corto periodo de tiempo. <br>Las configuraciones pueden realizarlas miembros no técnicos. <br>Cambios sencillos sobre la marcha en las configuraciones | Debe crear primero una aplicación con Livefyre Studio <br>No está automatizada |
| Livefyre.js | Medio | Integración de aplicaciones en el JavaScript de sus páginas <br>Caso de uso: Plantillas reutilizables (contenido editorial, revisiones de productos) | Utilice el conjunto completo de personalizaciones y configuraciones de aplicación <br>Automatiza el proceso para crear instancias de aplicaciones de forma dinámica desde el CMS en las páginas | Se necesita un desarrollador por adelantado. |
| API de SDK | Advanced | Recupere el contenido de Livefyre para utilizarlo en aplicaciones personalizadas <br>Personalice el front-end más allá de la oferta compatible <br>Caso de uso: Integraciones de datos y análisis y aplicaciones front-end personalizadas | Potencia total sobre la apariencia de la aplicación | Requiere desarrollo por adelantado. <br>Mayor nivel de esfuerzo de desarrollo para implementar. |
