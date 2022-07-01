---
title: Configurar caracteres especiales adicionales en la barra de herramientas del Editor web
description: Configuración de caracteres especiales adicionales en la barra de herramientas del Editor web
feature: Web Editor
role: User
exl-id: 0fbc05a5-a6b0-4f6b-bbc4-8fca03581d90
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Configuración de caracteres especiales adicionales en la barra de herramientas del Editor web

Hay una opción de acceso directo en la barra de herramientas del editor web para permitir que el autor inserte ya los caracteres especiales.
Lo mismo puede verse en la captura de pantalla de abajo:

![Caracteres especiales](assets/special-chars.png)


Esta lista de caracteres se puede configurar aquí. Si necesita agregar más caracteres a esto, siga los siguientes pasos:

+ Inicie sesión en AEM y abra el modo CRXDE Lite.

+ Cree el archivo símbolos.json en la siguiente ubicación: &#39;/apps/fmdita/xmleditor/&#39; (Puede copiar el valor predeterminado desde la ubicación &quot;/libs/fmdita/clientlibs/clientlibs/xmleditor/symbols.json&quot;)

+ Añada la definición especial de caracteres en el archivo símbolos.json como:

```
{
      "label": "Logical Symbols",
      "items": [
        {
          "name": "≥",
          "title": "Greater-Than or Equal To"
        },
        {
          "name": "≤",
          "title": "Smaller-Than or Equal To"
        }
      ]
}
```

La estructura del archivo símbolos.json se explica a continuación:

+ &quot;label&quot;: &quot;Símbolos lógicos&quot;: Esto especifica la categoría de los caracteres especiales. En el fragmento, se define una categoría con el nombre &quot;Símbolo lógico&quot;.

+ &quot;elementos&quot;: Define la colección de caracteres especiales de la categoría.

+ &quot;name&quot;: &quot;≥&quot;, &quot;título&quot;: &quot;Bueno que o igual a&quot;: Esta es la definición del carácter especial. Comienza con la etiqueta &quot;name&quot;, que no debe cambiarse. El nombre va seguido del carácter especial. El &quot;título&quot; es el nombre o título del carácter especial que aparece como información de objeto para ese carácter especial.

Puede definir varias definiciones de caracteres especiales dentro de una categoría.

Esto agregará otra categoría en el cuadro de diálogo de caracteres especiales:

![Categoría de símbolo especial](assets/special-char-category.png)

![Insertar carácter especial](assets/insert-special-char.png)

>[!MORELIKETHIS]
>
>+ [Guía de instalación y configuración](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/3-6/XML-Documentation-for-Adobe-Experience-Manager_Installation-Configuration-Guide_EN.pdf)

