---
description: Integre una aplicación Sidenotes siguiendo un proceso similar al de Aplicaciones
  principales.
seo-description: Integre una aplicación Sidenotes siguiendo un proceso similar al
  de Aplicaciones principales.
seo-title: Integración de Sidenotes
solution: Experience Manager
title: Integración de Sidenotes
uuid: 4 aa 14 ada -402 a -482 d-b 43 e -96 f 37 afa 6 c 53
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Integración de Sidenotes{#sidenotes-integration}

Integre una aplicación Sidenotes siguiendo un proceso similar al de Aplicaciones principales.

Como regla general, si se completa la integración de la aplicación principal, el código escrito para generar el `collectionMeta` objeto puede reutilizarse para Sidenotes.

También puede reutilizar `auth` los delegados existentes suministrando un `auth` delegado creado con `fyre.conv` Sidenotes en el `authDelegate` campo (opcional).

>[!NOTE]
>
>Los sidenotes le permiten incluir `network`, `siteId`y `articleId` en un único objeto, en lugar de pasarlos por separado en otras partes del constructor.

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

Como se indica en `collectionMeta` la sección Build, `collectionMeta` es un objeto JSON codificado. En el ejemplo anterior, el objeto JSON toma el siguiente formato antes de codificar JWT.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Para obtener más información, consulte `collectionMeta` el token.

## Configuración móvil

Sidenotes se ha optimizado para su uso en dispositivos móviles. Para obtener los mejores resultados con versiones móviles de la aplicación de Livefyre, defina la opción de escalable en no. Por ejemplo:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
