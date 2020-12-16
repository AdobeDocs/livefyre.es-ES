---
description: Qué esperar de la implementación de Livefyre Studio.
seo-description: Qué esperar de la implementación de Livefyre Studio.
seo-title: Proceso de implementación
solution: Experience Manager
title: Proceso de implementación
uuid: 9a0f394e-3467-47d1-9816-45e2130db440
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 3%

---


# Proceso de implementación{#implementation-process}

La duración de la implementación de Livefyre depende de la implementación y del alcance del trabajo.

## Visión General de la Arquitectura de Red Livefyre {#section_dgj_l32_rbb}

Livefyre utiliza los siguientes términos para discutir la arquitectura de red:

* Red. Dominio de nivel superior en el que planea usar Livefyre.
* Sitios. Un subdominio o una sección del sitio que forma parte de la red.
* de iOS. Representación del contenido del sitio. El contenido se muestra visualmente en las aplicaciones mediante las aplicaciones de visualización (mosaico, carrusel, tarjeta de características, etc.) o en formato de texto, mediante aplicaciones de conversación (comentarios, críticas, chat, etc.). Puede colocar una o más aplicaciones en sus sitios.
* Flujos. Los flujos son filtros que buscan en los medios sociales y otros sitios para recopilar contenido automáticamente para moderación o publicación directa en una aplicación.
* Contenido (por ejemplo, UGC, comentarios). Qué se muestra en las aplicaciones. El contenido puede ser visual (por ejemplo, una fotografía o un vídeo), solo audio o texto.

El siguiente diagrama muestra la relación entre la red, los sitios, las aplicaciones y el contenido.

![](assets/network_site_architecture.png)

Tiene su propia instancia de Livefyre, que es su panel central para moderar contenido, administrar usuarios y mucho más. Póngase en contacto con su CSM para obtener acceso a su instancia de Livefyre.

## Pasos para la integración {#section_s2j_d2x_tz}

Hay tres pasos principales para integrar Livefyre:

* Integración de aplicaciones

   Al implementar Livefyre, el estilo de implementación depende del caso de uso. Para [más sobre cada tipo de implementación](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Integración de autenticación

   Debe integrar el sistema de administración de usuarios existente con Livefyre para las aplicaciones de conversación y cualquier otra aplicación que requiera autenticación de usuario final en el sitio. Si actualmente no utiliza una herramienta de administración de usuarios, puede utilizar la Identidad de Livefyre. Para [más información sobre la identidad de Livefyre, qué es y cómo configurarla](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity).

* Personalización

   La personalización es opcional, pero la mayoría de los clientes personalizan las aplicaciones para adaptarse a su marca.

