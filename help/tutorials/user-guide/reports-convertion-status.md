---
title: Informe de estado de conversión
description: Obtenga información sobre cómo generar el informe de estado de conversión
exl-id: 41887af2-404f-41d7-b54c-ec49797200f0
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Informe de estado de conversión {#id205BBA00WZZ}

AEM Las guías de la aplicación proporcionan una función de conversión sólida para convertir documentos de diversos formatos a DITA. AEM El informe de estado de conversión proporciona una vista consolidada de todas las tareas de conversión ejecutadas por las guías de conversión de la aplicación

Siga estos pasos para ver el informe de estado de conversión:

1. Haga clic en el vínculo Adobe Experience Manager en la parte superior y elija **Herramientas**.

1. Seleccionar **Guías** de la lista de herramientas.

1. Haga clic en **Informe de estado de conversión** mosaico.

   El informe de estado de conversión se muestra para todas las tareas de conversión ejecutadas en el sistema.

   ![](images/conversion-status-report.png){width="800" align="left"}

1. La página del informe se divide en dos partes:

   - **Filter:**

      Puede filtrar los datos del informe en función del Tipo de archivo y el Estado de conversión. En Tipo de archivo, puede elegir ver los datos del informe de los documentos de tipo Documento de Word, HTML estructurado, XML y DocBook. En Estado, puede elegir ver los datos del informe de las tareas que se han ejecutado correctamente, con error, activas o en cola.

      La siguiente captura de pantalla muestra los datos del informe de las tareas de conversión que tienen los estados Error, Activo y En cola.

      ![](images/conversion-report-failed-active-queued.png){width="800" align="left"}

   - **Datos del informe:**

      Los datos del informe contienen las columnas siguientes:

      - **Nombre de archivo**: Nombre del archivo de origen en el que se ejecutó el proceso de conversión. Al hacer clic en el vínculo Nombre de archivo, se le redirige a la ubicación del documento de origen.

      - **Tipo de archivo**: tipo del documento de origen, que puede ser Word, HTML estructurado, XML y DocBook.

      - **Añadido por**: Nombre del usuario que ejecutó la tarea de conversión.

      - **Fecha de incorporación**: Fecha en la que se ejecutó la tarea. Al hacer clic en el vínculo Fecha de incorporación, se descarga el archivo de registro.

      - **Ruta**: Ruta completa del documento de origen.

      - **Estado**: Estado de las tareas de conversión: Correcto, Fallido, Activo o En cola.

      - **Output**: ruta del documento convertido correctamente. Al hacer clic en el vínculo Output, se le lleva a la ubicación en la que se guarda la salida.


**Tema principal:**[ Informes](reports-intro.md)
