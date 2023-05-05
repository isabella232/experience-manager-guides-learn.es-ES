---
title: Trabajar con el Editor de mapas básico
description: Aprenda a trabajar con el Editor de mapas básico
exl-id: 85194806-db3f-442b-a551-540d148d26ec
source-git-commit: 8823669fd29e8a40a41f9ca5d654b38fbea8e2fa
workflow-type: tm+mt
source-wordcount: '1394'
ht-degree: 0%

---

# Trabajar con el Editor de mapas básico {#id1942CM005Y4}

El Editor de mapas básico proporciona una sencilla función de arrastrar y soltar para agregar temas desde el repositorio de AEM para crear el mapa o mapa de datos DITA. Puede agregar temas anidados, tablas de relación \(reltable\), atributos e información de metadatos, y también validar el mapa para que sea correcto.

>[!NOTE]
>
> Si el administrador ha habilitado la opción Editor de mapas avanzado , no tendrá acceso al Editor de mapas básico. Todos los archivos de asignación se abrirán en el Editor de mapas avanzado de forma predeterminada.

Las secciones siguientes describen las distintas funciones disponibles en el Editor de mapas básico.

## Añadir temas a un archivo de asignación {#id193CBL0505Z}

Una vez creado un archivo de mapa, debe añadir temas al archivo de mapa. Con el Editor de mapas básico, puede agregar temas, tablas de relación u otros archivos de asignación.

Realice los siguientes pasos para crear el archivo de asignación:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación que desea editar.

1. Para obtener un bloqueo exclusivo en el archivo de mapa, seleccione el archivo de mapa y haga clic en **Comprobar**.

   >[!NOTE]
   >
   > Una vez que tenga un bloqueo exclusivo en un archivo de mapa, otros usuarios no podrán editar el mapa. Sin embargo, podrían trabajar en los temas dentro del archivo de mapa.

1. Con el archivo de mapa seleccionado, haga clic en **Editar**.

   El archivo de mapa se abre para su edición en el Editor de mapas. Con el Editor de mapas, se crea un mapa utilizando los temas disponibles actualmente que se muestran en el carril Referencias .

   ![](images/dita-map-01.png){width="800" align="left"}

1. Al usar la variable **Referencias** , vaya a la carpeta que contiene los temas o submapas que desea agregar.

   >[!NOTE]
   >
   > Puede añadir temas o submapas desde cualquier carpeta del carril Referencias .

1. Para agregar el primer tema al mapa, arrástrelo y suéltelo en el Editor de mapas básico.

   >[!NOTE]
   >
   > Después de agregar el primer vínculo, el vínculo Agregar nueva referencia está disponible cuando pasa el ratón sobre un tema existente en el mapa.

1. Para agregar temas subsiguientes o un submapa, arrastre y suelte el tema o submapa en la ubicación requerida en el mapa.

   Si agrega un submapa a su mapa DITA, el submapa se muestra como un vínculo en el mapa DITA. Para ver todos los temas del submapa, haga clic en el vínculo del submapa. El contenido del submapa se muestra en una nueva pestaña.

   >[!NOTE]
   >
   > Si suelta un tema nuevo en un tema existente en el mapa, recibirá un mensaje acerca de reemplazar el tema. Haga clic en Sí si desea reemplazar el tema, haga clic en No si no desea reemplazarlo. Puede utilizar CTRL+Z y CTRL+Y para deshacer o rehacer cualquier cambio en el mapa.

1. Haga clic en **Guardar**.


## Funciones disponibles en la barra de herramientas del Editor de mapas básico

La barra de herramientas principal del Editor de mapas básico permite realizar las siguientes tareas:

![](images/ditamap-toolbar-actions.png){width="800" align="left"}

**A: Buscar**

Puede buscar e incluir los temas requeridos de DAM. Al hacer clic en este icono, aparece el cuadro de diálogo Buscar :

![](images/search-dita-map.png){width="800" align="left"}

Introduzca las palabras clave que desee buscar, estas palabras clave se encuentran en los valores de nombre de archivo, contenido e incluso atributos del tema. Una vez que los resultados de la búsqueda estén disponibles, seleccione los temas deseados y haga clic en el botón Comprobar para añadir los archivos seleccionados al final de la estructura del mapa. Puede filtrar los resultados de la búsqueda especificando los parámetros Modificar fecha .

**B: Grupo**

