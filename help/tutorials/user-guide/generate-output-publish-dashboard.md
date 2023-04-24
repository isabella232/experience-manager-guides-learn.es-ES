---
title: Administrar tareas de publicación mediante el panel Publicar
description: Obtenga información sobre cómo administrar las tareas de publicación mediante el panel Publicar
source-git-commit: 8b6294425c6e60d1c5b37d98e99114014a104ee6
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---


# Administrar tareas de publicación mediante el panel Publicar {#id205CC08305Z}

Cuando tiene un gran conjunto de tareas de publicación ejecutándose en su sistema, resulta prácticamente imposible comprobar cada mapa DITA individualmente para monitorizar su tarea de publicación. AEM guías proporciona a los administradores y editores una vista unificada de todas las tareas de publicación que se ejecutan en el sistema. En el panel Publicar encontrará una lista de todas las tareas de publicación activas.

El panel Publicar proporciona una descripción general completa de todas las tareas de publicación que se están realizando en el sistema.

![](images/publish-dashboard.png)

El panel Publicar contiene los siguientes detalles:

- **Título de mapa** - El título de un archivo de mapa que se está publicando o que está en la cola de publicación.

- **Nombre del archivo** - El nombre del archivo del mapa DITA.

- **Ajuste preestablecido de salida** - Nombre del ajuste preestablecido de salida que se utiliza para generar la salida.

- **Iniciado por** - Nombre de usuario del usuario que inició la tarea de publicación.

- **Iniciado el** - Fecha y hora en que se inició la tarea de publicación.

- **Tiempo transcurrido** - Tiempo transcurrido desde que se ejecuta la tarea de publicación en el sistema.

- **Icono Eliminar** - Cancelar o finalizar una tarea de publicación.

El panel izquierdo del panel Publicar proporciona las siguientes opciones de filtrado:

- **Ajuste preestablecido de salida** : seleccione uno o varios ajustes preestablecidos de salida para los que desea ver las tareas de publicación activas actualmente. En la siguiente captura de pantalla, las tareas de publicación se filtran para mostrar solo las tareas que utilizan el ajuste preestablecido de salida AEM Sitio :

![](images/publish-dashboard-preset-filter.png)

- **Iniciado por** - Seleccione un nombre de usuario de la lista para mostrar las tareas de publicación iniciadas por el usuario seleccionado.

- **Mapa** - Seleccione un archivo de mapa de la lista para mostrar las tareas de publicación que se ejecutan para el mapa seleccionado.

## Acceso al panel Publicar {#id205CC100DY4}

Realice los siguientes pasos para acceder al panel Publicar:

>[!NOTE]
>
> Solo los administradores o publicadores pueden acceder al tablero Publicar.

1. Haga clic en el vínculo Adobe Experience Manager en la parte superior y elija **Herramientas**.

1. Select **Guías** de la lista de herramientas.

1. Haga clic en el **Publicar tablero** mosaico.

   El panel Publicar se abre con una lista de todas las tareas de publicación activas en el sistema.

   Si hace clic en el vínculo Nombre de archivo, se muestra la consola de asignación DITA del mapa seleccionado.

   ![](images/publish-dashboard-click-filename-link.png)


>[!NOTE]
>
> También puede acceder al panel Publicar en la pestaña Salidas mientras genera resultados desde el panel de mapas. Para obtener más información, consulte [Ver el estado de la tarea de generación de salida](generate-output-for-a-dita-map.md#viewing_output_history).

## Cancelar una tarea de publicación

Realice los siguientes pasos para cancelar una tarea de generación de salida desde el panel Publicar:

1. [Acceso al panel Publicar](#id205CC100DY4).

1. En la lista de tareas de publicación activas, haga clic en el icono de eliminación de una tarea que desee cancelar.

   ![](images/publish-dashboard-cancel-task.png)

1. Haga clic en **Sí** en el mensaje Confirmar cancelación .

   Se acepta el comando cancel y se intenta cancelar mientras la tarea permanezca activa. Una vez finalizada correctamente la tarea, se elimina de la lista de tareas activas actualmente. El estado de la tarea también se actualiza en la consola de asignación DITA como Cancelado. En la siguiente captura de pantalla, la variable *HTML5* se cancela desde el panel Publicar y su estado también se cambia en la consola de asignación DITA.

   ![](images/cancelled-output-task.png)


**Tema principal:**[ Generación de resultados](generate-output.md)

