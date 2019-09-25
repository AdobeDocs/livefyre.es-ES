---
description: Analizar la actividad de usuario, contenido y moderador del sitio.
seo-description: Analizar la actividad de usuario, contenido y moderador del sitio.
seo-title: Analytics
solution: Experience Manager
title: Analytics
uuid: b022aa77-59b9-422a-8d9f-fb9d8a1b0478
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Analytics{#analytics}

Analizar la actividad de usuario, contenido y moderador del sitio.

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analizar la actividad de usuario, contenido y moderador del sitio.

Livefyre Analytics proporciona acceso a los datos de red en tableros de fácil lectura para conversaciones, moderación y datos de usuario. Utilice estos tableros para supervisar la actividad y ejecutar análisis rápidos en el sitio.

Los tableros se pueden filtrar por sitio, fecha y actividad. Utilice el menú desplegable Red en la parte superior izquierda de la ventana para seleccionar un sitio para mostrar. Una vez generado, haga clic en el encabezado de una columna para ordenarla o pase el ratón por encima del gráfico para obtener información más específica sobre cualquier punto de datos.

Esta página describe:

* Selección de un intervalo [de fechas](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange) para el tablero
* [Mostrar u ocultar actividades disponibles](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [Exportación de datos de tablero](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [Panel Colecciones](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [Tablero de moderación](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [Tablero de usuarios](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Actualmente, Analytics admite actividades procedentes de las aplicaciones principales y la moderación de Livefyre. La mayoría de las actividades incluidas en estos tableros también están disponibles a través de los eventos [JavaScript de](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/)Livefyre, que pueden utilizarse para activar su propia herramienta de análisis personalizada o de terceros.

## Intervalo de fechas {#concept_798C438120E643B6BE262C9997DC87C4}

Haga clic en el menú desplegable de fechas para seleccionar un intervalo para mostrar. Utilice las fechas rápidas o seleccione una fecha de inicio y una de finalización en los calendarios proporcionados.

![](assets/analytics-date-range.png)

Fechas rápidas:

* **** Hoy: Muestra los datos desde la medianoche de la mañana del día actual, hasta la última hora completa antes de este momento.
* **** Ayer: Muestra los datos de las 24 horas anteriores.
* **** 7 días: Muestra los datos de los 7 días anteriores, sin incluir hoy.
* **** 30 días: Muestra los datos de los 30 días anteriores, sin incluir el día de hoy.
* **** Esta semana: Muestra los datos desde la medianoche de la mañana del domingo pasado, hasta la última hora completa antes de este momento.
* **** Este mes: Muestra datos desde la medianoche de la mañana del primer día del mes actual, hasta la última hora completa antes de este momento.
* **** Última semana: Muestra los datos de la semana pasada.
* **** Último mes: Muestra los datos del mes pasado.

## Mostrar/ocultar actividades {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

Las actividades son acciones que los usuarios realizan en el sitio, como comentar, marcar, compartir y moderar. Utilice el menú desplegable **Mostrar/Ocultar actividades** para seleccionar las actividades que desee incluir en el tablero.

>[!NOTE]
>
>Al seleccionar nuevos eventos para el filtro, se volverá a procesar la página sin cambiar la dirección URL.

![](assets/analytics-show-hide-activities.png)

Las actividades disponibles varían según el tipo de tablero y la exportación, y pueden incluir:

* **** Anuncios: Muestra los datos desde la medianoche de la mañana del día actual, hasta la última hora completa antes de este momento.
* **** Respuestas: Muestra los datos de las 24 horas anteriores.
* **** Cantidad de "Me gusta": Muestra los datos de los 7 días anteriores, sin incluir hoy.
* **** No me gusta: Muestra los datos de los 30 días anteriores, sin incluir el día de hoy.
* **** Contiene medios: Muestra los datos desde la medianoche de la mañana del domingo pasado, hasta la última hora completa antes de este momento.
* **** La publicación tiene carga de fotos: Muestra datos desde la medianoche de la mañana del primer día del mes actual, hasta la última hora completa antes de este momento.
* **** La publicación tiene un vínculo: Muestra los datos de la semana pasada.
* **** La publicación tiene @mentions: Muestra los datos del mes pasado.
* **** Aprobado: Muestra los datos del mes pasado.
* **** Bozo'd: Muestra los datos del mes pasado.
* **** Rastreado: Muestra los datos del mes pasado.
* **** Total de moderación: Muestra los datos del mes pasado.

## Exportación de datos de tablero {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Utilice el menú desplegable **Exportar** para exportar los datos del tablero como un archivo CSV.

* Resumen diario (solo colecciones): exporta el recuento diario de la última semana completa para cada colección.
* Datos de tabla: exporta todos los datos resumidos de colecciones (todas las columnas y todas las filas del informe actual).
* Datos sin procesar: exporta todos los eventos individuales que se utilizaron para crear el informe resumido actual.

>[!NOTE]
>
>Estos informes pueden tardar unos minutos en exportarse. Todas las marcas de hora son hora Unix.

## Colecciones {#concept_228D8E5553784DB8BABF3819A5FF0345}

El tablero Colecciones muestra la actividad de los usuarios por colección, lo que permite determinar el contenido más (y menos) interesante. Cada colección incluida en la lista incluye un vínculo a la página en la que se encuentra.

![](assets/analytics-collections.png)

## Moderación {#concept_98689B1E804B43CEA21E3F456107CCD9}

El tablero Moderación enumera los eventos por moderador, permitiéndole evaluar su actividad. Utilice este informe para encontrar los moderadores más activos y sus acciones de moderación más comunes.

>[!NOTE]
>
>Se enumerarán las actividades de moderación de Livefyre automatizada para el nombre del moderador Livefyre System.

![](assets/analytics-moderation.png)

## Usuarios {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

El tablero Usuarios muestra la actividad del sitio por usuario, lo que le permite analizar cómo interactúan los usuarios individuales con el sitio. Utilice este tablero para encontrar los usuarios más activos del sitio y evaluar las actividades del sitio más populares.

![](assets/analytics-users.png)

