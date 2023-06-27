---
title: AEM Configure nombres de archivo válidos para la salida del sitio de la
description: AEM Obtenga información sobre cómo configurar nombres de archivo válidos para la salida del sitio de la
source-git-commit: 4f15166b1b250578f07e223b0260aacf402224be
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---


# AEM Configure nombres de archivo válidos para la salida del sitio de la {#id214GK0X0KXA}

AEM De forma similar a la lista de caracteres de nombre de archivo válidos permitidos para los temas DITA, también se puede configurar una lista de caracteres de nombre de archivo válidos para la salida de sitio de la publicación de datos de página (). Algunos de los caracteres conocidos que no están permitidos en una dirección URL son: ``'<>`@$``. Estos caracteres están configurados para convertirse automáticamente en un guion bajo &quot;`_`AEM &quot; cuando se encuentran al generar nombres de archivo de salida del sitio de la.

Siga las instrucciones que se indican en [Anulaciones de configuración](download-install-additional-config-override.md#) para crear el archivo de configuración. AEM En el archivo de configuración, proporcione los siguientes detalles \(property\) para establecer caracteres válidos en la salida del sitio de la:

| PID | Clave de propiedad | Valor de propiedad |
|---|------------|--------------|
| `com.adobe.fmdita.common.SanitizeNodeNameImpl` | `aemsite.DisallowedFileNameChars` | AEM Agregue los caracteres que desee reemplazar con un guion bajo en los nombres de archivo de salida del sitio de la. <br> **Valor predeterminado**: ``'<\>\`@$`` |

**Tema principal:**[ Configurar nombres de archivo](conf-file-names.md)

