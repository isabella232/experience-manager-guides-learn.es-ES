---
title: Informe de historial de versiones de archivos revertido
description: Descubra cómo se revierte el informe del historial de versiones de archivos
exl-id: fa90b373-742a-4102-b00f-07e4113fef98
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# Informe de historial de versiones de archivos revertido {#id205BBC00PRK}

Cuando se trabaja en varias versiones simultáneas junto con varios autores, el contenido tiene varias versiones. Podría haber cierta información común en varias versiones, que diferentes autores podrían utilizar en su proyecto. Para manejar estas asignaciones de trabajo, los autores podrían terminar con varias versiones de archivos. Estas versiones podrían ser simplemente una versión más reciente de un archivo o una versión anterior. Es una tarea compleja identificar cuándo se revierte un archivo y por qué.

AEM guías le permite generar un informe del historial de versiones para un archivo individual o para todos los archivos de una carpeta. Este historial de versiones le ofrece una vista consolidada de todas las versiones de un archivo que se revirtieron y que crearon esas versiones, así como el motivo para crearlas.

Puede acceder a este informe desde los siguientes lugares:

- **IU de recursos**: seleccionando un archivo y abriendo el **Historial de versiones** desde el carril izquierdo. La variable **Historial de versiones** la vista contiene el **Revertir registros de versiones** en la parte inferior del panel. Al hacer clic en este vínculo, se muestra el historial del archivo seleccionado de las versiones revertidas.

   ![](images/revert-log-from-assets-ui.png){width="300" align="left"}

- **Vista previa del tema**: cuando esté previsualizando un tema, también puede que aparezca la variable **Historial de versiones** del carril izquierdo. Obtendrá un panel similar a la IU de Assets desde el que puede hacer clic en el **Revertir registros de versiones** para acceder al historial de versiones revertidas del documento activo.

- **Sección Herramientas de AEM**: también puede acceder a este informe desde AEM sección Herramientas . El siguiente procedimiento explica cómo puede acceder al historial de versiones revertidas desde la sección Herramientas de AEM.


Siga estos pasos para acceder al informe Historial de reversión :

1. Haga clic en el vínculo Adobe Experience Manager en la parte superior y elija **Herramientas**.

1. Select **Guías** de la lista de herramientas.

1. Haga clic en el **Historial de versiones revertidas** mosaico.

   Se muestra una página en blanco Revertir historial de versiones donde debe buscar y seleccionar un archivo o carpeta para generar el informe.

1. Haga clic en **Mostrar registros** para generar el informe del archivo o la carpeta seleccionados.

   ![](images/revert-version-history-report.png){width="800" align="left"}

   El informe contiene los siguientes detalles:

   - **Nombre del archivo**: Título del tema. Al hacer clic en el vínculo de título del tema, se abre la vista previa del tema.

   - **Marca de tiempo**: La fecha y hora en que se volvió al tema a una versión anterior.

   - **Usuario**: Nombre del usuario que ha cambiado a una versión anterior.

   - **Revertir desde**: Número de versión original del archivo desde el que se revirtió.

   - **Revertir a**: Versión a la que se ha revertido el archivo.

   - **Comentario**: Cualquier comentario del usuario que ha revertido el archivo.


**Tema principal:**[ Informes](reports-intro.md)
