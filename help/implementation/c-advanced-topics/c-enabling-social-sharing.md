---
description: Configure credenciales que permitan a los usuarios compartir contenido en varias redes sociales.
seo-description: Configure credenciales que permitan a los usuarios compartir contenido en varias redes sociales.
seo-title: Activación de Compartir en redes sociales
solution: Experience Manager
title: Activación de Compartir en redes sociales
uuid: f 584 a 0 ae -46 c 7-48 c 1-aea 4-36 da 9 f 1 e 259 b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830

---


# Activación de Compartir en redes sociales {#enabling-social-sharing}

Configure credenciales que permitan a los usuarios compartir contenido en varias redes sociales.

Para permitir que los usuarios compartan contenido en los sitios de medios sociales, implemente la función de uso compartido en redes sociales de Livefyre y cree un sistema oauth para proporcionar una autenticación correcta a dichos sitios. Con este sistema, Livefyre actúa en nombre del usuario cuando elige compartir contenido a través de medios sociales.

>[!NOTE]
>
>Distintos proveedores tienen distintos requisitos oauth. Consulte con sus proveedores para adquirir la información asociada con su implementación de oauth.

## Credenciales sociales requeridas {#section_gff_cjm_b1b}

Si utiliza un sistema de identidad de usuario personalizado, debe proporcionar sus credenciales sociales para permitir que los usuarios compartan en Twitter, Facebook o linkedin desde una aplicación de Livefyre.

>[!NOTE]
>
>Los clientes que utilicen Janrain Engage solo necesitan proporcionar su dominio de participación y la clave de participación de API.

Utilice el panel Configuración de integración de la Consola de administración para ingresar o actualizar las credenciales sociales siguientes.

### Credenciales requeridas:

* **Redirección proxy del cliente de ID de** cliente de Facebook oauth
* **Clave secreta** de API clave de linkedin
* **Secreto de API clave de autentificador de acceso a token** de acceso de Twitter

## Twitter {#section_qp5_1yl_b1b}

Las credenciales de Twitter están disponibles en el Panel de aplicaciones de Twitter. Para encontrar estas credenciales:

* Abra [la página Dev Dev Page](https://dev.twitter.com/apps) de Twitter como propietario de la aplicación, busque su aplicación y haga clic en el título.
* Desplácese hacia abajo hasta «Su autentificador de acceso» y tome los valores de «Token de acceso» y «Secreto de autentificador de acceso». »»

Debe:

* Introduzca un valor para el campo URL de llamada de retorno en la aplicación de Twitter. Aunque este campo puede ser un marcador de posición simple, no se puede dejar en blanco.
* Configure el tipo de aplicación para que tenga acceso **de lectura** y **escritura** .
* Confirme que la URL del sitio Web de la aplicación de Twitter esté en el mismo dominio de host que la aplicación de Livefyre Core.

>[!NOTE]
>
>Todas las aplicaciones que muestran contenido de Twitter son necesarias para cumplir los requisitos de visualización. Consulte las Pautas de visualización [de Twitter](https://dev.twitter.com/terms/display-requirements) para obtener más información.

## Linkedin {#section_lfz_zxl_b1b}

Las credenciales de linkedin están disponibles en la sección Claves oauth de las claves de API de la aplicación linkedin.

* Inicie sesión en su cuenta desde la página Desarrolladores de linkedin [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Pase el ratón sobre su nombre en la parte superior derecha y seleccione Claves de API en el menú desplegable.
* Haga clic en el título de la aplicación.
* Tome los valores Clave de API y Clave secreta de la sección Claves oauth

## Facebook {#section_zyb_gpl_b1b}

Las credenciales de Facebook están disponibles en la página Aplicaciones para desarrolladores.

* Abra [la página de aplicaciones para desarrolladores de Facebook](https://developers.facebook.com/apps) como propietario de la aplicación, busque su aplicación y haga clic en el título.
* Tome los valores para el ID de la aplicación y el secreto de aplicación. Para el Secreto de aplicación, es posible que deba hacer clic en el botón Mostrar para mostrarlo.

Compartir con Facebook requiere que configure una página de redirección para tomar solicitudes de Facebook y adherirse a las prácticas de dominio requeridas [por Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). La página debe estar alojada en su dominio para que Facebook pueda verificar que la solicitud proviene de una fuente legítima.

### Redireccionamiento de Facebook

La página alojada debe incluir el siguiente código:

### Ruby

Este es un ejemplo de Ruby y Rails para realizar el redireccionamiento de Facebook oauth.

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

Este es un ejemplo de Python y Django para realizar el redireccionamiento de Facebook oauth.

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

### Nodejs

Este es un ejemplo con nodejs y Sail/Express para realizar el redireccionamiento de Facebook oauth.

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

Este es un ejemplo con los controladores Java y Primavera para realizar el redireccionamiento de Facebook oauth.

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

## Configuración de proveedores de «publicación en» {#section_rdk_dpl_b1b}

De forma predeterminada, los botones de Facebook, linkedin y Twitter «Publicar en» se muestran en las aplicaciones de Livefyre Core. Utilice el parámetro posttobuttons para configurar qué proveedores aparecerán al incrustar la aplicación de Livefyre.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` es una matriz con cualquier subconjunto de las siguientes opciones:

* tw: Twitter
* fb: Facebook
* li: Linkedin
