---
title: Generar salida para un mapa DITA desde la consola de asignación
description: Obtenga información sobre cómo generar resultados para un mapa DITA desde la consola de mapas
exl-id: 98afbdd2-56d7-44b0-ad2a-25e9143c88f3
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# Generar salida para un mapa DITA desde la consola de asignación {#id1825FG00UHT}

Realice los siguientes pasos para generar resultados para un mapa DITA:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación DITA que desea publicar y haga clic en él.

   La consola de asignación DITA aparece con la lista de ajustes preestablecidos de salida disponibles para generar resultados.

1. Seleccione uno o varios ajustes preestablecidos de salida que desee utilizar para generar la salida.

   ![](images/generate-multiple-outputs-uuid.png){width="800" align="left"}

   >[!NOTE]
   >
   > Si está generando la salida AEM Sitio, el proceso de publicación utiliza la estructura definida en la variable `.ditamap` para crear AEM estructura del sitio.

1. Haga clic en el icono Generate para iniciar el proceso de generación de salida.


Puede ver el estado actual de la solicitud de generación de salida haciendo clic en Outputs. Para obtener más información, consulte [Ver el estado de la tarea de generación de salida](#viewing_output_history)

>[!IMPORTANT]
>
> Si un proceso de generación de salida para un ajuste preestablecido está en cola o en curso, no se puede iniciar otra tarea de generación de salida para el mismo ajuste preestablecido.

Puede generar la salida del PDF para uno o más ajustes preestablecidos de salida creados para una asignación DITA desde el Editor web. Para obtener más información, consulte [Utilice el panel Generación rápida para generar y ver los resultados de los ajustes preestablecidos](web-editor-quick-generate-panel.md#).

También puede generar la salida AEM Sitio para uno o más temas, o el mapa DITA completo desde el Editor Web. Para obtener más información, consulte [Publicación basada en artículos desde el Editor web](web-editor-article-publishing.md#id218CK0U019I).

## Generación de salida incremental {#generating_standalone_topic}

>[!NOTE]
>
> La generación de salida incremental solo se aplica para AEM salida del sitio. Además, solo puede regenerar temas DITA \(.dita/.xml\) a partir de un mapa DITA o submapas. Si selecciona un mapa DITA, submapa, grupo de temas o un tema con `@processing-role="resource-only"`, la opción regenerar no está disponible.

Podría haber varias instancias en las que actualizara solo unos pocos temas en su mapa DITA e insertara solo esos temas actualizados en vivo. Para gestionar estos escenarios, AEM guías le permite crear resultados incrementales. Si ha actualizado algunos temas, no es necesario volver a generar el mapa DITA completo. Solo se pueden seleccionar los temas actualizados y regenerarlos.

Si el mapa está cortado y ha actualizado un solo tema en ese mapa, entonces necesita volver a generar todo el mapa para el tema o contenido actualizado para reflejarlo en el resultado. No se obtiene la opción de regeneración de salida a nivel de tema, solo está disponible a nivel de mapa \(cortado\). Esto es aplicable al mapa principal y a todos los submapas.

Realice los siguientes pasos para volver a generar la salida de un tema específico o de un grupo de temas:

>[!IMPORTANT]
>
> Cuando se regenera la salida AEM Sitio, la salida se crea utilizando la versión actual de los archivos y no la línea de base adjunta.

1. En la interfaz de usuario de Assets, vaya al archivo de asignación DITA y haga clic en él.

   La consola de asignación DITA aparece con la lista de ajustes preestablecidos de salida disponibles para generar resultados.

1. Seleccione el **Temas** pestaña .

   Se muestra una lista de temas disponibles en el mapa DITA.

1. Seleccione los temas que desea regenerar.

   >[!NOTE]
   >
   > Si ha añadido nuevos temas al mapa de DITA, no podrá generar esos nuevos temas desde aquí. Primero debe publicar los temas recién añadidos utilizando la función de publicación de mapas DITA.

   ![](images/regenerate-topics.png){width="800" align="left"}

1. Haga clic en **Regenerar**.

   Aparecerá la página Regenerar temas seleccionados .

1. Seleccione el ajuste preestablecido de salida que desee utilizar para regenerar los temas seleccionados.

1. Haga clic en **Regenerar** para iniciar el proceso de generación de resultados.


>[!IMPORTANT]
>
> Si cambia el nombre de un título de tema y vuelve a generarlo, el título del tema actualizado no se refleja en la tabla de contenido del mapa DITA. Para actualizar el título del tema en la tabla de contenido, debe generar el mapa DITA completo.

Puede ver el estado actual de la solicitud de generación de salida haciendo clic en Outputs. Para obtener más información, consulte [Ver el estado de la tarea de generación de salida](#viewing_output_history).

## Ver el estado de la tarea de generación de salida {#viewing_output_history}

Una vez iniciada la tarea de generación de salida para un mapa o regenerado los temas seleccionados, AEM Guías envía esta tarea a la cola de generación de salida. Esta cola se actualiza en tiempo real, mostrando el estado de cada tarea de generación de salida en la cola.

Siga estos pasos para ver la cola de generación de resultados:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación para el que desea comprobar el estado de generación de resultados y haga clic en él.

1. Haga clic en **Salidas**.

   ![](images/output-queued.png){width="800" align="left"}

   La página Resultados se divide en dos partes:

   - **Salidas en cola:**

      Enumera las salidas que están a la espera de ser generadas o que están en proceso de generación. Las tareas en cola o en curso se muestran con un icono de color azul antes del nombre del ajuste preestablecido. También puede encontrar el ajuste de generación de salida o el ajuste preestablecido utilizado para la tarea en cola, el tipo, el usuario que inició la tarea, el tiempo transcurrido desde que se puso en cola la tarea y el estado actual.

      Haga clic en el vínculo para acceder a la **Publicar tablero** y ver el estado actual de ejecución. En el panel Publicar encontrará una lista de todas las tareas de publicación activas. La variable **Salidas en cola** y **Publicar tablero** solo se muestran cuando hay salidas que están a la espera de ser generadas o que están en proceso de generación. No aparecen cuando se han completado las tareas de salida.Para obtener más información sobre el panel Publicar, consulte [Administrar tareas de publicación mediante el panel Publicar](generate-output-publish-dashboard.md#).

   - **Productos generados**

      Enumera las tareas de salida que se han completado. De nuevo, la información mostrada aquí es similar a la sección Salida en cola con algunas diferencias. Tiene un nuevo conjunto de información en forma de icono de resultado de salida y de tiempo de generación de salida.

      En esta lista, puede tener tareas que se hayan ejecutado correctamente, tareas que se hayan ejecutado con un mensaje o tareas en las que se hayan producido errores. Las tareas correctas se muestran con un icono de color verde, las tareas con un mensaje tienen un icono de color naranja y las tareas fallidas se muestran con un icono de color rojo.

      Para todas las tareas, el proceso de publicación crea un archivo de registro \(logs.txt\) al que se puede acceder haciendo clic en el vínculo de la columna Generated At . Para las tareas que han fallado o tienen mensajes, puede consultar el archivo de registro, que se explica en la sección [Ver y comprobar el archivo de registro](generate-output-basic-troubleshooting.md#id1822G0P0CHS).

      >[!NOTE]
      >
      > Al hacer clic en un vínculo de la salida del PDF generado, se le pide que descargue el PDF. Este es el comportamiento predeterminado en las AEM 6.5 y 6.4.


## Cancelar una tarea de generación de salida {#id2061H100T5Z}

AEM guías proporciona a los editores una forma sencilla y sencilla de cancelar cualquier tarea de publicación en curso. Como editor, puede cancelar una tarea de publicación en curso desde la consola de asignación DITA o desde la [Publicar tablero](generate-output-publish-dashboard.md#).

Realice los siguientes pasos para cancelar una tarea de generación de salida desde la consola de asignación DITA:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación para el que desea cancelar una tarea de generación de salida en curso y haga clic en él.

1. Haga clic en **Salidas**.

1. En la lista Resultados en cola, pase el puntero sobre una tarea que desee cancelar.

1. Haga clic en el *Cancelar este trabajo* icono.

   ![](images/cancel-publish-task-map-console.png){width="800" align="left"}

1. Haga clic en **Sí** en el mensaje Confirmar cancelación .

   ![](images/confirm-cancel-output-map-condole.png){width="800" align="left"}

   Si la tarea aún no se ha iniciado, el comando cancel se ejecuta en la tarea. Para una tarea que se está cancelando, el estado se establece en Cancelando.

   Una vez cancelada la tarea correctamente, se mueve al **Productos generados** lista con un **Cancelado** estado. Cuando pasa el ratón sobre la tarea cancelada, se muestra el nombre del usuario que ha cancelado la tarea. En la siguiente captura de pantalla, la variable *HTML5* se ha cancelado la tarea.

   ![](images/cancelled-output-task.png){width="800" align="left"}


## Eliminar una tarea de salida de la consola de asignación DITA

Cuando se generan varias salidas para un mapa DITA, a lo largo de un período de tiempo la lista de Productos Generados para un mapa de este tipo se vuelve muy larga. Como editor, puede limpiar el historial de salida de cualquier archivo de asignación eliminando las tareas obsoletas del *Productos generados* lista. Tenga en cuenta que la salida no se elimina del sistema, solo la entrada de la salida generada se elimina del *Productos generados* lista.

Realice los siguientes pasos para quitar una tarea de salida de la lista Resultados generados:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación desde el que desea eliminar las tareas y haga clic en él.

1. Haga clic en **Salidas**.

1. En la lista Resultados generados, pase el puntero sobre una tarea que desee eliminar.

1. Haga clic en el icono eliminar .

   ![](images/delete-output-task.png){width="800" align="left"}

1. Haga clic en **Sí** en el mensaje Confirmar eliminación .

   La tarea se elimina de la lista Resultados generados .


**Tema principal:**[ Generación de resultados](generate-output.md)
