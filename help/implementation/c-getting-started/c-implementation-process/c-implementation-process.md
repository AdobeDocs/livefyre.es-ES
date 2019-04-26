---
description: Qué esperar al implementar Livefyre Studio.
seo-description: Qué esperar al implementar Livefyre Studio.
seo-title: Proceso de implementación
solution: Experience Manager
title: Proceso de implementación
uuid: 9 a 0 f 394 e -3467-47 d 1-9816-45 e 2130 db 440
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Proceso de implementación{#implementation-process}

El período de tiempo para implementar Livefyre depende de su implementación y alcance de trabajo.

## Descripción general de la arquitectura de red de Livefyre {#section_dgj_l32_rbb}

Livefyre usa los siguientes términos para analizar la arquitectura de red:

* Red. Dominio de nivel superior en el que planea utilizar Livefyre.
* Sitios. Subdominio o sección del sitio que forma parte de la red.
* Aplicaciones. Representación de contenido en el sitio. El contenido se muestra en aplicaciones visualmente, mediante Aplicaciones de visualización (Mosaico, Carrusel, Tarjeta de funciones, etc.) o en formato de texto, usar aplicaciones de conversación (comentarios, revisiones, chat, etc.). Puede colocar una o más aplicaciones en sus sitios.
* Flujos. Los flujos son filtros que buscan medios sociales y otros sitios para recopilar contenido automáticamente para moderación o publicación directa en una aplicación.
* Contenido (por ejemplo, UGC, comentarios). Qué se muestra en las aplicaciones. El contenido puede ser visual (por ejemplo, una foto o vídeo), solo audio o texto.

El siguiente diagrama muestra la relación entre Red, Sitios, Aplicaciones y Contenido.

![](assets/network_site_architecture.png)

Su propia instancia de Livefyre es su tablero central para moderar contenido, administrar usuarios y mucho más. Póngase en contacto con su CSM para obtener acceso a su instancia de Livefyre.

## Pasos de integración {#section_s2j_d2x_tz}

Existen tres pasos principales para integrar Livefyre:

* Integración de aplicaciones

   Cuando implemente Livefyre, el estilo de implementación depende del caso de uso. Para [obtener más información sobre cada tipo de implementación](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Integración de autenticación

   Debe integrar el sistema de administración de usuarios existente con Livefyre para las aplicaciones de conversación y cualquier otra aplicación que requiera autenticación de usuario final en el sitio. Si actualmente no utiliza ninguna herramienta de administración de usuarios, puede utilizar la identidad de Livefyre. Para [obtener más información sobre la identidad de Livefyre, qué es y cómo configurarlo](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity).

* Personalización

   La personalización es opcional, pero la mayoría de los clientes personalizan aplicaciones para adaptarse a su marca.

