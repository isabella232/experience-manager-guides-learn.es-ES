---
title: Vista previa de un tema
description: Obtenga información sobre cómo previsualizar un tema
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '1815'
ht-degree: 0%

---


# Vista previa de un tema {#id1696II000QR}

Una vez creado un tema, AEM guías genera una vista previa del tema. El modo Vista previa proporciona varias funciones que puede utilizar para trabajar con el documento.

Realice los pasos siguientes para obtener una vista previa de un tema:

1. En la interfaz de usuario de Assets, vaya al tema que desee ver.
1. Haga clic en el tema que desee ver.

   Se muestra una vista previa del tema en la interfaz de usuario de Assets.

   >[!NOTE]
   >
   > Puede ver la versión del tema activo o del mapa DITA en la esquina superior derecha de la pestaña del archivo del tema.

   >[!IMPORTANT]
   >
   > La posición de las siguientes funciones en la barra de herramientas Vista previa podría diferir en función de la configuración del servidor de AEM. Algunas de las funciones podrían estar disponibles en la barra de herramientas principal, mientras que otras podrían estar disponibles en el menú Más .

## Funciones disponibles en el modo de vista previa

![](images/preview-screen.png){width="800" align="left"}

Puede realizar las siguientes operaciones desde la barra de herramientas en el modo de vista previa:

**Propiedades**

Ver las propiedades del tema seleccionado. En función de su versión AEM, puede ver propiedades como metadatos, programar la activación \(de\)referencias, estado del documento y más.

>[!NOTE]
>
> La propiedad title de un tema se rellena automáticamente desde la variable `title` etiqueta del tema o mapa de DITA. Si realiza algún cambio en el título utilizando la ventana de propiedades, el cambio se pierde. Si desea actualizar la propiedad title, debe hacerlo con el editor web.

La página Propiedades contiene información útil sobre las referencias, como dónde se está utilizando un mapa o tema, o qué referencias hay en un documento. La página Propiedades enumera dos tipos de referencias para un documento: **Se usa en** y **Referencias salientes**.

La variable **Se usa en** las referencias enumeran los documentos en los que se hace referencia o se utiliza el archivo actual. La variable **Referencias salientes** enumera los documentos a los que se hace referencia en el documento actual.

El icono \(+\) en la variable **Se usa en** la sección referencias le permite navegar hacia arriba para encontrar dónde se está utilizando o haciendo referencia a ese tema.

![](images/used-in-dialog_cs.png){width="800" align="left"}

Al hacer clic en ![](images/right-arrow-used-in-dialog.svg)junto a un documento muestra el mapa o los archivos de tema a los que se remite dicho documento.

**Filtro condicional \(A/B\)**

Si el tema tiene contenido condicional, verá el icono A/B en la barra de herramientas. Al hacer clic en este icono se abre una ventana emergente que le permite filtrar el contenido según las condiciones disponibles en el tema.

>[!NOTE]
>
> El contenido condicional se resalta con un color de fondo claro en el Editor web.

![](images/conditional-popup_cs.png){width="300" align="left"}

**Editar**

- Abra el tema para editarlo en el Editor web. La variable **Editar** no estará disponible si el administrador ha activado la opción **Deshabilitar edición sin cierre de compra** . Con la opción habilitada, verá la variable **Editar** solo después de extraer un archivo de tema.

**Resolución clave**

- Si desea utilizar un archivo de espacio de claves para el tema, haga clic en el icono Resolución de clave . A continuación, puede elegir un espacio clave en la ventana emergente Resolución de clave .

**Origen**

- Abra el código fuente XML de un archivo. Para ver el código XML subyacente de un archivo de asignación, tema o DITAVAL, abra el archivo en el modo Vista previa y haga clic en el icono Origen. La ventana emergente Código fuente XML muestra el código fuente XML. Puede seleccionar un código específico del archivo o pulsar `Ctrl`+`a` para seleccionar todo el contenido.

   >[!NOTE]
   >
   > Para obtener la vista de código fuente de un archivo de asignación DITA, seleccione el archivo en la interfaz de usuario de Assets y haga clic en Fuente.

   ![](images/xml-source-code-view-from-preview_cs.png){width="800" align="left"}

**Compartir vínculo UUID**

- AEM guías le permite compartir los vínculos basados en UUID para mapas, temas y archivos de imagen DITA desde los siguientes lugares:

   - IU de recursos
   - Consola del mapa DITA
   - Vista previa del tema o la imagen

