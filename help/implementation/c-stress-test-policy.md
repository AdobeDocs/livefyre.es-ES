---
description: Ejecute pruebas de estrés contra la plataforma Livefyre.
title: Política de prueba de estrés
exl-id: cb87b6ca-4107-46fc-9b1e-dc9399ec6d3a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Directiva de prueba de estrés{#stress-test-policy}

Ejecute pruebas de estrés contra la plataforma Livefyre.

Este documento proporciona instrucciones sobre la ejecución de pruebas de estrés contra la plataforma Livefyre. Las pruebas ad hoc por clientes sin notificación están estrictamente prohibidas. Para obtener más información sobre [actividades prohibidas y permitidas](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Las pruebas de estrés son opcionales. No es necesario o no se espera que realice una prueba de estrés. Adobe Livefyre realiza pruebas de resistencia y validaciones regulares como parte del proceso de liberación. Si decide ejecutar pruebas, este documento describe los requisitos y restricciones para realizar pruebas de estrés.

## Notificación {#section_ihs_bfz_vdb}

Debe notificar a su especialista en el éxito del cliente de Livefyre y al consultor técnico del Adobe de sus pruebas planificadas tres o más semanas antes de su inicio.

Para notificar a Livefyre, envíe la siguiente información a su especialista en éxito de los clientes de Livefyre y al consultor técnico de Adobe:

* Finalidad y descripción de la prueba
* El caso de uso con el que está probando
* Lista de cualquier API de Livefyre que planee usar en la prueba
* Fecha, hora y duración de la prueba
* Direcciones IP desde las que se iniciarán las pruebas

## Requisitos {#section_khs_bfz_vdb}

Solo puede realizar pruebas si cumplen los siguientes requisitos:

* Debe recibir la aprobación explícita y por escrito de un consultor técnico de Adobe 3 semanas o más antes de comenzar la prueba.
* **Sólo puede realizar pruebas en la red UAT.**
* Debe realizar pruebas con escenarios realistas. Por ejemplo, puede no suponer que su propiedad vaya a atender *millones* de solicitudes de publicación todos los días, porque este no es un escenario realista. Si necesita ayuda para determinar si su escenario es realista o no, pregunte a su especialista en éxito del cliente de Livefyre o a su consultor técnico de Adobe.
* Las pruebas deben realizarse durante el horario laboral para el huso horario estándar del Pacífico \(UTC -7\).
* Es posible que necesite producir datos y su razonamiento para la prueba.

## Administración {#section_mhs_bfz_vdb}

Livefyre se reserva el derecho de finalizar una prueba en cualquier momento si realiza una prueba:

* En la red de producción.
* Sin la aprobación explícita y por escrito de un consultor técnico Adobe con tres semanas o más de antelación.
* Contra escenarios irreales.

Livefyre finaliza las pruebas bloqueando el acceso a las API, desactivando las redes Livefyre y rechazando una solicitud de prueba de carga si no cumple los requisitos.