Haga clic en la casilla de verificación situada a la izquierda de los temas y haga clic en Agrupar en la barra de herramientas para agrupar los temas seleccionados. Para obtener más información sobre la agrupación de temas, consulte la [topicgroup](https://docs.oasis-open.org/dita/v1.0/langspec/topicgroup.html) documentación en la especificación del lenguaje DITA OASIS.

**C: Eliminar**

Haga clic en la casilla de verificación a la izquierda de un tema y haga clic en Eliminar en la barra de herramientas para eliminar los temas seleccionados del mapa.

**D: Mostrar números/Ocultar números**

Mostrar la numeración \(u ocultar\) para los temas del mapa.

**E: Validar**

Compruebe si el mapa es válido o tiene errores.

**F: Modo predeterminado/Modo XML**

En el **Modo predeterminado**, al hacer clic en un vínculo de tema, se muestra la vista previa del tema en una nueva ficha. Al hacer clic en el botón **Modo predeterminado** cambia su modo a **Modo XML**. En **Modo XML**, al hacer clic en cualquier lugar de una fila de tema, se muestra el XML subyacente de las referencias de tema dentro del tema. En la vista XML de origen, hay un **Sangría automática** que reorganiza el código XML en formato presentable y fácil de leer. Si edita un mapa manualmente, la vista de origen también realiza comprobaciones de validación. En caso de que el XML contenga errores, lo mismo se resalta en la variable **Modo XML** y no se le permite guardar el archivo de asignación DITA. Si desea ver el XML de toda la asignación, haga clic en cualquier lugar fuera del límite del tema.


**Nota:** En el modo predeterminado, puede utilizar los métodos abreviados del teclado para deshacer \(`Ctrl+z`\) o rehacer \(`Ctrl+y`\) la última acción.


![](images/dita-map-invalid-source.png){width="650" align="left"}

**G: Propiedades de mapa**

Visualice el cuadro de diálogo Propiedades del mapa, donde puede establecer los atributos y la información de metadatos para el mapa. Para agregar un atributo, haga clic en el botón **Agregar** en la esquina inferior izquierda del cuadro de diálogo para obtener la variable **Atributo** lista desplegable. En la lista, seleccione el atributo que desee añadir. Si el atributo seleccionado tiene valores predefinidos especificados en el DTD, esos valores se presentarán en una nueva lista desplegable. Puede seleccionar el valor que desee en la lista desplegable. Si no hay ningún valor predefinido, se le mostrará un cuadro de texto para introducir un valor para el atributo seleccionado.

![](images/map-properties.png){width="300" align="left"}

## Funciones disponibles a nivel de tema en el Editor de mapas básico

Cuando pasa el puntero del ratón sobre un tema o un archivo de subasignación en el Editor de mapas básico, puede realizar las siguientes tareas:

![](images/ditamap-actions.png){width="650" align="left"}

**A: Mover a la izquierda o a la derecha**

Haga clic en los iconos de flecha izquierda o derecha para mover el tema a la izquierda o a la derecha. Mover un tema de este modo lo convierte en un tema secundario \(anidar\) o del mismo nivel \(eliminar anidamiento\) con respecto al tema que se encuentra encima.

**B: Propiedades**

Haga clic en el icono Propiedades para abrir el cuadro de diálogo Propiedades del tema. Con este cuadro de diálogo, puede establecer los atributos del tema y la información de metadatos. Para obtener más información sobre los atributos y metadatos de tema estándar, consulte la [topicref](https://docs.oasis-open.org/dita/v1.2/os/spec/langref/topicref.html) documentación en la especificación del lenguaje DITA OASIS.


![](images/map-properties-metadata.png){width="350" align="left"}

**C: Agregar nueva referencia**

Haga clic en el icono Añadir nueva referencia para añadir una nueva referencia como elemento del mismo nivel del tema actual.

**D: Añadir nueva definición de clave**

Haga clic en el icono Clave para añadir una nueva definición de clave. Cualquier clave anulada o clave que ya se haya definido en el mapa aparece en rojo. Si hace clic en el icono Propiedades de una definición clave, aparece el cuadro de diálogo Propiedades de la clave.

## Trabajar con tablas de relación en el Editor de mapas básico {#id1944B0I0COB}

Los editores de mapas de AEM Guías vienen con una potente función que le permite crear y editar tablas de relación en su mapa DITA.

Siga estos pasos para trabajar con tablas de relación en el Editor de mapas básico:

1. En la interfaz de usuario de Assets, vaya al mapa DITA en el que desea crear la tabla de relaciones.

1. Haga clic en el mapa DITA para abrirlo en la consola de asignación DITA.

1. Seleccione el **Temas** para ver una lista de los temas disponibles en el mapa de DITA.

   >[!TIP]
   >
   > La pestaña Temas le da la opción de descargar el archivo de mapa con sus dependientes. Para obtener más información, consulte [Exportación de un archivo de mapa DITA](authoring-download-assets.md#id218UBA00IXA).

1. En la barra de herramientas principal, haga clic en **Editar**.

   El archivo de mapa se abre en el Editor de mapas básico.

1. Select **Reltable** en la barra de herramientas.

   ![](images/reltable.png){width="650" align="left"}

1. Arrastre y suelte los temas de la lista de temas al editor Reltable .

   >[!NOTE]
   >
   > Puede agregar temas desde cualquier carpeta en el carril Referencias.

   ![](images/create-reltable.png){width="550" align="left"}

1. Para agregar un encabezado a la tabla de relaciones, haga clic en **Agregar nuevo encabezado**.

1. Para agregar una columna a la tabla de relaciones, haga clic en **Agregar una columna**.

   ![](images/complete-reltable.png){width="550" align="left"}

1. Haga clic en **Guardar**.


También puede realizar las siguientes acciones desde el editor de tablas de relación:

**Eliminar filas o columnas**

Si desea eliminar una columna de la tabla, active la casilla en el encabezado de columna y haga clic en Eliminar. Si desea quitar una fila de la tabla, active la casilla de verificación de la primera columna de la fila correspondiente y haga clic en Eliminar.

**Eliminar un tema**

Si desea eliminar un tema de la tabla, haga clic en el icono de cruz situado junto al tema.

**Eliminar la tabla de relaciones**

Si desea eliminar la tabla de relación, haga clic en cualquier lugar fuera de la tabla de relación y luego en Eliminar.

**Tema principal:**[ Trabajar con el Editor de mapas](map-editor.md)
