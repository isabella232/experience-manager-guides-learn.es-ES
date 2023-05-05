---
title: Ver el estado de la tarea de generación de salida
description: Obtenga información sobre cómo ver el estado de la tarea de generación de salida
exl-id: 6fdaa547-8446-4ce5-95c3-a63d9c1f27d2
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Ver el estado de la tarea de generación de salida {#viewing_output_history}

Una vez iniciada la tarea de generación de resultados para un documento de FrameMaker, AEM Guías envía esta tarea a la cola de generación de resultados. Esta cola se actualiza en tiempo real, mostrando el estado de cada tarea de generación de salida en la cola.

Siga estos pasos para ver la cola de generación de resultados:

1. En la interfaz de usuario de Assets, vaya al documento de FrameMaker para el que desea comprobar el estado de generación de resultados y haga clic en él.

1. Haga clic en Salidas.

   ![](images/output-queued-fm.png){width="800" align="left"}

1. La página Resultados se divide en dos partes:

   - **Salidas en cola:**

      Enumera las salidas que están a la espera de ser generadas o que están en proceso de generación. También puede encontrar el ajuste de generación de salida o el ajuste preestablecido utilizado para la tarea en cola, el tipo, el usuario que inició la tarea, el tiempo transcurrido desde que se puso en cola la tarea y el estado actual.

   - **Productos generados**

      Enumera las tareas de salida que se han completado. De nuevo, la información mostrada en esto es similar a la sección Salida en cola , con la única diferencia del tiempo de generación de salida.

      En esta lista, puede tener tareas que se hayan ejecutado correctamente o tareas que hayan fallado. Para las tareas que se han completado correctamente, el proceso de publicación crea un archivo de registro \(logs.txt\) al que se puede acceder haciendo clic en el vínculo de la columna Generated At .


**Tema principal:**[ Generar salida de documentos de FrameMaker](fm-output-generatation.md)
