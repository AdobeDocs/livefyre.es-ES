---
description: Integre una aplicación Sidenotes siguiendo un proceso similar al de las aplicaciones principales.
seo-description: Integre una aplicación Sidenotes siguiendo un proceso similar al de las aplicaciones principales.
seo-title: Integración de Sidenotes
solution: Experience Manager
title: Integración de Sidenotes
uuid: 4aa14ada-402a-482d-b43e-96f37afa6c53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Integración de Sidenotes{#sidenotes-integration}

Integre una aplicación Sidenotes siguiendo un proceso similar al de las aplicaciones principales.

Como regla general, si se completa la integración de la aplicación principal, el código escrito para generar el `collectionMeta` objeto puede reutilizarse para Sidenotes.

También puede reutilizar los delegados existentes `auth` suministrando un `auth` delegado creado con `fyre.conv` Sidenotes en el campo (opcional) `authDelegate` .

>[!NOTE]
>
>Sidenotes permite incluir `network`, `siteId`y `articleId` en un único objeto, en lugar de pasarlos por separado en otras partes del constructor.

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

Como se indica en la sección Generación `collectionMeta` , `collectionMeta` es un objeto JSON codificado. En el ejemplo anterior, el objeto JSON toma el siguiente formato antes de codificarse en JWT.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Para obtener más información, consulte el `collectionMeta` token.

## Configuración móvil

Sidenotes se ha optimizado para su uso en dispositivos móviles. Para obtener los mejores resultados con las versiones móviles de la aplicación Livefyre, establezca la opción escalable por el usuario en no. Por ejemplo:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
