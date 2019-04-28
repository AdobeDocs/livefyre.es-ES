---
description: El objeto config Sidenotes es un objeto JSON utilizado para especificar el contenido que la aplicación de Livefyre procesa en la página.
seo-description: El objeto config Sidenotes es un objeto JSON utilizado para especificar el contenido que la aplicación de Livefyre procesa en la página.
seo-title: Opciones de configuración de Sidenotes
solution: Experience Manager
title: Opciones de configuración de Sidenotes
uuid: 067 e 51 e 6-9720-4226-a 805-c 7 a 07 c 8 cdaa 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Opciones de configuración de Sidenotes{#sidenotes-configuration-options}

El objeto config Sidenotes es un objeto JSON utilizado para especificar el contenido que la aplicación de Livefyre procesa en la página.

El objeto contiene los parámetros siguientes:

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| Authdelegate | *required* object | Delegado de autenticación inicializado nuevo o antiguo. |
| Collectionmeta | *required* object | Consulte collectionmeta token para obtener más información. |
| Customicon | *optional* string | Define la URL de un icono de iniciador personalizado. Defaults to Livefyre Bubble. |
| Customstyles | *optional* object | Agrega estilos personalizados para cambiar el aspecto y la presentación de Sidenotes. Para obtener más información, consulte Estilos personalizados. |
| Disablestream | *optional* Boolean | Si es true, deshabilita el flujo en tiempo real en esta instancia Sidenotes (no en otros flujos de comentarios). El valor predeterminado es false. |
| entorno | *optional* string | Especifica el entorno de UAT de Livefyre. El único valor posible `t402.livefyre.com`es. Para producción, este parámetro debe eliminarse. |
| Iconvisibility | *objeto o* cadena opcional | Define si el icono Sidenotes estará visible al pasar el ratón por encima o por estático. Si es una cadena, se utilizará para ambas versiones del icono de bloque (vacío y tiene Sidenotes). Si un objeto es, debe especificar cada tipo: {vacío: &#39; hover &#39;, num: &#39; static &#39;}. El valor predeterminado es estático. |
| Inlinethreads | *optional* boolean | Si es true, los hilos Sidenote se insertan directamente después del bloque con el que están asociados. El valor predeterminado es false. |
| Numsidenotesel | *objeto,* cadena o matriz opcional | Especifica qué elemento decorará el widget de recuento Sidenotes. (Esta utilidad muestra el número de sidras en la página e información sobre Sidenotes). Si el selector de cadena coincide con más de un elemento, se elegirá la primera. (Utiliza la especificación del selector DOM de CSS 3). |
| position | *optional* string | Determina la posición de la ventana emergente cuando se hace clic en un elemento con Sidenotes habilitado. Los valores posibles son &quot;smart&quot;, &quot;left&quot;, &quot;right&quot;, &quot;bottom&quot;. El valor predeterminado es&#39;inteligente &#39;, que alinea la ventana emergente a la derecha de la página, a menos que no haya espacio suficiente (en cuyo caso se desplazará por debajo del contenido). |
| selectores | *objeto,* cadena o matriz requeridos | Especifica los elementos en los que deben aparecer los iconos del iniciador. (Utiliza la especificación del selector DOM de CSS 3). Si se trata de un objeto, incluye una sección «incluye» y una sección «excluye» que aplicará el selector de CSS para cualquier coincidencia incluida, y elimine cualquier elemento que coincida con las exclusiones. Si la cadena es, incluirá cualquier elemento coincidente en la página. Si la matriz es, enumera los elementos que incluir. |
| cadenas | *optional* object | Agrega cadenas de texto personalizadas para cambiar cualquier idioma o texto de la aplicación. Para obtener más información, consulte Cadenas personalizadas. |
| Threadcontainerel | *objeto,* cadena o matriz opcional | Especifica un elemento donde aparecerá el hilo de sidenotes. Este parámetro permite cambiar la posición del hilo. Si el selector de cadena coincide con más de un elemento, se elegirá la primera. (Utiliza la especificación del selector DOM de CSS 3). |

