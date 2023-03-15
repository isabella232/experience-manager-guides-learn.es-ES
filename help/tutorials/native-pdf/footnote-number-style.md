---
title: Función de publicación de PDF nativo | Utilizar estilos personalizados en notas al pie
description: Aprenda a aplicar estilo en los números de las notas al pie.
source-git-commit: ef562c43f5b70d3fe425427108ad8277e1456f24
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# Utilizar estilos personalizados en notas al pie

Las notas a pie de página son notas colocadas en la parte inferior de una página que comentan o citan una referencia para una parte designada del texto.

Puede aplicar estilo a los números de la llamada de nota al pie de página presentes en el contenido del tema y al marcador de nota al pie de página presente en la parte inferior de la página. Por ejemplo, puede agregar corchetes alrededor del número o cambiar su color. Estos estilos le ayudan a identificar fácilmente las notas al pie del documento.

```css
...
.footnote::footnote-call { 
content: "(" counter(footnote, decimal) ")"; 
} 

.footnote::footnote-marker { 
content: "(" counter(footnote, decimal) ")"; 
} 

...
```

En el ejemplo dado, se añade un corchete antes y después de la llamada de nota al pie y el marcador :

* Añada el prefijo &quot;(&quot; y el sufijo &quot;)&quot; utilizando el atributo content en la `footnote-call` estilo que agregará los corchetes alrededor del número de nota al pie en el contenido del tema.
* Añada el prefijo &quot;(&quot; y el sufijo &quot;)&quot; utilizando el atributo content en la `footnote-marker` estilo que agregará los corchetes alrededor del número de nota al pie de página en la parte inferior de la página.

<img src="./assets/pdf-output-footer-numbers.png" alt="Pie de página en la salida del PDF" width="500">
