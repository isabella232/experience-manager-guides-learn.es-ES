---
title: Temas de revisión
description: Descubra cómo revisar temas
source-git-commit: 849985574a4d21334ac73be3e664ff5ea9a898c4
workflow-type: tm+mt
source-wordcount: '2271'
ht-degree: 0%

---


# Temas de revisión {#id2056B0W0FBI}

Si es revisor, recibirá un correo electrónico de solicitud de revisión con el vínculo a los temas de revisión. Al hacer clic en el vínculo, accederá a la página de revisión, donde podrá agregar sus comentarios sobre los temas compartidos.

Siga estos pasos para revisar un tema:

1. Haga clic en el vínculo directo proporcionado en el correo electrónico de solicitud de revisión.

   El tema o el vínculo de asignación se abre en un explorador.

   >[!NOTE]
   >
   > También puede acceder al vínculo de revisión de temas desde el área de notificaciones de la Bandeja de entrada en la interfaz de usuario de AEM.

1. Según la forma en que se inicie la revisión del tema, podría ver cualquiera de las dos pantallas siguientes:

   >[!NOTE]
   >
   > La interfaz de usuario puede ser diferente si ha creado la revisión en:
   >
   > - Guías de AEM as a Cloud Service para la versión de noviembre de 2022 o anteriores
   > - Guías de AEM versión 4.1 o anterior




   La siguiente pantalla aparece cuando se utiliza un mapa DITA para iniciar el flujo de trabajo de revisión:

   ![](images/multiple-topics-review.png)

   Las siguientes opciones están disponibles en esta pantalla:

   - **A**: Nombre de la tarea de revisión.
   - **B**: Haga clic en el icono Vista de temas para mostrar u ocultar el panel de temas.

   - **C**: Los números resaltados por ***F*** se puede filtrar eligiendo la opción de filtro deseada desde aquí. Puede filtrar los comentarios por tipo, estado, revisor o versión. Por ejemplo, si desea ver cuántos comentarios de tachado se han realizado en cada uno de los temas que se están revisando, haga clic en el icono de filtro y, a continuación, elija **Tipo de revisión** \> **Eliminación**.

      >[!NOTE]
      >
      > Al aplicar los filtros, solo los comentarios que coincidan con los filtros seleccionados se mostrarán en el panel de comentarios. El número de comentarios filtrados se muestra a la izquierda en el panel de temas.

   - **D**: Un tema asignado para revisión al revisor actual se muestra en negro y se puede hacer clic en él. Cuando el revisor hace clic en un vínculo de tema, ese tema se coloca en la parte superior de la pantalla.
   - **E**: Un tema que no está disponible para revisión aparece atenuado. El tema se muestra en modo de solo lectura y no se le permite agregar comentarios de revisión sobre dichos temas.

   - **F**: Número de comentarios recibidos sobre un tema. Este número cambia según el filtro que aplique.

   Todos los temas del mapa se muestran como un solo documento compuesto. Los temas que el revisor puede revisar se muestran normalmente. No se muestran los temas que no se permite revisar en la revisión.

   ![](images/review-read-only.png)

   En la captura de pantalla anterior, el tema Descripción general se comparte para su revisión con el revisor actual, que se muestra normalmente. Sin embargo, el siguiente tema, Historial del contenido del vuelo, no se comparte para revisión y se muestra en modo de solo lectura. El tema que está actualmente en el centro de atención también se destaca en el TOC.

   La siguiente pantalla aparece cuando se selecciona un tema o varios temas y se comparten para su revisión:

   ![](images/review-composite-view.png)

   >[!NOTE]
   >
   > En el caso de varios temas, se muestran como un documento compuesto en la vista del documento. La captura de pantalla de arriba resalta dos temas diferentes presentados uno tras otro en una sola vista.

1. Abra el panel Comentarios haciendo clic en el botón **Comentarios** en la esquina superior derecha de la barra de herramientas.

   Para proporcionar comentarios de revisión, seleccione un tipo de comentario adecuado en la barra de herramientas y pulse Intro para enviar el comentario.

   >[!NOTE]
   >
   > El panel Comentarios muestra solo los comentarios dados sobre los temas actuales. Cuando se mueve el foco a otro tema, se muestran los comentarios dados en el otro tema.

