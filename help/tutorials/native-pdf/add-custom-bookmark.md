---
title: Función de publicación de PDF nativo | Agregar un marcador personalizado en la salida del PDF
description: Aprenda a crear hojas de estilo y crear estilos para el contenido.
source-git-commit: fb7ffbaefcdca4302e43d8369bc056c1f08a3ed6
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# Añadir un marcador personalizado en la salida del PDF

Por lo general, la tabla de contenido de un mapa DITA se duplica como marcadores en la salida final del PDF. Esta tabla de contenido se crea a partir de los títulos de temas o secciones de su mapa DITA. A veces, es posible que desee agregar un marcador personalizado a un contenido en particular en la salida del PDF para facilitar la navegación. Esto se puede lograr añadiendo un `outputclass` en el elemento y aplicándole el siguiente atributo:

`bookmark-level: 3`

Aquí, la variable `bookmark-level` es un atributo y un número `3` es el valor que indica el nivel en la jerarquía de marcadores donde se agrega el marcador. En el siguiente ejemplo, el tema de primer nivel &quot;Contactos&quot; tiene una tabla, &quot;Lista de contactos&quot;, en la que hemos añadido una `outputclass` con el valor de `custom-bookmark`.


<img src="./assets/custom-bookmark-attribute.png" width="500">

La siguiente definición de `custom-bookmark` se añade en el archivo CSS:

```css
…
/*Adding a custom bookmark*/
.custom-bookmark{
    bookmark-level: 2
}
…
```

En la salida del PDF, la variable *Lista de contactos* se añade en el segundo nivel de la lista de marcadores del PDF, como se muestra a continuación:

<img src="./assets/custom-bookmark-in-pdf-output.png" width="500">

>[!NOTE]
>
>Debe elegir el nivel correcto donde se agrega el marcador personalizado. Si especifica un número menor que el marcador del tema principal, el marcador personalizado tomará la posición del marcador principal y todos los demás marcadores se mostrarán como secundarios. Esto puede provocar una estructura de marcadores inesperada.

