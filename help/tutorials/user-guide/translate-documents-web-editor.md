---
title: Traducción de documentos desde el Editor Web
description: Obtenga información sobre cómo traducir documentos desde el Editor web
source-git-commit: 331871308035441f047b1ed588215b586daf3d28
workflow-type: tm+mt
source-wordcount: '1517'
ht-degree: 1%

---


# Traducción de documentos desde el Editor Web {#id21BKF0Z0YZF}

>[!TIP]
>
> Se recomienda utilizar esta función de traducción del Editor web si se ha actualizado a AEM Guías as a Cloud Service para la versión de febrero de 2022 o posterior.

AEM guías incluye una potente función en el Editor web que le permite traducir el contenido a varios idiomas. Puede crear un nuevo proyecto de traducción y luego agregar los trabajos de traducción al proyecto de traducción existente. También puede crear un proyecto de traducción multilingüe que incluya trabajos de traducción para todos los idiomas seleccionados.

>[!NOTE]
>
> El administrador puede configurar la ficha Administrar \(utilizada para la traducción\) en el Editor web. Para obtener más información, consulte *Configurar la función de traducción en el Editor web* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.

## Antes de empezar

Antes de realizar los pasos de este procedimiento, asegúrese de que ha creado las carpetas raíz y de destino del idioma necesarias

1. Cree una carpeta raíz para almacenar el contenido de origen. La carpeta raíz debe crearse con el nombre de idioma \ (como inglés\) o el código de idioma \(en\).
1. Cree las carpetas de destino a las que desee traducir el contenido. Por ejemplo, si desea traducir el contenido a alemán o francés, debe crear una carpeta con el nombre -de \(para alemán\) o -fr \(para francés\).

>[!NOTE]
>
> La carpeta raíz y las carpetas de destino deben crearse en el mismo nivel.

## Crear un proyecto de traducción

1. En el panel Repositorio, abra el archivo de asignación DITA en la vista Mapa.
1. Haga clic en el **Administrar** pestaña . El panel Traducción muestra el título hipervinculado del mapa DITA junto con la variable **Idiomas** lista.
1. En el **Idiomas** seleccione la configuración regional a la que desea traducir el proyecto. Puede seleccionar **Todo** para traducir el proyecto a todos los idiomas disponibles.

   >[!NOTE]
   >
   > La lista contiene las carpetas de idioma junto con sus códigos de idioma. Por ejemplo, francés \(fr\) y alemán \(de\).

   >[!IMPORTANT]
   >
   > El idioma muestra solo aquellos idiomas para los que se crea una carpeta de idioma en paralelo al idioma de origen. Tampoco se muestra una carpeta de idioma creada en otro nivel, como un nivel inferior desde la carpeta del idioma de origen. Asegúrese de crear todas las carpetas de idioma de destino en el mismo nivel que la carpeta de idioma de origen.

   ![](images/translation-languages.png)

