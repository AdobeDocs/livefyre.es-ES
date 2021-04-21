---
description: Cuente el número de elementos sociales depurados.
title: Contador social
exl-id: def7fba4-1c2e-4c7b-84f7-f9ede592d675
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 10%

---

# Contador social{#social-counter}

Cuente el número de elementos sociales depurados. Para obtener una lista completa de los puntos finales disponibles, consulte la sección [Referencia de API](https://api.livefyre.com/docs) de Livefyre.

La API del contador de Social devuelve recuentos de reglas de depuración coincidentes en una colección determinada para intervalos a lo largo de un período de tiempo.

>[!NOTE]
>
>Esta API solo está disponible para hashtags de Twitter.

API del contador social:

* Recurso
* Tipos de reglas
* Respuesta

## Recurso {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **networkName:** su nombre de red proporcionado por Livefyre. Por ejemplo: *labs* en `labs.fyre.co`.
* **consulta:** hash codificado base64 seguro para url de todo el sitio, ID de artículo, tupoles de tipo regla para los que se debe recuperar información de recuento (precodificado)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >La consulta está limitada a 10 sitios, ID de artículo y tupoles de tipo regla. (El ejemplo anterior contendría 3 tuplas).

* **** `(optional)` especifica el período de tiempo relativo o absoluto para el gráfico; from especifica el inicio y el valor predeterminado es 24 horas atrás, si se omite.
* **** `(optional)` hasta especifica el período de tiempo relativo o absoluto para el gráfico; hasta especifica el principio y el valor predeterminado es la hora actual (ahora), si se omite.

### Tiempo relativo

| Abreviación | Unidad |
|---|---|
| s | Segundos |
| min | Minutos |
| h | Horas |
| d | Días |
| w | semanas |
| mon | 30 días (mes) |
| y | 365 Días (Año) |

Ejemplo:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Tiempo absoluto {#section_xqr_jgc_11b}

FORMATO: HH:MM_YYYMMDD

| Abreviación | Significado |
|---|---|
| HH | Horas (en formato de reloj de 24 horas) |
| MM | Minutos |
| YYYY | Año de 4 dígitos |
| MM | Mes |
| DD | Día |

Ejemplo:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## Tipos de reglas {#section_v53_xqb_11b}

| Valor | Tipo |
|---|---|
| 2 | Twitter |

Ejemplo:

Para obtener recuentos a lo largo del último minuto para el sitio `123456` y el ID de artículo `some-article-id` y el tipo de regla `2`, por ejemplo: `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

Respuesta de ejemplo:

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