1. Haga clic en **Cerrar** una vez que haya completado la revisión del tema. Al hacer clic en el botón **Cerrar** , se le redirigirá a la página desde la que accedió al tema de revisión.

## Funciones adicionales disponibles en la pantalla de revisión

**Vista de documento y vista de tema** - De forma predeterminada, si se comparten varios temas para su revisión, se muestra una vista de documento compuesto de los temas a los revisores. En caso de una revisión del mapa DITA, todos los temas en el mapa se presentan en forma de un documento único, que se asemeja a una vista de libro. Si lo desea, también puede hacer clic en un tema en particular y solo ese tema se mostrará en la pantalla de revisión.

Cuando vea un solo tema, obtendrá una opción adicional para volver a la vista del documento. En la siguiente captura de pantalla, se abre para su revisión un tema particular de un archivo de mapa. La opción resaltada — **Mostrar vista de documento** permite al usuario volver a la vista de documento del archivo de mapa.

![](images/switch-document-view.png)

**Uso de diferentes tipos de herramientas de comentarios** - Puede agregar comentarios en línea resaltando el texto, marcando el texto, insertando texto o agregando una nota de comentario. A continuación se describen los distintos tipos de herramientas de comentarios que se proporcionan en la barra de herramientas Comentarios:

![](images/comments-toolbar.png)

- **Resaltar** \(![](images/review-highlight-icon.svg)\): Para añadir un comentario resaltado, seleccione el texto y haga clic en el icono Resaltar . O bien, haga clic en el icono Resaltar y seleccione el texto deseado:

   ![](images/highlight-comment.png)

   Aparece una ventana emergente en el panel Comentarios donde puede agregar su comentario para el contenido resaltado.

- **Tachado** \(![](images/review-text-strike-through-icon.svg)\): Si desea sugerir la eliminación de contenido, puede hacerlo seleccionando el contenido y haciendo clic en el icono Tachado . O bien, seleccione el texto deseado y haga clic en la tecla Supr:

   Aparece una ventana emergente en el panel Comentarios donde puede agregar su comentario para el contenido eliminado.

- **Insertar texto** \(![](images/review-insert-text-icon.svg)\): Si desea insertar texto, haga clic en el icono Insertar texto y coloque el cursor donde desee insertar el texto y escriba la información. O bien, coloque el cursor donde desee insertar texto y empiece a escribir. La información añadida aparece en fuente de color verde:

- **Agregar comentario**\(![](images/review-comment-icon.svg)\): Si desea agregar un tipo de comentario de nota adhesiva, haga clic en el icono Agregar comentario e introduzca el comentario en la ventana emergente.


**Barra de herramientas contextual**

También puede resaltar o tachar rápidamente el texto con la barra de herramientas contextual. Siga estos pasos para comentar con la barra de herramientas contextual:

1. Seleccione el texto que desee resaltar o tachar. Aparecerá la barra de herramientas contextual.

   ![](images/review-quick-launch-toolbar.png)

1. Haga clic en el **Resaltar** o **Tachado** icono.
1. Puede agregar comentarios en el panel de comentarios para la acción de resaltado o tachado.

**Revisar mediante el panel Comentarios** - El panel Comentarios muestra una lista de comentarios sobre el tema actual. En este panel también se muestran los comentarios de otros revisores si el tema se envía a varios revisores. Cada comentario del panel de comentarios está vinculado al texto correspondiente del tema actual. Ayuda a identificar el texto comentado. Cada comentario muestra el nombre del revisor que ha agregado el comentario junto con la marca de tiempo.

Los comentarios se muestran en el orden del texto comentado en el documento. Por ejemplo, hay un comentario destacado en la primera oración y un comentario de texto insertado en la segunda oración del primer párrafo. A continuación, el comentario de texto resaltado se muestra antes del comentario de texto insertado.

Las tareas que puede realizar mediante el panel Comentarios se describen a continuación:

