---
description: Configure Adobe Analytics y Dynamic Tag Manager (DTM) para recopilar datos para aplicaciones de Livefyre.
title: Uso de Livefyre con Adobe Analytics y Dynamic Tag Manager (DTM)
exl-id: a866782d-fca6-48bf-9fb8-5080e396919b
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 1%

---

# Uso de Livefyre con Adobe Analytics y Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configure Adobe Analytics y Dynamic Tag Manager (DTM) para recopilar datos para aplicaciones de Livefyre.

## Paso 1: Configuración de eventos en Adobe Analytics {#section_iks_kgd_4cb}

Asigne eventos de Livefyre a uno o más eventos de éxito personalizados en el Administrador de grupos de informes de Adobe Analytics.

Para obtener más información sobre el Administrador del grupo de informes, consulte [Administrador del grupo de informes](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en).

1. Inicie sesión en Adobe Analytics como usuario administrador.
1. Abra el Administrador del grupo de informes de administración de Adobe Analytics.
1. Cree un nuevo grupo de informes o elija uno existente.
1. Edite el grupo de informes haciendo clic en el grupo de informes que desea modificar y, a continuación, vaya a **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Asigne los eventos de Livefyre a uno o más eventos de éxito personalizados.

## Paso 2: Configuración de variables de conversión

Asigne variables de conversión de Livefyre (eVars) a variables de conversión en el Administrador del grupo de informes de administración de Adobe Analytics. Las variables de conversión actúan como una función de clasificación para determinar cómo se planea identificar los datos recopilados de los eventos de Livefyre.

1. En el Administrador del grupo de informes, haga clic en **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Elija las variables de conversión personalizadas (eVars) que desee usar y asígnelas a las variables de conversión de Livefyre. Para asignar una variable de conversión de Livefyre a una variable de conversión personalizada:

   * Habilitar la variable de conversión
   * Asigne un nombre a la variable de conversión.
   * Asigne un tipo a la variable de conversión

1. Guarde las variables de conversión personalizadas.

## Paso 3: Usar DTM para agregar su grupo de informes con eventos de Livefyre {#section_t15_2hd_4cb}

Utilice etiquetas para integrar Analytics con eventos de Livefyre. Para ello, cree una nueva propiedad y herramienta y añada el nuevo grupo de informes con eventos de Livefyre a la propiedad . Para obtener más información, consulte [Información general sobre etiquetas](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html).

No es necesario realizar este paso si ya tiene una propiedad o herramienta configurada para el grupo de informes configurado con eventos de Livefyre.

1. En DTM, cree o edite una propiedad existente.
1. Cree o edite una herramienta Adobe Analytics existente.
1. Si no existe una herramienta Adobe Analytics existente, haga clic en el botón **[!UICONTROL Add a Tool]**.
Establezca los siguientes parámetros para la herramienta:

   * Establezca **[!UICONTROL Tool Type]** en **[!UICONTROL Adobe Analytics]**.
   * Activar **[!UICONTROL Automatic Configuration]**.
   * Activar **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Agregue o confirme el nombre del grupo de informes con eventos de Livefyre al campo **[!UICONTROL Report Suites]**.

## Paso 4: Configurar una regla de carga de página para configurar la administración de Analytics {#section_jfj_j3d_4cb}

Configure una regla de carga de página para extraer todos los datos. La regla de carga de página permite colocar el código javascript personalizado en la regla que registra el evento cuando se carga la página.

>[!NOTE]
>
>No utilice reglas basadas en eventos o reglas de llamada directa.

1. En DTM, seleccione la pestaña **[!UICONTROL Rules]** .
1. Haga clic **[!UICONTROL Page Load Rules]**.
1. Haga clic en el botón **[!UICONTROL Create New Rule]**.
1. Abra la sección **[!UICONTROL Conditions]** haciendo clic en el botón **[!UICONTROL Plus]**.
1. Déclencheur la regla. Elija los tipos de déclencheur **[!UICONTROL DOM Ready]** o **[!UICONTROL Onload]** si desea retrasar o implementar la regla de forma asíncrona.
1. (Opcional) Añada parámetros adicionales para limitar las páginas que muestran aplicaciones de Livefyre. Para obtener más información sobre las opciones de configuración adicionales, consulte [Información general sobre etiquetas](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html).
1. En **[!UICONTROL Javascript/ Third Party Tags]**, haga clic en la pestaña **[!UICONTROL Non-sequential]** y, a continuación, haga clic en **[!UICONTROL Add New Script]**.
1. Seleccione **[!UICONTROL Sequential HTML]** como tipo de script.
1. Agregue la siguiente secuencia de comandos al editor de código y haga clic en **[!UICONTROL Save Code]**.

   La siguiente secuencia de comandos llama a la regla de llamada directa `livefyre_analytics` después de que se cargue JavaScript de Livefyre. El siguiente ejemplo de script comprueba cada 400 ms para ver si `livefyre.analytics` está en la página. Una vez que la página se carga, livefyre.analytics envía la información de seguimiento.

   ```
   /**
   * Poll for Livefyre.analytics object to exist since it gets loaded via the
   * Livefyre.js JavaScript file. Depending on the timing, this could already
   * exist or need a little time.
   */
   function pollForAnalytics() {
   if (Livefyre.analytics) {
     _satellite.track('livefyre_analytics');
       return true;
     }
     setTimeout(pollForAnalytics, 400);
   }
   setTimeout(pollForAnalytics, 400);
   ```

