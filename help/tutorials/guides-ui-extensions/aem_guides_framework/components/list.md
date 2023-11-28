---
sidebar_position: 5
source-git-commit: 42052b37724f97e34ab007db4cc3d9f9524ad3a2
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---


# Lista

Para mostrar una lista, se utiliza la lista de componentes.

```js title="list.js"
const listJSON =  {
    "component": "list", //tells the component name
    "data": "@languages", // an array of list items
},
```

En este caso, el lenguaje es una simple matriz de cadenas. `languages = ["English", "Hindi", "French"]`
Si queremos procesar una lista de objetos, podemos especificar la estructura utilizando la configuración del elemento.

```js title="list.js"
const listJSON =  {
    "component": "list", //tells the component name
    "data": "@projects", // an array of list items
    "itemConfig": { // used to define the structure of the list items.
    "component": "widget",
    "id": "checkbox_label"
    }
},
```

Normalmente itemConfig es una `widget`. Para obtener más información sobre los widgets, vaya a [Widgets](../Widgets/basic_widget.md)

La lista procesada tendrá este aspecto:

![lista](./imgs/list.png "Lista")