- Al hacer clic en un comentario, se resalta y muestra la ubicación del comentario correspondiente en el documento.
- Puede agregar respuestas a comentarios.
- Puede editar su propio comentario haciendo clic en su texto comentado en el panel Comentarios y luego seleccionando **Editar** en el menú Opciones.
- Puede eliminar sus propios comentarios haciendo clic en el comentario en el panel Comentarios y luego seleccionando la opción **Eliminar** en el menú Opciones.

   ![](images/review-comment-options-menu.png)

   >[!NOTE]
   >
   > El menú Opciones solo aparece cuando pasa el ratón por encima de sus propios comentarios. Otros revisores no la muestran para los comentarios.

- Todos los usuarios participantes pueden responder a los comentarios enviados por otros usuarios. En un comentario, haga clic en **Responder** y pulse Intro para enviar una respuesta.

**Modo de vista previa**

- Al abrir un tema en el modo de vista previa, se muestra cómo se mostrará un tema cuando lo vea un autor después de aplicar todos los cambios. Por ejemplo, todo el texto insertado se muestra como texto normal y todo el texto marcado como \(eliminado\) se elimina del contenido.

- La siguiente captura de pantalla muestra el contenido de *Consulte* modo:

![](images/review-author-mode.png)

La siguiente captura de pantalla muestra el contenido de *Vista previa* modo:

![](images/review-preview-mode.png)

**Añadir archivos adjuntos a los comentarios** - Si desea complementar su comentario proporcionando información adicional disponible en algún otro archivo, puede adjuntarla con su comentario. Como revisor, puede añadir fácilmente uno o varios archivos del sistema local al comentario. Se puede agregar un archivo a todas las formas de comentarios compatibles: Resaltar, Tachar, Insertar texto o Comentario.

Al insertar cualquiera de los comentarios, aparece el elemento emergente de comentarios. Después de proporcionar comentarios o información adicional en la ventana emergente, puede enviarla pulsando Intro. Una vez agregado el comentario, se obtiene la opción de agregar un adjunto a ese comentario.

![](images/comment-pop-up-panel.png)

En la captura de pantalla anterior, el documento contiene la ventana emergente del comentario destacado y el comentario también se agrega en el panel Comentarios. El icono de archivo adjunto ![](images/file-attach-review.svg)está disponible junto con el comentario en ambas ubicaciones.

Realice los siguientes pasos para agregar datos adjuntos al comentario:

1. Haga clic en el *Agregar archivo adjunto* icono ![](images/file-attach-review.svg) en el comentario con el que desea añadir un archivo adjunto.

   Aparecerá el cuadro de diálogo Abrir archivo.

1. Seleccione uno o varios archivos que desee adjuntar.

   Los archivos seleccionados se muestran junto con el comentario en el panel Comentarios.

   En el panel Comentarios puede ver el nombre del archivo y su tamaño. También tiene la opción de eliminar un archivo haciendo clic en el icono de eliminación ![](images/Delete_icon.svg) asociado al nombre del archivo.

1. Haga clic en **Enviar**.

   Los archivos adjuntos se cargan y se añaden al comentario.


**Notas adicionales sobre el trabajo con archivos adjuntos:**

- De forma predeterminada, solo se muestran dos archivos adjuntos a un comentario. Si hay más archivos, **Ver archivo adjunto** a la derecha muestra el número de todos los archivos adjuntos \ (que son más de dos\) asociados al comentario. Puede hacer clic en el número para ver todos los archivos adjuntos. Por ejemplo, si tiene cuatro archivos adjuntos con un comentario, verá +2 en el botón .

![](images/review-view-attachment.png)

- Al pasar el puntero del ratón sobre un archivo adjunto, se ofrecen las opciones para descargarlo o quitarlo. La eliminación del archivo adjunto solo está disponible si el revisor actual ha añadido ese comentario, como se muestra en la siguiente captura de pantalla:

![](images/current-user-comment-options.png)

Los demás revisores o autores solo obtienen la opción descargar archivo adjunto.

![](images/other-reviewer-download.png)

- Puede descargar todos los archivos adjuntos asociados a un comentario desde el **Ver archivos adjuntos** diálogo. Seleccione los archivos adjuntos y haga clic en el botón **Descargar** en el nivel de comentario.

