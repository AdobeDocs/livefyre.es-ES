---
description: Contabilice el número de elementos sociales seleccionados.
seo-description: Contabilice el número de elementos sociales seleccionados.
seo-title: Contador social
solution: Experience Manager
title: Contador social
uuid: fa 9 aa 1 a 8-6 a 04-4 bc 1-9 bfe-e 42 c 1250 fd 48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Contador social{#social-counter}

Contabilice el número de elementos sociales seleccionados. Para obtener una lista completa de los puntos finales disponibles, consulte la sección Referencia [de la API](https://api.livefyre.com/docs) de Livefyre.

La API de contador social devuelve recuentos para reglas de depuración coincidentes en una colección determinada para intervalos durante un período de tiempo.

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

* **Networkname:** Su Livefyre ha proporcionado el nombre de la red. Por ejemplo: *labs* in `labs.fyre.co`.
* **query:** El hash codificado de la base 64 de todo el sitio, ID del artículo, tuples de tipo regla para los que se debe recuperar información de recuento (precodificado)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >La consulta está limitada a 10 sitios, ID de artículo y tuples de regla. (El ejemplo anterior contiene 3 tonos).

* **from** `(optional)` especifica the relative or absolute time period to graph; from especifica the start and defaults to 24 hours, if omused.
* **hasta** `(optional)` que especifica el período de tiempo relativo o absoluto al gráfico; hasta que especifica el comienzo y el valor predeterminado del tiempo actual (ahora), si se omite.

### Tiempo relativo

| Abreviación | Unidad |
|---|---|
| s | Segundos |
| min | Minutos |
| h | Horas |
| d | Días |
| w | Semanas |
| mon | 30 días (mes) |
| y | 365 días (año) |

Ejemplo:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Tiempo absoluto {#section_xqr_jgc_11b}

FORMATO: HH: MM_ AAAAMMDD

| Abreviación | Significado |
|---|---|
| HH | Horas (en formato de reloj de 24 h) |
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

Para obtener recuentos en el último momento del sitio `123456` y del ID de artículo `some-article-id` y de artículo `2`, por ejemplo: `123456:some-article-id;2:`

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
