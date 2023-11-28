---
sidebar_position: 4
source-git-commit: 0f20681fa4de859053c8d2baae0e53f347ce5859
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 2%

---


# Icono

Para mostrar un icono utilizamos el componente, icono.
El componente de área de texto en la JUI representa un HTML `<icon/>`.

Iconos disponibles en [Iconos de espectro de Adobe](https://spectrum.adobe.com/page/icons/) son compatibles con nuestra aplicación.

```js title="icon.js"
const iconJSON =  {
    "component": "icon", //tells the component name
    "icon": "info", // name of the icon to be used
    "size": "S", // size of the icon
    "title": "Information" // tooltip corresponding to the icon.
},
```

también se pueden añadir iconos a los botones.

El icono procesado tendrá este aspecto:

![icono](./imgs/info_icon.png "Icono")
