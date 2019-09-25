---
description: Notas de la versión de la versión del 18 de enero de 2018.
seo-description: Notas de la versión de la versión del 18 de enero de 2018.
seo-title: 18 de enero de 2018
solution: Experience Manager
title: 18 de enero de 2018
uuid: 8141f431-c154-4c8f-bcd-b7c712fe5f7d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# January 18, 2018{#january}

Notas de la versión de la versión del 18 de enero de 2018.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | Aplicaciones | Se ha corregido un error que impedía que los avatares se procesaran correctamente cuando se usaba un archivo jpeg. |
| Error, | ModQ | Se ha corregido un error que permitía a los clientes de S1 filtrar por colecciones en ModQ. |
| Error, | Flujos | Se ha corregido un error que rompía una regla de flujo cuando el filtro de idioma se establecía como "ninguno". |
| Error, | Flujos | Se ha corregido un error que impedía guardar las reglas de flujo de YouTube. |
| Error, | Flujos | Se corrige un error en el cual los usuarios podían crear entradas geográficas con formato incorrecto en las reglas de flujo y guardarlas, lo que ocasionaba que fallara el flujo. Ahora, los usuarios ya no pueden guardar etiquetas geográficas con formato incorrecto. |
| Error, | Studio | Se ha corregido un problema que impedía que algunos usuarios iniciaran sesión en Livefyre. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de versión** |
|---|---|---|
| Error, | Biblioteca | Corrección de errores de seguridad. Todas las llamadas de autenticación ahora se realizan mediante el protocolo HTTPS en lugar de HTTP. |
| Mejora | Etiquetas inteligentes | Ahora, Adobe Sensei etiqueta automáticamente el contenido transmitido de forma inteligente al guardarlo en una carpeta o publicarlo en una aplicación. |
| Error, | Flujos | Se corrigió un problema en el cual las reglas de flujo de Instagram no reconocían caracteres japoneses. |
| Mejora | Flujos | Ahora los clientes pueden utilizar los operadores lógicos ( CUALQUIER, TODOS, NO) para crear filtros detallados de etiquetas inteligentes en flujos que depuran contenido mucho más preciso. Por ejemplo, si utilizo la etiqueta #himalyas puedo elegir mostrar solo imágenes que incluyan "montañas nevadas". |
| Error, | Studio | Se ha corregido un error que mostraba caracteres especiales en nombres como HTML. |

