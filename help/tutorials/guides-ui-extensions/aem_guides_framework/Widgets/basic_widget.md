---
sidebar_position: 1
source-git-commit: 0f20681fa4de859053c8d2baae0e53f347ce5859
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---



# Widgets

Se pueden combinar varios componentes básicos, como se describe en la sección Componentes, para crear un widget.
Los widgets se pueden utilizar para crear un nuevo componente &quot;más complejo&quot; o para dar estructura a los elementos de un componente.

¡Vamos a sumergirnos en el concepto de widget!

Empezaremos por hacer un widget simple para mostrar una lista de idiomas.

```js title="basicWidget.js"
const widgetJSON =  {
    "component": "div", 
    "id": "widget_languages", 
    "items": [ // adding components to the widget
        {
            "component": "div",
            "items": [
                {
                    "component": "icon",
                    "icon": "info"
                },
                {
                    "component": "label",
                    "label": "List of some languages"
                }
            ]
        },
        {
            "component": "list",
            "data": "@languages"
        }
    ]
},
```

Aquí, `@languages` es una matriz definida en el modelo de `widget_languages` como: [&quot;Inglés&quot;, &quot;Francés&quot;, &quot;Hindi&quot;, &quot;Español&quot;, &quot;Urdu&quot;]

El widget básico procesado tendrá este aspecto:

![basic_widget](imgs/basic_widget.png "Widget básico")
