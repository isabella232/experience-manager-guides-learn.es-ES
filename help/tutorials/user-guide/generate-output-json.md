---
title: JSON
description: Aprenda a utilizar JSON
source-git-commit: 8b6294425c6e60d1c5b37d98e99114014a104ee6
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 1%

---


# JSON {#id231KK0180T4}

Puede crear el ajuste preestablecido de JSON desde el Editor web:

En el panel Repositorio, abra el archivo de asignación DITA en la vista Mapa, luego, en la pestaña Salida, seleccione el icono + para crear un ajuste preestablecido de salida y, a continuación, seleccione JSON en la lista desplegable Tipo del cuadro de diálogo Agregar ajuste preestablecido.

En el editor web, las siguientes configuraciones se han organizado en la sección **General** pestaña:

- Ruta de salida
- Archivo de índice
- Aplicar condiciones usando \(Si las condiciones están definidas para un mapa\)
- Usar línea de base \(Si se crea una línea de base para un mapa\)
- Propiedades que se propagarán en la salida
- Flujo de trabajo de posgeneración

Para obtener más información, consulte [Configuración JSON](#id231KJA00REJ).

**Desde el panel de mapas**

Para abrir los ajustes preestablecidos de salida para el PDF, haga clic en un archivo de asignación DITA desde la interfaz de usuario de Assets, luego haga clic en Ajustes preestablecidos de salida y, a continuación, haga clic en la opción HTML5. En el panel Mapa, haga clic en **Editar** en la parte superior para actualizar las distintas configuraciones y, a continuación, haga clic en **Guardar**.

**Configuración JSON**

Las siguientes opciones están disponibles para el ajuste preestablecido JSON:

>[!NOTE]
>
> También puede editar el archivo JSON en el Editor web.

| Opciones de salida JSON | Descripción |
| --- | --- |
| Ruta de salida | La ruta dentro del repositorio de AEM donde se almacena la salida JSON. |
| Archivo de índice | Puede asignar un nombre al archivo de índice que está creando para la salida JSON. De forma predeterminada, selecciona el nombre de archivo del mapa DITA y añade un sufijo (como `map_filename_index.json`).<br><br>También puede utilizar variables al configurar el archivo de índice. Para obtener más información sobre el uso de variables, consulte [Utilice variables para configurar las opciones Ruta de destino, Nombre del sitio o Nombre de archivo](generate-output-use-variables.md#id18BUG70K05Z). |
| Aplicar condiciones usando | Seleccione una de las siguientes opciones:<br><br>* **Ninguno aplicado**: Seleccione esta opción si no desea aplicar ninguna condición en la salida publicada.<br>* **Archivo DITAVAL**: Seleccione archivos DITAVAL para generar contenido personalizado. Puede seleccionar varios archivos DITAVAL utilizando el cuadro de diálogo Examinar o escribiendo la ruta del archivo. Utilice el icono cruzado cerca del nombre del archivo para eliminarlo. Los archivos DITAVAL se evalúan en el orden especificado, por lo que las condiciones especificadas en el primer archivo tienen prioridad sobre las condiciones coincidentes especificadas en los archivos posteriores. Puede mantener el orden de los archivos añadiendo o eliminando archivos. Si el archivo DITAVAL se mueve a otra ubicación o se elimina, no se elimina automáticamente del panel de mapas. Debe actualizar la ubicación en caso de que los archivos se muevan o eliminen. Puede pasar el ratón sobre el nombre del archivo para ver la ruta en el repositorio de AEM donde se almacena el archivo. Sólo puede seleccionar archivos DITAVAL y se muestra un error si ha seleccionado cualquier otro tipo de archivo.<br>* **Ajuste preestablecido de condición**: Seleccione un ajuste preestablecido de condición en la lista desplegable para aplicar una condición al publicar la salida. La opción está visible si ha añadido una condición presente en la ficha Ajustes preestablecidos de condición de la consola de asignación DITA. Para obtener más información sobre el ajuste preestablecido de condición, consulte [Usar ajustes preestablecidos de condición](generate-output-use-condition-presets.md#id1825FL004PN). |
| Usar línea de base | Si ha creado una Línea de base para el mapa DITA seleccionado, seleccione esta opción para especificar la versión que desea publicar.<br><br>Consulte [Trabajo con línea de base](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) para obtener más información. |
| Propiedades que se propagarán en la salida | Seleccione las propiedades que desee procesar como metadatos. Estas propiedades se establecen desde la página Propiedades del mapa DITA o del archivo de mapa de libros. Las propiedades que seleccione en la lista desplegable se enumeran debajo del campo Propiedades .<br><br>**Nota**: También puede definir propiedades personalizadas y pasar los metadatos a la salida mediante la publicación DITA-OT. Para obtener más información, consulte [Trabajar con metadatos](metadata-dita.md#id21BJ00QD0XA). |
| Flujo de trabajo de posgeneración | Al elegir esta opción, se muestra una nueva lista desplegable Flujo de trabajo de posgeneración que contiene todos los flujos de trabajo configurados en AEM. Debe seleccionar un flujo de trabajo que desee ejecutar después de completar el flujo de trabajo de generación de resultados.<br><br>**Nota**: Para obtener más información sobre la creación de un flujo de trabajo personalizado de generación posterior a la salida, consulte _Personalización del flujo de trabajo de generación posterior a la salida_ en la guía as a Cloud Service Instalar y configurar guías de Adobe Experience Manager . |

**Tema principal:**[ Explicación de los ajustes preestablecidos de salida](generate-output-understand-presets.md)

