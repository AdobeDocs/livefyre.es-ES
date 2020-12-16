---
description: 'null'
seo-description: 'null'
seo-title: Uso de Livefyre con Adobe Analytics y Administrador dinámico de etiquetas (DTM) lk xavn   vefyre con Adobe Analytics y Administrador dinámico de etiquetas (DTM)
uuid: 9a1c25c0-c474-46ff-82ac-e89357007c7f
translation-type: tm+mt
source-git-commit: 573e815799fbae2c2c4f1d98a01ea0ae04108a34
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 1%

---


# Usar Livefyre con Adobe Analytics y el Administrador dinámico de etiquetas (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configure Adobe Analytics y el Administrador dinámico de etiquetas (DTM) para recopilar datos para las aplicaciones de Livefyre.

## Paso 1: Configurar Eventos en Adobe Analytics {#section_iks_kgd_4cb}

Asigne eventos de Livefyre a uno o varios Eventos de éxito personalizados en el Administrador de grupos de informes de Adobe Analytics.

Para obtener más información sobre el Administrador de grupos de informes, consulte [Administrador de grupos de informes](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html).

1. Inicie sesión en Adobe Analytics como usuario administrador.
1. Abra el Administrador del grupo de informes de administración de Adobe Analytics.
1. Cree un nuevo grupo de informes o elija uno existente.
1. Para editar el grupo de informes, haga clic en el grupo de informes que desea modificar y luego navegue a **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Asigne los eventos de Livefyre a uno o varios Eventos de éxito personalizados.

## Paso 2: Configurar variables de conversión

Asigne variables de conversión de Livefyre (eVars) a variables de conversión en el Administrador del grupo de informes de administración de Adobe Analytics. Las variables de conversión actúan como una función de clasificación para determinar cómo se planea identificar los datos recopilados de los eventos de Livefyre.

1. En el Administrador de grupos de informes, haga clic en **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Elija las variables de conversión personalizadas (eVars) para utilizarlas y asignarlas a las variables de conversión de Livefyre. Para asignar una variable de conversión de Livefyre a una variable de conversión personalizada:
* Habilitar la variable de conversión
* Asigne un nombre a la variable de conversión
* Asigne un tipo a la variable de conversión
1. Guarde las variables de conversión personalizadas.

## Paso 3: Utilice la DTM para Añadir el grupo de informes con Eventos de Livefyre {#section_t15_2hd_4cb}

Añada Adobe Analytics a DTM para que Analytics funcione. Para ello, cree una nueva propiedad y herramienta y agregue el nuevo grupo de informes con eventos de Livefyre a la propiedad. Para obtener más información sobre la DTM, consulte [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).

No es necesario que realice este paso si ya tiene una propiedad o herramienta configurada para el grupo de informes que configuró con eventos de Livefyre.

1. En DTM, cree o edite una propiedad existente.
1. Cree o edite una herramienta de Adobe Analytics existente.
1. Si no existe una herramienta Adobe Analytics existente, haga clic en el botón **[!UICONTROL Add a Tool]**.
Defina los parámetros siguientes para la herramienta:

   * Establezca **[!UICONTROL Tool Type]** en **[!UICONTROL Adobe Analytics]**.
   * Activar **[!UICONTROL Automatic Configuration]**.
   * Activar **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Añada o confirme el nombre del grupo de informes con eventos de Livefyre en el campo **[!UICONTROL Report Suites]**.

## Paso 4: Configure una regla de carga de página para configurar la administración de Analytics {#section_jfj_j3d_4cb}

Configure una regla de carga de página para extraer todos los datos. La regla de carga de página permite colocar javascript personalizado en la regla que registra el evento cuando se carga la página.

>[!NOTE]
>
>No utilice reglas basadas en Eventos ni reglas de llamadas directas.