1. Haga clic **[!UICONTROL Save Code]**.
1. Haga clic **[!UICONTROL Save Rule]**.

## Paso 5: Crear una regla de llamada directa para crear la configuración de asignación de Adobe Analytics para Livefyre {#section_gvp_b1g_pdb}

Existen otras formas de implementar Livefyre con DTM mediante eventos personalizados, campos de interfaz de usuario de Adobe Analytics en DTM y elementos de datos. Este documento utiliza JavaScript personalizado para lograr el mismo efecto.

1. En DTM, seleccione la pestaña **Rules** y haga clic en **Direct Call Rules**.
1. Haga clic en el botón **Crear nueva regla**.
1. Asigne un nombre a la nueva regla **Livefyre Analytics**.
1. Expanda el área de configuración **conditions**.
1. En el campo **String**, introduzca `livefyre_analytics`.
1. Expanda la sección Javascript / Etiqueta de terceros y haga clic en el botón **Agregar nuevo script**.
1. Introduzca **Configuración de análisis de Livefyre** en el cuadro de entrada **Nombre de etiqueta**.
1. Seleccione **Javascript no secuencial**.
1. Introduzca el siguiente código de configuración de Livefyre en el editor de código y haga clic en el botón **Save Code**.

   ```
   var s = _satellite.getToolsByType('sc')[0].getS();
   
   var evarMap = {
     appId: 'eVar81',
     appType: 'eVar82'
   };
   
   var eventMap = {
     FlagCancel: 'event82',
     FlagClick: 'event82',
     FlagDisagree: 'event82',
     FlagOffensive: 'event82',
     FlagOffTopic: 'event82',
     FlagSpam: 'event82',
     Like: 'event82',
     Load: 'event81',
     RequestMore: 'event82',
     ShareButtonClick: 'event82',
     ShareFacebook: 'event82',
     ShareOnPostClick: 'event82',
     ShareTwitter: 'event82',
     ShareURL: 'event82',
     SortStream: 'event82',
     TwitterLikeClick: 'event82',
     TwitterReplyClick: 'event82',
     TwitterRetweetClick: 'event82',
     TwitterUserFollow: 'event82'
   };
   
    function trackLivefyreEvent(data) {
     var event = eventMap[data.type];
     console.log('Track:', data.type, event);
   
     if (!event) {
       console.warn(data.type, 'is not mapped   to an event in AA');
       return;
     }
     var vars = ['events'];
     switch (event) {
       case 'event82': s.eVar83 = data.type;
         vars.push('eVar83');
         break;
       default:
     }
       ['generator', 'evars'].forEach(function (type) {
       var obj = data[type];
       for (var d in obj) {
         if (obj.hasOwnProperty(d) && evarMap[d]) {
           s[evarMap[d]] = obj[d];
           vars.push(evarMap[d]);
         }
       }
     });
     s.linkTrackVars = vars.join(',');
     s.linkTrackEvents = event;
     s.events = event;
   
     console.log('linkTrackVars:',  s.linkTrackVars);
     console.log('linkTrackEvents:',  s.linkTrackEvents);
     console.log('events:', s.events);
     s.tl();
     }
     ]
   
     /**
   ```

   * Agrega un controlador de análisis para todos los eventos de análisis de Livefyre. Para cada evento, establece los datos en un objeto global y, a continuación, envía el evento.

   ```
   */
   function addAnalyticsHandler() {
     Livefyre.analytics.addHandler(function (events) {
       (events || []).forEach(function (data) {
         console.log('Event handled:', data.type);
         trackLivefyreEvent(data);
       });
     });
   }
   addAnalyticsHandler();
   ```

