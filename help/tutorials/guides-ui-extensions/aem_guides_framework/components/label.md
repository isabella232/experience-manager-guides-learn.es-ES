---
sidebar_position: 2
source-git-commit: 0f20681fa4de859053c8d2baae0e53f347ce5859
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 2%

---


# Etiqueta

Para mostrar cualquier texto o cadena, utilizamos el componente, la etiqueta.
El componente de etiqueta de la JUI representa un HTML `<label/>`.

A continuación se muestra un ejemplo para añadir una etiqueta estática

```js title="staticLabel.js"
const staticLabelJSON =  {
    "component": "label", //tells the component name
    "label": "This is an example label", // the string to be displayed
}
```

Debajo de JSON se muestra una cadena dinámica:

```js title="dynamicLabel.js"
const labelJSON =  {
    "component": "label", //tells the component name
    "label": "@name", // the variable storing the text to be displayed
},
```

La etiqueta procesada tendrá este aspecto:

![etiqueta](./imgs/label.png "Etiqueta")