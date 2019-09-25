---
description: Cuenta el número de elementos sociales seleccionados.
seo-description: Cuenta el número de elementos sociales seleccionados.
seo-title: Contador social
solution: Experience Manager
title: Contador social
uuid: fa9aa1a8-6a04-4bc1-9bfe-e42c1250fd48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Contador social{#social-counter}

Cuenta el número de elementos sociales seleccionados. Para obtener una lista completa de los extremos disponibles, consulte la sección Referencia [de la](https://api.livefyre.com/docs) API de Livefyre.

La API de contador social devuelve recuentos de reglas de depuración coincidentes en una colección determinada para intervalos a lo largo de un período de tiempo.

>[!NOTE]
>
>Esta API solo está disponible para hashtags de Twitter.

API de contador social:

* Recurso
* Tipos de reglas
* Respuesta

## Recurso {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **** networkName:El nombre de red proporcionado por Livefyre. Por ejemplo: *laboratorios* en `labs.fyre.co`.
* **** consulta: El hash codificado de base64 seguro para url de todo el sitio, ID del artículo, tuplas de tipo de regla para las que se debe recuperar información de recuento (precodificado)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >La consulta está limitada a 10 tutoriales de tipo regla, ID de artículo, sitio y sitio. (El ejemplo anterior contendría 3 tuplas).

* **from** `(optional)` especifica el período de tiempo relativo o absoluto para el gráfico; from especifica el comienzo y el valor predeterminado es 24 horas atrás, si se omite.
* **hasta** que `(optional)` especifique el período de tiempo relativo o absoluto para el gráfico; hasta especifica el principio y el valor predeterminado es la hora actual (ahora), si se omite.

### Tiempo relativo

| Abreviación | Unidad |
|---|---|
| s | Segundos |
| min | Minutos |
| h | Horas |
| d | Días |
| w | semanas |
| mon | 30 días (mes) |
| y | 365 días (año) |

Ejemplo:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Hora absoluta {#section_xqr_jgc_11b}

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

Para obtener recuentos a lo largo del último minuto para la ID del sitio `123456` y del artículo `some-article-id` y el tipo de regla `2`, por ejemplo: `123456:some-article-id;2:`

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