Una nueva opción **Compartir vínculo UUID** se muestra en la barra de herramientas de las áreas mencionadas anteriormente. La siguiente captura de pantalla muestra la variable **Compartir vínculo UUID** en el modo Vista previa de un tema:

![](images/share-uuid-link_cs.png){width="800" align="left"}

En la interfaz de usuario de Asset, esta opción está visible al seleccionar un archivo. En el modo de Vista previa, esta opción está disponible en la barra de herramientas principal de forma predeterminada. En una consola de asignación DITA, esta opción está visible en la sección Ajustes preestablecidos de salida .

Una vez copiada la URL, la misma puede compartirse con otros usuarios para proporcionarles acceso directo al archivo. Este vínculo sigue siendo válido incluso cuando el archivo se mueve a otra ubicación del repositorio. La única vez que el vínculo falla es cuando el archivo se elimina del repositorio.

Si comparte el vínculo desde la consola de asignación DITA o el modo de vista previa de un archivo, el usuario accederá a la misma vista del archivo. Sin embargo, cuando comparte el vínculo de un archivo de mapa desde la interfaz de usuario de Assets, el usuario es conducido a la consola del mapa. Del mismo modo, para un tema o archivo de imagen, se muestra la vista previa del archivo.

>[!IMPORTANT]
>
> El vínculo no se puede usar como vínculo de referencia en otro tema, solo proporciona acceso directo al archivo en el repositorio. Además, el vínculo sigue siendo válido siempre y cuando el archivo esté disponible en el repositorio. Incluso si el archivo se mueve a otra ubicación del repositorio, el vínculo sigue siendo válido. El vínculo solo fallará cuando el archivo se elimine del repositorio.

**Proteger/Proteger**

- Activa o desactiva las funciones Desproteger y Proteger. Cuando se extrae un archivo, el usuario actual obtiene un permiso de escritura exclusivo en el archivo. Se puede abrir un archivo extraído en el Editor web para editarlo. Una vez que haya realizado los cambios necesarios, haga clic en el icono de protección para guardar el archivo en DAM.

Al retirar un tema, el estado del archivo se muestra como desprotegido en la vista de tarjeta y en la vista de lista.

Archivo extraído en la vista de tarjeta:

![](images/checkout-card-62.png){width="300" align="left"}

Archivo extraído en la vista de lista:

![](images/checkout-list-62.png){width="550" align="left"}

Si la columna Protegido no está visible, seleccione **Configuración de vista** under **Vista de lista** y seleccione **Protegido** en el **Configurar columnas** diálogo.

![](images/list-view-settings-check-out_cs.png){width="800" align="left"}

>[!TIP]
>
> Consulte la sección Versiones de contenido en la guía Prácticas recomendadas para conocer las prácticas recomendadas relacionadas con el trabajo con la extracción y el registro de archivos.

**Diferencia de versiones basada en web**

- Si el tema ha sufrido algunos cambios, puede encontrar fácilmente los cambios realizados en diferentes versiones de ese tema. Para averiguar los cambios en las distintas versiones de un tema:

   >[!IMPORTANT]
   >
   > El método descrito en el siguiente procedimiento solo es aplicable a archivos DITA. Para archivos que no sean DITA, utilice la vista Cronología para crear versiones o restaurar una versión existente de un archivo.

   1. Abra el tema en modo Vista previa.

   1. En el carril izquierdo, haga clic en **Historial de versiones** y seleccione una versión.

      ![](images/timeline-versions62_cs.png){width="800" align="left"}

   1. En las versiones de la lista, seleccione la que desee utilizar como versión base y haga clic en **Vista previa de la versión**. La vista previa de la versión seleccionada se muestra en la ventana Vista previa de la versión .

   1. En el **Mostrar diferencia** , seleccione la versión con la que desea comparar la versión base.

      ![](images/show-diff-list-cropped.png){width="800" align="left"}

      El contenido modificado se resalta en la vista previa del tema. El contenido resaltado en verde significa que el contenido recién añadido y el contenido en rojo es el contenido eliminado.

      ![](images/version-difference.png){width="800" align="left"}


### Rama, revertir y versiones posteriores {#id193PG0Y051X}

