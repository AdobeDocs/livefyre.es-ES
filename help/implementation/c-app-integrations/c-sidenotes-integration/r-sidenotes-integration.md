---
description: Integre una aplicación Sidenotes siguiendo un proceso similar al de las aplicaciones principales.
title: Integración de notas
exl-id: 368951b1-fef2-46d8-b89c-68c46962e937
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---

# Integración de notas{#sidenotes-integration}

Integre una aplicación Sidenotes siguiendo un proceso similar al de las aplicaciones principales.

Como regla general, si se completa la integración de la aplicación principal, el código escrito para generar el objeto `collectionMeta` puede reutilizarse para las notas.

También puede reutilizar los `auth` delegados existentes suministrando un `auth` delegado creado con `fyre.conv` a Sidenotes en el campo (opcional) `authDelegate`.

>[!NOTE]
>
>Las notas permiten incluir `network`, `siteId` y `articleId` en un único objeto, en lugar de pasarlas por separado en otras partes del constructor.

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

Como se indica en la sección Generación `collectionMeta` , `collectionMeta` es un objeto JSON codificado. En el ejemplo anterior, el objeto JSON toma el siguiente formato antes de estar codificado en JWT.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Para obtener más información, consulte el token `collectionMeta`.

## Configuración móvil

Las notas se han optimizado para su uso en dispositivos móviles. Para obtener mejores resultados con las versiones móviles de su aplicación Livefyre, establezca la opción escalable por el usuario en no. Por ejemplo:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
