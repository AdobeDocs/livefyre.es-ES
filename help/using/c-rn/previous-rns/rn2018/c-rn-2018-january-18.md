---
description: Notas de la versión de la versión del 18 de enero de 2018.
seo-description: Notas de la versión de la versión del 18 de enero de 2018.
seo-title: 18 de enero de 2018
solution: Experience Manager
title: 18 de enero de 2018
uuid: 8141 f 431-c 154-4 c 8 f-bbcd-b 7 c 712 fe 5 f 7 d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 18 de enero de 2018{#january}

Notas de la versión de la versión del 18 de enero de 2018.

## Versión de producción

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Error | Aplicaciones | Se ha corregido un error que impedía que Avatars se procesara correctamente al utilizar un archivo JPEG. |
| Error | Modq | Se ha corregido un error para los clientes de S 1 que permitía filtrar por colecciones en modq. |
| Error | Flujos | Se ha corregido un error que rompió una regla de flujo cuando el filtro de idioma se establecía como "ninguno". |
| Error | Flujos | Se ha corregido un error que impedía guardar reglas de flujo de Youtube. |
| Error | Flujos | Corrige un error en el que los usuarios podían crear entradas geográficas con formato incorrecto en reglas de flujo y guardarlas, lo que provocaba errores en el flujo. Ahora, los usuarios ya no pueden guardar etiquetas geográficas con formato incorrecto. |
| Error | Studio | Se ha corregido un problema que impedía que algunos usuarios iniciaran sesión en Livefyre. |

## Versión de UAT

| **Tipo de problema** | **Componente** | **Versión de la versión** |
|---|---|---|
| Error | Biblioteca | Corrección de errores de seguridad. Todas las llamadas de autenticación se realizan ahora mediante el protocolo HTTPS en lugar de HTTP. |
| Mejora | Etiquetas inteligentes | El contenido transmitido ahora es etiquetado automáticamente por Adobe Sensei cuando se guarda en una carpeta o se publica en una aplicación. |
| Error | Flujos | Se corrigió un problema en el cual las reglas de flujo de Instagram no reconocían caracteres japoneses. |
| Mejora | Flujos | Los clientes ahora pueden utilizar operadores lógicos (ANY, ALL, NOT) para crear filtros de etiquetas inteligentes detallados en flujos que depuran contenido mucho más preciso. Por ejemplo, si utilizo el hashtag # himalyas, puede seleccionar mostrar solo imágenes que incluyan "nevadas" "montañas". |
| Error | Studio | Se ha corregido un error que mostraba caracteres especiales en nombres como HTML. |