- En un entorno de creación típico, debe crear una nueva rama de un tema para atender a una versión específica. Al igual que cualquier otro sistema de administración de versiones, AEM guías le permite crear una rama a partir de una versión existente de un tema o revertir a una versión anterior de un tema. Mediante las funciones de administración de versiones que ofrecen las guías de AEM, puede realizar las siguientes tareas:

   - Crear una rama a partir de una versión existente de un tema
   - Crear versiones posteriores en una rama nueva
   - Revertir a una versión específica de un tema

   La siguiente ilustración muestra la ramificación típica y el sistema de versiones siguiente:

   ![](images/branching_illustration.png){width="550" align="center"}

   Para cualquier tema nuevo, la primera versión se numerará como 1.0. A partir de entonces, cada versión nueva del tema se guardará con un número incremental, como 1.1, 1.2, etc. Una vez creada una rama de un tema, se crea una rama nueva tomando el número de versión desde donde se crea la rama y añadiendo un 0 al final de la versión. Como se ve en la ilustración, se crea una nueva rama a partir de la versión 1.1 de un tema. La nueva rama tiene la versión 1.1.0. A partir de entonces, cada vez que guarda una nueva versión del tema en esta rama, obtiene un número de versión incremental, como 1.1.1, 1.1.2, etc.

   Al igual que la ramificación, también puede revertir su versión de trabajo o actual a cualquier versión que exista en el repositorio. Para volver a una versión, simplemente seleccione la versión deseada del tema y haga clic en **Revertir a esta versión** en el **Historial de versiones** panel.

   Siga estos pasos para crear una rama, volver a una versión y mantener las versiones posteriores de un tema:

   >[!IMPORTANT]
   >
   > El método descrito en el siguiente procedimiento solo es aplicable a archivos DITA. Para archivos que no sean DITA, utilice la vista Cronología para crear versiones o restaurar una versión existente de un archivo.

   1. Acceda al tema en la interfaz de usuario de Assets.

      >[!NOTE]
      >
      > También puede abrir el tema en modo de vista previa y continuar con el paso 3.

   1. Seleccione el tema para el que desea crear una rama.

   1. En el carril izquierdo, haga clic en **Historial de versiones**.

      >[!NOTE]
      >
      > Se muestra una lista de versiones disponibles para el tema seleccionado. Cada versión contiene la marca de tiempo, el nombre de usuario, el comentario de la versión y [label](web-editor-use-label.md#) información.

   1. Seleccione una versión desde la que desee crear una rama. En la siguiente captura de pantalla, se selecciona la versión 1.2 para crear una rama.

      ![](images/branching.png){width="300" align="left"}

      >[!NOTE]
      >
      > La versión actual de un tema contiene *\(Actual\)* mencionado junto al número de versión.

   1. Haga clic en **Revertir a esta versión**.

      Aparece un mensaje que le solicita que confirme la creación de una rama nueva.

   1. *\(Opcional\)* En el mensaje, se obtiene una opción para seleccionar la variable **Guardar La Copia De Trabajo Actual Como Una Nueva Versión**. Las dos acciones siguientes son posibles en función de la selección de esta opción:

      - Si selecciona esta opción, se creará una rama a partir de la versión 1.1. Y también se creará una nueva versión del tema a partir de la copia de trabajo actual del tema y se guardará como la siguiente versión - 1.4.

         ![](images/next_version_created_over_working_copy.png){width="300" align="left"}

         La versión 1.2 se convierte en su copia de trabajo actual del tema. Cualquier versión guardada después de esto se crea en la nueva rama de 1.1. Por ejemplo, la versión posterior de un nuevo tema en esta rama se guardará como 1.2.0.

         ![](images/new_version_in_branch.png){width="300" align="left"}

      - Si no selecciona esta opción, no se creará ninguna versión nueva de la copia de trabajo actual del tema. Se crea una nueva rama a partir de la versión 1.2 del tema. Cualquier versión posterior del tema se guarda en la rama 1.2 como 1.2.0, 1.2.1, etc.

         ![](images/new_version_without_working_copy.png){width="300" align="left"}
   1. Haga clic en **Aceptar**.
   Se crea una rama nueva a partir de la versión seleccionada del tema. El proceso anterior también es aplicable para revertir a una versión específica de un tema. Si cambia a una versión específica técnicamente, se creará una rama nueva a partir de la versión seleccionada y se convertirá en la copia de trabajo actual del tema. También puede ver el historial de archivos que se han revertido en el informe Historial de versiones revertidas. Para obtener más información sobre este informe, consulte [Informe de historial de versiones de archivos revertido](reports-reverted-file-version-history.md#).

**Tema principal:**[ Crear y previsualizar temas](create-preview-topics.md)

