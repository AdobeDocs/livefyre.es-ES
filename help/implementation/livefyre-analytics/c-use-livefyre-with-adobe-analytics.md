---
description: 'null'
seo-description: 'null'
seo-title: Utilizar Livefyre con Adobe Analytics y Administrador dinámico de etiquetas (DTM) lk xavvn vefyre con Adobe Analytics y Administrador dinámico de etiquetas (DTM)
uuid: 9 a 1 c 25 c 0-c 474-46 ff -82 ac-e 89357007 c 7 f
translation-type: tm+mt
source-git-commit: 55bfc0a545bb4a1093c29bd11e764c9799135324

---


# Utilizar Livefyre con Adobe Analytics y Administrador dinámico de etiquetas (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configure Adobe Analytics y Administrador dinámico de etiquetas (DTM) para recopilar datos de aplicaciones de Livefyre.

## Paso 1: Configuración de eventos en Adobe Analytics {#section_iks_kgd_4cb}

Asigne eventos de Livefyre a uno o más eventos de éxito personalizados en el Administrador del grupo de informes de Adobe Analytics.

Para obtener más información sobre el Administrador de grupos de informes, consulte [Administrador del grupo de informes](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html).

1. Inicie sesión en Adobe Analytics como usuario de administrador.
1. Abra Administrador del grupo de informes de administración de Adobe Analytics.
1. Cree un nuevo grupo de informes o elija uno existente.
1. Para modificar el grupo de informes, haga clic en el grupo de informes que desee modificar y vaya **[!UICONTROL Edit Settings > Conversion > Success Events]** a.
1. Asigne eventos de Livefyre a uno o más eventos de éxito personalizados.

## Paso 2: Configurar variables de conversión

Asigne variables de conversión de Livefyre (evars) a variables de conversión del Administrador del grupo de informes de administración de Adobe Analytics. Las variables de conversión actúan como una función de ordenación para determinar cómo se pretende identificar los datos recopilados de los eventos de Livefyre.

1. En el Administrador de grupos de informes, haga clic **[!UICONTROL Edit Settings > Conversion > Conversion Variables]** en.
1. Elija las variables de conversión personalizadas (evars) para usarlas y asignarlas a las variables de conversión de Livefyre. Para asignar una variable de conversión de Livefyre a una variable de conversión personalizada:
* Habilitar la variable de conversión
* Asigne un nombre a la variable de conversión
* Asigne un tipo a la variable de conversión
1. Guarde las variables de conversión personalizadas.

## Paso 3: Utilizar DTM para agregar el grupo de informes con eventos de Livefyre {#section_t15_2hd_4cb}

Agregue Adobe Analytics a DTM para que funcione Analytics. Para ello, cree una nueva propiedad y herramienta y agregue el nuevo grupo de informes con eventos de Livefyre a la propiedad. Para obtener más información sobre la DTM, consulte [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).

No necesita realizar este paso si ya tiene una propiedad o una herramienta configurada para el grupo de informes que configuró con eventos de Livefyre.

1. En DTM, cree o edite una propiedad existente.
1. Cree o edite una herramienta de Adobe Analytics existente.
1. Si una herramienta Adobe Analytics existente no existe, haga clic en **[!UICONTROL Add a Tool]** el botón.
Establezca los parámetros siguientes para la herramienta:
* Establecida **[!UICONTROL Tool Type]** en **[!UICONTROL Adobe Analytics]**.
* Enable **[!UICONTROL Automatic Configuration]**.
* Enable **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Agregue o confirme el nombre del grupo de informes con eventos de Livefyre al **[!UICONTROL Report Suites]** campo.

## Paso 4: Configurar una regla de carga de página para configurar la administración de análisis {#section_jfj_j3d_4cb}

Configure una regla de carga de página para obtener todos los datos. La regla de carga de página permite colocar javascript personalizado en la regla que registra el evento cuando se carga la página.

>[!NOTE]
>
>No utilice reglas basadas en eventos ni reglas de llamadas directas.

