---
description: Notas de la versión de la versión del 18 de enero de 2018.
title: 18 de enero de 2018
exl-id: aaf49dc9-64eb-4354-8bcb-04039fa25f10
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 7%

---

# 18 de enero de 2018{#january}

Notas de la versión de la versión del 18 de enero de 2018.

## Versión de producción

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | Aplicaciones | Se ha corregido un error que impedía que los avatares se representaran correctamente cuando se estaba utilizando un archivo jpeg. |
| Error, | ModQ | Se ha corregido un error para los clientes de S1 que permitía el filtrado por colecciones en ModQ. |
| Error, | Transmisiones | Se ha corregido un error que rompía una regla de flujo cuando el filtro de idioma estaba establecido como &quot;ninguno&quot;. |
| Error, | Transmisiones | Se ha corregido un error que impedía guardar las reglas de flujo de YouTube. |
| Error, | Transmisiones | Corrige un error en el que los usuarios podían crear entradas geográficas con formato incorrecto en las reglas de flujo y guardarlas, lo que provocaba que el flujo fallara. Ahora, los usuarios ya no pueden guardar etiquetas geográficas con formato incorrecto. |
| Error, | Studio | Se ha corregido un problema que impedía que algunos usuarios iniciaran sesión en Livefyre. |

## Versión de UAT

| **Tipo de incidencia** | **Componente** | **Nota de la versión** |
|---|---|---|
| Error, | Biblioteca | Corrección de errores de seguridad. Todas las llamadas de autenticación se realizan ahora mediante el protocolo HTTPS en lugar de HTTP. |
| Mejora | Etiquetas inteligentes | Adobe Sensei ahora etiqueta automáticamente el contenido transmitido de forma inteligente, ya que se guarda en una carpeta o se publica en una aplicación. |
| Error, | Transmisiones | Se ha corregido un problema por el cual las reglas de flujo de Instagram no reconocían caracteres japoneses. |
| Mejora | Transmisiones | Los clientes ahora pueden usar los operadores lógicos ( CUALQUIERA, TODOS, NO) para crear filtros detallados de etiquetas inteligentes en flujos que depuran contenido mucho más preciso. Por ejemplo, si utilizo la etiqueta #himalyas puedo elegir mostrar solamente imágenes que incluyan &quot;montañas nevadas&quot;. |
| Error, | Studio | Se ha corregido un error que mostraba caracteres especiales en nombres como HTML. |
