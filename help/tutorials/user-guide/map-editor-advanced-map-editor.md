---
title: Trabajar con el editor de mapas avanzado
description: Aprenda a trabajar con el editor de mapas avanzado
exl-id: 4f48d489-d13e-4285-8870-373f0324f5f6
source-git-commit: 3bca42f0954afc2362ab24f369e698113324dbc3
workflow-type: tm+mt
source-wordcount: '3675'
ht-degree: 0%

---

# Trabajar con el editor de mapas avanzado {#id1942D0S0IHS}

El Editor de mapas avanzado incorpora una interfaz de usuario intuitiva y es similar al Editor web. Cuando se abre un archivo de mapa en el Editor web, se obtiene la opción de editar el archivo de mapa mediante la interfaz del Editor de mapas avanzado. El Editor de mapas avanzado permite agregar referencias de temas, referencias clave, estructurar el contenido y mucho más.

Además de editar archivos de mapa directamente desde el Editor Web, también puede abrir archivos de tema en un mapa para editar el Editor Web. En este tema se describen las funciones del Editor de mapas avanzado y cómo se pueden abrir y editar archivos en un mapa DITA en el Editor web.

## Añadir temas a un archivo de asignación

Realice los siguientes pasos para crear el archivo de asignación con el Editor de mapas avanzado:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación que desea editar.

   >[!NOTE]
   >
   > Asegúrese de que no ha activado el modo de selección de recursos.

1. Para obtener un bloqueo exclusivo en el archivo de mapa, seleccione el archivo de mapa y haga clic en **Comprobar**.

   >[!NOTE]
   >
   > Una vez que tenga un bloqueo exclusivo en un archivo de mapa, otros usuarios no podrán editar el mapa. Sin embargo, podrían trabajar en los temas dentro del archivo de mapa. Si el administrador ha configurado el editor web para extraer archivos antes de editarlos, no podrá editar un archivo hasta que lo desproteja. Del mismo modo, si está configurado, se le pedirá que proteja cualquier archivo extraído antes de cerrarlo

1. Con el archivo de mapa seleccionado, haga clic en **Editar temas**.

   ![](images/edit-map-main-menu.png){width="800" align="left"}

   O bien, también puede seleccionar el **Editar temas** en el menú de acción del archivo de asignación:

   ![](images/edit-map-action-menu.png){width="800" align="left"}

   El archivo de asignación se abre para su edición en el Editor web.

