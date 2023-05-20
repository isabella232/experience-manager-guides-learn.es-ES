---
title: Función de publicación nativa de PDF | Usar JavaScript para trabajar con contenido o estilo
description: Aprenda a crear hojas de estilo de uso y a crear estilos para el contenido.
exl-id: 2f301f6a-0d1c-4194-84c2-0fddaef8d3ec
source-git-commit: e2349fc14143e5e49f8672ef1bfa48984df3b1c7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 1%

---

# Usar JavaScript para trabajar con contenido o estilo

La función Publicación de PDF nativo permite ejecutar JavaScript para manipular el contenido o el estilo aplicados al contenido antes de que se genere el PDF final. Esta función le proporciona un control completo sobre cómo se genera la salida final. Por ejemplo, es posible que desee agregar información de aviso legal a la salida del PDF, que reside en otro PDF. Con JavaScript, puede añadir la información de aviso legal una vez que el PDF se haya creado para el contenido base, pero antes de que se genere el PDF final.\
Para admitir la ejecución de JavaScript, la función de publicación de PDF nativo le ofrece las siguientes funciones de devolución de llamada:

* `window.pdfLayout.onBeforeCreateTOC(callback)`: Esta función de llamada de retorno se ejecuta antes de que se genere la tabla de contenido.
* `window.pdfLayout.onBeforePagination(callback)`: Esta función de llamada de retorno se ejecuta después de generar la TDC, pero antes de que se añadan saltos de página en el PDF.
* `window.pdfLayout.onAfterPagination(callback)`: Esta función de llamada de retorno se ejecuta después de añadir la tabla de contenido y los saltos de página en el PDF.

>[!NOTE]
>
>Internamente, se mantiene una secuencia de ejecución para estas funciones de rótulo. En primer lugar, se ejecuta onBeforeCreateTOC, seguido de onBeforePagination y, por último, se ejecuta onAfterPagination.

En función del tipo de contenido o modificación de estilo que desee realizar, puede elegir qué función de llamada de retorno utilizar. Por ejemplo, si desea agregar contenido, se recomienda hacerlo antes de generar la TDC. Del mismo modo, si desea realizar algunas actualizaciones de estilo, se pueden realizar antes o después de la paginación.

En el ejemplo siguiente, la posición de los títulos de las figuras cambia de arriba a abajo de las imágenes. Para ello, debe habilitar la opción de ejecución de JavaScript en el ajuste preestablecido. Para ello, realice los siguientes pasos:

1. Abra la programación para editarla.
1. Vaya a la **Avanzadas** pestaña.
1. Seleccione el **Habilitar JavaScript** opción.
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
>El `window.addEventListener('DOMContentLoaded', function ()` se debe llamar a la función antes de utilizar las funciones de llamada de retorno.

A continuación, se debe llamar a esta secuencia de comandos desde un archivo de plantilla que se utiliza para generar la salida del PDF. Para nuestro ejemplo, lo añadiremos en la plantilla del índice. Asegúrese de que la variable `<script>` se añade dentro de un `<div>` dentro de `<body>` etiqueta. Si lo agrega en el `<head>` o fuera del `<body>` , el script no se ejecutará.

<img src="./assets/js-added-resources-template.png" width="500">

La salida generada con este código y la plantilla muestran el título de la figura debajo de la imagen:

<img src="./assets/fig-title-below-image.png" width="500">
