---
description: Personalice las marcas de fecha y hora usando Livefyre. js.
seo-description: Personalice las marcas de fecha y hora usando Livefyre. js.
seo-title: Personalizar la marca de fecha y hora
solution: Experience Manager
title: Personalizar la marca de fecha y hora
uuid: 632 ea 405-56 b 7-4664-8 d 2 b -0 dd 0 a 7611 bd 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizar la marca de fecha y hora{#customize-the-date-and-time-stamp}

Personalice las marcas de fecha y hora usando Livefyre. js.

Las aplicaciones de Livefyre proporcionan el parámetro de opción datetimeformat para especificar el formato de fecha como se describe a continuación.

* [Terminología](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formato](#c_date_time_stamp/section_ynx_gn4_xz)
* [Designación de símbolos](#c_date_time_stamp/section_inq_2n4_xz)

## Terminología {#section_xsk_jn4_xz}

* **Las marcas de hora absolutas** se definen como horas exactas y específicas (p. ej., 1 de enero de 2012 a las 12:00)
* **Las marcas de hora relativas** se definen como tiempos generales y menos precisos (por ejemplo, hace 25 segundos, hace 14 minutos, hace 1 día, 1 año atrás, etc.)

## Formato {#section_ynx_gn4_xz}

El parámetro datetimeformat tiene el siguiente comportamiento predeterminado cuando no se proporciona ningún argumento:

* Formato de fecha de envío de: MMMM d aaaa (para el 8 de enero de 2012)
* 20160 minutos (14 días) hasta un tiempo absoluto (14 días hasta que las marcas de hora relativas pasan a ser marcas de hora absolutas)

El parámetro datetimeformat acepta tres posibles tipos de argumento: datetime, format y string.

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

Objeto que especifica absoluteformat y/o minutesuntilabsolutetime. A minutesuntilabsolutetime con un valor de -1 hará que el tiempo absoluto sea inmediato.

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

Una función que toma como argumento un objeto Date y devuelve una cadena de fecha y hora que se mostrará

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

Las funciones de formato de datetime siguen la especificación de patrón definida en JDK, ICU y CLDR, con una modificación menor para el uso habitual en JS. Para obtener más información, consulte la Documentación de la biblioteca de cierres [de Google](https://developers.google.com/closure/library/docs/overview).

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

Los elementos marcados con &#39; *&#39; aún no son compatibles.

Los elementos marcados con &#39; #&#39; funcionan de forma diferente a Java.

El recuento de las letras patrón determina el formato.

* **Texto:** 4 o más, utilice el formulario completo. Si hay menos de 4, utilice un formulario abreviado o abreviado si existe. (Por ejemplo: «EEEE» produce «Lunes», «EEE» produce «Mon».)
* **Número:** el número mínimo de dígitos. Los números más cortos se rellena con cero a esta cantidad (por ejemplo: Si «m» produce «6», «mm» produce «06».) Año se administra especialmente; es decir, si el recuento de&#39;y&#39;es 2, el año se truncará a 2 dígitos. (Por ejemplo: si «aaaa» produce «1997», «aa» produce «97».) A diferencia de otros campos, los segundos fraccionarios se rellenan a la derecha con cero.
* **Texto y número:** 3 o sobre, utilice texto. Menor que 3, utilice número. (Por ejemplo: «M» produce «1», «MM» produce «01», «MMM» produce «Jan» y «MMMM» produce «Enero».)

Cualquier carácter del patrón que no esté en los rangos de [&#39;a &#39;. &#39;&#39;z&#39;] y [&#39;A &#39;. &#39;&#39;Z&#39;] se tratará como texto citado. Por ejemplo, caracteres como &#39;: &#39;,&#39;. &#39;,&#39;&#39;,&#39; #&#39; y &#39; @&#39; aparecerán en el texto de hora resultante incluso aunque no estén incluidos dentro de comillas simples.
