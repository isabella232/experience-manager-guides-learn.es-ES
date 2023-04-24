---
title: Generar PDF
description: Obtenga información sobre cómo generar resultados de PDF
source-git-commit: 8b6294425c6e60d1c5b37d98e99114014a104ee6
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 1%

---


# PDF {#id205BE600HAH}

Puede crear el ajuste preestablecido de PDF de dos formas:

**Desde el Editor web:** En el panel Repositorio, abra el archivo de asignación DITA en la vista Mapa y, a continuación, en la ficha Salida, seleccione el icono + para crear un ajuste preestablecido de salida y, a continuación, seleccione PDF en la lista desplegable Tipo del cuadro de diálogo Agregar ajuste preestablecido.

>[!NOTE]
>
> Puede elegir el método para generar el PDF mediante DITA-OT, Native PDF o FMPS \ (si el administrador del sistema lo ha configurado\).

En el editor web, las configuraciones se han organizado en las pestañas General y Avanzado :

**General**

La variable **General** contiene las siguientes configuraciones:

- Ruta de salida
- Argumentos de la línea de comandos DITA-OT
- Nombre de transformación
- Nombre de archivo del PDF
- Aplicar condiciones usando \(Si las condiciones están definidas para un mapa\)
- Usar línea de base \(Si se crea una línea de base para un mapa\)
- Flujo de trabajo de posgeneración

**Avanzado**

La pestaña Advanced contiene las siguientes configuraciones:

- Habilitar versiones
- Limpiar archivos temporales DITA-OT

