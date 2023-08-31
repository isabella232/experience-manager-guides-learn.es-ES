---
title: PDF nativo | Configuración del proceso de nodo para la publicación de PDF nativo
description: Obtenga información sobre cómo configurar el proceso de nodo para la publicación nativa de PDF
source-git-commit: 45974b88a5b1bbbd2d83ea5cc18e0def2f15c51f
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# Configuración del proceso de nodos para la publicación nativa de PDF

La publicación del PDF nativo inicia un proceso NodeJs independiente para convertir los archivos generados en el proceso de publicación en un PDF final. Es posible que tenga que modificar las configuraciones de este proceso de nodo ejecutando la publicación del PDF nativo para admitir diferentes escenarios. Por ejemplo, para ejecutar cargas de trabajo más grandes debe aumentar el tamaño máximo de pila disponible para el proceso NodeJs generado.

Siga las instrucciones que se indican en [Anulaciones de configuración](../cs-install-guide/download-install-additional-config-override.md) para crear el archivo de configuración. En el archivo de configuración, proporcione los siguientes detalles (propiedad):

| PID | Clave de propiedad | Valor de propiedad |
|---|---|---|
| `com.adobe.fmdita.config.ConfigManager` | `native.pdf.node.opts` | Valor de cadena para establecer cualquier estándar `NODE_OPTIONS`.<BR> Valor predeterminado: &quot;&quot; |