1. En la DTM, seleccione la ficha **[!UICONTROL Rules]**.
1. Haga clic **[!UICONTROL Page Load Rules]**.
1. Haga clic en el botón **[!UICONTROL Create New Rule]**.
1. Abra la sección **[!UICONTROL Conditions]** haciendo clic en el botón **[!UICONTROL Plus]**.
1. Activar la regla. Elija los tipos de activadores **[!UICONTROL DOM Ready]** o **[!UICONTROL Onload]** si desea retrasar o implementar la regla de forma asíncrona.
1. (Opcional) Añada parámetros adicionales para limitar las páginas que muestran las aplicaciones de Livefyre. Para obtener más información sobre las opciones de configuración adicionales, consulte [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).
1. En **[!UICONTROL Javascript/ Third Party Tags]**, haga clic en la ficha **[!UICONTROL Non-sequential]** y luego haga clic en **[!UICONTROL Add New Script]**.
1. Seleccione **[!UICONTROL Sequential HTML]** como tipo de secuencia de comandos.
1. Añada la siguiente secuencia de comandos en el editor de código y haga clic en **[!UICONTROL Save Code]**.

   La siguiente secuencia de comandos llama a la regla de llamada directa `livefyre_analytics` después de que se cargue JavaScript de Livefyre. El siguiente ejemplo de secuencia de comandos comprueba cada 400 ms para ver si `livefyre.analytics` está en la página. Una vez que se carga la página, livefyre.analytics envía la información de seguimiento.

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

## Paso 5: Crear una regla de llamada directa para construir la configuración de asignación de Adobe Analytics para Livefyre {#section_gvp_b1g_pdb}

Existen otras formas de implementar Livefyre con la DTM mediante eventos personalizados, campos de la interfaz de usuario de Adobe Analytics en la DTM y elementos de datos. Este documento utiliza JavaScript personalizado para lograr el mismo efecto.

1. En la DTM, seleccione la ficha **Reglas** y haga clic en **Reglas de llamadas directas**.
1. Haga clic en el botón **Crear nueva regla**.
1. Asigne un nombre a la nueva regla **Análisis de Livefyre**.
1. Expanda el área de configuración **conditions**.
1. En el campo **String**, introduzca `livefyre_analytics`.
1. Expanda la sección Etiqueta de JavaScript/terceros y haga clic en el botón **Añadir nueva secuencia de comandos**.
1. Introduzca **Configuración de análisis de Livefyre** en el cuadro de entrada **Nombre de etiqueta**.
1. Seleccione **Javascript no secuencial**.
1. Introduzca el siguiente código de configuración de Livefyre en el editor de código y haga clic en el botón **Guardar código**.

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

   * Añade un controlador de análisis para todos los eventos de análisis de Livefyre. Para cada evento, establece los datos en un objeto global y, a continuación, distribuye el evento.

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

1. Vaya a la ficha **[!UICONTROL Approvals]**.
1. Haga clic **[!UICONTROL Approve]**.
1. Haga clic en **[!UICONTROL Yes, approve]** para confirmar su aprobación.
1. Ir a **[!UICONTROL Overview > Publish Queue]**.
1. Seleccione la regla que desea publicar.
1. Haga clic **[!UICONTROL Publish Selected]**.
1. Haga clic en **[!UICONTROL Publish]** para confirmar que desea publicar.

## Script {#section_xkb_vft_mcb}

El siguiente código de muestra asigna las eVars específicas a las eVars de Livefyre disponibles. El nombre de la variable de conversión de Livefyre ( `eVar`) (por ejemplo, `appId`) se asigna al nombre configurado en el Administrador de grupos de informes (por ejemplo, `eVar81`). Cambie los nombres `eVar` de esta secuencia de comandos a las variables de conversión personalizadas.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

El siguiente código de muestra asigna los eventos específicos que configuró en el Administrador de grupos de informes con los eventos de Livefyre disponibles. En este ejemplo, `event82` se configura como cualquier evento de interacción del usuario sin diferenciar qué tipo de evento de interacción del usuario (por ejemplo, indicar que gusta o compartir contenido). Esta es una manera eficaz de registrar toda la información de interacción del usuario en un bloque. También puede asignar los eventos en la interfaz de usuario de DTM Analytics con la referencia a elementos de datos.

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

El siguiente código diferencia los tipos de evento que `event82` registra. La variable de conversión, `eVar83` registra el tipo de interacción del usuario y la secuencia de comandos configura `eVar83` para separar los datos de interacción del usuario por tipo. Por lo tanto `eVar83` le permite desglosar los datos registrados en tipos específicos de interacciones del usuario.

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

El siguiente ejemplo de código agrega un controlador para escuchar todos los eventos que se producen. Utiliza la regla de carga de página al cargar, espera a que existan eventos y, a continuación, configura el controlador para todos los eventos de la aplicación y los rastrea. No es necesario modificar este código.

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

* [Administrador del grupo de informes](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)
* [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)
* [Reglas](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
