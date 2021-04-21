---
description: El objeto de configuración Sidenotes es un objeto JSON utilizado para especificar el contenido que la aplicación Livefyre representa en la página.
title: Opciones de configuración de notas
exl-id: efebf9e5-6623-4953-a8f6-c58495304ac1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---

# Muestra las opciones de configuración{#sidenotes-configuration-options}

El objeto de configuración Sidenotes es un objeto JSON utilizado para especificar el contenido que la aplicación Livefyre representa en la página.

El objeto contiene los siguientes parámetros:

| Parámetro | Tipo | Descripción |
|--- |--- |--- |
| authDelegate | ** requiredobject | Delegado de autenticación inicializado de estilo nuevo o antiguo. |
| collectionMeta | ** requiredobject | Consulte collectionMeta token para obtener más información. |
| customIcon | ** cadena opcional | Establece la dirección URL de un icono de lanzador personalizado. El valor predeterminado es la burbuja de Livefyre. |
| customStyles | ** optionalobject | Añade estilos personalizados para cambiar el aspecto de las notas. Para obtener más información, consulte Estilos personalizados. |
| disableStream | ** opcionalBoolean | Si es true, deshabilita la transmisión en tiempo real en esta instancia de Sidenotes (no en otros flujos de comentarios). El valor predeterminado es false. |
| entorno | ** cadena opcional | Especifica el entorno UAT de Livefyre. El único valor posible es `t402.livefyre.com`. Para la producción, se debe eliminar este parámetro. |
| iconVisibility | ** objeto opcional o cadena | Define si el icono Notas estará visible al pasar el ratón o si estará estático. Si se trata de una cadena, se utilizará para ambas versiones del icono de bloque (vacío y con notas). Si un objeto es necesario especificar cada tipo: {vacío: &quot;hover&quot;, num: ‘static’}. El valor predeterminado es estático. |
| inlineThreads | ** opcional booleano | Si es true, los subprocesos de Sidenote se insertan directamente después del bloque con el que están asociados. El valor predeterminado es false. |
| numSidenotesEl | ** objeto opcional, cadena o matriz | Especifica qué elemento decorará el widget de recuento Sidenotes. (Este widget muestra el número de notas de la página y la información sobre notas). Si el selector de cadenas coincide con más de un elemento, se elige el primero. (Utiliza la especificación del selector CSS3 DOM). |
| position | ** cadena opcional | Determina la posición de la ventana emergente cuando se hace clic en un elemento que tiene Sidenotes habilitado. Los valores posibles son &quot;inteligente&quot;, &quot;izquierda&quot;, &quot;derecha&quot;, &quot;inferior&quot;. El valor predeterminado es &quot;inteligente&quot;, que alinea la ventana emergente a la derecha de la página a menos que no haya suficiente espacio (en cuyo caso, se moverá a debajo del contenido). |
| selectores | ** requerido, objeto, cadena o matriz | Especifica los elementos en los que deben aparecer iconos de lanzador. (Utiliza la especificación del selector CSS3 DOM). Si es un objeto, incluye una sección &quot;incluye&quot; y una sección &quot;excluye&quot; que aplicarán el selector de CSS a todas las inclusiones coincidentes y eliminarán los elementos que coincidan con las exclusiones. Si es una cadena, incluirá cualquier elemento coincidente en la página. Si es una matriz, enumera los elementos que desea incluir. |
| cadenas | ** optionalobject | Agrega cadenas de texto personalizadas para cambiar cualquier idioma o texto en la aplicación. Para obtener más información, consulte Cadenas personalizadas. |
| threadContainerEl | ** objeto opcional, cadena o matriz | Especifica un elemento en el que aparecerá el subproceso de las notas laterales. Este parámetro le permite cambiar la posición del subproceso. Si el selector de cadenas coincide con más de un elemento, se elige el primero. (Utiliza la especificación del selector CSS3 DOM). |
