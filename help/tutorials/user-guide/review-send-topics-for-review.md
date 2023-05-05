---
title: Enviar temas para revisión
description: Aprenda a enviar temas para su revisión
exl-id: 7a9b36ad-44d4-4952-9906-d95feb95d0c6
source-git-commit: 8823669fd29e8a40a41f9ca5d654b38fbea8e2fa
workflow-type: tm+mt
source-wordcount: '2733'
ht-degree: 0%

---

# Enviar temas para revisión {#id199RD0S035Z}

El flujo de trabajo de revisión crea un entorno de varios revisores, donde el iniciador especifica una lista de temas para revisión, agrega varios revisores y asigna una cronología para la tarea de revisión. AEM guías permite a los usuarios que pertenecen a los grupos Autores y Editores iniciar una revisión.

Como el flujo de trabajo de revisión es específico del proyecto, el iniciador de la revisión debe formar parte del equipo del proyecto o tener derechos para crear un proyecto. En el momento de crear un proyecto, se definen los integrantes del equipo para el proyecto y se les asignan varias funciones o grupos. Para obtener más información sobre los proyectos, consulte [Creación de un proyecto DITA](authoring-create-dita-project.md#).

Puede crear una tarea de revisión desde:

- **Editor web**: Permite enviar un tema individual o un mapa DITA para su revisión. Tenga en cuenta que el flujo de trabajo para crear una tarea de revisión es común en el Editor web y en la interfaz de usuario de Assets. Solo difiere el método de inicio del flujo de trabajo de revisión. Para obtener información sobre el inicio del flujo de trabajo de revisión desde el Editor web, consulte la [Crear tarea de revisión](web-editor-features.md#id215OCJ00JXA) en el Editor web.

- **IU de recursos**: Permite enviar uno o varios temas y el mapa DITA para su revisión. En este tema se trata el uso compartido de documentos para su revisión desde el flujo de trabajo de la interfaz de usuario de Assets.


Desde la interfaz de usuario de Assets, hay dos formas en las que un autor/editor puede crear una tarea de revisión:

- Enviar uno o más temas para su revisión
- Enviar varios temas desde un mapa DITA para su revisión

## Enviar uno o más temas para su revisión {#id1721E600FY4}

>[!IMPORTANT]
>
> Antes de crear una tarea de revisión, asegúrese de que ha creado un proyecto y ha agregado revisores a dicho proyecto.

Para crear una tarea de revisión y enviar temas para revisión, realice los siguientes pasos:

>[!NOTE]
>
> Solo puede crear una tarea de revisión si es un autor o editor de un proyecto DITA.

1. Vaya a la carpeta requerida en la interfaz de usuario de Assets.

1. Haga clic en el icono Seleccionar de la acción rápida y seleccione los temas que desee enviar para su revisión.

   ![](images/select-asset-62.png){width="300" align="left"}

1. En la barra de herramientas, haga clic en **Crear tarea de revisión**. Se muestra la página de creación de la tarea de revisión.

   >[!NOTE]
   >
   > Puede crear una tarea de revisión solo para los temas que tengan una revisión. Si el tema seleccionado no tiene una revisión, se le mostrará un mensaje.

   ![](images/create-review-task-023.png){width="650" align="left"}

1. Escriba un **Título** para la tarea y seleccione una DITA **Proyecto** en la lista desplegable.

1. En el **Asignar a** en el campo desplegable , seleccione los revisores a los que desee enviar los temas para su revisión.

   Puede asignar una tarea de revisión a usuarios individuales del proyecto o a grupos de usuarios. Tenga en cuenta que solo puede asignar una tarea de revisión a usuarios individuales cuando forme parte del grupo de administradores del proyecto; de lo contrario, solo verá los grupos de usuarios en el campo Asignar a .

   >[!NOTE]
   >
   > El flujo de trabajo de revisión es específico del proyecto. Cuando cree proyectos, agregue los integrantes del equipo al proyecto y asígnelos a grupos. Así que cuando seleccionas el proyecto aquí, puedes elegir a los miembros que forman parte de ese proyecto. Para obtener más información sobre los proyectos, consulte [Creación de un proyecto DITA](authoring-create-dita-project.md#).

1. Escriba un **Descripción** para la tarea.

   Esta descripción se utiliza como el cuerpo del correo electrónico de notificación enviado a los revisores.

1. Seleccione el **Fecha de vencimiento** y tiempo para marcar el plazo de revisión.

   >[!NOTE]
   >
   > Al alcanzar la fecha límite, se envía un correo electrónico al iniciador para que le notifique de que la tarea de revisión se ha completado. El iniciador puede ampliar el plazo de la tarea de revisión desde el [Revisar tablero](review-manage-tasks-review-dashboard.md#).

1. Seleccione el mapa raíz de la **Ruta de mapa de ruta**. Esta hoja de ruta se utiliza para resolver todas las referencias clave y los términos del glosario utilizados en el contenido de revisión. Si no selecciona la hoja de ruta, las referencias clave o los términos de glosario asociados con el tema DITA no se resuelven antes de enviar el tema para su revisión.

   Si está creando la revisión de un mapa DITA, de forma predeterminada **Ruta de mapa de ruta** se establece en la ruta de ese mapa. Si está creando la revisión para uno o varios temas, de forma predeterminada, la variable **Ruta de mapa de ruta** se establece en el mapa definido en Preferencias de usuario.

   >[!NOTE]
   >
   > El mapa raíz seleccionado tiene la prioridad más alta para resolver las referencias clave. Para obtener más información, consulte [Resolución de referencias clave](map-editor-other-features.md#id176GD01H05Z).

1. Como puede asignar diferentes revisores a diferentes temas, **Permitir que los usuarios asignados revisen cualquier tema** controla si los revisores pueden revisar todos los temas de una tarea de revisión o solo los temas que tienen asignados para revisión.

   Si desea permitir que todos los revisores revisen cualquier tema de la tarea de revisión, seleccione **Permitir que los usuarios asignados revisen cualquier tema**.

   Si no selecciona esta opción, los revisores agregados a la variable **Asignar a** tendrá acceso para revisar solo los temas que se les asignen.

1. Haga clic en **Siguiente**.

   Se muestra la página Contenido .

   ![](images/content_page_review.png){width="800" align="left"}

1. En la página Contenido, seleccione una versión del tema que desee compartir para su revisión.

   Puede utilizar uno de los siguientes métodos para seleccionar una versión:

   - *\(Predeterminado\)* Elija la opción **Su última versión** para seleccionar la última revisión guardada de los temas.
   - Elija la **Versión activada** y especifique la fecha y la hora a la que desea seleccionar una versión en la fecha y hora especificadas. Si no hay ninguna versión de tema disponible en la fecha especificada, se selecciona una versión disponible inmediatamente después de la fecha y hora especificadas.
   - Elija la **Seleccionar una etiqueta** y seleccione una etiqueta en la lista desplegable.
1. Después de realizar la selección para elegir una versión, haga clic en **Aplicar**.

   La versión basada en la opción seleccionada se elige para los temas.

   >[!NOTE]
   >
   > También puede seleccionar manualmente la versión que desee en el **Versión** lista desplegable de cada tema.

1. Haga clic en **Siguiente**.

   Se muestra la página Revisores, donde puede agregar o quitar revisores. De forma predeterminada, los revisores añadidos en el campo Asignar a se añaden automáticamente a cada tema seleccionado para la revisión.

   ![](images/add-reviewers-topics.png){width="650" align="left"}

1. En la página Revisores, puede agregar o quitar revisores. Las siguientes operaciones están disponibles en la página Revisores :

   - **Seleccionar todo**: Selecciona todos los temas de la lista de temas. Puede realizar fácilmente una operación por lotes después de seleccionar todos los temas.
   - **Borrar selección**: Anula la selección de los temas seleccionados en la lista de temas.

      >[!NOTE]
      >
      > También puede seleccionar o anular la selección de un tema individualmente haciendo clic en la casilla de verificación situada junto al tema.

   - **Agregar**: Muestra el cuadro de diálogo Agregar revisores . Puede escribir el nombre de un revisor o función de usuario \(o grupo\) que desea agregar como revisor a los temas seleccionados.
   - **Eliminar**: Muestra el cuadro de diálogo Eliminar revisores . Puede escribir el nombre de un revisor o función de usuario \(o grupo\) que desee eliminar como revisor de los temas seleccionados.

      >[!NOTE]
      >
      > También puede eliminar una revisión de un tema haciendo clic en el signo de cruz en el cuadro del revisor.

   - **Volver a asignar**: Muestra el cuadro de diálogo Volver a asignar revisores . Puede escribir el nombre de un revisor o función de usuario \(o grupo\) al que desee asignar la tarea de revisión. Esto elimina todos los revisores existentes de los temas seleccionados y asigna los revisores recién seleccionados a esos temas.
   - **Exportar**: Permite exportar los detalles de la tarea de revisión en un archivo CSV. El archivo contiene detalles como la ruta y el título del tema, el nombre del revisor y la versión de los temas enviados para revisión.
   - **Editar revisores**: Al hacer clic en ![](images/edit_pencil_icon.svg)en la lista de temas se muestra el cuadro de diálogo Editar revisores . Puede agregar o quitar revisores del tema seleccionado de este cuadro de diálogo.
1. Haga clic en **Crear** para crear la tarea de revisión.

   Se muestra un mensaje de confirmación cuando la tarea de revisión se crea correctamente. La variable [Estado del documento](web-editor-document-states.md#) para los temas enviados para revisión se configura en Revisión.

   >[!NOTE]
   >
   > También puede hacer clic en la campana Notifications en la parte superior derecha de la pantalla y confirmar que la tarea de revisión se ha creado correctamente. En el panel Notificaciones , encontrará una notificación para cada uno de los revisores que formaban parte de la tarea de revisión y una notificación para el iniciador de la revisión.


Se envía un correo electrónico a todos los revisores para notificar que se les ha asignado un tema o varios temas para su revisión. El correo electrónico contiene un vínculo directo en el que pueden hacer clic y acceder al tema en una ventana del explorador.

En caso de que se asignen varios temas, los revisores pueden verlos y seleccionarlos en una lista desplegable de temas del explorador web.

## Enviar varios temas para su revisión desde un mapa DITA

Un mapa DITA es una organización lógica de temas dentro de un libro. Cuando envía un tema individual para su revisión, el revisor no obtiene ninguna información sobre la ubicación de ese tema en el libro. Si un revisor tiene información sobre la ubicación exacta del tema que se está revisando, obtiene un mejor contexto del tema que se está revisando.

AEM guías le permite enviar uno o más temas en un mapa DITA para su revisión al mismo tiempo. El revisor puede ver el archivo de asignación completo junto con los temas que se han compartido para su revisión. Esto facilita al revisor obtener un contexto del tema en el mapa o en el archivo del libro.

Puede compartir el mismo mapa DITA en para revisarlo en varias tareas de revisión. Por ejemplo, si en un mapa DITA hay los temas A, B, C, D y E. En una tarea de revisión puede compartir A, B y C para su revisión y en otra tarea de revisión puede enviar los temas C, D y E para su revisión. El proceso de revisión permite compartir el mismo tema y el mismo archivo de asignación en varias tareas de revisión. Para el tema común en varias tareas de revisión, los comentarios dados en una tarea de revisión no sobrescriben ni combinan con los comentarios en las otras tareas de revisión.

>[!IMPORTANT]
>
> En caso de que se haya compartido un tema de un archivo de mapa en varias tareas de revisión, su estado mostraría En revisión hasta que se hayan completado todas las tareas de revisión.

Para enviar uno o varios temas junto con el archivo de asignación para su revisión, realice los siguientes pasos:

>[!IMPORTANT]
>
> Una vez que inicie una revisión a través de un archivo de mapa, no debe cambiar la estructura del archivo de mapa añadiendo nuevos temas o eliminando temas existentes.

1. Vaya a la carpeta requerida en la interfaz de usuario de Assets.

   >[!NOTE]
   >
   > Asegúrese de que la vista de la consola esté configurada en vista de tarjeta o vista de lista.

1. Seleccione el mapa desde el que desea enviar los temas para su revisión.

1. En la barra de herramientas, haga clic en **Crear tarea de revisión**. Se muestra la página de creación de la tarea de revisión.

1. Escriba un **Título** para la tarea y seleccione una DITA **Proyecto** en la lista desplegable.

   >[!NOTE]
   >
   > Puede crear una tarea de revisión solo para los temas que tengan una revisión. Si el mapa contiene temas que no tienen una revisión, se le mostrará un mensaje con una lista de esos archivos. Los archivos sin revisión se excluyen de la tarea de revisión.

1. En el **Asignar a** en el campo desplegable , seleccione los revisores a los que desee enviar los temas para su revisión.

   Puede asignar una tarea de revisión a usuarios individuales del proyecto o a grupos de usuarios. Tenga en cuenta que solo puede asignar una tarea de revisión a usuarios individuales cuando forme parte del grupo de administradores del proyecto; de lo contrario, solo verá los grupos de usuarios en el campo Asignar a .

   >[!NOTE]
   >
   > El flujo de trabajo de revisión es específico del proyecto. Cuando cree proyectos, agregue los integrantes del equipo al proyecto y asígnelos a grupos. Así que cuando seleccionas el proyecto aquí, puedes elegir a los miembros que forman parte de ese proyecto. Para obtener más información sobre los proyectos, consulte [Creación de un proyecto DITA](authoring-create-dita-project.md#).

1. Escriba un **Descripción** para la tarea.

   Esta descripción se utiliza como el cuerpo del correo electrónico de notificación enviado a los revisores.

1. Seleccione el **Fecha de vencimiento** y tiempo para marcar el plazo de revisión.

   >[!NOTE]
   >
   > Al alcanzar la fecha límite, se envía un correo electrónico al iniciador para que le notifique de que la tarea de revisión se ha completado. El iniciador puede ampliar el plazo de la tarea de revisión desde el [Revisar tablero](review-manage-tasks-review-dashboard.md#).

1. Como puede asignar diferentes revisores a diferentes temas, **Permitir que los usuarios asignados revisen cualquier tema** controla si los revisores pueden revisar todos los temas de una tarea de revisión o solo los temas que tienen asignados para revisión.

   Si desea permitir que todos los revisores revisen cualquier tema de la tarea de revisión, seleccione **Permitir que los usuarios asignados revisen cualquier tema**.

   Si no selecciona esta opción, los revisores agregados a la variable **Asignar a** tendrá acceso para revisar solo los temas que se les asignen.

1. Haga clic en **Siguiente**.

   La página Contenido se muestra con todos los temas a los que se hace referencia desde el archivo de asignación. Si su mapa DITA contiene mapas anidados, los temas de los mapas anidados también se enumeran aquí.

   ![](images/content-page-map-review.png){width="800" align="left"}

1. En la página Contenido, seleccione una versión del tema que desee compartir para su revisión.

   Puede utilizar uno de los siguientes métodos para seleccionar una versión:

   - *\(Predeterminado\)* Elija la opción **Su última versión** para seleccionar la última revisión guardada de los temas.
   - Elija la **Versión activada** y especifica la fecha y la hora en las que se seleccionará una versión según la fecha y la hora. Si no hay ninguna versión de tema disponible en la fecha especificada, se selecciona una versión disponible inmediatamente después de la fecha y hora especificadas.
   - Elija la **Seleccionar una etiqueta** y seleccione una etiqueta en la lista desplegable. Todos los temas que contienen la etiqueta seleccionada se seleccionan en la **Versión** lista desplegable.
   - Elija la **Seleccionar una línea de base** y seleccione una línea de base en la lista desplegable. Todas las versiones de temas que forman parte de la línea base seleccionada se seleccionan en la **Versión** lista desplegable.
1. Después de realizar la selección para elegir una versión, haga clic en **Aplicar**.

   La versión basada en la opción seleccionada se elige para los temas.

   >[!NOTE]
   >
   > También puede seleccionar manualmente la versión que desee en el **Versión** lista desplegable de cada tema.

1. Haga clic en **Siguiente**.

   Se muestra la página Revisores, donde puede agregar o quitar revisores. De forma predeterminada, los revisores añadidos en el campo Asignar a se añaden automáticamente a cada tema seleccionado para la revisión.

1. En la página Revisores, puede agregar o quitar revisores. Las siguientes operaciones están disponibles en la página Revisores :

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

   >[!IMPORTANT]
   >
   > Debe asignar al menos un revisor para crear la tarea de revisión.

1. Haga clic en **Crear** para crear la tarea de revisión.

   Se muestra un mensaje de confirmación cuando la tarea de revisión se crea correctamente. La variable [Estado del documento](web-editor-document-states.md#) para los temas enviados para revisión se configura en Revisión.

   >[!NOTE]
   >
   > También puede hacer clic en el panel Notificaciones en la parte superior derecha de la interfaz y confirmar que la tarea se ha creado correctamente. En el panel Notificaciones, encontrará una notificación para cada una de las revisiones que formaron parte de la tarea de revisión y una notificación para el iniciador de la revisión.

   >[!IMPORTANT]
   >
   > Una vez iniciada una revisión, no debe mover ni eliminar el mapa o los temas de DITA a una ubicación diferente. Al hacerlo, se interrumpirá el proceso de revisión.


Se envía un correo electrónico a todos los revisores para notificar que se les han asignado temas para su revisión. El correo electrónico contiene un vínculo directo en el que pueden hacer clic y acceder al tema en una ventana del explorador. Los temas junto con el mapa DITA se abren en el modo de revisión.

**Tema principal:**[ Revisión de temas o mapas](review.md)
