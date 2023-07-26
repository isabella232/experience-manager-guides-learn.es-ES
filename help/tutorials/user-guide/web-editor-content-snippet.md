---
title: Inserción de un fragmento de contenido desde la fuente de datos
description: Aprenda a insertar un fragmento de contenido desde la fuente de datos
source-git-commit: 0f1c9d545dfc6dc53742c6f8d89cd48d33de2681
workflow-type: tm+mt
source-wordcount: '1549'
ht-degree: 0%

---


# Uso de datos de la fuente de datos

A **fuente de datos** es un sistema en el que se almacenan y administran los datos de su organización. Estos son los sistemas de registro como JIRA, bases de datos SQL, PIM o PLM. AEM Guías de proporciona la función para conectarse con la fuente de datos y utilizar los datos de ellas.

## Panel Fuentes de datos

Seleccionar **Fuentes de datos** ![](images/data-source-icon.svg) en el panel izquierdo para ver las fuentes de datos conectadas. El panel Fuentes de datos se abre y muestra todas las fuentes de datos conectadas. Para obtener más información, consulte [Configuración de un conector de fuente de datos](../install-guide/conf-data-source-connector.md).

>[!NOTE]
>
> Verá las fuentes de datos para las que el administrador ha configurado el conector.


## Mostrar vista de lista o vista de mosaico

Puede alternar entre la vista de lista o la vista de mosaico para ver los distintos orígenes de datos en forma de lista o como mosaicos.

Seleccione una fuente de datos para ver los generadores de fragmentos de contenido y los generadores de temas disponibles para la fuente de datos seleccionada.

### Vista de lista   ![](images/data-sources-list-view-icon.svg)

![](images/data-sources-list-view.png){width="300" align="left"}


### Vista en mosaico   ![](images/data-sources-tile-view-icon.svg)

![](images/data-sources-tile-view.png){width="300" align="left"}

Los datos de las fuentes de datos se pueden utilizar de dos maneras:
- Insertar un fragmento de contenido
- Crear un tema


## Inserción de un fragmento de contenido desde la fuente de datos

AEM Guías de proporciona la función para conectarse con la fuente de datos. Puede recuperar los datos, insertarlos en los temas y editarlos. Puede crear fácilmente un fragmento de contenido mediante el generador de fragmentos de contenido y reutilizarlo dentro de sus temas.

Realice los siguientes pasos para crear un fragmento de contenido mediante el generador de fragmentos de contenido e insertarlo en el tema:

1. Seleccionar **Fuentes de datos** ![](images/data-source-icon.svg)   en el panel izquierdo para ver las fuentes de datos conectadas.

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
      - Si ha seleccionado la plantilla de tabla SQL, puede ver los datos SQL en formato de tabla.
      - Si ha seleccionado la plantilla de lista ordenada por jira, puede ver una lista ordenada para los problemas de Jira.

   1. La vista de origen muestra los datos en la vista de origen DITA.
      ![](images/add-content-snippet-generator.png){width="800" align="left"}
1. Para guardar los resultados de la consulta, escriba el nombre del generador y haga clic en **AÑADIR**.   Se agrega a la lista un nuevo generador de fragmentos de contenido.

   >[!NOTE]
   >
   > Debe seguir la convención de nomenclatura de archivos para el nombre del nuevo generador de contenido. No puede haber un espacio en el nombre del generador de fragmentos de contenido. Tampoco puede guardar un nuevo generador de contenido con el nombre de un generador de contenido existente. Se produce un error.

### Opciones de un generador de fragmentos de contenido

Haga clic con el botón derecho en un generador de fragmentos de contenido para abrir Opciones. Con las opciones, puede realizar las siguientes operaciones:

- **Previsualizar**: utilice esta opción para abrir un panel y ver una pequeña fracción de cómo se muestran los datos en la salida.
- **Insertar**: utilice esta opción para insertar el fragmento de contenido seleccionado en el tema abierto para su edición en el Editor Web. A medida que los datos se insertan como un fragmento, también puede editarlos dentro del tema en el Editor Web.

  >[!NOTE]
  > 
  > La opción Insertar sólo aparece mientras está editando un tema.

- **Editar**: utilice esta opción para realizar cambios en el generador de fragmentos de contenido y guardarlo.
- **Eliminar**: utilice esta opción para eliminar el generador de fragmentos de contenido seleccionado.
- **Duplicar**: utilice esta opción para crear un duplicado o una copia del generador de fragmentos de contenido seleccionado. El duplicado se crea con un sufijo (como generator_1) de forma predeterminada.

### Insertar un fragmento de consulta

También puede utilizar la variable **Insertar fragmento de consulta** ![](images/data-source-icon.svg)   en la barra de herramientas principal para insertar el fragmento de datos en los temas.  Puede seleccionar un generador en la lista desplegable, editar la consulta o cambiar la plantilla e insertar los datos en el tema.

![](images/insert-content-snippet.png){width="800" align="left"}


## Creación de un tema mediante el generador de temas

Un generador de temas le ayuda a crear temas que contienen datos de sus fuentes. Puede crear rápidamente un generador de temas y, a continuación, generar los temas mediante el generador. Cada tema puede contener datos en varios formatos, como tablas, listas y párrafos.   Por ejemplo, en un tema, puede agregar una tabla que incluya los detalles de todos los productos nuevos y una lista de todos los productos que se suspenderán para su venta.

