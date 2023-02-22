---
title: Función de publicación de PDF nativo | Utilizar JavaScript para trabajar con contenido o estilo
description: Aprenda a crear hojas de estilo y crear estilos para el contenido.
source-git-commit: 09918abbdade934468dea1c55d0ca2cd60622b35
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 1%

---


# Uso de JavaScript para trabajar con contenido o estilo

La función Publicación de PDF nativos permite ejecutar JavaScript para manipular el contenido o el estilo que se aplique al contenido antes de que se genere el PDF final. Esta función le permite controlar completamente cómo se genera el resultado final. Por ejemplo, es posible que desee agregar información de aviso legal a la salida del PDF, que reside en otro PDF. Con JavaScript, se puede añadir la información de aviso legal una vez que se haya creado el PDF para el contenido base, pero antes de que se genere el PDF final.\
Para admitir la ejecución de JavaScript, la función Publicación de PDF nativos le ofrece las siguientes funciones de llamada de retorno:

* `window.pdfLayout.onBeforeCreateTOC(callback)`: Esta función de llamada de retorno se ejecuta antes de que se genere el TOC.
* `window.pdfLayout.onBeforePagination(callback)`: Esta función de llamada de retorno se ejecuta después de que se genere la tabla de contenido, pero antes de que se agreguen los saltos de página en el PDF.
* `window.pdfLayout.onAfterPagination(callback)`: Esta función de llamada de retorno se ejecuta después del TOC y los saltos de página se añaden en el PDF .

>[!NOTE]
>
>Internamente, se mantiene una secuencia de ejecución para estas funciones de llamada. En primer lugar, se ejecuta onBeforeCreateTOC, se ejecuta onBeforePagination y, finalmente, se ejecuta onAfterPagination.

En función del tipo de contenido o de modificación de estilo que desee realizar, puede elegir qué función de llamada de retorno utilizar. Por ejemplo, si desea añadir contenido, se recomienda hacerlo antes de que se genere la tabla de contenido. Del mismo modo, si desea realizar algunas actualizaciones de estilo, estas se pueden realizar antes o después de la paginación.

En el siguiente ejemplo, la posición de los títulos de las figuras cambia de a encima de las imágenes a debajo de las imágenes. Para ello, debe activar la opción de ejecución de JavaScript en el ajuste preestablecido. Para ello, realice los siguientes pasos:

1. Abra el ajuste preestablecido para editarlo.
1. Vaya a la **Avanzadas** pestaña .
1. Seleccione el **Habilitar JavaScript** .
1. Guarde el ajuste preestablecido y cierre.

A continuación, cree un archivo JavaScript con el siguiente código y guárdelo en la carpeta Recursos de la plantilla:

```css
...
/*
* DITA only allows the figure title to be placed above images 
* This JavaScript code is used to move the figure title below the image
* */
window.addEventListener('DOMContentLoaded', function () {
    window.pdfLayout.onBeforeCreateTOC(function() {
        var titleNodes = document.querySelectorAll('.fig > .title')
        for (var i = 0; i < titleNodes.length; i++) {
            var titleNode = titleNodes[i]
            var figNode = titleNode.parentNode
            var imageNode = figNode.querySelector('.image')
            if(imageNode && imageNode.parentNode !== figNode) {
              imageNode = imageNode.parentNode
            }
            if (figNode && imageNode && imageNode.parentNode === figNode) {
                figNode.insertBefore(imageNode, titleNode)
            }
        }
    })
});
...
```

>[!NOTE]
>
>La variable `window.addEventListener('DOMContentLoaded', function ()` antes de utilizar las funciones de rellamada.

A continuación, se debe llamar a esta secuencia de comandos desde un archivo de plantilla que se utilice para generar la salida del PDF. Para nuestro ejemplo, lo agregaremos en la plantilla de tabla de contenido. Asegúrese de que la variable `<script>` se añade dentro de un `<div>` dentro de la variable `<body>` etiqueta. Si lo agrega en la variable `<head>` o fuera de la etiqueta `<body>` , la secuencia de comandos no se ejecutará.

<img src="./assets/js-added-resources-template.png" width="500">

El resultado generado con este código, y la plantilla muestra el título de la figura debajo de la imagen:

<img src="./assets/fig-title-below-image.png" width="500">
