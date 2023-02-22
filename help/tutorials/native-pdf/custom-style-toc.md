---
title: Función de publicación de PDF nativo | Aplicar estilo personalizado en entradas de TDC y contenido del tema
description: Aprenda a crear hojas de estilo y crear estilos para el contenido.
source-git-commit: 09918abbdade934468dea1c55d0ca2cd60622b35
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Aplicar estilo personalizado en entradas de TDC y contenido del tema

A veces, es posible que desee aplicar estilo personalizado en las entradas de la tabla de contenido o en un tema concreto. Esto se puede lograr asociando un `outputclass` con la variable `<topicref>` del mapa de DITA. Además, si desea aplicar un formato personalizado a todo un tema, también se puede lograr ampliando la definición de estilo del atributo en el CSS.

Veamos un ejemplo de un tema nuevo que desea enviar para su revisión. Para identificar fácilmente el tema actualizado, debe agregar una `outputclass` a la variable `<topicref>` del mapa DITA y, a continuación, defina un estilo personalizado para el mismo en el CSS.

En el siguiente ejemplo, la variable *Historial de vuelos* se ha asignado un `outputclass` con el valor de `new-topic`.

<img src="./assets/new-topic-attribute-in-map.png" width="500">

La definición de clase de la variable `new-topic` en una CSS puede definir el estilo para los elementos siguientes:
* La entrada principal en el TOC o mini-TOC
* Título del tema en el contenido principal
* Todo el contenido del tema, incluido el título

Veamos cómo se puede definir cada uno de estos escenarios en el CSS. En la siguiente definición CSS de la variable `new-topic` , se ha cambiado el color del texto.

```css
…
.new-topic {
  color: #CC5309
}
…
```

Esta definición controla el color del texto en la tabla de contenido y el título del tema. La siguiente salida de PDF muestra los diferentes colores aplicados en la entrada TOC:

<img src="./assets/pdf-output-toc-entry.jpg" width="500">

El título del tema también tiene el mismo estilo.

<img src="./assets/pdf-output-topic-title.jpg" width="500">

Si desea que la entrada de TDC y el título del tema tengan estilos diferentes, puede definirlos por separado como se muestra a continuación:

```css
...
/*for styling TOC entry */
.new-topic {
  color: #CC3509
}

/* for styling topic's title */
.new-topic.title {
  color: #092ACC
}
...
```

Por último, también puede aplicar estilos a todo el contenido dentro del tema. Para ello, debe añadir un sufijo &quot;`-content`&quot; al nombre de la clase. En el siguiente ejemplo, se ha añadido una barra de cambios a todo el contenido del tema:

```css
...
/* for styling the topic's content */
.new-topic-content {
  -ro-change-bar-color: #A609CC;
}
...
```

Con los atributos de estilo anteriores, se agrega una barra de cambios a la izquierda del objeto *Historial de vuelo* como se muestra a continuación:

<img src="./assets/pdf-output-topic-content.jpg" width="500">