El generador de temas puede crear los temas que contienen los datos y un mapa DITA para todos los temas. También puede `<conref>` estos temas aparecen en el contenido. Esto le permite mantener los datos sincronizados con la fuente de datos y actualizarlos fácilmente.



### Crear un tema

Realice los siguientes pasos para crear un tema con el generador de temas:

1. Seleccione una fuente de datos para ver los generadores de fragmentos de contenido y los generadores de temas disponibles para la fuente de datos seleccionada.

   ![](images/data-sources.png){width="300" align="left"}
1. Seleccionar **Añadir** ![](images/Add_icon.svg) y seleccione **Generador de temas** en el menú desplegable para agregar un nuevo generador de temas. El **Agregar generador de temas** se abre el panel.



1. Introduzca los valores en los campos bajo las siguientes tres pestañas del **Agregar generador de temas** panel:

   **Recuperar configuración**

   ![](images/topic-generator-fetch-configuration.png){width="300" align="left"}


   1. Introduzca la consulta en **Consulta de datos** cuadro de texto.
   1. Seleccione la plantilla que se asigna a la fuente de datos desde el **Plantilla de asignación de datos** desplegable.

   >[!NOTE]
   >
   > Si el administrador ha configurado plantillas personalizadas, también se mostrarán dichas plantillas en la lista desplegable (según las configuraciones de ruta de plantilla realizadas por el administrador). Por ejemplo, se puede crear una plantilla de tema que contenga una lista ordenada, tablas, párrafos u otros elementos DITA.

   1. Introduzca el **Nodo raíz**. Este es el nodo en el que desea acceder a los datos. A continuación, el generador de temas crea cada tema en el nivel definido en el nodo raíz. Por ejemplo, puede agregar &quot;problemas&quot; como nodo raíz en Jira. Por lo tanto, si una consulta devuelve 13 problemas, obtendrá 13 temas, un tema para cada problema.

   1. Clic **Buscar** para recuperar los datos del origen de datos y aplicar la plantilla a los datos resultantes de la consulta SQL. La vista previa muestra una pequeña fracción de cómo aparece el tema en el formato de la plantilla seleccionada. Por ejemplo, puede ver un solo problema de Jira con todos los campos resultantes de la consulta.
   1. Introduzca el nombre del generador del tema.

      >[!NOTE]
      > 
      > Debe seguir la convención de nomenclatura de archivos para el nombre del nuevo generador de temas. No puede haber un espacio en el nombre del generador de temas. Tampoco puede guardar un nuevo generador de temas con el nombre de un generador de temas existente. Se produce un error.

   **Configuración de salida**

   ![](images/topic-generator-output-configuration.png){width="300" align="left"}

   1. Introduzca el **Ruta de salida** Especifica dónde desea guardar los temas.
   1. En el **Convenciones de nomenclatura de temas**, puede introducir un valor o una variable con etiquetas de velocidad. Los nuevos temas seguirán la convención. Por ejemplo, puede introducir la variable `$key` para crear temas basados en claves Jira.
   1. Habilitar la opción **Generación de un mapa** si desea crear un mapa que contenga todos los temas generados.
   1. Introduzca el nombre del nuevo mapa DITA.

   >[!NOTE]
   >
   > El generador de temas genera el mapa DITA en la misma ruta de salida que los temas.

   **Metadatos**

   Seleccione las propiedades de metadatos de la lista desplegable para pasarlas a los temas. **Nombre** La lista desplegable enumera las propiedades personalizadas y predeterminadas.

   Por ejemplo, en la siguiente captura de pantalla, `dc:description`, `dc:language`, `dc:title`, y `docstate` son las propiedades predeterminadas para las que se pueden definir los valores. Puede crear una propiedad personalizada como autor y definir su valor.

   ![](images/topic-generator-metadata.png){width="300" align="left"}



1. Introduzca el nombre del generador y haga clic en **Guardar** para guardar los resultados de la consulta. Se agrega un nuevo generador de temas a la lista.

1. Clic **Guardar y generar** para guardar el generador de temas y generar nuevos temas a partir del generador de temas.



   ![](images/edit-topic-generator.png){width="650" align="left"}

   >[!NOTE]
   >
   > Si los temas ya existen, el generador actualiza los datos de los temas existentes.

### Opciones para un generador de temas

Haga clic con el botón derecho en un generador de temas para abrir **Opciones**. Con las opciones, puede realizar las siguientes operaciones:

- **Previsualizar**: utilice esta opción para abrir un panel y ver una pequeña fracción de cómo se muestran los datos en la salida.
- **Generar contenido**: Esta opción genera los temas para el generador de temas seleccionado. También puede utilizar esta opción para actualizar los temas existentes. Se conecta a la fuente de datos y obtiene los datos actualizados.

  >[!NOTE]
  >
  >Si el tema ya existe, puede sobrescribir los datos del tema o guardarlos como una nueva versión.

  ![](images/generate-topic-options.png)

- **Editar**: utilice esta opción para cambiar y guardar el generador de temas.
- **Eliminar**: utilice esta opción para eliminar el generador de temas seleccionado.
- **Duplicar**: Esta opción crea un duplicado o una copia del generador de temas seleccionado. El duplicado se crea con un sufijo (como `topic-sample_1`) de forma predeterminada.




