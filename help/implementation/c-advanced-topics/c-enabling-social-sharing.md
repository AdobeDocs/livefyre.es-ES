---
description: Configure credenciales que permitan a los usuarios compartir contenido en varias redes sociales.
title: Habilitación del uso compartido en medios sociales
exl-id: 08ac9766-52ea-432f-8b4f-bf68cb8b62bc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Habilitación del uso compartido en medios sociales {#enabling-social-sharing}

Configure credenciales que permitan a los usuarios compartir contenido en varias redes sociales.

Para permitir que los usuarios compartan contenido entre sitios de medios sociales, implemente la función Uso compartido en medios sociales de Livefyre y cree un sistema OAuth que proporcione la autenticación adecuada a estos sitios. Con este sistema, Livefyre actúa en nombre del usuario cuando decide compartir contenido a través de los medios sociales.

>[!NOTE]
>
>Los distintos proveedores tienen diferentes requisitos de OAuth. Consulte con sus proveedores para obtener la información asociada con su implementación de OAuth.

## Credenciales sociales {#section_gff_cjm_b1b} requeridas

Si utiliza un sistema de identidad de usuario personalizado, debe proporcionar sus credenciales sociales para permitir que los usuarios compartan con Twitter, Facebook o LinkedIn desde una aplicación de Livefyre.

>[!NOTE]
>
>Los clientes que utilizan Janrain Engage solo deben proporcionar su clave de API de participación y dominio de participación.

Utilice el panel Configuración de integración del Admin Console para introducir o actualizar las siguientes credenciales sociales.

### Credenciales requeridas:

* **** Redireccionamiento de proxy OAuth secreto de ID de cliente de FacebookClient
* **** Secreto de API de clave de LinkedInAPI
* **** Secreto de la API clave de la API secreta del token de acceso de TwitterAccess

## Twitter {#section_qp5_1yl_b1b}

Las credenciales de twitter están disponibles en Twitter App Dashboard. Para encontrar estas credenciales:

* Abra [Página de desarrolladores de aplicaciones de Twitter](https://dev.twitter.com/apps) como propietario de la aplicación, busque la aplicación y haga clic en el título.
* Desplácese hacia abajo hasta &quot;Su token de acceso&quot; y obtenga los valores de &quot;Token de acceso&quot; y &quot;Secreto de token de acceso&quot;.

Debe:

* Introduzca un valor para el campo Callback URL en la aplicación Twitter. Aunque este campo puede ser un marcador de posición simple, no se puede dejar en blanco.
* Establezca el Tipo de aplicación para tener acceso **read** y **write**.
* Confirme que la URL del sitio web de la aplicación de Twitter se encuentra en el mismo dominio de host que la aplicación principal de Livefyre.

>[!NOTE]
>
>Todas las aplicaciones que muestran contenido de Twitter deben seguir sus requisitos de visualización. Consulte las [Directrices para la visualización de Twitter](https://dev.twitter.com/terms/display-requirements) para obtener más información.

## LinkedIn {#section_lfz_zxl_b1b}

Las credenciales de linkedIn están disponibles en la sección Claves de OAuth de las claves de API de su aplicación de LinkedIn.

* Inicie sesión en su cuenta desde la página Desarrolladores de LinkedIn [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Pase el ratón sobre su nombre en la parte superior derecha y seleccione Claves de API en el menú desplegable.
* Haga clic en el título de la aplicación.
* Tome los valores de Clave de API y Clave secreta de la sección Claves de OAuth

## Facebook {#section_zyb_gpl_b1b}

Las credenciales de facebook están disponibles en la página Aplicaciones para desarrolladores .

* Abra [Página de aplicaciones para desarrolladores de Facebook](https://developers.facebook.com/apps) como propietario de la aplicación, busque la aplicación y haga clic en el título.
* Recopile los valores de App ID y App Secret. Para el Secreto de la aplicación, es posible que tenga que hacer clic en el botón Mostrar para mostrarlo.

Para compartir con Facebook es necesario configurar una página de redireccionamiento que tome las solicitudes de Facebook y se adhiera a las prácticas de dominio requeridas por [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). La página debe alojarse en su dominio para que Facebook pueda comprobar que la solicitud procede de un origen legítimo.

### Redireccionamiento de facebook

La página alojada debe incluir el siguiente código:

### Ruby

Este es un ejemplo de uso de Ruby y Rails para hacer el redireccionamiento de Facebook OAuth.

```ruby
require "base64" 
  
class Controller < ActionController::Base 
   def base64url_decode(str) 
      str.gsub! '-_', '+/' 
      Base64.decode64(str.ljust(str.length+str.length%4, '=')) 
   end 
  
   def index 
      lfoauth = params[:lfoauth] 
      if not lfoauth 
         render :status => :forbidden, :text => 'Missing lfoauth.' 
      end 
  
      redirect = base64url_decode lfoauth 
  
      match = /^(http:\/\/|https:\/\/)?([^\/?]+)/i.match(redirect) 
      host = match[2] 
  
         if not host.include? 'fyre.co' 
      render :status => :forbidden, :text => 'Invalid host.' 
         end 
  
         sep = (redirect.include? '?') ? '&' : '?' 
      params.delete :lfoauth 
  
         rdir = redirect + sep + params.to_query 
      redirect_to rdir 
   end 
end
```

### Python

Este es un ejemplo de uso de Python y Django para hacer el redireccionamiento de Facebook OAuth.

```python
import base64, re 
from django.views.decorators.http import require_GET 
from django.http.response import HttpResponseRedirect, HttpResponseBadRequest 
  
def base64url_decode(st): 
    return base64.b64decode(re.sub("-_","+/", st).ljust(len(st)+len(st)%4, '=')) 
  
@require_GET 
def handle_lfoauth(request): 
    lfoauth = request.GET.get('lfoauth', None) 
    import pdb; pdb.set_trace() 
    if not lfoauth: 
        return HttpResponseBadRequest('Missing lfoauth.') 
     
    redirect = base64url_decode(lfoauth) 
     
    match = re.match(r"^(http:\/\/|https:\/\/)?([^\/?]+)", redirect, re.IGNORECASE) 
    host = match.group(2) 
     
    # validate the destination to secure this proxy 
    if not 'fyre.co' in host: 
        return HttpResponseBadRequest('Invalid host.') 
     
    # if params were included in the uri already, append with &, otherwise ? 
    sep = '&' if '?' in redirect else '?' 
     
    # remove lfoauth from query param 
    dict_ = request.GET.copy() 
    dict_.pop('lfoauth') 
  
    # attach remaining param to redirect 
    rdir = redirect + sep + dict_.urlencode() 
  
    # this does the actual redirection 
    return HttpResponseRedirect(rdir)
```

### NodeJS

Este es un ejemplo de uso de NodeJS y Sail/Express para realizar el redireccionamiento de Facebook OAuth.

```nodejs
/* 
 * 
 */ 
var S = require('string'), 
     querystring = require('querystring'); 
  
var base64UrlDecode = function(str) { 
     var temp = S(str.replace('-_', '+/')).padRight(str.length+(str.length%4), '=').s 
     return new Buffer(temp, 'base64').toString('utf8'); 
} 
  
module.exports = { 
  index: function(req, res) { 
     var lfoauth = req.param('lfoauth'); 
  
     if (typeof lfoauth === 'undefined') { 
        res.send(400, 'Missing lfoauth.'); 
     } 
  
     var redirect = base64UrlDecode(lfoauth); 
  
     var match = redirect.match(/^(http:\/\/|https:\/\/)?([^\/?]+)/i); 
     var host = match[2] 
  
     if (host.indexOf('fyre.co') <= -1) { 
        res.send(400, 'Invalid host.'); 
     } 
  
     var sep = redirect.indexOf('?') > -1 ? '&' : '?'; 
  
     delete req.query['lfoauth']; 
     var rdir = redirect + sep + querystring.stringify(req.query); 
  
     res.redirect(rdir); 
  }, 
  
  _config: {} 
};
```

### Java

Este es un ejemplo del uso de controladores Java y Spring para realizar el redireccionamiento de Facebook OAuth.

```java
/* 
 *  
 */ 
import java.util.Collection; 
import java.util.HashMap; 
import java.util.Map; 
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 
  
import org.apache.commons.codec.binary.Base64; 
import org.apache.commons.lang.StringUtils; 
import org.jboss.resteasy.spi.BadRequestException; 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.RequestParam; 
import org.springframework.web.servlet.View; 
import org.springframework.web.servlet.view.RedirectView; 
  
@Controller 
public class RedirectController { 
    @RequestMapping("/fbredirect") 
    public View facebook(@RequestParam Map<string,object> allRequestParams) { 
        if (!allRequestParams.containsKey("lfoauth")) { 
            throw new BadRequestException("Missing lfoauth."); 
        } 
             
        String redirect = base64UrlDecode((String) allRequestParams.get("lfoauth")); 
  
        Pattern p = Pattern.compile("^(http:\\/\\/|https:\\/\\/)?([^\\/?]+)", Pattern.CASE_INSENSITIVE); 
        Matcher m = p.matcher(redirect); 
        if (!m.find() || !m.group(2).contains("fyre.co")) { 
            throw new BadRequestException("Invalid host."); 
        } 
         
        Map<string, object=""> params = new HashMap<string, object="">(allRequestParams); 
        params.remove("lfoauth"); 
        String rdir = redirect + (redirect.contains("?") ? '&' : '?') + mapToQueryString(params); 
         
        return new RedirectView(rdir); 
    } 
     
    private String base64UrlDecode(String str) { 
        return new String(Base64.decodeBase64(StringUtils.rightPad(str.replaceAll("-_", "+/"), str.length()+(str.length()%4), '='))); 
    } 
     
    private String mapToQueryString(Map<string, object=""> map) { 
        String queryparam = ""; 
        for (String key : map.keySet()) { 
            if (map.get(key) instanceof Collection) { 
                for (Object item : (Collection) map.get(key)) { 
                    queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, item.toString())); 
                } 
            } else { 
                queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, map.get(key).toString())); 
            } 
        } 
        return StringUtils.removeEnd(queryparam, "&"); 
    } 
}
```

### PHP

```php
<?php 
/* 
Purpose: Provide a landing page for the last step of successful oAuth 
         that is on the correct (Facebook approved) domain. 
  
Location: This file should be hosted on the same domain as your  
          Facebook App's "site url". 
  
Input Parameters:  
    - (GET) lfoauth: This should be a url-safe base64-encoded URL that  
      is the "real" final redirection URL. Livefyre sets this. 
  
      For testing purposes, this can be set to a url-safe base64-encoded  
      URL of your choosing, but the domain name must end in .fyre.co in  
      order to be considered valid. 
  
    - (GET) [all other parameters]: Any other parameters should simply  
      be passed thru on the redirection URL. If the decoded URL from "lfoauth"  
      includes querystring parameters, then the additional parameters included  
      with the initial request should be appended with "&..." 
  
Output: The response should indicate that the browser redirect (302) to the  
        "real" URL which is encoded in the "lfoauth" parameter. 
  
*/ 
  
function base64url_decode($data) { 
  return base64_decode(str_pad(strtr($data, '-_', '+/'), strlen($data) % 4, '=', STR_PAD_RIGHT)); 
} 
  
if (isset($_GET['lfoauth'])) { 
    // Warning: If implemented with non-PHP, b64 may fail because we have  
    // stripped padding (trailing ='s), to comply with Facebook parameters.   
    // The decode needs to be non-strict in this sense. 
  
    $rdir = base64url_decode($_GET['lfoauth']); 
  
    // validate the destination to secure this proxy 
    preg_match("/^(https?:\/\/)?([^\/?]+)/i", $rdir, $domain_only);    
    $host = $domain_only[2]; 
    if (!strstr($host,'fyre.co')) { 
        echo "Error - this redirection is not allowed! ".$host; 
        exit; 
    } 
  
    // if params were included in the uri already, append with &, otherwise ? 
    $sep = strstr($rdir,'?') ? '&' : '?'; 
  
    // don't include this in the params we add to the redirect url 
    unset($_GET['lfoauth']); 
  
    // assemble a new querystring from the remaining inbound GET params 
    $rdir = $rdir.$sep.http_build_query($_GET); 
  
    // this does the actual redirection, PHP's implementation is weird 
    header('Location: '.$rdir); 
} 
?>
```

## Configuración de Proveedores de &quot;Anuncio a&quot; {#section_rdk_dpl_b1b}

De forma predeterminada, los botones &quot;Publicar en&quot; de Facebook, LinkedIn y Twitter se muestran en las aplicaciones principales de Livefyre. Utilice el parámetro postToButton para configurar qué proveedores aparecerán al incrustar la aplicación Livefyre.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` es una matriz con cualquier subconjunto de las siguientes opciones:

* tw: Twitter
* fb: Facebook
* li: linkedIn
