---
description: Qué esperar en la implementación de Livefyre Studio.
title: Proceso de implementación
exl-id: 82bf8c09-946a-4be8-97bf-5b9868a4e031
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 3%

---

# Proceso de implementación{#implementation-process}

La duración de la implementación de Livefyre depende de su implementación y del ámbito de trabajo.

## Descripción general de la arquitectura de red de Livefyre {#section_dgj_l32_rbb}

Livefyre utiliza los términos siguientes para tratar la arquitectura de red:

* Red. Dominio de nivel superior en el que planea utilizar Livefyre.
* Sitios. Un subdominio o sección de sitio que forma parte de la red.
* de iOS. Representación del contenido del sitio. El contenido se muestra en las aplicaciones visualmente mediante las aplicaciones de visualización (Mosaic, Carrusel, Feature Card, etc.) o en formato de texto, usando aplicaciones de conversación (comentarios, revisiones, chat, etc.). Puede colocar una o más aplicaciones en sus sitios.
* Transmisiones. Los flujos son filtros que buscan en medios sociales y otros sitios para recopilar contenido automáticamente para moderación o publicación directa en una aplicación.
* Contenido (por ejemplo, UGC, comentarios). Qué se muestra en las aplicaciones. El contenido puede ser visual (por ejemplo, una foto o un vídeo), solo audio o texto.

En el diagrama siguiente se muestra la relación entre Red, Sitios, Aplicaciones y Contenido.

![](assets/network_site_architecture.png)

Tiene su propia instancia de Livefyre, que es su panel central para moderar contenido, administrar usuarios y mucho más. Póngase en contacto con su CSM para obtener acceso a su instancia de Livefyre.

## Pasos para la integración {#section_s2j_d2x_tz}

Hay tres pasos principales para integrar Livefyre:

* Integración de aplicaciones

   Al implementar Livefyre, el estilo de implementación depende de su caso de uso. Para obtener [más información sobre cada tipo de implementación](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Integración de autenticación

   Debe integrar su sistema de administración de usuarios existente con Livefyre para aplicaciones de conversación y cualquier otra aplicación que requiera autenticación de usuarios finales en su sitio. Si actualmente no utiliza una herramienta de administración de usuarios, puede utilizar la identidad de Livefyre. Para obtener [más información sobre la identidad de Livefyre, qué es y cómo configurarla](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity).

* Personalización

   La personalización es opcional, pero la mayoría de los clientes personalizan las aplicaciones para adaptarse a su marca.
