---
description: Instalación de bibliotecas para tareas del lado del servidor de Livefyre
title: Instalación
exl-id: d74f85be-14c0-4f6d-8f16-b688282c0eb0
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---

# Instalación{#installation}


## Java {#section_yd3_3zk_rz}

Para instalar la biblioteca Java, agregue esta dependencia al POM de su proyecto:

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

La biblioteca Java depende de los siguientes módulos:

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

Para obtener más información, lea los documentos de Java o consulte la fuente en [GitHub](https://github.com/Livefyre/livefyre-java-utils).

## NodeJS {#section_swj_pwq_rz}

Para instalar la biblioteca NodeJS, ejecute esta línea:

`$ npm install livefyre`

La biblioteca NodeJS depende de los siguientes módulos:

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Para obtener más información, lea los documentos de NodeJs o vea la fuente en [GitHub](https://github.com/Livefyre/livefyre-nodejs-utils).

Vínculos: [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Para instalar la biblioteca PHP con Composer, añádala a su composer.json:

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

A continuación, instale utilizando:

```
composer.phar install 
```

Si **no** utiliza el Compositor, obtenga la versión más reciente de la biblioteca utilizando:

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Para usar la biblioteca, agregue lo siguiente a su script PHP:

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

La biblioteca PHP tiene dependencias en los siguientes módulos:

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

Para obtener más información, lea los documentos PHP o vea la fuente en [GitHub](https://github.com/Livefyre/livefyre-php-utils).

Vínculos: [ext-json](https://php.net/manual/en/book.json.php), [Solicitudes](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Para instalar la biblioteca Python, ejecute esta línea:

`$ pip install livefyre`

La biblioteca Python depende de los siguientes módulos:

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Para obtener más información, lea los documentos de Python o vea la fuente en [GitHub](https://github.com/Livefyre/livefyre-python-utils).

Vínculos: [PyJWT](https://github.com/progrium/pyjwt), [Solicitudes](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum34](https://pypi.python.org/pypi/enum34), [OrderedDict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Para instalar la biblioteca Ruby, añada esta línea al Gemfile de su aplicación:

```
gem 'livefyre' 
```

O instálelo usted mismo:

`$ gem install livefyre`

La biblioteca Ruby tiene dependencias en los siguientes módulos:

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Para obtener más información, lea los documentos de Ruby o consulte la fuente en [GitHub](https://github.com/Livefyre/livefyre-ruby-utils).

Vínculos: [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST Client](https://github.com/rest-client/rest-client/), [Direccionable](https://github.com/sporkmonger/addressable)
