---
title: Función de publicación nativa de PDF | Utilizar estilos personalizados en notas al pie
description: Aprenda a aplicar estilo a los números de las notas al pie.
exl-id: f1068f2f-2ace-4bdb-b5a4-46b03d4e43d6
source-git-commit: 7b48633ef2418fa7c91842a8d2c2a4177017ef58
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# Usar estilos personalizados en las notas al pie

Las notas al pie son notas colocadas en la parte inferior de una página que comenta o cita una referencia para una parte designada del texto.

Puede aplicar estilo a los números de la llamada de nota al pie presentes en el contenido del tema y al marcador de nota al pie presente en la parte inferior de la página. Por ejemplo, puede agregar corchetes alrededor del número o cambiar su color. Estos estilos le ayudan a identificar fácilmente las notas al pie de página del documento.

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

En el ejemplo dado, se agrega un corchete antes y después de la llamada y el marcador de la nota al pie:

* Añada el prefijo &quot;(&quot; y el sufijo &quot;)&quot; utilizando el atributo content en `footnote-call` estilo que agregará los corchetes alrededor del número de nota al pie en el contenido del tema.
* Añada el prefijo &quot;(&quot; y el sufijo &quot;)&quot; utilizando el atributo content en `footnote-marker` estilo que agregará los corchetes alrededor del número de nota al pie en la parte inferior de la página.

<img src="./assets/pdf-output-footer-numbers.png" alt="Pie de página en salida de PDF" width="500">