1. En DTM, seleccione **[!UICONTROL Rules]** la ficha.
1. Haga clic **[!UICONTROL Page Load Rules]** en.
1. Haga clic en **[!UICONTROL Create New Rule]** el botón.
1. Abra **[!UICONTROL Conditions]** la sección haciendo clic en **[!UICONTROL Plus]** el botón.
1. Active la regla. Elija **[!UICONTROL DOM Ready]** o **[!UICONTROL Onload]** active tipos si desea retrasar o implementar la regla asincrónicamente.
1. (Opcional) Agregue parámetros adicionales para limitar las páginas que muestran aplicaciones de Livefyre. Para obtener más información acerca de las opciones de configuración adicionales, consulte [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. En, **[!UICONTROL Javascript/ Third Party Tags]** haga clic en la **[!UICONTROL Non-sequential]** ficha y, a continuación, haga clic **[!UICONTROL Add New Script]** en.
1. Seleccione **[!UICONTROL Sequential HTML]** como tipo de secuencia de comandos.
1. Agregue la siguiente secuencia de comandos al editor de código y haga clic **[!UICONTROL Save Code]**en.
La siguiente secuencia de comandos llama a `livefyre_analytics` la regla de llamada directa después de que se cargue el JavaScript de Livefyre. El siguiente ejemplo de secuencia de comandos comprueba cada 400 ms para ver si `livefyre.analytics` está en la página. Una vez que se carga la página, livefyre. analytics envía información de seguimiento.

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

1. Haga clic **[!UICONTROL Save Code]** en.
1. Haga clic **[!UICONTROL Save Rule]** en.

## Paso 5: Crear una regla de llamada directa para construir la configuración de asignación de Adobe Analytics para Livefyre {#section_gvp_b1g_pdb}

Existen otros modos de implementar Livefyre con DTM mediante eventos personalizados, campos de interfaz de usuario de Adobe Analytics en DTM y elementos de datos. Este documento utiliza Javascript personalizado para lograr el mismo efecto.

1. En la DTM, seleccione la ficha **Reglas** y, a continuación, haga clic en Reglas de llamadas **directas**.
1. Haga clic en el botón **Crear nueva regla** .
1. Asigne un nombre a la nueva regla **de Livefyre Analytics**.
1. Expanda **el área** de configuración de condiciones.
1. En el campo **Cadena** , introduzca `livefyre_analytics`.
1. Expanda la sección Etiqueta de terceros/Javascript y haga clic en el botón **Agregar nueva secuencia de comandos** .
1. Introduzca **la configuración de Analyefyre Analytics** en el cuadro **de entrada Nombre** de etiqueta.
1. Seleccione **Javascript no secuencial**.
1. Introduzca el siguiente código de configuración de Livefyre en el editor de código y haga clic en el **botón Guardar código** .

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

* Agrega un controlador de análisis para todos los eventos de análisis desde Livefyre. Para cada evento, establece los datos en un objeto global y, a continuación, distribuye el evento.

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
1. Click on **Save Rule**.

## Step 6: Approve changes for Page Load Rule {#section_pxc_11t_ycb}

1. Go to **[!UICONTROL Approvals]** tab.
1. Click **[!UICONTROL Approve]**.
1. Click **[!UICONTROL Yes, approve]** to confirm your approval.
1. Go to **[!UICONTROL Overview > Publish Queue]**.
1. Select the Rule to publish.
1. Click **[!UICONTROL Publish Selected]**.
1. Click **[!UICONTROL Publish]** to confirm that you want to publish.

## Script {#section_xkb_vft_mcb}

The following sample code maps the specific eVars to available Livefyre eVars. The Livefyre conversion variable ( `eVar`) name (for example, `appId`) maps to the name you set up in the Report Suite Manager (for example, `eVar81`). Change the `eVar` names in this script to the custom conversion variables.
```

var s =_ satellite. gettoolsbytype`('sc')[0]`. getS ();
var evarmap = {appid: &#39; Evar 81 &#39;,
apptype: &#39; Evar 82 &#39;};

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventmap = {flagcancel: &#39; event 82 &#39;,\
Clic: &#39; event 82 &#39;,\
Flagrechazar: &#39; event 82 &#39;,\
Flagofensiva: &#39; event 82 &#39;,\
Flagofftopic: &#39; event 82 &#39;,\
Rasspam: &#39; event 82 &#39;,\
Me gusta: &#39; event 82 &#39;,
Load: &#39; event 81 &#39;,\
Requestmore: &#39; event 82 &#39;,\
Sharebuttonclick: &#39; event 82 &#39;,\
Sharefacebook: &#39; event 82 &#39;,\
Shareonpostclick: &#39; event 82 &#39;,\
Sharetwitter: &#39; event 82 &#39;,\
Shareurl: &#39; event 82 &#39;,\
Sortstream: &#39; event 82 &#39;,\
Twitterlikeclick: &#39; event 82 &#39;,
twitterreplyclick: &#39; event 82 &#39;,\
Twitterretweetclick: &#39; event 82 &#39;,\
Twitteruserfollow: &#39; event 82 &#39;};

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function tracklivefyreevent (data) {\
var event = eventmapdata[. type];
console. log (&#39; Track: &#39;, data. type, event);

if (! event) {console.
warn (data. type,&#39; is not maped to an event in AA &#39;);\
return;}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars = [&#39; events &#39;];\
switch (event) {case&#39;event
82 &#39;: s. evar 83 = data. type;\
vars. push (&#39; evar 83 &#39;);\
break;
predeterminado:}

[&#39; generator &#39;,&#39; evars &#39;]. foreach (function (type) {\
var obj = datatype[];
for (var d in obj) {if
(obj. hasownproperty (d) &amp; &amp; evarmapd[]) {\
s [evarmapd[]] = objd[];\
vars. push (evarmapd[]);}}});

s. linktrackvars = vars. join (&#39;,&#39;);\
s. linktrackevents = event;\
s. events = event;

console. log (&#39; linktrackvars: &#39;, s. linktrackvars);\
console. log (&#39; linktrackevents: &#39;, s. linktrackevents);\
console. log (&#39; events: &#39;, s. events);

s. tl ();}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* Agrega un controlador de análisis para todos los eventos de análisis desde Livefyre. Para cada evento, establece los datos en un objeto global y, a continuación, distribuye el evento.

*/function
addanalyticshandler () {Livefyre.
analytics. addhandler (function (events) {(events) || []). Foreach (function (data) {console.
log (&#39; Event gestionado: &#39;, data. type);
Tracklivefyreevent (data);});});}

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

