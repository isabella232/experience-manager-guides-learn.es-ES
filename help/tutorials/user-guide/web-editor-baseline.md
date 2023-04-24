---
title: Crear y administrar líneas de base desde el Editor web
description: Obtenga información sobre cómo crear y administrar líneas de base desde el Editor web
source-git-commit: 873111892d5b479f80a40c0b18cda9b538f5a1de
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 0%

---


# Crear y administrar líneas de base desde el Editor web {#id223MB0ZF043}

>[!TIP]
>
> Se recomienda utilizar esta función de línea de base del Editor web si se ha actualizado a AEM versión as a Cloud Service de marzo o posterior.

AEM guías proporciona la función de línea de base integrada en el Editor web que permite a los usuarios crear líneas de base y utilizarlas para publicar o traducir temas de distintas versiones.

## Crear una línea de base

Puede crear una línea de base desde el Editor web siguiendo estos pasos:

1. En el panel Repositorio, abra el archivo de asignación DITA en la vista Mapa.
1. Haga clic en el **Administrar** pestaña . La variable **Línea de base** muestra las líneas de base del mapa DITA.

   ![](images/baseline-manage.png)

1. En el **Línea de base** , haga clic en el icono + en la parte superior derecha. Puede crear una línea de base con una versión específica de los temas y el contenido al que se hace referencia disponible en una fecha y hora específicas, o con una etiqueta definida para una versión de los temas.
1. Introduzca un nombre para la línea base en **Nombre de línea de base**.
1. En **Opción de línea de base**, puede elegir **Usar versión de archivo** o **Usar etiquetas** opción:

   **Usar versión de archivo**: Puede crear una línea de base estática con una versión específica de los temas y el contenido al que se hace referencia disponible en una fecha y hora específicas, o con una etiqueta definida para una versión de los temas:

   - En **Establezca la última versión en función de,** seleccione una de las siguientes opciones:


      1. **Fecha** &lt;time stamp=&quot;&quot;>: Selecciona la versión de los temas en la fecha y hora especificadas.
      1. **Etiqueta**: Seleccione esta opción para elegir los temas según la etiqueta que se les haya aplicado. Si los temas tienen etiquetas especificadas para ellos, las etiquetas se enumeran en la lista desplegable. Puede elegir una etiqueta de la lista. También puede agregar una etiqueta en el cuadro de texto.\
         Al seleccionar **Etiqueta,** puede elegir las referencias directas e indirectas.
      - Para las referencias directas dentro del mapa DITA, se le da la opción de utilizar la última versión de temas que no tienen la etiqueta especificada aplicada a ellos.

      >[!NOTE]
      >
      > Si introduce una etiqueta que no existe y selecciona la opción **No crear una línea de base** a continuación, la creación de la línea de base falla y da un mensaje de error cerca del nombre de la línea de base en el panel Línea de base.

      - Para las referencias indirectas dentro del mapa DITA, se le da una opción adicional para utilizar la última versión de los temas que no tienen la etiqueta especificada aplicada en ellos. También puede elegir **Seleccionar automáticamente** para el contenido al que se hace referencia y el sistema selecciona automáticamente la versión del contenido al que se hace referencia correspondiente a la versión del contenido en la que se hace referencia.

   Una vez que haya seleccionado una etiqueta o versión como fecha, todos los temas a los que se hace referencia y los archivos multimedia del mapa se seleccionan según corresponda. Esta selección de temas no se muestra en la interfaz de usuario, pero se guarda en el servidor.

   **Usar etiquetas**: Seleccione esta opción para la creación de la línea de base a fin de elegir los temas según la etiqueta que se les aplique.

   Las líneas de base basadas en etiquetas se actualizan dinámicamente. Si genera una línea de base, descarga una línea de base o crea un proyecto de traducción con una línea de base, los archivos se seleccionan dinámicamente en función de las etiquetas actualizadas. Por ejemplo, si ha utilizado la versión 1.2 de un tema con Label Release 1.0 para la línea de base y la versión 1.5 actualizada posteriormente con Label Release 1.0, la línea de base se actualizará dinámicamente y se utilizará la versión 1.5.

   ![](images/dynamic-baseline.png)

   - **Seleccionar etiquetas**: Si los temas tienen etiquetas especificadas para ellos, las etiquetas se enumeran en la variable **Seleccionar etiquetas** lista desplegable. Puede elegir la etiqueta\(s\) de la lista. A las etiquetas seleccionadas primero se les da mayor prioridad que a las posteriores.
