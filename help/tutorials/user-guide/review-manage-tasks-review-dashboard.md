---
title: Administrar tareas de revisión mediante el panel de revisión
description: Obtenga información sobre cómo administrar tareas de revisión mediante el panel de revisión
source-git-commit: f3d747082103c73a365ee400cbd4dcdabd36eabf
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%

---


# Administrar tareas de revisión mediante el panel de revisión {#id2056B0Y70X4}

El flujo de trabajo de revisión de la administración puede incluir una variedad de tareas. Por ejemplo, puede que desee agregar revisores para un tema en particular o ampliar el plazo para una revisión. También es posible que desee marcar la tarea de revisión como completa si cree que todas las partes interesadas han dado su opinión. Estas tareas se pueden administrar mediante el panel de revisión.

Realice los siguientes pasos para acceder y utilizar el panel de revisión:

>[!NOTE]
>
> Puede administrar tareas de revisión solo para aquellos proyectos para los que sea el Autor \(o iniciador\). Aunque sea un revisor o un publicador \(usuario\), no tendrá acceso a ninguna de las tareas del proyecto.

1. En el **Proyectos** , haga clic en el proyecto de revisión que desee administrar.

   Se muestra un panel Proyecto con mosaicos de tareas.

   ![](images/review-management.png)

1. Haga clic en los tres puntos del **Reseñas** mosaico.

   Se muestra el panel de revisión. El tablero enumera todas las tareas de revisión que ha creado.

   ![](images/review-dashboard.png)

   El panel de revisión muestra los detalles sobre la tarea de revisión, como el nombre de la tarea, quién inició la revisión, la fecha en que se inició la revisión, la fecha de vencimiento, el estado, el número de comentarios nuevos que el autor no ha aceptado o rechazado y el nombre de los revisores. Las tareas se enumeran en el orden de las tareas recién creadas a las tareas más antiguas.

   >[!NOTE]
   >
   > Si hace clic en el vínculo Revisar tarea, se abre el tema o el archivo de asignación enviado para revisión.

