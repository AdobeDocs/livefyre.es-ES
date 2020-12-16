---
description: Ejecute pruebas de resistencia contra la plataforma Livefyre.
seo-description: Ejecute pruebas de resistencia contra la plataforma Livefyre.
seo-title: Directiva de prueba de esfuerzo
solution: Experience Manager
title: Directiva de prueba de esfuerzo
uuid: f2d49b55-f4fc-485f-9aea-a17ce64813ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---


# Directiva de prueba de estrés{#stress-test-policy}

Ejecute pruebas de resistencia contra la plataforma Livefyre.

Este documento proporciona directrices sobre la ejecución de pruebas de resistencia contra la plataforma Livefyre. Las pruebas ad hoc realizadas por clientes sin notificación están estrictamente prohibidas. Para obtener más información sobre [actividades prohibidas y permitidas](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Las pruebas de estrés son opcionales. No es necesario o se espera que realice una prueba de estrés. Adobe Livefyre realiza pruebas de resistencia y validaciones periódicas como parte del proceso de liberación. Si decide ejecutar pruebas, este documento describe los requisitos y las limitaciones para realizar pruebas de resistencia.

## Notificación {#section_ihs_bfz_vdb}

Debe notificar a su especialista en éxito del cliente de Livefyre y al consultor técnico del Adobe acerca de las pruebas planificadas con tres o más semanas de anticipación de cuándo planea realizar el inicio.

Para notificar a Livefyre, envíe la siguiente información a su especialista en éxito de clientes de Livefyre y al consultor técnico de Adobe:

* Finalidad y descripción del ensayo
* Caso de uso con el que está probando
* Lista de cualquier API de Livefyre que planee utilizar en la prueba
* Fecha, hora y duración de la prueba
* Direcciones IP desde las cuales se iniciarán las pruebas

## Requisitos {#section_khs_bfz_vdb}

Sólo puede realizar pruebas si cumplen los siguientes requisitos:

* Debe recibir la aprobación explícita y por escrito de un consultor técnico de Adobe 3 semanas o más antes de comenzar la prueba.
* **Sólo puede realizar pruebas en la red UAT.**
* Debe realizar pruebas con escenarios realistas. Por ejemplo: no puede suponer que su propiedad vaya a atender *millones* de solicitudes de anuncios todos los días, porque no es un escenario realista. Si necesita ayuda para determinar si su escenario es realista o no, pregunte a su especialista en éxito para el cliente de Livefyre o al consultor técnico de Adobe.
* Las pruebas deben realizarse durante el horario laboral del huso horario estándar del Pacífico \(UTC -7\).
* Es posible que necesite producir datos y sus motivos para la prueba.

## Gobierno {#section_mhs_bfz_vdb}

Livefyre se reserva el derecho de finalizar una prueba en cualquier momento si realiza una prueba:

* En la red de producción.
* Sin la aprobación explícita y por escrito de un consultor técnico Adobe con tres semanas o más de antelación.
* Contra escenarios irreales.

Livefyre finaliza las pruebas bloqueando el acceso a las API, desactivando las redes Livefyre y rechazando una solicitud de prueba de carga si no cumple los requisitos.
