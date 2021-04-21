---
description: Personalice las marcas de fecha y hora con Livefyre.js.
title: Personalizar la marca de fecha y hora
exl-id: 77130793-00ba-4a5c-8318-4221d971da6c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---

# Personalizar la marca de fecha y hora{#customize-the-date-and-time-stamp}

Personalice las marcas de fecha y hora con Livefyre.js.

Las aplicaciones de Livefyre proporcionan el parámetro de opción, datetimeFormat, para especificar el formato de fecha como se describe a continuación.

* [Terminología](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formato](#c_date_time_stamp/section_ynx_gn4_xz)
* [Designación de símbolos](#c_date_time_stamp/section_inq_2n4_xz)

## Terminología {#section_xsk_jn4_xz}

* **Las** Marcas de hora absolutas se definen como horas exactas y específicas (por ejemplo, 1 de enero de 2012 a las 12:00 h)
* **Las** marcas de tiempo relativas se definen como tiempos generales y menos precisos (por ejemplo, hace 25 segundos, hace 14 minutos, hace 1 día, hace 1 año, etc.)

## Formato {#section_ynx_gn4_xz}

El parámetro datetimeFormat tiene el siguiente comportamiento predeterminado cuando no se proporciona ningún argumento:

* Formato de fecha y hora: MMMM d aaaa (para el 8 de enero de 2012)
* 20160 Minutos (14 días) hasta el tiempo absoluto (14 días hasta que las marcas de tiempo relativas se conviertan en marcas de tiempo absolutas)

El parámetro datetimeFormat acepta tres tipos de argumento posibles: fecha, hora, formato y cadena.

```
// Example 1 (Datetime format string)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": 'MMM d y Ka' 
}; 
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Un objeto que especifica AbsoluteFormat y/o minutesUntilAbsoluteTime. Un minutesUntilAbsoluteTime con un valor de -1 hará que el tiempo sea absoluto inmediato.

```
// Example 2 (Object)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": { 
      minutesUntilAbsoluteTime: 10, 
      absoluteFormat: 'MMM d y Ka' 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Una función que toma como argumento un objeto Date y devuelve una cadena datetime que se va a mostrar

```
// Example 3 (Function accepting a Date object, returning a datetime string to display) 
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": function(theDateInput) { 
      return +theDateInput; 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

## Designación de símbolos {#section_inq_2n4_xz}

Funciones de formato de fecha y hora siguiendo la especificación de patrón definida en JDK, ICU y CLDR, con pequeñas modificaciones para uso típico en JS. Para obtener más información, consulte la [Documentación de la biblioteca de cierre de Google](https://developers.google.com/closure/library/docs/overview).

```
  Symbol Meaning Presentation        Example 
  ------   -------                 ------------        ------- 
  G        era designator          (Text)              AD 
  y#       year                    (Number)            1996 
  Y* year (week of year)     (Number)            1997 
  u* extended year           (Number)            4601 
  M        month in year           (Text & Number)     July & 07 
  d        day in month            (Number)            10 
  h        hour in am/pm (1~12)    (Number)            12 
  H        hour in day (0~23)      (Number)            0 
  m        minute in hour          (Number)            30 
  s        second in minute        (Number)            55 
  S        fractional second       (Number)            978 
  E        day of week             (Text)              Tuesday 
  e* day of week (local 1~7) (Number)            2 
  D* day in year             (Number)            189 
  F* day of week in month    (Number)            2 (2nd Wed in July) 
  w* week in year            (Number)            27 
  W* week in month           (Number)            2 
  a        am/pm marker            (Text)              PM 
  k        hour in day (1~24)      (Number)            24 
  K        hour in am/pm (0~11)    (Number)            0 
  z        time zone               (Text)              Pacific Standard Time 
  Z        time zone (RFC 822)     (Number)            -0800 
  v        time zone (generic)     (Text)              Pacific Time 
  g* Julian day              (Number)            2451334 
  A* milliseconds in day     (Number)            69540000 
  '        escape for text         (Delimiter)         'Date=' 
  ''       single quote            (Literal)           'o''clock'
```

Los elementos marcados con &quot;*&quot; aún no son compatibles.

Los elementos marcados con &quot;#&quot; funcionan de forma diferente a Java.

El recuento de letras de patrón determina el formato.

* **Texto:** 4 o más, utilice el formulario completo. Menos de 4, utilice un formulario corto o abreviado si existe. (Por ejemplo: &quot;EEEE&quot; produce &quot;lunes&quot;, &quot;EEE&quot; produce &quot;Mon&quot;.)
* **Número:** el número mínimo de dígitos. Los números más cortos se añaden con cero a esta cantidad (por ejemplo: Si &quot;m&quot; produce &quot;6&quot;, &quot;mm&quot; produce &quot;06&quot;.). El año se manipula especialmente; es decir, si el recuento de &quot;y&quot; es 2, el año se truncará a 2 dígitos. (Por ejemplo: si &quot;yyyy&quot; produce &quot;1997&quot;, &quot;yy&quot; produce &quot;97&quot;.) A diferencia de otros campos, los segundos fraccionarios se añaden a la derecha con cero.
* **Texto y número:** 3 o más, use texto. Menor que 3, utilice número. (Por ejemplo: &quot;M&quot; produce &quot;1&quot;, &quot;MM&quot; produce &quot;01&quot;, &quot;MMM&quot; produce &quot;Jan&quot; y &quot;MMMM&quot; produce &quot;Enero&quot;.)

Cualquier carácter del patrón que no esté en los rangos de [‘a’..’z’] y [‘A’.&quot;Z’] se tratará como texto citado. Por ejemplo, en el texto temporal resultante aparecerán caracteres como ‘:’, ‘.’, ‘, ‘#’ y ‘@’, aunque no se acepten entre comillas simples.