- También puede eliminar los archivos adjuntos asociados a un comentario desde la **Ver archivos adjuntos** diálogo. Seleccione los archivos adjuntos y haga clic en el botón **Eliminar** icono.

![](images/attach-files-comments-panel.png)


**Panel Condiciones** - Si el tema tiene contenido condicional, verá la variable **Condiciones** \(![](images/conditions-icon.svg)\) a la derecha. Haga clic en **Condiciones** abre el panel Condiciones , que le permite resaltar el contenido según las condiciones disponibles en el tema.

: De forma predeterminada **Resaltar todas las condiciones** está activada, se seleccionan todas las condiciones, se muestra todo el contenido y se muestra el contenido condicional como resaltado tanto en modo de revisión como de previsualización.

: Puede desactivar **Resaltar todas las condiciones** y vea todo el contenido presente en el tema como texto normal sin ningún resaltado.

![](images/review-conditions-panel.png)

Puede elegir ocultar o mostrar una condición específica.

- Si oculta una condición, el contenido que tenga esa condición no se resalta en el modo de revisión.
- Si muestra una condición, el contenido condicionado se resalta en el modo de revisión. Por ejemplo, en la siguiente captura de pantalla, solo el contenido utiliza dos condiciones: `win` y `mac` está resaltado.


![](images/review-condition-normal-mode.png)

En el modo de vista previa, el contenido no condicionado y el contenido condicionado que utiliza las dos condiciones mostradas: `win` y `mac` se muestra. El contenido condicional restante para el que están ocultas las condiciones no se muestra.

**Revisión en tiempo real** - El panel Comentarios se actualiza en tiempo real con comentarios y los comentarios o acciones del autor sobre los comentarios.

- Varios revisores podrán dejar comentarios o responder comentarios simultáneamente en el mismo documento. Para saber quién está revisando el documento, pase el ratón sobre el icono de usuario en la esquina superior derecha de la pantalla.

- Si un tema es parte de varias tareas de revisión, los comentarios realizados en una tarea no se muestran en la otra tarea.

- Hacer clic en el icono Comentario obsoleto \(![](images/outdated-comment-icon.svg)\) muestra las diferencias entre la última y la versión comentada del documento. Los números de versión \(de las versiones que se comparan\) se muestran en la parte superior de los documentos.

   ![](images/comments-page-review-mode.png)

   >[!NOTE]
   >
   > Cuando pasa el ratón por encima del icono Comentario obsoleto, se muestra el número de versión del tema en el que se agregó el comentario. Por ejemplo, si se ha proporcionado un comentario en la versión 1.0, se muestra lo mismo.

- Al hacer clic en un comentario obsoleto se abre la versión de ese comentario en el panel izquierdo. La versión anterior se muestra en el panel izquierdo y la versión actual se muestra en el panel derecho. Todos los comentarios de la versión obsoleta se importan en el lado izquierdo. Puede comparar la versión anterior con la versión actual.

**Filtrar comentarios** - Puede filtrar los comentarios de un documento para ver los comentarios específicos que necesite. Para filtrar los comentarios, haga clic en el botón **Filtro** icono \(![](images/filter-search-icon.svg)\) que aparece en el menú de la derecha del cuadro de texto Buscar comentarios del panel Comentarios.

Seleccione una o varias de las siguientes opciones de filtrado en la sección **Tipo de filtro** diálogo y haga clic en **Aplicar**.

- **Tipo de revisión** - Filtra en función del tipo de comentarios: Resaltar, Eliminar, Inserción o Comentario.
- **Estado de revisión** - Filtra en función del estado del comentario como Aceptado, Rechazado o Ninguno.
- **Revisores** - Filtra según el nombre del revisor.

- **Versiones** - Filtrar sobre la base de los comentarios recibidos en una versión particular del tema.

   Al usar los filtros, los comentarios en el panel derecho se filtran según la selección y el número de comentarios en el panel izquierdo se actualiza en consecuencia.


Para eliminar el filtro y ver todos los comentarios, anule la selección de todos los filtros del **Tipo de filtro** diálogo y haga clic en **Aplicar**.

**Tema principal:**[ Revisión de temas o mapas](review.md)

