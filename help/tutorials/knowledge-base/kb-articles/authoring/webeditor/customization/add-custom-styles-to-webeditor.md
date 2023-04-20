---
title: Añadir estilos personalizados al editor de guías
description: Aprenda a añadir estilos personalizados para cambiar el aspecto del sitio web de las guías.
source-git-commit: 9e7d5bb4c8f6c6ebe21bfcebdd7d2e13971b8df2
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Añadir estilos personalizados al editor de guías

En este artículo aprenderemos a añadir estilos personalizados para cambiar el aspecto predeterminado del webeditor.

Esto implicará los siguientes pasos:
- Adición de estilos personalizados mediante la configuración del Editor XML de perfiles de carpeta
- Elección del perfil de carpeta respectivo en webeditor y prueba de los cambios


## Implementación tomando un ejemplo

Comprendamos esto con un ejemplo en el que queremos mostrar la descripción breve y el título como bloques independientes con algunos aspectos de estilo en el editor.

![Vista previa del editor web con estilos personalizados](../../../assets/authoring/webeditor-customstyles-preview.png)


## Implementación de


### Adición del CSS personalizado al perfil de carpeta

Utilice los perfiles de carpeta para comprobar la variable *css_layout.css* en la pestaña &quot;Configuración del editor XML&quot; y añada el CSS que tenga estilos personalizados

[utilice este vínculo para obtener más información sobre el perfil de carpeta y la configuración del diseño de plantilla CSS](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/videos/advanced-user-guide/editor-configuration.html?lang=en#customize-the-css-template-layout)

Utilice lo siguiente para configurar el estilo anterior en su sitio web:
- Uso [css_layout.css](../../../assets/authoring/webeditor-customstyles-css_layout.css) y cárguelo en el perfil de carpeta que elija
- Instale el paquete adjunto [webeditor-style-resources.zip](../../../assets/authoring/webeditor-styles-resources.zip) uso de AEM administrador de paquetes para instalar los recursos utilizados en el archivo CSS anterior

```
This will install the resources at path "/content/dam/resources" which will include sub-folders "fonts" and "images"
```


### Pruebas

- Abrir editor web
- En las preferencias del usuario, elija el perfil de carpeta en el que ha añadido los estilos personalizados. Si lo agregó al Perfil global, probablemente ya esté usando eso.
- Abra un tema y verá que el área de edición debe tener una interfaz de usuario personalizada

```
Please note this is compatible to AEM Guides version 4.2 and AEM Guides cloud version 2303 (March)
```


## Referencias

También puede estar interesado en la sesión de expertos sobre las configuraciones y personalizaciones de webeditor que se tratan en [Sesión de expertos sobre web](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/knowledge-base/expert-session/webbased-authoring-jan2023.html?lang=en)