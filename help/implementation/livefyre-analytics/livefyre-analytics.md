---
description: Analice la actividad de usuario, contenido y moderador del sitio.
title: Analytics
exl-id: dc0545ec-2294-44ab-87c4-67eb30c3f787
source-git-commit: 9cd6617c4204b2c09787ea294227f640018928ce
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 1%

---

# Analytics{#analytics}

Analice la actividad de usuario, contenido y moderador del sitio.

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analice la actividad de usuario, contenido y moderador del sitio.

Livefyre Analytics proporciona acceso a sus datos de red en tableros fáciles de leer para conversaciones, moderación y datos de usuario. Utilice estos tableros para supervisar la actividad y ejecutar análisis rápidos en sus sitios.

Los tableros se pueden filtrar por sitio, fecha y actividad. Utilice el menú desplegable Red en la parte superior izquierda de la ventana para seleccionar un sitio para mostrar. Una vez generado, haga clic en el encabezado de una columna para ordenarla o pase el ratón por encima del gráfico para obtener información más específica sobre cualquier punto de datos.

Esta página describe:

* Selección de un intervalo de fechas para el tablero
* Mostrar/ocultar actividades disponibles
* Exportación de datos del panel
* El panel Colecciones
* Panel de moderación
* El panel Usuarios

>[!NOTE]
>
>Actualmente, Analytics admite actividades que se originan en las aplicaciones principales y la moderación de Livefyre. La mayoría de las actividades incluidas en estos paneles también están disponibles a través de Eventos JavaScript de Livefyre, que pueden utilizarse para impulsar su propia herramienta de análisis personalizada o de terceros.

## Intervalo de fechas {#concept_798C438120E643B6BE262C9997DC87C4}

Haga clic en el menú desplegable de fechas para seleccionar un intervalo que mostrar. Utilice las fechas rápidas o seleccione una fecha de inicio y de finalización de los calendarios proporcionados.

![](assets/analytics-date-range.png)

Fechas rápidas:

* **Hoy:** Muestra datos desde la medianoche de la mañana del día actual hasta la última hora completa antes de este momento.
* **Ayer:** Muestra los datos de las 24 horas anteriores.
* **7 días:** Muestra los datos de los 7 días anteriores, sin incluir el día actual.
* **30 días:** Muestra los datos de los 30 días anteriores, sin incluir el día actual.
* **Esta semana:** Muestra datos desde la medianoche del domingo pasado, hasta la última hora completa antes de este momento.
* **Este mes:** Muestra datos desde la medianoche del primer día del mes actual hasta la última hora completa antes de este momento.
* **La semana pasada:** Muestra los datos de la semana pasada.
* **Último mes:** Muestra los datos del mes pasado.

## Mostrar/ocultar actividades {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

Las actividades son acciones que los usuarios realizan en el sitio, como comentar, marcar, compartir y moderar. Utilice la variable **Mostrar/ocultar actividades** para seleccionar las actividades que desea incluir en el panel.

>[!NOTE]
>
>Si se seleccionan nuevos eventos para el filtro, se volverá a procesar la página sin cambiar la dirección URL.

![](assets/analytics-show-hide-activities.png)

Las actividades disponibles varían según el tipo de panel y la exportación, y pueden incluir:

* **Anuncios:** Muestra datos desde la medianoche de la mañana del día actual hasta la última hora completa antes de este momento.
* **Respuestas:** Muestra los datos de las 24 horas anteriores.
* **Cantidad de &quot;Me gusta&quot;:** Muestra los datos de los 7 días anteriores, sin incluir el día actual.
* **No me gusta:** Muestra los datos de los 30 días anteriores, sin incluir el día actual.
* **Contiene medios:** Muestra datos desde la medianoche del domingo pasado, hasta la última hora completa antes de este momento.
* **El anuncio tiene carga de foto:** Muestra datos desde la medianoche del primer día del mes actual hasta la última hora completa antes de este momento.
* **El anuncio tiene un vínculo:** Muestra los datos de la semana pasada.
* **La publicación tiene @mentions:** Muestra los datos del mes pasado.
* **Aprobado:** Muestra los datos del mes pasado.
* **Bozo&#39;d:** Muestra los datos del mes pasado.
* **Destruido:** Muestra los datos del mes pasado.
* **Total de moderación:** Muestra los datos del mes pasado.

## Exportación de datos del panel {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Utilice la variable **Exportar** menú desplegable para exportar los datos del tablero como un archivo CSV.

* Resumen diario (solo colecciones): exporta los recuentos diarios de la última semana completa para cada colección.
* Datos de tabla: exporta todos los datos resumidos de Colecciones (todas las columnas y todas las filas del informe actual).
* Datos sin procesar: exporta todos los eventos individuales que se utilizaron para crear el informe resumido actual.

>[!NOTE]
>
>Estos informes pueden tardar unos minutos en exportarse. Todas las marcas de tiempo son hora Unix.

## Colecciones {#concept_228D8E5553784DB8BABF3819A5FF0345}

El panel Colecciones enumera la actividad del usuario por colección, lo que le permite determinar el contenido más (y menos) interesante. Cada colección incluida en la lista incluye un vínculo a la página en la que se puede encontrar.

![](assets/analytics-collections.png)

## Moderación {#concept_98689B1E804B43CEA21E3F456107CCD9}

El tablero Moderación enumera los eventos por moderador, lo que le permite evaluar su actividad. Utilice este informe para encontrar los moderadores más activos y las acciones de moderación más comunes.

>[!NOTE]
>
>Se enumerarán las actividades de moderación automatizada de Livefyre para el nombre de moderador Livefyre System.

![](assets/analytics-moderation.png)

## Usuarios {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

El tablero Usuarios muestra la actividad del sitio por usuario, lo que le permite analizar cómo interactúan los usuarios individuales con el sitio. Utilice este tablero para encontrar los usuarios más activos del sitio y para evaluar las actividades del sitio más populares.

![](assets/analytics-users.png)