1. **Referencias indirectas**: Para las referencias indirectas dentro del mapa DITA, se ofrecen las siguientes opciones:

   - **Seleccionar automáticamente**: Puede elegir **Seleccionar automáticamente** para el contenido al que se hace referencia y el sistema selecciona automáticamente la versión del contenido al que se hace referencia correspondiente a la versión del contenido en la que se hace referencia.

   - **Usar etiqueta seleccionada**: Puede crear una línea de base con la etiqueta seleccionada definida para una versión de los temas.
   - **Usar la última versión o la copia de trabajo**: Utilice la versión más reciente de los temas que no tengan la etiqueta especificada aplicada o si no se ha creado ninguna versión, utilice la copia de trabajo de los temas para crear la línea de base.
1. Haga clic en **Aplicar**.

Se crea la línea base. La creación de la línea de base se realiza de forma asíncrona, por lo que puede seguir trabajando en otros archivos del Editor web. Una vez creada la línea de base, aparece un mensaje emergente que confirma la creación de la línea de base y que también recibe una notificación de bandeja de entrada para la misma.

## Administrar líneas de base

Puede administrar las líneas de base existentes mediante las distintas funciones del panel Línea de base.

- Puede buscar una línea de base existente mediante el cuadro de texto del panel Línea de base. Utilice la variable **Aplicar filtro** para mostrar todas las líneas de base o mostrar las líneas de base con el estado de creación como Correcto, En curso o Fallido.
- Utilice la variable **Actualizar** en el panel Línea de base para volver a comprobar todas las líneas de base y mostrar una nueva lista de líneas de base para el mapa DITA que se abre en la vista Mapa.
- Puede ver o editar el contenido de una línea de base existente haciendo doble clic en la línea de base de la lista del panel Línea de base. La ventana de edición de línea de base del centro muestra el archivo de asignación DITA, el contenido o los temas del mapa y el contenido al que se hace referencia.


![](images/baseline-options.png)

También puede realizar las siguientes operaciones en la línea de base desde el menú Opciones:

- **Editar**, **Duplicar,** o **Eliminar** una línea de base existente.
- Agregue, elimine o realice cambios en las etiquetas existentes desde el **Administrar etiquetas** . Si el administrador ha configurado etiquetas predefinidas, se le mostrarán en la lista desplegable Agregar etiqueta . Para obtener más información sobre cómo agregar etiquetas, consulte [Usar etiquetas](web-editor-use-label.md#).

   >[!NOTE]
   >
   > El proceso para añadir o quitar etiquetas se produce de forma asíncrona, por lo que puede seguir trabajando en otros archivos del Editor web. Una vez añadida o eliminada la etiqueta, se muestra un mensaje emergente que confirma que la etiqueta se ha añadido o eliminado, y también recibe una notificación de bandeja de entrada para la misma.

- **Editar propiedades** de una línea base existente que haya establecido al crear la línea base.
- Exporte la instantánea de una línea de base en un archivo CSV con la variable **Exportar línea de base** .

**Filtros de línea de base**

Uso del icono Filtros en la sección **Filtros de línea de base** , puede aplicar filtros en la línea de base abierta en la ventana de edición de línea de base:

![](images/baseline-filter.png)

- Filtre los archivos en función de su nombre o ubicación.
- Filtre los archivos en función de los valores de diferentes columnas, como Tipo de archivo, Tipo de referencia, etc.
- Elija las columnas que desea mostrar en la ventana de edición de la línea de base.

>[!NOTE]
>
> Puede hacer clic en un encabezado de columna y ordenar los archivos en función de las columnas de la ventana de edición de línea de base.

**Guardar o restablecer una línea de base**

Una vez editada la línea de base, puede hacer clic en el botón **Guardar** en la parte superior para guardar los cambios en la línea base. Puede hacer clic en el botón **Restablecer** si no desea guardar el cambio y restablecer la línea de base. Al hacer clic en el botón **Restablecer** se muestra una advertencia que indica que se perderán los cambios sin guardar.

**Tema principal:**[ Trabajar con el Editor web](web-editor.md)

