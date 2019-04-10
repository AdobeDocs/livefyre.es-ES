---
description: Instalación de bibliotecas para tareas en el servidor de Livefyre
seo-description: Instalación de bibliotecas para tareas en el servidor de Livefyre
seo-title: Instalación
solution: Experience Manager
title: Instalación
uuid: f 60 b 4 cc 7-178 f -4 a 16-ba 75-f 1 d 0 d 171 c 52 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Instalación{#installation}


## Java {#section_yd3_3zk_rz}

Para instalar la biblioteca Java, agregue esta dependencia al POM del proyecto:

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

La biblioteca Java tiene dependencias en los módulos siguientes:

```
<dependency> 
   <groupId>com.sun.jersey</groupId> 
   <artifactId>jersey-client</artifactId> 
   <version>[1.18.1,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.code.gson</groupId> 
   <artifactId>gson</artifactId> 
   <version>[2.3,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.guava</groupId> 
   <artifactId>guava</artifactId> 
   <version>[18.0,)</version> 
</dependency> 
<dependency> 
   <groupId>org.apache.commons</groupId> 
   <artifactId>commons-lang3</artifactId> 
   <version>[3.0.1,)</version> 
</dependency> 
<dependency> 
   <groupId>org.bitbucket.b_c</groupId> 
   <artifactId>jose4j</artifactId> 
   <version>[0.4.1,)</version> 
</dependency> 
```

Para obtener más información, lea los documentos de Java o vea la fuente en [github](https://github.com/Livefyre/livefyre-java-utils).

## Nodejs {#section_swj_pwq_rz}

Para instalar la biblioteca nodejs, ejecute esta línea:

`$ npm install livefyre`

La biblioteca nodejs tiene dependencias en los módulos siguientes:

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Para obtener más información, lea los documentos de nodejs o vea la fuente en [github](https://github.com/Livefyre/livefyre-nodejs-utils).

Vínculos: [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Para instalar la biblioteca PHP con Compositor, agregue esto a su compositor. json:

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

A continuación, instale mediante:

```
composer.phar install 
```

Si **no** utiliza Compositor, obtenga la versión más reciente de la biblioteca utilizando:

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Para utilizar la biblioteca, agregue lo siguiente a la secuencia de comandos PHP:

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

La biblioteca PHP tiene dependencias en los módulos siguientes:

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

Para obtener más información, lea los documentos PHP o consulte la fuente en [github](https://github.com/Livefyre/livefyre-php-utils).

Vínculos: [ext-json](https://php.net/manual/en/book.json.php), [solicitudes](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Para instalar la biblioteca Python, ejecute esta línea:

`$ pip install livefyre`

La biblioteca Python tiene dependencias en los módulos siguientes:

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Para obtener más información, lea los documentos Python o vea la fuente en [github](https://github.com/Livefyre/livefyre-python-utils).

Vínculos: [Pyjwt](https://github.com/progrium/pyjwt), [Requests](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum 34](https://pypi.python.org/pypi/enum34), [ordereddict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Para instalar la biblioteca Ruby, agregue esta línea al archivo Gemfile de la aplicación:

```
gem 'livefyre' 
```

O instalarlo usted mismo:

`$ gem install livefyre`

La biblioteca Ruby tiene dependencias en los módulos siguientes:

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Para obtener más información, lea los documentos de Ruby o vea la fuente en [github](https://github.com/Livefyre/livefyre-ruby-utils).

Vínculos: [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST Client](https://github.com/rest-client/rest-client/), [Direcsable](https://github.com/sporkmonger/addressable)