1. También puede utilizar las siguientes opciones:

   **Usar línea de base:** Puede seleccionar una línea de base para traducir el proyecto. Haga clic en Usar línea de base y seleccione una línea de base creada en el mapa. Todos los archivos que forman parte de la Línea de base seleccionada se muestran en la página Traducción . Una vez traducido el contenido, puede exportar la línea de base traducida. Para obtener más información sobre la exportación de la línea de base traducida, consulte [Exportar línea de base traducida](generate-output-use-baseline-for-publishing.md#id196SE600GHS).

   **Usar la última versión como**: Elija filtrar la versión de los temas en función de su fecha y hora de creación. Cuando selecciona una fecha y hora, solo se muestra la última versión de los archivos creados en la fecha y hora seleccionadas o antes de esta.

1. Haga clic en **Aplicar**. Se muestra una lista con detalles de temas y recursos asociados.
1. Seleccione los temas que desea enviar para su traducción.

   También puede utilizar las siguientes opciones de filtrado de temas:

   - **Título**: Título del archivo de origen
   - **Nombre del archivo**: Nombre del archivo de origen
   - **Tipo de archivo**: Tipo del archivo de origen. Las opciones disponibles son Mapa, Tema e Imagen.
   - **Tipo de referencia**: Referencias directas o indirectas
   - **Versión**: Número de versión del archivo de origen
   - **Etiqueta de versión**: Etiqueta de la versión seleccionada del archivo de origen
   - **Versión de Target**: Número de versión del archivo de destino
   - **Estado del documento**: Estado del archivo de origen. Las opciones disponibles son Borrador, Revisión y Revisado.
   - **Idioma de Target**: El idioma al que desea traducir el archivo de origen
   - **Estado de traducción**: Las opciones disponibles son: Sin sincronización, sin copia, en curso y en sincronización.
   - **Etiqueta de Target**: Etiqueta de la versión seleccionada del archivo de destino
1. Haga clic en **Enviar para traducción** en la esquina superior derecha.

   ![](images/translation-send.png)

1. En el menú desplegable, seleccione **Crear un nuevo proyecto de traducción**.

   ![](images/translation-project-types.png)

   Además de un nuevo proyecto de traducción, también puede seleccionar entre las siguientes opciones:

   - Puede elegir **Crear una estructura** solo para el proyecto de traducción.
   - Puede seleccionar **Crear un nuevo proyecto de traducción multilingüe** que incluye trabajos de traducción para todos los idiomas que haya seleccionado para la traducción. Por ejemplo, si ha seleccionado francés, alemán y español, creará un proyecto que contiene trabajos de traducción para los tres idiomas.
   - Si ya tiene un proyecto de traducción, puede agregar temas a ese proyecto. Seleccione Agregar a **Proyecto de traducción existente** en la lista Proyecto y elija un proyecto en la lista Proyecto de traducción existente. Puede ordenar estos proyectos por orden más reciente, ascendente o descendente.

      >[!NOTE]
      >
      > Si el proyecto existente es un proyecto de creación de ámbitos, se ha añadido &#39;\(Creación de ámbitos\)&#39; en su nombre.

   - Si necesita crear el ámbito para traducir un proyecto, puede seleccionar **Crear un nuevo proyecto de traducción de ámbitos**. Esto no enviará las copias para su traducción y se mantiene el estado de traducción original de los archivos. No hay ningún impacto en la copia del idioma de destino de los temas referidos que se envían para el ámbito.
1. En el campo **Título del proyecto**, introduzca un título.
1. Haga clic en **Crear** para crear un nuevo proyecto de traducción.

   Se crea un nuevo proyecto de traducción con la versión seleccionada de los temas. En este momento, se muestra un mensaje emergente que confirma la creación del proyecto de traducción. Una vez que todas las copias de idioma de destino estén disponibles en el proyecto de traducción, se obtiene una notificación en la Bandeja de entrada. Una vez que las copias de idioma de destino están disponibles en el proyecto de traducción, puede continuar e iniciar el trabajo de traducción. Para obtener más información, consulte [Iniciar el trabajo de traducción](translation-first-time.md#id225IK030OE8).

   >[!NOTE]
   >
   > Si rechaza la traducción para uno o más temas de un trabajo de traducción, la variable **En curso** el estado de traducción de todos los temas rechazados vuelve a su estado original. El estado de los temas referidos se comprueba y se revierte según el estado de traducción más reciente. Además, los archivos de traducción creados en el proyecto de destino no se eliminan aunque la traducción se rechace para ellos.


## Pasar la etiqueta de versión a la versión de destino

AEM guías le permite pasar la etiqueta del archivo de origen al archivo de destino. Esto le ayudará a identificar fácilmente la versión de origen del archivo traducido.

Para añadir la etiqueta de versión de origen en la copia de destino, el administrador del sistema debe seleccionar la opción **Propagación de las etiquetas de la versión de origen a la versión de destino** en el **Traducción** en **Configuración del editor**.

Por ejemplo, si tiene algunos archivos de origen con la etiqueta de versión `Release 1.0` aplicados a ellos, también puede pasar la etiqueta de origen \(`Release 1.0`\) al archivo traducido.

![](images/translation-pass-source-label.png)

>[!NOTE]
>
> La etiqueta de origen solo está adjunta a una versión de destino. Si mueve la etiqueta de origen a otra versión, se refleja automáticamente en la etiqueta de destino más reciente.

## Ver diferencia de versión para archivos fuera de sincronización 

AEM guías proporciona la función para comprobar las diferencias entre la versión seleccionada y la última versión de origen traducida de los temas. Puede elegir traducir la variable **Sin sincronización** archivos basados en los cambios realizados.

![](images/translation-version-diff.png)

Seleccione el **Mostrar diferencia** icono \(![](images/show-difference-icon.svg)\) para ver las diferencias entre la última versión traducida y la versión actual del archivo seleccionado.

>[!NOTE]
>
> **Mostrar diferencia** icono \(![](images/show-difference-icon.svg)\) solo aparece para archivos DITA que tienen el estado de traducción como **Sin sincronización**.

La variable **Diferencia de versiones** se abre. Muestra la variable **Última versión traducida** y **Versión seleccionada** a la izquierda. La ventana de vista previa muestra las diferencias entre la última versión traducida y la versión seleccionada del tema.

![](images/version-diff.png)

## Descartar recursos fuera de sincronización

Si realiza cambios en algunos de los recursos, esos recursos quedan fuera de sincronización. Puede volver a traducir los recursos modificados o elegir rechazar el estado de falta de sincronización. Por ejemplo, si ha realizado algunos cambios muy menores que realmente no necesitan una traducción, puede marcar su estado a In Sync.

Para descartar el estado de falta de sincronización, realice los siguientes pasos:

1. Seleccione los recursos fuera de sincronización para los que desea cambiar el estado.
1. Seleccione el **Marcar en sincronización** botón \(![](images/translation-mark-in-sync-icon.svg)\) en la parte superior. La variable **Marcar en sincronización** se abre.

   ![](images/translation-mark-in-sync.png)

1. Haga clic en **Forzar sincronización**. Establece el estado en Sincronizado para los recursos sin sincronizar seleccionados.

>[!NOTE]
>
> **Marcar en sincronización** botón \(![](images/translation-mark-in-sync-icon.svg)\) solo aparece para los recursos que tienen el estado de traducción como No sincronizado.

## Ver proyectos de traducción en curso para un mapa o tema

Es posible que algunas de las referencias del panel de traducción estén en estado de progreso. Estas referencias tienen un **En curso** vincular en **Estado de traducción** para abrir el Navegador. Al hacer clic en el vínculo, la variable **Proyectos en curso** se abre. En el cuadro de diálogo, puede ver la lista de todos los proyectos de traducción en curso \(junto con el idioma de destino\) que contienen la referencia seleccionada.

>[!NOTE]
>
> Puede ver el vínculo In Progress para los proyectos traducidos creados en AEM guías as a Cloud Service para la versión de febrero de 2023 o posterior.

Haga clic en el nombre de la referencia en el cuadro de diálogo para abrirla en el modo de previsualización. También puede hacer clic en el proyecto de traducción para iniciar la traducción.

![](images/translation-in-progress.png)

**Tema principal:**[ Trabajar con el Editor web](web-editor.md)