1. Haga clic en el **Editar** icono.

   ![](images/edit-map-icon.png){width="550" align="left"}

   El mapa se abre en la interfaz del Editor de mapas avanzado. Si ha abierto un nuevo archivo de mapa, solo se mostrará el título del mapa en el editor.

   ![](images/new-map-file-in-editor.png){width="800" align="left"}

   - **A** - \(*Barra de herramientas principal*\): Esto es similar a la barra de herramientas principal del Editor web. Consulte [Barra de herramientas principal](web-editor-features.md#id2051EA0G05Z) en el Editor web para obtener más información.

   - **B** - \(*Barra de herramientas secundaria*\) Esta es la barra de herramientas secundaria que le permite trabajar con archivos de mapa. Para obtener más información sobre las funcionalidades disponibles en la barra de herramientas secundaria, consulte [Funciones disponibles en la barra de herramientas del Editor de mapas avanzado](#id205DEC0005Z).

   - **C** - \(*Mapa de vistas*\): Permite cambiar el Editor de mapas entre el diseño, el autor, el origen y la vista previa. La variable **Diseño** view le permite organizar los temas en un mapa DITA. Esto proporciona el árbol o la vista jerárquica del mapa. La variable **Autor** permite editar los temas en el Editor de mapas. Esto también proporciona la vista WYSIWYG del archivo de mapa. La variable **Fuente** permite trabajar con el XML subyacente del archivo de asignación. La vista previa le ofrece una vista consolidada de todos los temas y submapas dentro del archivo de asignación. La variable **Cerrar** cierra el archivo de asignación.

   - **D** - \(*Panel izquierdo*\): Permite acceder al panel izquierdo, que le permite acceder a Favoritos, Repositorio, Mapa, Esquema y otras funciones. Puede expandirla o contraerla haciendo clic en el icono Expandir barra lateral \(![](images/sidebar-expand-icon.svg)\). Para obtener más información sobre las funciones disponibles en el panel izquierdo, consulte [Panel izquierdo](web-editor-features.md#id2051EA0M0HS) en el Editor web.

   - **E** - \(*Área media*\): Asignación del área de edición de contenido.

   - **F** - \(*Panel derecho*\): Otorga acceso al panel Propiedades . Puede ver las propiedades del contenido y las propiedades del mapa del tema o mapa seleccionado. Para obtener más información sobre las funcionalidades disponibles en este panel, consulte [Panel derecho](web-editor-features.md#id2051EB003YK) en el Editor web.

1. En el panel izquierdo, cambie a **Vista del repositorio**.

1. En el repositorio de AEM, vaya a la carpeta que contiene los temas o submapas que desea agregar.

1. Seleccione el tema o el archivo de asignación en el **Vista del repositorio** y arrástrela y suéltela en el área de edición de contenido del mapa \(central\).

   El tema se añade en el mapa.

   ![](images/map-editor-add-topic.png){width="800" align="left"}

1. Para agregar temas subsiguientes o un submapa, arrastre y suelte el tema o submapa en la ubicación requerida en el mapa.

   Tenga en cuenta los siguientes puntos al crear el archivo de asignación:

   - El archivo se añade en una ubicación donde la barra horizontal aparece en el área de edición del mapa. En la siguiente captura de pantalla, la variable *Información general* se agregará entre *Descripción general* y *Sitio de lanzamiento y aterrizaje* temas.

      ![](images/horizontal-line-in-adv-map-editor.png){width="350" align="left"}

   - Para reemplazar un tema, coloque el tema en la parte superior, izquierda o derecha del tema que desea reemplazar. Una barra vertical a la izquierda o a la derecha de un tema indica que se reemplazará con el tema que se va a soltar en él.

      ![](images/vertical-bar-left-right.png){width="550" align="left"}

      Sin embargo, antes de reemplazar un tema, aparece un mensaje de confirmación. El tema se reemplaza solo después de que usted haya dado la confirmación.

      ![](images/replace-topic-confirm.png){width="300" align="left"}

   - Si agrega un submapa a su mapa DITA, el submapa se muestra como un vínculo en el mapa DITA. Para ver todos los temas del submapa, pulse Ctrl+clic en el vínculo del submapa. El contenido del submapa se muestra en una nueva pestaña. Del mismo modo, para abrir un tema desde el mapa de DITA, pulse Ctrl+clic en el vínculo del tema y se abrirá en la nueva pestaña.

   - Puede utilizar las teclas de método abreviado CTRL+Z y CTRL+Y o sus iconos respectivos en la barra de herramientas para deshacer o rehacer cualquier cambio en el mapa.

   - Para cambiar la posición de un tema, seleccione el tema \ (haciendo clic en el icono del tema\) y, a continuación, arrástrelo y suéltelo en la ubicación deseada en el archivo de asignación. Asegúrese de que la barra horizontal esté visible en el lugar donde desee colocar el tema. En la siguiente captura de pantalla, el tema *Sitio de lanzamiento y aterrizaje* se está moviendo después de *Información general* tema.

      ![](images/move-topic-adv-map-editor.png){width="350" align="left"}

   - Para comprobar las propiedades del archivo de asignación, haga clic con el botón derecho en cualquier lugar del área de edición del mapa y seleccione **Propiedades** en el menú contextual. En función de su versión AEM, puede ver propiedades como metadatos, programar la activación \(de\)referencias, estado del documento y más.

1. Haga clic en **Guardar**.


## Funciones disponibles en la barra de herramientas del Editor de mapas avanzado {#id205DEC0005Z}

La barra de herramientas del Editor de mapas avanzado es similar al tema Editor web. Las operaciones básicas como alternar el panel izquierdo, guardar el mapa, crear una nueva versión del mapa, deshacer o rehacer la última operación y eliminar los elementos seleccionados son comunes en ambos editores. Para obtener más información sobre cómo funcionan estas operaciones, consulte [Conozca las funciones del Editor web](web-editor-features.md#) para obtener más información.

Las siguientes operaciones específicas del mapa también están disponibles en la barra de herramientas de las vistas Diseño y Autor:

## Vista Diseño {#id205DEC0005Z_layout_view}

Cuando se abre un mapa para editarlo, se abre la vista Diseño del Editor de mapas. La vista Diseño muestra la jerarquía del mapa en una vista de árbol y le permite organizar los temas en un mapa.

>[!NOTE]
>
> La vista Diseño solo muestra las referencias presentes en un mapa. Si se rompen las referencias, se mostrará un pequeño símbolo cruzado a la izquierda de la referencia

Puede realizar las siguientes tareas en la vista Diseño:

**Insertar referencia de tema** - ![](images/insert-topic-reference.png)

Muestra el cuadro de diálogo de búsqueda de temas. Vaya al archivo de tema o asignación que desea insertar y haga clic en Seleccionar para agregarlo al mapa.
![](images/insert-topic-reference-dialog.png){width="800" align="left"}


**Insertar grupo de temas** - ![](images/insert-topic-group.png)

Inserte el `topicgroup` elemento. Para obtener más información sobre la agrupación de temas, consulte la [topicgroup](https://docs.oasis-open.org/dita/v1.0/langspec/topicgroup.html) documentación en la especificación del lenguaje DITA OASIS.

**Insertar definición de clave** - ![](images/Key_icon.svg)

Muestra el cuadro de diálogo Insertar clave. Utilice este cuadro de diálogo para definir cualquier definición de clave que desee utilizar en el mapa.

![](images/insert-key-definition-dialog.png){width="300" align="left"}

**Insertar antes o después** - ![](images/insert_element_before_icon.svg) / ![](images/insert_element_after_icon.svg)

Muestra el cuadro de diálogo Insertar elemento. Seleccione el elemento que desea insertar en el mapa. Dependiendo de la operación, el nuevo elemento se inserta antes o después del elemento actual en el mapa.

**Insertar materia frontal** - ![](images/frontmatter.svg)

Este icono se muestra al abrir un mapa de libros para editarlo. Puede insertar componentes al principio del libro como una Tabla de contenido, un Índice y una Lista de tablas.

**Insertar asunto posterior** - ![](images/backmatter.svg)

Este icono se muestra al abrir un mapa de libros para editarlo. Puede insertar componentes para un final del libro, como un Índice, un Glosario y una Lista de figuras.

**Mover el elemento seleccionado de izquierda a derecha** - ![](images/left-arrow-icon.png) / ![](images/right-arrow-icon.png)

Haga clic en la flecha izquierda para mover el tema hacia la izquierda en la jerarquía. Esto esencialmente promueve el tema respectivo un nivel superior en la jerarquía. Por ejemplo, si hace clic en la flecha izquierda mientras se selecciona un tema secundario, se convierte en el mismo tema del tema que está encima. Del mismo modo, si hace clic en la flecha derecha, el tema se inserta hacia la derecha, convirtiéndolo en el elemento secundario del tema que se encuentra encima.

**Subir/Bajar el elemento seleccionado![](images/arrowup.svg)** - / ![](images/arrowdown.svg)

Haga clic en los iconos de flecha arriba o abajo para subir o bajar el tema en la jerarquía.

>[!NOTE]
>
> También puede arrastrar y soltar las referencias para moverlas en un mapa.

**Bloquear/desbloquear** - ![](images/LockClosed_icon.svg) / ![](images/LockOpen_icon.svg)

Obtiene un bloqueo en el archivo de mapa y libera el bloqueo. Si tiene cambios no guardados en el archivo de mapa, se le pedirá que guarde el archivo de mapa en el momento de liberar el bloqueo. Los cambios se guardan en la versión actual del archivo de asignación.

**Combinar** - ![](images/merge-icon.svg)

Para obtener más información sobre la combinación de contenido de una versión diferente de un archivo, consulte [Combinar](web-editor-features.md#id205DF04E0HS) en el Editor web.

**Historial de versiones** - ![](images/version-history-web-editor-ico.svg)

Compruebe las versiones y etiquetas disponibles en el tema activo y vuelva a cualquier versión desde el propio editor.

**Etiqueta de versión** - ![](images/version-label-icon.svg)

Muestra el cuadro de diálogo de administración de etiquetas de versión. Seleccione una versión en la lista desplegable. Elija la etiqueta que desee aplicar a la versión seleccionada y haga clic en **Agregar etiqueta** para agregarlo.

**Opciones de vista** - ![](images/view-options.svg)

Muestra un menú desplegable que le da la opción de Mostrar números de línea, Mostrar casilla de verificación y Mostrar nombre de archivo.

- **Mostrar números de línea**

Muestra u oculta el número de línea de cada tema. Los números de línea se muestran en función del nivel de la jerarquía.

- **Mostrar casilla de verificación**

Muestra u oculta una casilla de verificación para cada tema. Puede utilizar la casilla de verificación para seleccionar los temas y realizar diversas tareas mediante el menú Opciones . Para obtener más información, consulte la [Opciones](#id228ID8006H8) para abrir el Navegador.

- **Mostrar nombre de archivo**

Muestra el nombre de archivo de los títulos de los temas.

>[!NOTE]
>
> Al pasar el puntero sobre el título de un tema, se mostrará la ruta del archivo.


**Ver temas basados en filtros condicionales** Si ha aplicado alguna condición a un tema, aparece un icono de filtro a la derecha del tema. Cuando pasa el puntero sobre un icono de filtro, se muestra la condición aplicada y su valor de atributo.

**Menú Opciones de la vista Presentación**

Además de organizar los temas en el archivo de asignación, también puede realizar las siguientes acciones utilizando el menú Opciones disponible para un elemento en la vista Diseño:

![](images/map-editor-options-menu.png){width="650" align="left"}

- **Agregar**: Puede elegir agregar un tema nuevo o una referencia vacía del Editor de mapas:
   - **Referencia vacía**: Esta opción le permite añadir una referencia vacía en el mapa DITA. Puede hacer doble clic en la referencia vacía insertada más adelante y añadir los detalles del tema. Para obtener más información, consulte la [Crear un tema](web-editor-features.md#id228ICI0105U) en el Editor web.
   - **Nuevo tema**: Cuando elige crear un tema nuevo desde el menú, aparece el cuadro de diálogo Crear nuevo tema . En el cuadro de diálogo Crear nuevo tema, proporcione los detalles necesarios y haga clic en Crear. Para obtener más información, consulte la [Crear un tema](web-editor-features.md#id228ICI0105U) en el Editor web.
- **Mover**: Puede elegir mover un tema hacia arriba/abajo/derecha/izquierda en la jerarquía. También puede arrastrar y soltar un tema o un mapa desde el panel del repositorio al mapa abierto en el Editor de mapas.
- **Deshacer**: Deshacer la última operación en la vista Presentación.
- **Rehacer**: Rehaga la última operación en la vista Diseño.
- **Copiar**: Copie la referencia seleccionada del archivo de asignación.

   >[!NOTE]
   >
   > Puede mostrar y, a continuación, seleccionar las casillas de verificación para copiar varias referencias.

- **Pegar**: Pegue las referencias copiadas en la ubicación actual de la jerarquía.
- **Eliminar**: Elimine las referencias seleccionadas del archivo de asignación.

   >[!NOTE]
   >
   > Puede mostrar y, a continuación, seleccionar las casillas de verificación para eliminar varias referencias.


## Panel derecho en el Editor de mapas

El panel derecho muestra las Propiedades de contenido y las Propiedades de mapa en la vista Diseño del Editor de mapas.

**Propiedades de contenido**

El panel Propiedades del contenido contiene información sobre el tipo de tema seleccionado actualmente en el mapa, su URL de vínculo y sus atributos. Para obtener más información, consulte [Propiedades de contenido](web-editor-features.md#id228IDB00HMM) en el Editor web.

- **Otros atributos** Si el administrador ha creado un perfil para los atributos, obtendrá esos atributos junto con sus valores configurados. Con el panel de propiedades de contenido, puede elegir esos atributos y asignarlos al contenido relevante de su tema. También puede asignar atributos configurados por su administrador en la sección **Atributos de visualización** en la configuración del editor. Los atributos definidos para un elemento se muestran en las vistas Presentación y Esquema. Esto le ayuda a ver rápidamente todos los temas de un mapa para los que se define un atributo en particular. Por ejemplo, todos los temas que tienen el atributo platform definido como &quot;Android&quot;.

   ![](images/layout-inline-attributes.png){width="650" align="left"}


   Para obtener más información, consulte la *Atributos de visualización* dentro de la variable *Configuración del editor* descripción de la función en el [Panel izquierdo](web-editor-features.md#id2051EA0M0HS) para obtener más información.

- **Metadatos** Con los metadatos , puede establecer la información de los metadatos. Puede definir el título de navegación, el texto del vínculo, la descripción corta y las palabras clave.

Para obtener más información sobre los atributos y metadatos de tema estándar, consulte la [topicref](https://docs.oasis-open.org/dita/v1.2/os/spec/langref/topicref.html) documentación en la especificación del lenguaje DITA OASIS.

**Propiedades de mapa**

Muestra el cuadro de diálogo Propiedades del mapa, donde puede definir los atributos y la información de metadatos para el mapa.

## Vista Autor {#id205DEC0005Z_author_view}

La variable **Autor** permite editar el mapa DITA en el Editor web. Esto muestra la vista WYSIWYG del Editor de mapas y algunos de los iconos mostrados en la vista Autor son los mismos que la vista Diseño. Para obtener más información, consulte [Vista Diseño](#id205DEC0005Z_layout_view). Además, puede ver los siguientes iconos y realizar las tareas relacionadas desde la vista Autor:

**Insertar antes o después** - ![](images/insert_element_before_icon.svg) / ![](images/insert_element_after_icon.svg)

Muestra el cuadro de diálogo Insertar elemento. Seleccione el elemento que desea insertar en el mapa. Dependiendo de la operación, el nuevo elemento se inserta antes o después del elemento actual en el mapa.

**Insertar elemento** - ![](images/Add_icon.svg)

Muestra el cuadro de diálogo Insertar elemento. Seleccione el elemento que desea insertar. Puede utilizar el teclado para desplazarse por la lista de elementos y pulsar Intro para insertar el elemento requerido. Como alternativa, puede hacer clic directamente en el elemento para insertarlo en el mapa.

**Insertar tabla de relación** - ![](images/relationship_table_icon.svg)

Inserta una tabla de relación en el mapa. Como el concepto de trabajar con la tabla de relaciones es el mismo que se explica en la sección Editor de mapas básico , consulte [Trabajar con tablas de relación en el Editor de mapas básico](map-editor-basic-map-editor.md#id1944B0I0COB) para obtener más información.

**Insertar contenido reutilizable** - ![](images/content-reuse-icon.png)

Muestra el cuadro de diálogo Reutilizar contenido . Utilice este cuadro de diálogo para insertar el contenido que desea reutilizar en el mapa.

**Actualizar atributo de título de navegación** - ![](images/navtitle-refresh-icon.svg)

Sincroniza el `title` elemento de un archivo al que se hace referencia en un mapa con el valor especificado en su `@navtitle` atributo. Puede añadir diferentes tipos de archivos de referencia en un mapa, por ejemplo, tema, referencia, tarea, asignaciones \(sub\), etc. La mayoría de estos archivos admiten el `@navtitle` atributo. Si un archivo contiene la variable `@navtitle` y luego la variable `@navtitle` para el mismo archivo en el mapa se actualiza. En caso de que `@navtitle` no está presente, por lo que la variable `@navtitle` se agrega a ese archivo de referencia y a su `title` también se actualiza para mostrar la variable `@navtitle`.

>[!NOTE]
>
> El administrador puede configurar la adición automática `@navtitle` a cada archivo de referencia que agregue a un mapa. Para obtener más información sobre la configuración de la adición automática `@navtitle` atributo, consulte *Incluir el atributo @navtitle de forma predeterminada* en Instalar y configurar las guías de Adobe Experience Manager as a Cloud Service.

Haga clic en el icono Actualizar atributo de título de navegación para sincronizar el `title` y `@navtitle` valores del atributo.

**Alternar vista de etiquetas** - ![](images/Label_icon.svg)

Muestra u oculta las etiquetas XML. Las etiquetas sirven como indicaciones visuales que indican el límite de un elemento. En este modo, si desea insertar una referencia de tema o asignación, arrastre y suelte el archivo deseado antes o después de la etiqueta . La barra horizontal no se muestra en el modo Vista de etiquetas.

**Habilitar/Deshabilitar el seguimiento de cambios** - ![](images/track-change-icon.svg)

Puede realizar un seguimiento de todas las actualizaciones realizadas en el archivo de asignación activando el modo Seguimiento de cambios . Después de habilitar el seguimiento de cambios, todas las inserciones y eliminaciones se capturan en el documento. Para obtener más información, consulte [Habilitar/Deshabilitar el seguimiento de cambios](web-editor-features.md#id205DF0203Y4) en el Editor web.

**Crear tarea de revisión** - ![](images/create-review-task-icon.svg)

Puede crear una tarea de revisión del tema actual o del archivo de asignación directamente desde el Editor web. Abra el archivo para el que desea crear la tarea de revisión y haga clic en Crear tarea de revisión para iniciar el proceso de creación de la revisión. Siga las instrucciones indicadas en la [Revisión de temas o mapas](review.md#) para obtener más información.

## Editar temas a través de un mapa DITA {#id17ACJ0F0FHS}

Editar un tema individual no le da al autor el contexto completo. Un autor no tendría información sobre dónde se coloca un tema en un mapa DITA. Sin esta información contextual, a los autores les resulta un poco difícil crear contenido.

AEM guías permite a los autores abrir un mapa DITA en el Editor web y ver la colocación de los temas dentro del mapa. Esto ayuda a los autores a saber exactamente dónde se coloca el tema en el mapa y a crear contenido más relevante. Además, si hay varios autores trabajando en un proyecto, pueden saber qué temas están disponibles en el mapa y reutilizar el contenido, cuando sea necesario.

Para editar temas a través de un mapa DITA, realice los siguientes pasos:

1. En la interfaz de usuario de Assets, vaya al mapa DITA que contiene los temas que desea editar.
1. Haga clic en el mapa DITA para abrirlo en la consola de asignación DITA.
1. Seleccione el **Temas** para ver una lista de los temas disponibles en el mapa de DITA.

   >[!TIP]
   >
   > La pestaña Temas le da la opción de descargar el archivo de mapa con sus dependientes. Para obtener más información, consulte [Exportación de un archivo de mapa DITA](authoring-download-assets.md#id218UBA00IXA).

1. En la barra de herramientas principal, haga clic en **Editar temas**.

   El mapa DITA se abre en el Editor web.

   >[!NOTE]
   >
   > También puede seleccionar el archivo de asignación DITA en la interfaz de usuario de Assets y hacer clic en **Editar temas** en la barra de herramientas principal para iniciar el Editor web.

   ![](images/web-editor-map-view_cs.png){width="350" align="left"}

1. \(*Opcional*\) También puede seleccionar un tema del mapa y extraer el archivo antes de editarlo. Para desproteger archivos\(s\), seleccione uno o varios archivos en el panel izquierdo y haga clic en **Cierre de compra**. También puede liberar el bloqueo de cualquier archivo seleccionando el archivo extraído y haciendo clic en el botón **Cancelar cierre de compra y desbloquear** en la vista Mapa.

   >[!IMPORTANT]
   >
   > Si el administrador ha configurado la variable **Deshabilitar edición sin cierre de compra** , debe desproteger el archivo antes de editarlo. Si no extrae el archivo, el documento se abrirá en el editor en modo de solo lectura.

   La siguiente captura de pantalla resalta los iconos de Cierre de compra y Bloqueo \(A\), Cancelar cierre de compra y Desbloquear \(B\), Guardar como nueva versión y Desbloquear \(C\), Editar \(D\), Vista previa \(E\), diferentes iconos que muestran diferentes tipos de archivo DITA \(F\) y archivos desprotegidos \(G\).

   ![](images/file-checkout-map-editor.png){width="550" align="left"}

1. Haga clic en el vínculo de cualquier tema para abrirlo en el Editor web para editarlo.

   Puede abrir varios temas en el editor y cada uno se abre en una nueva pestaña del editor. Incluso si el mapa DITA contiene submapas, los temas de los submapas también se abren en una nueva pestaña para su edición. Si desea ver los temas bajo un submapa, puede hacer clic en y expandir el submapa.

   ![](images/web-editor-multiple-topics.png){width="800" align="left"}

   Si hace clic en un archivo de mapa, el mapa se abre en una nueva pestaña del explorador web.

1. Una vez que haya terminado de editar los temas, puede hacer lo siguiente:

   - Puede guardarlos individualmente. Si hace clic en **Cerrar sin guardar** En los temas verá un cuadro de diálogo que le pedirá que guarde los temas no guardados:

      ![](images/save-multiple-topics.PNG){width="550" align="left"}

      Puede elegir guardar todos los temas seleccionados o anular la selección de los temas que no desee guardar.

   - Puede registrar el tema utilizando la variable **Guardar como nueva versión y desbloquear** botón. Al guardar una revisión del tema, se crea una nueva revisión y también se libera el bloqueo.
   - Si el administrador ha habilitado la opción de proteger archivos al cerrar, se le mostrará un mensaje para guardar archivos cada vez que se cierren los archivos extraídos. Con esta opción habilitada, cuando cierre el editor con archivos modificados, se mostrará la lista de archivos extraídos que deben guardarse. Los archivos extraídos se muestran con un icono de bloqueo:

      ![](images/save-on-close.PNG){width="550" align="left"}

      - Haga clic en **Cerrar sin guardar** cierra los archivos sin guardar ningún cambio.

      - Al hacer clic en **Guardar** guarda los cambios, pero no protege los archivos.

      - Al seleccionar la variable **Comprobación de archivos** y, a continuación, haga clic en la opción **Guardar** comprueba en los archivos \(crea otra versión\) y también guarda los archivos.


## Vista previa de un mapa

Además de poder ver la posición de cada fichero de tema dentro de un mapa, es deseable ver el contenido del mapa en un flujo consecutivo. La función Vista previa de mapa permite ver todo el contenido del archivo de mapa con un solo clic. No es necesario generar un resultado del archivo de mapa para ver cómo se verá el mapa completo una vez publicado. Simplemente puede acceder a la vista previa del mapa y todos los temas y submapas se representan en forma de libro.

Puede acceder a la vista previa de un mapa desde:

- **IU de recursos**: En la interfaz de usuario de Assets, vaya a la ubicación del mapa, seleccione el archivo de mapa y elija **Vista previa del mapa** en la barra de herramientas. La vista previa del mapa se muestra en una nueva ficha. Puede ver el contenido de todos los temas en el modo de vista previa. En esta vista, no puede editar ningún tema.

   >[!NOTE]
   >
   > Si la variable *Vista previa del mapa* no está visible en la barra de herramientas principal, puede que se haya movido debajo de la opción **Más** barra de herramientas.

- **Editor de mapas avanzado**: En el Editor de mapas avanzado, haga clic en el icono Vista previa para ver la vista previa del mapa actual.

   ![](images/map-preview-icon.png){width="350" align="left"}

   Puede realizar las siguientes tareas adicionales en el modo de vista previa:

   - Haga clic con el botón derecho en un tema y seleccione **Editar** para abrir el tema y editarlo en una nueva ficha.

      >[!NOTE]
      >
      > Si no tiene derechos de edición, el tema se abrirá en modo de solo lectura.

   - Vaya al tema deseado haciendo clic en el título del tema en el árbol de mapas \(en el panel izquierdo\).

   - El tema actual en la vista previa del mapa también se resalta en el árbol del mapa.


**Tema principal:**[ Trabajar con el Editor de mapas](map-editor.md)