1. Seleccione una tarea de revisión.

   Se muestra Editar propiedades y [Estado](#check-review-status-id199RF0A0UHS) en la barra de herramientas.

1. Si hace clic en **Editar propiedades**, se muestra la página Detalles de la tarea .

   Hay tres fichas en la página Detalles de la tarea: Tarea, Contenido y Revisores. Las siguientes secciones explican las distintas funciones disponibles en cada pestaña.


## Ficha Tarea

![](images/review-task-page.png)

Puede realizar las siguientes acciones en la sección **Tarea** pestaña:

- Modifique el título de la tarea en la **Título** campo .
- Agregue asignadores predeterminados en la variable **Asignar a** lista desplegable. Los revisores que agregue desde aquí tendrán acceso para revisar todos los temas que forman parte de esta tarea de revisión. Puede elegir eliminar o agregar de forma selectiva más revisores a temas específicos de la [Pestaña Revisores](#reviewer-tab-id199RF0N0MUI).
- Actualice la descripción de la tarea en el **Descripción** campo .
- Modifique el **Fecha de vencimiento**. Puede adelantar o posponer la fecha límite para la finalización de la tarea.
- Seleccione la opción para restringir el acceso de los usuarios solo a aquellos temas que tengan asignados.
- Haga clic en **Actualizar** para actualizar los detalles modificados.
- Haga clic en **Completar** para marcar la tarea de revisión como completada antes de la fecha de vencimiento. Cuando la tarea de un tema individual se marca como Completa, la revisión del tema seleccionado se cierra. Sin embargo, en el caso de temas compartidos para revisión a través de un mapa DITA, marcar la tarea de asignación DITA como Completa cerrará la revisión de todos los temas dentro del mapa que fueron compartidos para revisión.
- Haga clic en **Duplicar** para crear una copia de la tarea de revisión. El proceso de creación de una tarea de revisión duplicada es similar a la creación de una nueva tarea de revisión. Una vez iniciado el flujo de trabajo de tareas duplicadas, se muestra la página Crear tarea de revisión . Debe proporcionar los detalles de la nueva tarea tal como se explica en [Enviar temas para revisión](review-send-topics-for-review.md#).

   Si ha seleccionado una tarea de revisión creada a partir de un mapa DITA, se le mostrarán los temas que forman parte del mapa. A continuación, puede elegir los temas que desea incluir en la nueva tarea de revisión.

   En caso de que la tarea de revisión se duplique de una o varias revisiones de temas, entonces solo esos temas se muestran en la lista de tareas de revisión. Puede optar por compartir estos temas para su revisión con un conjunto diferente de revisores.

- Haga clic en **Cerrar** para ir a la página Bandeja de entrada.

## Pestaña Contenido

![](images/review-content-page.png)

Puede realizar las siguientes acciones en la sección **Contenido** pestaña:

- Cambie la versión del tema enviado para revisión. Puede elegir la versión más reciente del tema, la versión con fecha, la versión con etiqueta específica o la versión con una línea de base específica \ (para un mapa DITA\).

- Haga clic en **Actualizar** para compartir la versión actualizada del tema con los revisores. Los revisores reciben una notificación por correo electrónico que indica que la versión más reciente del tema se ha enviado para su revisión. La próxima vez que un revisor abra el tema, verá la versión actualizada del mismo.

   >[!NOTE]
   >
   > En el caso de una versión actualizada de un tema, los comentarios antiguos también se conservan en la versión más reciente. Los revisores también pueden ver las diferencias entre las dos versiones.

- Haga clic en **Completar** para marcar la tarea de revisión como completada antes de la fecha de vencimiento. Cuando la tarea de un tema individual se marca como Completa, la revisión del tema seleccionado se cierra. Sin embargo, en el caso de temas compartidos para revisión a través de un mapa DITA, marcar la tarea de asignación DITA como Completa cerrará la revisión de todos los temas dentro del mapa que fueron compartidos para revisión.

- Haga clic en **Duplicar** para crear una nueva tarea de revisión utilizando la tarea actual como base.


## Pestaña Revisores {#reviewer-tab-id199RF0N0MUI}

![](images/reviewers-tab.png)

Puede realizar las siguientes acciones en la sección **Revisores** pestaña:

- **Seleccionar todo**: Selecciona todos los temas de la lista de temas. Puede realizar fácilmente una operación por lotes después de seleccionar todos los temas.
- **Borrar selección**: Anula la selección de los temas seleccionados en la lista de temas.

   >[!NOTE]
   >
   > También puede seleccionar o anular la selección de un tema individualmente haciendo clic en la casilla de verificación situada junto al tema.

- **Agregar**: Muestra el cuadro de diálogo Agregar revisores . Puede escribir el nombre de un revisor o función de usuario \(o grupo\) que desea agregar como revisor a los temas seleccionados.
- **Eliminar**: Muestra el cuadro de diálogo Eliminar revisores . Puede escribir el nombre de un revisor o función de usuario \(o grupo\) que desee eliminar como revisor de los temas seleccionados.
- **Volver a asignar**: Muestra el cuadro de diálogo Volver a asignar revisores . Puede escribir el nombre de un revisor o función de usuario \(o grupo\) al que desee asignar la tarea de revisión. Esto elimina todos los revisores existentes de los temas seleccionados y asigna los revisores recién seleccionados a esos temas.
- **Exportar**: Permite exportar los detalles de la tarea de revisión en un archivo CSV. El archivo contiene detalles como la ruta y el título del tema, el nombre del revisor y la versión de los temas enviados para revisión.
- **Editar revisores**: Al hacer clic en ![](images/edit_pencil_icon.svg)en la lista de temas se muestra el cuadro de diálogo Editar revisores . Puede agregar o quitar revisores del tema seleccionado de este cuadro de diálogo.

## Comprobar el estado de una tarea de revisión {#check-review-status-id199RF0A0UHS}

En la página principal Revisar tablero, si selecciona una tarea de revisión y hace clic en **Estado**, se muestra el informe de estado de la tarea de revisión:

![](images/review-status-report.png)

El informe de estado de la tarea de revisión contiene los siguientes detalles:

- Nombre\(s\) del revisor al que se asigna la tarea de revisión.
- La columna Estado indica el estado de la revisión. El estado puede ser uno de los siguientes:
   - **No iniciado**: El revisor aún no ha abierto el vínculo de revisión.
   - **En curso**: El revisor ha abierto el vínculo de revisión y está revisando el tema.
   - **Completar**: El revisor ha completado la revisión completando la tarea de revisión que se le ha asignado. La tarea de revisión se encuentra en la Bandeja de entrada de notificaciones de AEM para cada revisor.
- Cuando un revisor abre un vínculo de revisión y navega a un tema en particular, ese tema se agrega a la lista Temas revisados . Esto ayuda a los autores a determinar si los revisores han abierto sus secciones respectivas o no. Si se formulan observaciones, éstas se muestran entre corchetes.
- Número total de observaciones formuladas sobre todos los temas. En el caso de varios temas que se están revisando, el número de comentarios para cada tema se menciona \(entre corchetes\) en relación con el nombre del tema.
- La fecha en la que el revisor accedió por última vez a cualquier tema.

**Tema principal:**[ Revisión de temas o mapas](review.md)

