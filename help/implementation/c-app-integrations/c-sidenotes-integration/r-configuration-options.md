---
description: El objeto de configuración Sidenotes es un objeto JSON utilizado para especificar el contenido que la aplicación Livefyre representa en la página.
seo-description: El objeto de configuración Sidenotes es un objeto JSON utilizado para especificar el contenido que la aplicación Livefyre representa en la página.
seo-title: Muestra las opciones de configuración
solution: Experience Manager
title: Muestra las opciones de configuración
uuid: 067e51e6-9720-4226-a805-c7a07c8cdaa0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Muestra las opciones de configuración{#sidenotes-configuration-options}

El objeto de configuración Sidenotes es un objeto JSON utilizado para especificar el contenido que la aplicación Livefyre representa en la página.

El objeto contiene los parámetros siguientes:

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| authDelegate | *objeto requerido* | Delegado de autenticación inicializado de estilo nuevo o antiguo. |
| collectionMeta | *objeto requerido* | Consulte collectionMeta token para obtener más información. |
| customIcon | *cadena opcional* | Define la dirección URL de un icono de iniciador personalizado. Valores predeterminados de la burbuja Livefyre. |
| customStyles | *objeto opcional* | Agrega estilos personalizados para cambiar el aspecto de Sidenotes. Para obtener más información, consulte Estilos personalizados. |
| disableStream | *booleano opcional* | Si es true, deshabilita el flujo en tiempo real en esta instancia de Sidenotes (no en otros flujos de comentarios). El valor predeterminado es false. |
| entorno | *cadena opcional* | Especifica el entorno UAT de Livefyre. El único valor posible es `t402.livefyre.com`. Para la producción, este parámetro debe eliminarse. |
| iconVisibility | *objeto opcional* o cadena | Define si el icono de Sidenotes estará visible al pasar el ratón o si será estático. Si es una cadena, se utilizará para ambas versiones del icono de bloque (vacío y con Sidenotes). Si hay un objeto, debe especificar cada tipo: {empty: "hover", num: ‘static’}. El valor predeterminado es estático. |
| inlineThwords | *booleano opcional* | Si es true, los subprocesos de Sidenote se insertan directamente después del bloque con el que están asociados. El valor predeterminado es false. |
| numSidenotesEl | *objeto opcional* , cadena o matriz | Especifica qué elemento decorará el widget de recuento de Sidenotes. (Esta utilidad muestra el número de notas de la página y la información sobre las notas de identidad). Si el selector de cadenas coincide con más de un elemento, se elegirá el primero. (Utiliza la especificación del selector CSS3 DOM). |
| position | *cadena opcional* | Determina la posición de la ventana emergente cuando se hace clic en un elemento que tiene Sidenotes activado. Los valores posibles son "inteligente", "izquierda", "derecha", "inferior". El valor predeterminado es ‘inteligente’, que alinea la ventana emergente a la derecha de la página a menos que no haya espacio suficiente (en cuyo caso se moverá a debajo del contenido). |
| selectores | *objeto, cadena o matriz requerido* | Especifica los elementos en los que deben aparecer los iconos del iniciador. (Utiliza la especificación del selector CSS3 DOM). Si es un objeto, incluye una sección "incluye" y una sección "excluye" que aplicará el selector de CSS a cualquier inclusión coincidente y eliminará los elementos que coincidan con las exclusiones. Si es una cadena, incluirá cualquier elemento coincidente en la página. Si matriz, enumera los elementos que se van a incluir. |
| cadenas | *objeto opcional* | Agrega cadenas de texto personalizadas para cambiar cualquier idioma o texto en toda la aplicación. Para obtener más información, consulte Cadenas personalizadas. |
| threadContainerEl | *objeto opcional* , cadena o matriz | Especifica un elemento en el que aparecerá el subproceso de las notas al final. Este parámetro le permite cambiar la posición del subproceso. Si el selector de cadenas coincide con más de un elemento, se elegirá el primero. (Utiliza la especificación del selector CSS3 DOM). |