1. Haga clic en **Guardar regla**.

## Paso 6: Aprobar cambios para la regla de carga de página {#section_pxc_11t_ycb}

1. Vaya a la pestaña **[!UICONTROL Approvals]**.
1. Haga clic **[!UICONTROL Approve]**.
1. Haga clic en **[!UICONTROL Yes, approve]** para confirmar la aprobación.
1. Ir a **[!UICONTROL Overview > Publish Queue]**.
1. Seleccione la regla que desea publicar.
1. Haga clic **[!UICONTROL Publish Selected]**.
1. Haga clic en **[!UICONTROL Publish]** para confirmar que desea publicar.

## Script {#section_xkb_vft_mcb}

El siguiente código de ejemplo asigna las eVars específicas a las eVars de Livefyre disponibles. El nombre de la variable de conversión de Livefyre ( `eVar`) (por ejemplo, `appId`) se asigna al nombre configurado en el Administrador del grupo de informes (por ejemplo, `eVar81`). Cambie los nombres `eVar` de esta secuencia de comandos por las variables de conversión personalizadas.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS();
var evarMap = {
  appId: 'eVar81',
  appType: 'eVar82'
};
```

El siguiente código de ejemplo asigna los eventos específicos configurados en el Administrador de grupos de informes con los eventos de Livefyre disponibles. En este ejemplo, `event82` se configura como cualquier evento de interacción del usuario sin diferenciar qué tipo de evento de interacción del usuario (por ejemplo, indicar que gusta o compartir contenido). Esta es una forma eficaz de registrar toda la información de interacción del usuario en un bloque. También puede asignar los eventos en la interfaz de usuario de DTM Analytics con referencias a elementos de datos.

```
var eventMap = {
  FlagCancel: 'event82',
  FlagClick: 'event82',
  FlagDisagree: 'event82',
  FlagOffensive: 'event82',
  FlagOffTopic: 'event82',
  FlagSpam: 'event82',
  Like: 'event82',
  Load: 'event81',
  RequestMore: 'event82',
  ShareButtonClick: 'event82',
  ShareFacebook: 'event82',
  ShareOnPostClick: 'event82',
  ShareTwitter: 'event82',
  ShareURL: 'event82',
  SortStream: 'event82',
  TwitterLikeClick: 'event82',
  TwitterReplyClick: 'event82',
  TwitterRetweetClick: 'event82',
  TwitterUserFollow: 'event82'
};
```

El siguiente ejemplo indica que si no hay ningún evento en esta lista, no haga nada. No es necesario modificar esta sección de código.

```
function trackLivefyreEvent(data) {
  var event = eventMap[data.type];
  console.log('Track:', data.type, event);

  if (!event) {
    console.warn(data.type, 'is not mapped to an event in AA');
    return;
  }
```

El siguiente código diferencia los tipos de eventos que `event82` registra. La variable de conversión, `eVar83` registra el tipo de interacción del usuario y la secuencia de comandos configura `eVar83` para separar los datos de interacción del usuario por tipo. Por lo tanto, `eVar83` le permite dividir los datos registrados en tipos específicos de interacciones del usuario.

```
  var vars = ['events'];
  switch (event) {
    case 'event82': s.eVar83 = data.type;
      vars.push('eVar83');
      break;
    default:
  }

  ['generator', 'evars'].forEach(function (type) {
    var obj = data[type];
    for (var d in obj) {
      if (obj.hasOwnProperty(d) && evarMap[d]) {
        s[evarMap[d]] = obj[d];
        vars.push(evarMap[d]);
      }
    }
  });

  s.linkTrackVars = vars.join(',');
  s.linkTrackEvents = event;
  s.events = event;

  console.log('linkTrackVars:', s.linkTrackVars);
  console.log('linkTrackEvents:', s.linkTrackEvents);
  console.log('events:', s.events);

  s.tl();
}
```

El siguiente ejemplo de código añade un controlador para escuchar todos los eventos que se producen. Utiliza la regla de carga de página al cargar, espera a que existan eventos, luego configura el controlador para todos los eventos de la aplicación y los rastrea. No es necesario modificar este código.

```
/**
* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event.
*/
function addAnalyticsHandler() {
  Livefyre.analytics.addHandler(function (events) {
    (events || []).forEach(function (data) {
      console.log('Event handled:', data.type);
      trackLivefyreEvent(data);
    });
  });
}
```

## Más información

Para obtener más información sobre los temas tratados en esta página, consulte:

* [Administrador del grupo de informes](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)
* [Información general sobre etiquetas](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
