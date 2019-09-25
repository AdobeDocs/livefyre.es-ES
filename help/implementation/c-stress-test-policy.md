---
description: Ejecute pruebas de resistencia contra la plataforma Livefyre.
seo-description: Ejecute pruebas de resistencia contra la plataforma Livefyre.
seo-title: Directiva de prueba de esfuerzo
solution: Experience Manager
title: Directiva de prueba de esfuerzo
uuid: f2d49b55-f4fc-485f-9aea-a17ce64813ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Directiva de prueba de esfuerzo{#stress-test-policy}

Ejecute pruebas de resistencia contra la plataforma Livefyre.

Este documento proporciona instrucciones sobre cómo ejecutar pruebas de resistencia contra la plataforma Livefyre. Las pruebas ad hoc realizadas por clientes sin notificación están estrictamente prohibidas. Para más información sobre actividades [](#c_stress_test_policy/section_mhs_bfz_vdb)prohibidas y permitidas.

>[!NOTE]
>
>Las pruebas de estrés son opcionales. No es necesario o se espera que realice una prueba de estrés. Adobe Livefyre realiza pruebas de resistencia y validaciones periódicas como parte del proceso de lanzamiento. Si decide ejecutar pruebas, este documento describe los requisitos y las restricciones para realizar pruebas de resistencia.

## Notificación {#section_ihs_bfz_vdb}

Debe notificar a su especialista en éxito para clientes de Livefyre y al consultor técnico de Adobe acerca de las pruebas planificadas con tres o más semanas de anticipación del momento en que tiene previsto comenzar.

Para notificar a Livefyre, envíe la siguiente información a su especialista en éxito para clientes de Livefyre y al consultor técnico de Adobe:

* Finalidad y descripción del ensayo
* Caso de uso con el que está probando
* Lista de todas las API de Livefyre que planea utilizar en la prueba
* Fecha, hora y duración de la prueba
* Direcciones IP desde las cuales iniciará las pruebas

## Requisitos {#section_khs_bfz_vdb}

Sólo puede realizar pruebas si cumplen los siguientes requisitos:

* Debe recibir la aprobación explícita y por escrito de un consultor técnico de Adobe 3 semanas o más antes de comenzar la prueba.
* **Sólo puede realizar pruebas en la red UAT.**
* Debe realizar pruebas con escenarios realistas. Por ejemplo, puede que no suponga que su propiedad atenderá *millones* de solicitudes de anuncios todos los días, ya que no se trata de un escenario realista. Si necesita ayuda para determinar si su escenario es realista o no, pregunte a su especialista en éxito para clientes de Livefyre o al consultor técnico de Adobe.
* Las pruebas deben realizarse durante el horario laboral del huso horario estándar del Pacífico \(UTC -7\).
* Es posible que necesite producir datos y sus motivos para la prueba.

## Gobernanza {#section_mhs_bfz_vdb}

Livefyre se reserva el derecho de finalizar una prueba en cualquier momento si realiza una prueba:

* En la red de producción.
* Sin la aprobación explícita y por escrito de un consultor técnico de Adobe con tres semanas o más de antelación.
* Contra escenarios irreales.

Livefyre finaliza las pruebas bloqueando el acceso a las API, desactivando las redes Livefyre y rechazando una solicitud de prueba de carga si no cumple los requisitos.