Para obtener más información, consulte [configuración del PDF](#id231KIM004X1).

**Desde el panel de mapas**

Para abrir los ajustes preestablecidos de salida para el PDF, haga clic en un archivo de asignación DITA desde la interfaz de usuario de Assets y, a continuación, haga clic en Ajustes preestablecidos de salida y, a continuación, haga clic en la opción PDF . En el panel Mapa, haga clic en **Editar** en la parte superior para actualizar las distintas configuraciones y, a continuación, haga clic en **Guardar**.

**configuración del PDF**

Las siguientes opciones están disponibles para la salida del PDF:

| opciones del PDF | Descripción |
| --- | --- |
| Tipo de salida | El tipo de salida que desea generar. Para generar la salida del PDF, seleccione la opción PDF . |
| Nombre de la configuración | Asigne un nombre descriptivo a la configuración de salida del PDF que está creando. Por ejemplo, puede especificar _Salida de clientes internos_ o _salida de usuarios finales_. |
| Argumentos de la línea de comandos DITA-OT | Especifique los argumentos adicionales que desea que DITA-OT procese durante la generación de resultados. Para obtener más información sobre los argumentos de línea de comandos admitidos en DITA-OT, consulte [Documentación de DITA-OT](https://www.dita-ot.org/). |
| Aplicar condiciones usando | Seleccione una de las siguientes opciones:<br><br>* **Ninguno aplicado**: Seleccione esta opción si no desea aplicar ninguna condición en la salida publicada.<br>* **Archivo DITAVal**: Seleccione archivos DITAVal para generar contenido personalizado. Puede seleccionar varios archivos DITAVal mediante el cuadro de diálogo Examinar o escribiendo la ruta de acceso del archivo. Utilice el icono cruzado cerca del nombre del archivo para eliminarlo. Los archivos DITAVal se evalúan en el orden especificado, por lo que las condiciones especificadas en el primer archivo tienen prioridad sobre las condiciones coincidentes especificadas en los archivos posteriores. Puede mantener el orden de los archivos añadiendo o eliminando archivos. Si el archivo DITAVal se mueve a otra ubicación o se elimina, no se elimina automáticamente del panel de mapas. Debe actualizar la ubicación en caso de que los archivos se muevan o eliminen. Puede pasar el ratón sobre el nombre del archivo para ver la ruta en el repositorio de AEM donde se almacena el archivo. Sólo puede seleccionar archivos DITAVal y se muestra un error si ha seleccionado cualquier otro tipo de archivo. FrameMaker Publishing Server no admite varios archivos DITAVAL.<br>* **Ajuste preestablecido de condición**: Seleccione un ajuste preestablecido de condición en la lista desplegable para aplicar una condición al publicar la salida. La opción está visible si ha añadido una condición presente en la ficha Ajustes preestablecidos de condición de la consola de asignación DITA. Para obtener más información sobre el ajuste preestablecido de condición, consulte [Usar ajustes preestablecidos de condición](generate-output-use-condition-presets.md#id1825FL004PN). |
| Generar PDF mediante | Seleccione DITA-OT para generar el PDF. |
| Ejecutar flujo de trabajo de posgeneración | Al elegir esta opción, se muestra una nueva lista desplegable Flujo de trabajo de posgeneración que contiene todos los flujos de trabajo configurados en AEM. Debe seleccionar un flujo de trabajo que desee ejecutar después de completar el flujo de trabajo de generación de resultados.<br><br>**Nota**: Para obtener más información sobre la creación de un flujo de trabajo personalizado de generación posterior a la salida, consulte Personalización del flujo de trabajo de generación posterior a la salida en Instalar y configurar guías de Adobe Experience Manager as a Cloud Service. |
| Nombre de transformación | Especifique el tipo de salida que desea generar. Esto es necesario si desea generar resultados utilizando su propio complemento personalizado, que está integrado en el complemento DITA-OT. Por ejemplo, si desea generar una salida XHTML, especifique `xhtml`. Para obtener una lista de transformaciones disponibles en DITA-OT, consulte [Transformaciones DITA-OT (formatos de salida)](http://www.dita-ot.org/2.3/user-guide/AvailableTransforms.html) en la Guía del usuario de OASIS DITA-OT. |
| Nombre de archivo | Especifique el nombre de archivo con el que desea guardar el PDF.<br><br>También puede utilizar variables al configurar el nombre de archivo del PDF. Para obtener más información sobre el uso de variables, consulte [Utilice variables para configurar las opciones Ruta de destino, Nombre del sitio o Nombre de archivo](generate-output-use-variables.md#id18BUG70K05Z).<br><br>**Nota**: Si no proporciona un nombre de archivo, se utilizará el título del mapa DITA para generar el nombre del archivo del PDF final. Si el mapa no tiene título, se utilizará el nombre de archivo del mapa DITA para nombrar el PDF final. El nombre del archivo se saneará usando las reglas configuradas en el sistema para gestionar cualquier carácter no válido. |
| Ruta de destino | La ruta dentro del repositorio de AEM donde se almacena el PDF.<br><br>También puede utilizar variables al establecer la ruta de destino. Para obtener más información sobre el uso de variables, consulte [Utilice variables para configurar las opciones Ruta de destino, Nombre del sitio o Nombre de archivo](generate-output-use-variables.md#id18BUG70K05Z). |
| Limpiar archivos temporales DITA-OT | Seleccione esta opción para limpiar los archivos temporales generados por DITA-OT. La ubicación donde DITA-OT almacena archivos temporales se encuentra en el registro de generación de salida.<br><br>Si está experimentando errores mientras genera resultados a través de DITA-OT, puede anular la selección de esta opción para conservar los archivos temporales. A continuación, puede utilizar esos archivos para solucionar los errores de generación de resultados. |
| Usar línea de base | Si ha creado una Línea de base para el mapa DITA seleccionado, seleccione esta opción para especificar la versión que desea publicar.<br><br>Consulte [Trabajo con línea de base](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) para obtener más información. |
| Propiedades | Seleccione las propiedades que desee procesar como metadatos. Estas propiedades se establecen desde la página Propiedades del mapa DITA o del archivo de mapa de libros. Las propiedades que seleccione en la lista desplegable se enumeran debajo del **Propiedades** y se eliminan de la lista desplegable. Una vez establecidas, estas propiedades también se copian en los temas dentro del mapa.<br><br>Nota: También puede pasar los metadatos a la salida mediante la publicación DITA-OT. Para obtener más información, consulte [Pasa los metadatos a la salida utilizando DITA-OT](pass-metadata-dita-ot.md#id21BJ00QD0XA). |

**Tema principal:**[ Explicación de los ajustes preestablecidos de salida](generate-output-understand-presets.md)

