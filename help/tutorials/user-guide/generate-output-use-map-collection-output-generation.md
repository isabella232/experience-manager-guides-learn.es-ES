---
title: Usar la colección de mapas para la generación de resultados
description: Aprenda a utilizar la colección de mapas para la generación de resultados
exl-id: 32e3af6c-9670-42cc-8dbe-9f99fbc60adf
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 1%

---

# Usar la colección de mapas para la generación de resultados {#id1723F20G0HS}

En cualquier organización, un producto puede tener varios tipos de documentación. Como especialista en publicaciones, le gustaría controlar qué salida desea generar para qué documento. Además, debería haber una forma de publicar varios documentos por lotes con un solo clic.

AEM guías permite organizar el contenido para su publicación mediante un tablero denominado Colección de mapas. Una colección de mapas le permite ensamblar todos los tipos diferentes de documentos en una sola unidad. Puede elegir el tipo de salida que desea generar para cada documento de la colección de mapas. Además, también puede generar resultados y ver el progreso de generación de resultados desde el panel de publicación.

La colección de mapas le da la opción de ver si hay algún cambio en cualquier mapa de la última salida publicada. Puede ver los detalles en la ficha Mapas y ajustes preestablecidos de la colección de mapas y, a continuación, volver a publicar la salida si es necesario. Para obtener más información, consulte Adición de un mapa a una colección de mapas.

## Crear una colección de mapas y agregar mapas DITA

Para crear una colección de mapas y agregar mapas DITA a la colección, realice los pasos siguientes:

1. En la interfaz de usuario de Assets, haga clic en **Asignar colecciones**.

   Si el vínculo Asignar colecciones no está disponible, seleccione la opción **Navegación** en el carril izquierdo y, a continuación, haga clic en **Asignar colecciones**.

   ![](images/access-map-collection-left-rail.png){width="350" align="left"}

1. Introduzca un Título para la colección de mapas.
1. Haga clic en **Crear**.

   Se muestra un mensaje de éxito al crear la colección de mapas.

1. Haga clic en **Cerrar** en el mensaje de éxito.

   El archivo de asignación recién creado se muestra en la página Asignar colecciones .

1. Haga clic en el cuadro gris del mosaico de la colección que desee editar.
1. Haga clic en **Editar** y haga clic en **Adición de mapas**.
1. Busque y añada los mapas DITA que desee agregar a la colección de mapas.

   De forma predeterminada, todos los ajustes preestablecidos y configuraciones regionales asociados con el mapa se añaden automáticamente.

1. Seleccione la salida deseada activando o desactivando el botón deslizante.
1. Haga clic en **Listo**.

   Los archivos de asignación DITA se añaden a la colección de mapas.

   ![](images/maps_presets_62_63.png){width="800" align="left"}

Las siguientes opciones de filtrado y los detalles de asignación se muestran en la página de recopilación:

- **Filtro:** El último carril muestra los siguientes filtros:
   - **Modificado**: Puede seleccionar Sí o No. Si selecciona sí, solo los mapas DITA modificados se mostrarán en la tabla Mapas y ajustes preestablecidos.
   - **Ajuste preestablecido**: Seleccione un ajuste preestablecido para el que desee filtrar los archivos de asignación. Por ejemplo, si elige *Sitio AEM* preestablecido, solo se muestran los mapas que tienen la variable *Sitio AEM* ajuste preestablecido de salida configurado en ellos.
   - **Idioma**: Puede seleccionar cualquiera de los códigos de idioma disponibles y mostrar solo el idioma seleccionado en la tabla Mapas y ajustes preestablecidos.
- **Mapas y ajustes preestablecidos** tabla: La tabla Mapas y ajustes preestablecidos presenta información en las columnas siguientes:
   - **Mapa**: Muestra el título del archivo de asignación DITA.
   - **Idioma**: Muestra el idioma del mapa DITA.
   - **Ajuste preestablecido**: Muestra el tipo de ajuste preestablecido de salida configurado en el archivo de asignación.
   - **Modificado**: Indica si el mapa de DITA se actualiza después de la última publicación. En función de esta información, puede decidir si desea volver a publicar la salida de este mapa DITA o no.
   - **Última generación**: Muestra la fecha y la hora del último resultado generado.

## Configuración y generación del resultado mediante una colección de mapas

Para configurar y generar la salida mediante una colección de mapas, realice los pasos siguientes:

1. Abra la colección de mapas.
1. \(Opcional\) Realice una de las siguientes acciones en función de sus necesidades:
   - Aplique Filtros desde el carril izquierdo para filtrar los mapas modificados, el ajuste preestablecido de salida o el idioma.
   - Si es necesario, haga clic en **Editar** y cambie la salida deseada activando o desactivando el botón deslizante.
1. Realice una de las siguientes acciones:

   - Para generar el resultado de los mapas seleccionados, seleccione los archivos de mapa y haga clic en **Generar seleccionados**.
   - Para generar la salida de todos los mapas DITA con sus ajustes preestablecidos configurados, haga clic en **Generar todo**.

   >[!IMPORTANT]
   >
   > Si un proceso de generación de salida para un ajuste preestablecido o mapa DITA está en cola o en curso, no se puede iniciar otra tarea de generación de salida para el mismo ajuste preestablecido o mapa.


## Eliminar una colección de mapas o un mapa DITA de la colección de mapas

- Para eliminar una colección de mapas, seleccione una colección en la página Colección de mapas y haga clic en **Eliminar**.
- Para eliminar un mapa DITA de una colección de mapas, abra Colección de mapas en modo de edición, seleccione el archivo de mapa DITA y haga clic en **Quitar de la colección**.

   Esto también eliminará de la colección de mapas cualquier ajuste preestablecido o configuración regional asociado con el mapa DITA.


## Cancelar una tarea de generación de salida de una colección de mapas

Similar a la forma de cancelar una tarea de generación de salida de la variable [Consola de asignación DITA](generate-output-for-a-dita-map.md#id2061H100T5Z) o [Publicar tablero](generate-output-publish-dashboard.md#), puede cancelar una tarea de generación de salida desde una colección de mapas. Acceda a la pestaña Salidas de una colección de mapas, vaya a la tarea de publicación que desea cancelar y haga clic en el botón **Cancelar este trabajo** para cancelar la tarea de publicación.

![](images/cancel-publish-task-map-collection.png){width="800" align="left"}

**Tema principal:**[ Generación de resultados](generate-output.md)
