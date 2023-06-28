---
title: Inserción de un fragmento de contenido desde la fuente de datos
description: Aprenda a insertar un fragmento de contenido desde la fuente de datos
source-git-commit: 6061d35b86790e24c6f55e4ccac5dbb40c43aae8
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---


# Inserción de un fragmento de contenido desde la fuente de datos

AEM Guías de proporciona la función para conectarse con la fuente de datos. Puede recuperar los datos, insertarlos en los temas y editarlos. Puede crear fácilmente un fragmento de contenido mediante el generador de fragmentos de contenido y reutilizarlo dentro de sus temas.

Realice los siguientes pasos para crear un fragmento de contenido mediante el generador de fragmentos de contenido e insertarlo en el tema:

1. Seleccionar **Fuentes de datos** ![](images/data-source-icon.svg)   en el panel izquierdo para ver las fuentes de datos conectadas. El panel Fuentes de datos se abre y muestra todas las fuentes de datos conectadas. Para obtener más información, consulte [Configuración de un conector de fuente de datos](../cs-install-guide/conf-data-source-connector.md).

   >[!NOTE]
   >
   > Verá las fuentes de datos para las que el administrador ha configurado el conector.

1. Seleccione una fuente de datos para ver los generadores de fragmentos de contenido disponibles para la fuente de datos seleccionada.
   ![](images/code-snippet-generator.png){width="300" align="left"}
1. Seleccionar **Añadir** para agregar un nuevo generador de fragmentos de contenido. El **Añadir generador de fragmentos de contenido** se abre el panel.

1. Introduzca la consulta en el cuadro de texto Consulta de datos.
1. Seleccione la plantilla que se asigna a la fuente de datos desde el **Plantilla de asignación de datos** desplegable.
Las plantillas listas para usar del origen de datos seleccionado se muestran en la lista desplegable. Por ejemplo, puede ver la plantilla &quot;sql-table&quot; para la fuente de datos denominada &quot;PostgreSQL&quot;.

   >[!NOTE]
   >  
   > Si el administrador ha configurado plantillas personalizadas, también se le mostrarán esas plantillas en la lista desplegable (según las configuraciones de ruta de plantilla realizadas por el administrador).

1. Clic **Buscar** para recuperar los datos del origen de datos y aplicar la plantilla a los datos resultantes de la consulta SQL.

1. Los datos se pueden ver en la vista previa o en la vista de origen DITA.

   1. La vista previa muestra cómo se mostrarán los datos cuando se inserten en el contenido. La vista previa muestra una pequeña fracción de los datos con el formato de la plantilla seleccionada.
Por ejemplo:
      * Si ha seleccionado la plantilla de tabla SQL, puede ver los datos SQL en formato de tabla.
      * Si ha seleccionado la plantilla de lista ordenada por jira, puede ver una lista ordenada para los problemas de Jira.

   1. La vista de origen muestra los datos en la vista de origen DITA.
      ![](images/add-content-snippet-generator.png){width="800" align="left"}
1. Para guardar los resultados de la consulta, escriba el nombre del generador y haga clic en **AÑADIR**.   Se agrega a la lista un nuevo generador de fragmentos de contenido.

   >[!NOTE]
   >
   > Debe seguir la convención de nomenclatura de archivos para el nombre del nuevo generador de contenido. No puede haber un espacio en el nombre del generador de fragmentos de contenido. Tampoco puede guardar un nuevo generador de contenido con el nombre de un generador de contenido existente. Se produce un error.

## Opciones de un generador de fragmentos de contenido

Haga clic con el botón derecho en un generador de fragmentos de contenido para abrir Opciones. Con las opciones, puede realizar las siguientes operaciones:
* **Insertar**: utilice esta opción para insertar el fragmento de contenido seleccionado en el tema abierto para su edición en el Editor Web. A medida que los datos se insertan como un fragmento, también puede editarlos dentro del tema en el Editor Web.

  >[!NOTE]
  > 
  > La opción Insertar sólo aparece mientras está editando un tema.

* **Editar**: utilice esta opción para realizar cambios en el generador de fragmentos de contenido y guardarlo.
* **Eliminar**: utilice esta opción para eliminar el generador de fragmentos de contenido seleccionado.
* **Duplicar**: utilice esta opción para crear un duplicado o una copia del generador de fragmentos de contenido seleccionado. El duplicado se crea con un sufijo (como generator_1) de forma predeterminada.

### Insertar un fragmento de consulta

También puede utilizar la variable **Insertar fragmento de consulta** ![](images/data-source-icon.svg)   en la barra de herramientas principal para insertar el fragmento de datos en los temas.  Puede seleccionar un generador en la lista desplegable, editar la consulta o cambiar la plantilla e insertar los datos en el tema.

![](images/insert-content-snippet.png){width="800" align="left"}




