---
description: Ejecute pruebas de estrés en la plataforma de Livefyre.
seo-description: Ejecute pruebas de estrés en la plataforma de Livefyre.
seo-title: Política de prueba de estrés
solution: Experience Manager
title: Política de prueba de estrés
uuid: f 2 d 49 b 55-f 4 fc -485 f -9 aea-a 17 ce 64813 ee
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Política de prueba de estrés{#stress-test-policy}

Ejecute pruebas de estrés en la plataforma de Livefyre.

Este documento proporciona instrucciones para ejecutar pruebas de estrés en la plataforma de Livefyre. Las pruebas ad hoc realizadas por clientes sin notificación están estrictamente prohibidas. Para obtener más información sobre [actividades prohibidas y permitidas](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Las pruebas de estrés son opcionales. No es obligatorio o no debe realizar una prueba de estrés. Adobe Livefyre realiza pruebas y pruebas de estrés normales como parte del proceso de lanzamiento. Si elige ejecutar pruebas, este documento describe los requisitos y las restricciones para llevar a cabo pruebas de estrés.

## Notificación {#section_ihs_bfz_vdb}

Debe notificar a su consultor de éxito de clientes de Livefyre y al consultor técnico de Adobe de las pruebas planeadas tres o más semanas antes de la hora de inicio.

Para notificar a Livefyre, envíe la siguiente información al especialista en éxito del cliente de Livefyre y al consultor técnico de Adobe:

* Finalidad y descripción de la prueba
* El caso de uso en el que está probando
* Lista de las API de Livefyre que planea utilizar en la prueba
* Fecha, hora y duración de la prueba
* Direcciones IP desde las cuales iniciar las pruebas

## Requisitos {#section_khs_bfz_vdb}

Solo puede realizar pruebas si cumplen los requisitos siguientes:

* Debe recibir la aprobación explícita y explícita de un consultor técnico de Adobe 3 semanas o más antes de comenzar la prueba.
* **Solo puede realizar pruebas en la red UAT.**
* Debe probar los escenarios realistas. Por ejemplo, es posible que no dé por sentado que su propiedad ofrecerá *millones* de solicitudes de anuncio todos los días, ya que esto no es un escenario realista. Si necesita ayuda para determinar si su escenario es realista o no, consulte al especialista de éxito de clientes de Livefyre o al consultor técnico de Adobe.
* Las pruebas deben realizarse durante el horario laboral de la zona horaria estándar del Pacífico del Pacífico\ (UTC -7\).
* Es posible que necesite producir datos y su razonamiento para la prueba.

## Administración {#section_mhs_bfz_vdb}

Livefyre se reserva el derecho de finalizar una prueba en cualquier momento si realiza una prueba:

* En la red de producción.
* Sin la aprobación explícita y explícita de un consultor técnico de Adobe con tres semanas o más por adelantado.
* Contra escenarios no reales.

Livefyre finaliza las pruebas bloqueando el acceso a las API, desactivando las redes de Livefyre y rechazando una solicitud de prueba de carga si no cumple los requisitos.
