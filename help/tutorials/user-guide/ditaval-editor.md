---
title: Uso del editor DITAVAL
description: Aprenda a utilizar el editor DITAVAL
source-git-commit: c6eceb8ea3ce41f12ea1f689dc8aeab2b4ba3d9c
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---


# Editor DITAVAL {#ditaval-editor}

Los archivos DITAVAL se utilizan para generar resultados condicionales. En un solo tema, puede agregar condiciones utilizando atributos de elemento para condicionalizar el contenido. A continuación, se crea un archivo DITAVAL en el que se especifican las condiciones que se deben recopilar para generar contenido y qué condición se debe excluir de la salida final.

AEM guías le permite crear y editar fácilmente archivos DITAVAL con el editor DITAVAL. El editor DITAVAL recupera los atributos \(o etiquetas\) definidos en su sistema y puede utilizarlos para crear o editar archivos DITAVAL. Para obtener más información sobre la creación y administración de etiquetas en AEM, consulte [Administración de etiquetas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/tags.html?lang=en) en AEM documentación.

## Crear archivo DITAVAL

Realice los siguientes pasos para crear un archivo DITAVAL:

1. En la interfaz de usuario de Assets, vaya a la ubicación en la que desea crear el archivo DITAVAL.

1. Haga clic en **Crear** \> **Tema DITA**.

1. En la página Modelo, seleccione la plantilla de archivo DITAVAL y haga clic en **Siguiente**.

1. En la página Propiedades , especifique la variable **Título** y **Nombre** para el archivo DITAVAL.

   >[!NOTE]
   >
   > El nombre se sugiere automáticamente en función del título del archivo. Si desea especificar manualmente el nombre del archivo, asegúrese de que el Nombre no contenga espacios, apóstrofo o llaves y termine con .ditaval.

1. Haga clic en **Crear**. Aparecerá el mensaje Tema creado.

   Puede elegir abrir el archivo DITAVAL para editarlo en el editor DITAVAL o guardar el archivo de tema en el repositorio AEM.


## Editar archivo DITAVAL

Realice los siguientes pasos para editar un archivo DITAVAL:

1. En la interfaz de usuario de Assets, vaya al archivo DITAVAL que desea editar.

1. Para obtener un bloqueo exclusivo sobre el archivo, seleccione el archivo y haga clic en **Comprobar**.

1. Seleccione el archivo y haga clic en **Editar** para abrir el archivo en AEM editor DITAVAL de guías.

   El editor DITAVAL permite realizar las siguientes tareas:

   A: Alternar panel izquierdo Alternar la vista del panel izquierdo. Si ha abierto el archivo DITAVAL a través del mapa DITA, el mapa y el repositorio se muestran en este panel. Para obtener más información sobre cómo abrir un archivo a través de un mapa DITA, consulte [Editar temas a través de un mapa DITA](map-editor-advanced-map-editor.md#id17ACJ0F0FHS).

   B: Guardar Guarda los cambios realizados en el archivo. Todos los cambios se guardan en la versión actual del archivo.

   C: Agregar propiedad Agregue una sola propiedad en el archivo DITAVAL.

   ![](images/ditaval-editor-props.png)

   La primera lista desplegable muestra los atributos DITA permitidos que puede utilizar en el archivo DITAVAL. Se admiten cinco atributos: `audience`, `platform`, `product`, `props`y `otherprops`.

   La segunda lista desplegable muestra los valores configurados para el atributo seleccionado. A continuación, la siguiente lista desplegable muestra las acciones que puede configurar en el atributo seleccionado. Los valores permitidos en la lista desplegable de acciones son: `include`, `exclude`, `passthrough`y `flag`. Para obtener más información sobre estos valores, consulte la definición de [prop](http://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/ditaval/ditaval-prop.html#ditaval-prop) elemento en la documentación de OASIS DITA

   D: Agregar todas las propiedades Si desea agregar todas las propiedades o atributos condicionales definidos en el sistema con un solo clic, utilice la función Agregar todas las propiedades .

   >[!NOTE]
   >
   > Si todas las propiedades condicionales definidas ya existen en el archivo DITAVAL, no puede añadir más propiedades. Aparece un mensaje de error en esta situación.

   ![](images/ditaval-all-props.png)

1. Una vez que haya terminado de editar el archivo DITAVAL, haga clic en **Guardar**.

   >[!NOTE]
   >
   > Si cierra el archivo sin guardar, se perderán los cambios. Si no desea confirmar los cambios en AEM repositorio, haga clic en **Cerrar** y, a continuación, haga clic en **Cerrar sin guardar** en el **Cambios no guardados** diálogo.


## Vistas del editor DITAVAL

El editor DITAVAL de AEM Guías admite la visualización de archivos DITAVAL en dos modos o vistas diferentes:

**Autor**: Esta es una vista típica de lo que ve es lo que obtiene \(WYSISYG\) del editor DITAVAL. Puede agregar o quitar propiedades mediante la interfaz de usuario sencilla, que presenta las propiedades, sus valores y acciones en la lista desplegable. En la vista Autor, tiene las opciones para insertar una propiedad individual e insertar todas las propiedades con un solo clic.

También puede encontrar la versión del archivo DITAVAL en el que está trabajando manteniendo el puntero sobre el nombre de archivo.

**Fuente**: La vista Código fuente muestra el XML subyacente que conforma el archivo DITAVAL. Además de realizar ediciones de texto normales en esta vista, un autor también puede agregar o editar propiedades mediante el catálogo inteligente.

Para invocar el Catálogo inteligente, coloque el cursor al final de cualquier definición de propiedad e introduzca &quot;&lt;&quot;. El editor mostrará una lista de todos los elementos XML válidos que puede insertar en esa ubicación.

![](images/ditaval-source-view.png)

