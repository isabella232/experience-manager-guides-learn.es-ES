---
title: Conozca las funciones del Editor web
description: Obtenga información sobre las funciones del Editor web
exl-id: 38b378ff-da24-4560-a17f-a2c547aea1b8
source-git-commit: f7eea65f58927527dbd90138a653f75ee181d141
workflow-type: tm+mt
source-wordcount: '14387'
ht-degree: 0%

---

# Conozca las funciones del Editor web {#id176NC500V5Z}

Esta sección lo acompaña a través de las distintas funciones disponibles en el Editor web. Se puede dividir el Editor web en las siguientes secciones o áreas:

- [Barra de herramientas principal](#id2051EA0G05Z)
- [Barra de herramientas secundaria](#id2051EA0J0Y4)
- [Panel izquierdo](#id2051EA0M0HS)
- [Área de edición de contenido](#id2051EB000UI)
- [Panel derecho](#id2051EB003YK)

La siguiente subsección trata los detalles de las distintas secciones del Editor web.

## Barra de herramientas principal {#id2051EA0G05Z}

La barra de herramientas principal se encuentra en la parte superior de la interfaz del Editor web y proporciona funciones de nivel de archivo y varios modos de creación disponibles en el Editor web. Las funciones disponibles en la barra de herramientas superior se explican de la siguiente manera:

**Guardar todos** - ![](images/SaveFloppy_icon.svg)

Guarda los cambios realizados en todos los temas abiertos. Si tiene varios temas abiertos en el Editor web, haga clic en **Guardar todo** o utilizando **Crtl**+**S** las teclas de método abreviado guardan todos los documentos en un solo clic. No es necesario guardar individualmente cada documento.

>[!NOTE]
>
> La operación Guardar no crea una nueva versión de los temas. Para crear una nueva versión, seleccione Guardar como nueva versión.

**Guardar como nueva versión** - ![](images/save-revision-icon.png)

Guarda los cambios realizados en el tema y también crea una nueva versión del tema. Si está trabajando en un tema recién creado, la información de la versión se muestra como **ninguno**.

![](images/save-all-first-version-none_cs.png){width="800" align="left"}

El número de versión cambia con cada nueva versión que se cree para el tema o el archivo de asignación.

Cuando decide guardar un tema o una asignación mediante **Guardar como nueva versión**, aparece el cuadro de diálogo siguiente:

![](images/save-as-new-version-dialog.PNG){width="300" align="left"}

Introduzca comentarios y etiquetas de versión para identificar los cambios y haga clic en **Guardar** para crear una nueva versión del archivo.

Al elegir el *Guardar como nueva versión*, la primera versión del tema se crea en DAM, que también se convierte en la versión activa del tema. Posteriormente, si vuelve a una versión anterior del tema, se convierte en su versión activa actual.

Si el administrador tiene etiquetas de versión preconfiguradas, verá dichas etiquetas en una lista desplegable. Puede elegir una etiqueta de la lista de etiquetas disponibles y guardar el documento.

![](images/web-editor-pre-defined-labels.PNG){width="300" align="left"}

En el momento de guardar un tema, puede agregar un comentario que especifique los cambios realizados en el tema. Este comentario se muestra en el Historial de versiones del tema.

Si el tema se está revisando, los revisores recibirán una notificación que indicará que hay una versión más reciente del tema disponible. Pueden acceder fácilmente a la última revisión de su documento y seguir revisando la última versión de su tema.

Al pasar el puntero sobre el título de un tema, se mostrará la ruta del archivo y el número de versión.

![](images/mouse-hover-on-title_cs.png){width="800" align="left"}

>[!NOTE]
>
> Una vez que una versión de su tema esté disponible, también puede añadir etiquetas a su tema. Estas etiquetas se pueden utilizar para crear una línea de base para publicar una versión específica del documento. Para obtener más información sobre el uso de etiquetas en los temas, consulte [Usar etiquetas](web-editor-use-label.md#).

**Deshacer y rehacer** - ![](images/Undo_icon.svg) / ![](images/Redo_icon.svg)

Deshacer o rehacer la última acción.

**Eliminar elemento** - ![](images/Delete_icon.svg)

Elimina el elemento seleccionado actualmente o el elemento donde se coloca el cursor.

**Buscar y reemplazar** - ![](images/FindAndReplace_icon.svg)

La función Buscar y reemplazar está disponible en los modos de vista Autor y Origen. La barra de texto Buscar y reemplazar aparece en la parte inferior del área de edición del tema. Puede utilizar las teclas de método abreviado **CTRL**+**F** para invocar la barra Buscar y reemplazar.

![](images/find-replace-bar.png){width="800" align="left"}

Uso del icono de configuración \(![](images/settings-find-replace-icon.svg)\), puede alternar la variable **Ignorar mayúsculas y minúsculas** y **Palabra completa solamente** opciones de búsqueda. Para realizar una búsqueda que no distingue entre mayúsculas y minúsculas, active \(o seleccione\) la variable **Ignorar mayúsculas y minúsculas** . Si desea realizar la búsqueda que distingue entre mayúsculas y minúsculas, desactive \(o anule la selección\) de **Ignorar mayúsculas y minúsculas** . También puede elegir buscar una palabra entera.

La búsqueda es instantánea, lo que significa que a medida que escribe la frase o palabra de búsqueda en la variable **Buscar** , el término se busca inmediatamente y se selecciona en el tema. Del mismo modo, para reemplazar un texto en el tema, introduzca el término de búsqueda y su reemplazo en los campos respectivos y haga clic en el botón **Reemplazar** o **Reemplazar todo** botón.

En la vista de origen, Buscar y reemplazar es extremadamente útil para buscar un elemento o atributo específico. Por ejemplo, si desea reemplazar el valor de la variable `@product` , se puede realizar fácilmente desde la vista Origen. La vista Autor no permite realizar búsquedas en función de un atributo o elemento. Sin embargo, debe tener precaución al usar la variable **Reemplazar todo** , ya que podría sobrescribir el código XML.

**Configuración del editor** - ![](images/editor_settings_icon.svg)

La configuración del editor solo está disponible para usuarios administrativos. Con las preferencias, un administrador puede configurar las siguientes opciones:

>[!NOTE]
>
> Si está actualizando cualquier configuración predeterminada, debe volver a abrir los documentos para que los cambios entren en vigor.

- **General**: La configuración General permite configurar el diccionario para utilizarlo con el Editor web. Esta pestaña contiene tres secciones: **Revisión ortográfica**, **Condición** y **Creación**.

   ![](images/editor-setting-general.png){width="650" align="left"}

   - **Revisión ortográfica**: Hay dos opciones: **Revisión de ortografía AEM** y **Revisión ortográfica del explorador**. De forma predeterminada, el editor utiliza la función Revisión de ortografía del explorador , donde la revisión ortográfica se realiza mediante el diccionario integrado del explorador. Puede cambiar a AEM revisión ortográfica para utilizar AEM diccionario, que también se puede personalizar para agregar su lista de palabras personalizada. Para obtener más información sobre la personalización AEM diccionario, consulte *Personalizar AEM diccionario predeterminado* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.


   - **Condición**

      - **Resaltar texto condicional en la vista Autor**: Seleccione esta opción para resaltar el texto condicional en la vista de autor. El contenido condicional se resalta con el color definido para la condición.

      - **Validar con atributos de condición**: Seleccione esta opción para permitir la validación de los valores definidos para los atributos. Esto evita que agregue cualquier valor incorrecto.

      - **Mostrar la clave con el título en el panel Esquema de asunto**: Seleccione esta opción para mostrar las claves junto con los títulos en el esquema de temas. Si no selecciona esta opción, solo se muestran los títulos. Por ejemplo, aquí las claves &#39;os&#39;, &#39;audience&#39; y &#39;other&#39; también se muestran junto con los títulos.

         ![](images/subject-scheme-title.png){width="550" align="left"}

      - **Mostrar esquema de sujeto en el panel Condiciones**: Seleccione esta opción para ver un esquema de temas en el panel condiciones. Si anula la selección de esta opción, las condiciones definidas se muestran en el panel condiciones.
   - **Creación**

      - **Habilitar Reemplazar todo**: Seleccione esta opción para ver el icono Reemplazar todo en el panel Buscar y reemplazar .


**Paneles**: Esta configuración controla los paneles que se muestran en el panel izquierdo del editor. Puede alternar el conmutador para mostrar u ocultar el panel deseado.

![](images/editor-setting-panel.png){width="650" align="left"}

>[!NOTE]
>
> Si se ha configurado un panel personalizado, también aparece en la lista de paneles. Puede alternar el conmutador para mostrar u ocultar el panel personalizado. Para obtener más información sobre la configuración, consulte la *Configuración de un panel personalizado en el panel izquierdo* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.

- **Lista de elementos**: Como administrador, puede controlar la lista de elementos que un autor puede insertar mediante el [Insertar elemento](#id204SG30105Z) y también define el nombre para mostrar del elemento. La configuración Lista de elementos le permite especificar el nombre del elemento según las especificaciones DITA y una etiqueta que desee utilizar en lugar del nombre del elemento definido DITA:

   ![](images/editor-setting-element-list.png){width="650" align="left"}

En la captura de pantalla anterior, la variable `b` al elemento se le ha dado una etiqueta Negrita, `codeblock` recibe una etiqueta de Bloque de código junto con otros elementos. Si selecciona la opción **Usar solo los elementos anteriores** , solo los elementos válidos \(en el punto de inserción actual\) de esta lista se mostrarán en la ventana emergente Insertar elemento.

En la siguiente captura de pantalla, solo se muestran en el contexto actual 3 de los 4 elementos configurados de la captura de pantalla anterior:

![](images/editor-setting-insert-element-list.PNG){width="300" align="left"}

- **Lista de atributos**: Al igual que la Lista de elementos, puede controlar la lista de atributos y sus nombres para mostrar que se muestren en la lista de atributos de un elemento. En la siguiente captura de pantalla, solo se han configurado 3 atributos para que se muestren en la lista de atributos de un elemento:

![](images/editor-setting-attributes-list.png){width="650" align="left"}

Con esta configuración, cuando intente añadir un atributo a un elemento, solo verá la lista de atributos configurados en la lista.

![](images/editor-setting-add-attributes-list.png-to-element.PNG){width="300" align="left"}

- **Atributos de visualización**: Al igual que la Lista de atributos, se puede controlar la lista de atributos que se desea mostrar en la lista de atributos de un elemento. De forma predeterminada, cuatro **Atributos de visualización** — se ha configurado audiencia, plataforma, producto y props para que se muestren en la lista de atributos de un elemento. También puede agregar un atributo de visualización utilizando la variable **Agregar** en la parte superior. También puede eliminar cualquiera de los atributos de visualización utilizando la variable **Eliminar** icono.

Los atributos definidos para un elemento se muestran en las vistas Presentación y Esquema.

![](images/editor-settings-display-attributes.png){width="550" align="left"}

- **Traducción**: Esta pestaña contiene la opción para propagar las etiquetas de origen a la versión de destino.

   - **Propagación de las etiquetas de la versión de origen a la versión de destino**: Seleccione esta opción para pasar la etiqueta de la versión del archivo de origen al archivo traducido. De forma predeterminada, está desactivado.

   ![](images/editor-setting-translation.png){width="550" align="left"}


**Preferencias de usuario** - ![](images/user_preference_editor_icon.svg)

Las Preferencias de usuario están disponibles para todos los autores. Con las preferencias, un autor puede configurar las siguientes opciones:

![](images/user_preference_editor.PNG){width="550" align="left"}

- **Tema**: Puede elegir entre los temas Claro, Más claro, Oscuro u Más oscuro para el editor. En el caso del tema Más claro, las barras de herramientas y los paneles utilizan un fondo de color gris más claro. En el caso del tema Claro, las barras de herramientas y los paneles utilizan fondo de color gris claro. En el caso del tema más oscuro, las barras de herramientas y los paneles utilizan un fondo de color negro más oscuro. En el caso del tema Oscuro, las barras de herramientas y los paneles utilizan un fondo de color negro. En todos los temas, el área de edición de contenido se muestra en un fondo de color blanco.

- **Perfiles de carpeta**: El Perfil de carpeta controla varias configuraciones relacionadas con atributos condicionales, plantillas de creación, ajustes preestablecidos de salida y configuraciones del Editor web. El Perfil global se muestra de forma predeterminada. Además, si el administrador ha configurado perfiles de carpeta en el sistema, esos perfiles de carpeta también se muestran en la lista Perfiles de carpeta.

   Las configuraciones del Editor web que un administrador puede definir en el perfil de carpeta incluyen: personalización de la interfaz de usuario, incluidos los iconos de la barra de herramientas, el diseño del Editor web, los fragmentos y el mapa raíz. Para obtener más información, consulte *Configuración de perfiles globales o de nivel de carpeta* en el as a Cloud Service Instalar y configurar guías de Adobe Experience Manager .

   >[!NOTE]
   >
   > El nombre del perfil de carpeta actual se muestra como una etiqueta para el icono Preferencias de usuario en la barra de herramientas principal.

- **Ruta base**: De forma predeterminada, al acceder al repositorio de AEM desde el Editor web, se muestran los recursos desde la ubicación /content/dam. Es muy probable que su carpeta de trabajo sea unas pocas carpetas dentro de la carpeta /content/dam/ . Le llevaría unos clics llegar a la carpeta de trabajo cada vez. Puede establecer la ruta base en la carpeta de trabajo y la vista del repositorio le mostrará el contenido de esa ubicación por adelantado. Esto reduce el tiempo para acceder a la carpeta de trabajo. Además, cuando inserta cualquier referencia o archivo multimedia en el tema, la ubicación de exploración del archivo comienza con la carpeta establecida en la ruta base.

- **Seleccionar mapa raíz**: Seleccione un archivo de asignación DITA para resolver referencias clave o entradas de glosario. El mapa raíz seleccionado tiene la prioridad más alta para resolver las referencias clave. Para obtener más información, consulte [Resolución de referencias clave](map-editor-other-features.md#id176GD01H05Z).


>[!NOTE]
>
> Si no desea utilizar ningún mapa raíz, asegúrese de que la variable **Seleccionar mapa raíz** está en blanco.

**Modos de autor, origen y vista previa**

Para obtener más información sobre los distintos modos de creación y visualización de documentos, consulte [Vistas del Editor web](web-editor-views.md#).

## Barra de herramientas secundaria {#id2051EA0J0Y4}

La barra de herramientas secundaria aparece al abrir un tema para editarlo en el Editor web. Las funciones disponibles en la barra de herramientas secundaria se explican de la siguiente manera:

**Insertar elemento** - ![](images/Add_icon.svg)

Inserta un elemento válido en la ubicación actual o en la siguiente ubicación válida. Si está trabajando dentro de un elemento de bloque como un `note`y, a continuación, utilice el icono Insertar elemento para insertar un nuevo elemento después del `note` elemento. En la siguiente captura de pantalla se ha insertado un elemento de nota dentro del elemento p \(párrafo\):

![](images/note-in-para-insert-element_cs.png){width="800" align="left"}

Si pulsa Intro en el elemento de nota, se crea un nuevo párrafo dentro del propio elemento de nota. Para insertar un nuevo elemento fuera de la nota, haga clic en el elemento p \(resaltado en la captura de pantalla\) en la ruta de exploración de los elementos y haga clic en el icono Insertar elemento o presione ***Alt***+***Entrar*** para abrir la ventana emergente Insertar elemento. A continuación, seleccione el elemento deseado y pulse Intro para insertar el elemento seleccionado después del elemento de nota.

También puede añadir un elemento entre dos elementos cuando aparezca un cursor de bloque parpadeante.

![](images/Block-cursor.png){width="300" align="left"}

Por ejemplo, si está trabajando en un tema DITA y el cursor de bloque parpadea entre la descripción breve y el cuerpo, puede agregar `prolog` y luego agregar copyright, autor y otros detalles.

Otra forma de introducir un nuevo elemento es mediante el menú contextual. Haga clic con el botón derecho en cualquier lugar del documento para invocar el menú contextual. En este menú, elija Insertar elemento para mostrar el cuadro de diálogo Insertar elemento y elija el elemento que desea insertar.

![](images/insert-element-before-after.png){width="300" align="left"}

**Insertar párrafo** - ![](images/Paragraph_icon.svg)

Inserte un elemento de párrafo en la ubicación actual o siguiente válida.

**Insertar/Quitar lista numerada** - ![](images/TextNumbered_icon.svg)

Crea una lista numerada en la ubicación actual o en la siguiente ubicación válida. Si está en una lista numerada y hace clic en este icono, el elemento se convierte en un párrafo normal.

**Insertar/Quitar lista con viñetas** - ![](images/BulletList_icon.svg)

Crea una lista con viñetas en la ubicación actual o en la siguiente ubicación válida. Si está en una lista con viñetas y hace clic en este icono, el elemento se convierte en un párrafo normal.

**Insertar tabla** - ![](images/Table_icon.svg)

Inserta una tabla en la ubicación actual o en la siguiente ubicación válida. Haga clic en el icono Insertar tabla para abrir el cuadro de diálogo Insertar tabla :

![](images/table-properties.png){width="550" align="left"}

Puede especificar el número de filas y columnas necesarias en la tabla. Si desea mantener la primera fila como encabezado de tabla, seleccione la opción Establecer primera fila como encabezado. Para añadir un título a la tabla, introdúzcalo en el campo Title .

Una vez insertada una tabla, puede modificarla con el menú contextual.

![](images/table-context-menu_cs.png){width="550" align="left"}

Con el menú contextual de la tabla, puede:

- Insertar celdas, filas o columnas

- Combinar celdas en direcciones derecha y abajo

- Dividir celdas horizontal o verticalmente

- Eliminar celdas, filas o columnas

- Creación de un fragmento a partir de la tabla

- Generar ID


También puede definir atributos en varias celdas, filas completas o columnas de una tabla. Por ejemplo, para alinear la celda de la tabla, arrastre y seleccione la celda requerida. En el panel Propiedades de contenido \(a la derecha\), la propiedad **Tipo** cambia a **Entrada múltiple**. En la sección Otros atributos , seleccione la opción `@valign` de la lista desplegable de atributos. En la lista desplegable de valores, seleccione la alineación de texto que desee aplicar en las celdas de tabla seleccionadas.

![](images/align-table-cell_cs.png){width="800" align="left"}

**Insertar imagen** - ![](images/Image_icon.svg)

Inserta una imagen en la ubicación actual o en la siguiente ubicación válida. Haga clic en el icono Insertar imagen para abrir el cuadro de diálogo Insertar imagen y, a continuación, busque y seleccione la imagen que desee insertar.

>[!NOTE]
>
> También puede agregar una imagen arrastrándola y soltándola desde el sistema local en el artículo. En este caso, el archivo de imagen se agrega usando la variable **Cargar recursos** flujo de trabajo.  Para obtener más información, consulte la **Cargar recursos** flujo de trabajo en [Panel izquierdo](web-editor-features.md#id2051EA0M0HS) para obtener más información.


![](images/insert-image.png){width="650" align="left"}

Puede agregar Título de imagen/figura y Texto alternativo para la imagen en el cuadro de diálogo Insertar imagen.

Puede buscar el archivo de imagen requerido introduciendo el nombre del archivo en la barra Tipo para buscar en la parte superior y también filtrando los resultados de búsqueda por Ruta \(para buscar en\), Colecciones, Tipo de archivo y Etiquetas. Una vez encontrado el archivo de imagen requerido, seleccione el archivo y haga clic en Seleccionar para insertar la imagen en el documento. Puede insertar varios formatos de archivos de imagen, como `.png`, `.svg`, `.gif`, `.jpg`, `.eps`, `.ai`, `.psd`, y más.

Una vez que haya insertado una imagen, puede cambiar la altura, la anchura, la ubicación y los atributos desde el panel Propiedades del contenido. Haga clic en un archivo de imagen y, a continuación, realice cambios en el panel Propiedades de contenido en el carril derecho.

![](images/image-properties.png){width="800" align="left"}

El campo Source muestra el UUID del archivo de imagen insertado. Puede encontrar la ruta completa del archivo de imagen insertado pasando el puntero del ratón sobre el campo Origen. La ruta se muestra en la información del objeto.

Para cambiar el tamaño de una imagen, proporcione el valor Alto o Ancho para el archivo de imagen. La relación de aspecto de la imagen se mantiene automáticamente. Si lo desea, también puede optar por no mantener la relación de aspecto del archivo de imagen haciendo clic en el icono de bloqueo \(de Mantener relación de aspecto\) y proporcionando los valores de altura y anchura.

También puede especificar la configuración de colocación de la imagen como En línea o Desglosar. Si elige utilizar la opción de colocación de salto, puede elegir dónde alinear la imagen \(Izquierda, Centro o Derecha\).

También puede agregar otras propiedades para un archivo de imagen seleccionando las propiedades requeridas en la variable **Atributos** campo .

>[!NOTE]
>
>También puede definir áreas en las que se puede hacer clic \(mapa de imagen\) en la imagen. Para obtener más información, consulte la **Insertar/Editar mapa de imagen** descripción de la función en el [Panel izquierdo](web-editor-features.md#id2051EA0M0HS) para obtener más información.

**Menú contextual para archivos de imagen o medios**

También puede realizar algunas operaciones comunes para imágenes y archivos multimedia mediante el menú contextual. Haga clic con el botón derecho en cualquier lugar de la imagen para invocar el menú contextual.

El menú contextual proporciona opciones para cortar, copiar o pegar la imagen o el medio. Puede insertar un elemento antes o después del elemento seleccionado. También tiene la opción de cambiar el nombre de un elemento o desajustarlo. Puede localizar la imagen o los medios seleccionados en el repositorio o ver la previsualización del archivo en la interfaz de usuario de Assets.

Las otras opciones del menú contextual le permiten copiar la ruta, editar un mapa de imagen, crear un fragmento o generar ID para el elemento seleccionado.

**Insertar multimedia** - ![](images/insert-multimedia-icon.svg)

Inserta diferentes tipos de archivos multimedia. Haga clic en el icono Insertar multimedia y elija el tipo de archivo que desea insertar. Los formatos multimedia admitidos son:

- Archivo de audio
- Archivo de vídeo
- YouTube
- Vimeo

Al seleccionar la opción Archivo de audio o vídeo , se le muestra la vista del repositorio para examinar y seleccionar el archivo deseado. Si elige YouTube o Vimeo, aparece el cuadro de diálogo Insertar multimedia. Pegue el vínculo del archivo de vídeo en el campo Vínculo web y haga clic en Insertar para agregar el vídeo en la ubicación actual o siguiente válida del documento.

>[!NOTE]
>
> Al añadir un vínculo de vídeo de YouTube, debe reemplazar la cadena `watch?v=` con `embed` en la dirección URL. Por ejemplo, para añadir un vínculo de vídeo de YouTube: `https://www.youtube.com/**watch?v**=WlIKQOrmZcs`, debe agregarlo como: `https://www.youtube.com/**embed/**WlIKQOrmZcs`. Este cambio garantiza que el vídeo se incruste en la salida AEM Sitio y PDF.

También puede agregar el archivo de audio o vídeo desde el cuadro de diálogo Insertar multimedia. Seleccione la opción Archivo de audio/vídeo y haga clic en el icono Examinar para iniciar la vista del repositorio. Seleccione el archivo de audio o vídeo del repositorio y haga clic en Seleccionar para añadir el vínculo del archivo en el campo Archivo de audio/vídeo . Si elige un archivo de vídeo, también se mostrará una vista previa del archivo en el área de vista previa. Puede reproducir el archivo de vídeo para ver su previsualización.

![](images/insert-multimedia.png){width="650" align="left"}

**Insertar referencia cruzada** - ![](images/Reference_icon.svg)

Inserte referencias de tipo: Referencia de contenido, Referencia de clave de contenido, Referencia de clave, Referencia de archivo, Vínculo web o Vínculo de correo electrónico.

Haga clic en el **Seleccionar archivo** icono \(para referencia de contenido y referencia de archivo\) o **Seleccionar mapa** icono \(para Referencia de clave de contenido y Referencia de clave\) y seleccione el archivo o contenido que desee vincular.

![](images/insert-references.png){width="650" align="left"}

En el documento se añade un vínculo de la referencia seleccionada. El menú contextual del vínculo le ofrece las opciones para:

- **Insertar elemento**: Muestra una lista de elementos válidos que puede insertar en un contexto determinado.
- **Copiar UUID**: Copia el UUID de la referencia insertada.
- **Copiar ruta**: Copia la ruta completa de la referencia insertada.
- **Crear fragmento**: Crea un fragmento reutilizable a partir de la referencia insertada.
- **Generar ID**: Genera un ID único para la referencia insertada.

También puede buscar utilizando el UUID del archivo al que desea hacer referencia. En el caso de los vínculos de Contenido y Referencia clave, introduzca el UUID del archivo al que desea vincular y el archivo se busca y muestra automáticamente en la sección Vista previa . Al especificar el UUID del archivo, no es necesario mencionar explícitamente la extensión de archivo para los archivos .xml. La extensión .xml se adjunta automáticamente al UUID.

![](images/insert-content-using-uuid-search.png){width="650" align="left"}

Si el administrador ha activado la opción UUID en *XMLEditorConfig*, verá el UUID del contenido al que se hace referencia en la variable **Vínculo** propiedad.

![](images/ref-link-uuid_cs.png){width="800" align="left"}

>[!NOTE]
>
> Si la variable **Habilitar UUID** no está activada, se muestra la ruta relativa del contenido al que se hace referencia.

>[!IMPORTANT]
>
> Aunque la ruta relativa del contenido al que se hace referencia se muestra en la variable **Vínculo** , internamente el vínculo se crea utilizando el UUID del contenido al que se hace referencia.

>[!TIP]
>
> Consulte la sección Referencias en la guía de prácticas recomendadas para conocer las prácticas recomendadas relacionadas con el contenido.

**Filtrar búsqueda**

Puede buscar texto en los archivos presentes en la ruta seleccionada del repositorio de AEM. Por ejemplo, se busca &quot;general&quot; en la captura de pantalla que aparece a continuación. También puede limitar la búsqueda mediante filtros mejorados. Puede buscar todos los archivos DITA, como los temas DITA y los mapas DITA presentes en la ruta seleccionada.

Puede buscar archivos que no sean DITA, como archivos de imagen, multimedia y documentos en la ruta seleccionada. También puede buscar valores específicos en los atributos de los elementos DITA. También puede buscar archivos que el usuario especificado haya extraído.

![](images/reference-search-filters.png){width="650" align="left"}

>[!NOTE]
>
> El administrador del sistema también puede configurar los filtros de texto y mostrar u ocultar otros filtros. Para obtener más información, consulte Configuración de filtros de texto en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.

Se muestra la lista de archivos filtrados que contienen el texto buscado. Por ejemplo, en la captura de pantalla anterior, se muestran los archivos que contienen el texto &quot;general&quot;. También puede obtener una vista previa del contenido del archivo.

**Insertar contenido reutilizable** - ![](images/content-reuse-icon.svg)

Vuelva a utilizar el contenido que existe en cualquier otro documento del proyecto. Puede insertar contenido vinculando directamente al contenido en un archivo o utilizando una referencia clave; consulte [Resolución de referencias clave](map-editor-other-features.md#id176GD01H05Z). Al hacer clic en el icono Insertar contenido reutilizable , aparece el cuadro de diálogo Reutilizar contenido :

![](images/reuse-content-dialog.png){width="650" align="left"}

En el cuadro de diálogo Reutilizar contenido, seleccione archivo DITA para referencias de archivo o el archivo de asignación DITA que contiene las referencias clave. Una vez seleccionadas, el tema o las referencias clave se muestran en el cuadro de diálogo. Puede seleccionar la ID/clave del tema que desea insertar y hacer clic en Hecho para insertar el contenido dentro del tema.

Para insertar la Referencia de contenido, también puede introducir el UUID del archivo y el contenido reutilizable de ese archivo se muestra en la sección Vista previa .

Según la configuración para insertar vínculos, puede ver el UUID del contenido insertado o la ruta relativa en el panel Propiedades o en la vista Código fuente. El vínculo siempre se crea utilizando el UUID del contenido al que se hace referencia. Consulte Configuración de vínculos basados en UUID en el as a Cloud Service Instalar y configurar guías de Adobe Experience Manager .

>[!NOTE]
>
> Para añadir contenido antes o después del contenido referido, utilice *Alt*+*Left* Flecha o Alt+*Right* Teclas de flecha para mover el cursor a la ubicación deseada.

También puede incrustar el contenido de referencia dentro del tema haciendo clic con el botón derecho en el contenido de referencia y eligiendo **Reemplazar referencia por contenido** en el menú contextual.

**Insertar caracteres especiales** -  ![](images/insert-special-chars-icon.svg)

Inserta caracteres especiales en el tema. Haga clic en el icono Insertar carácter especial para abrir el cuadro de diálogo Insertar carácter especial .

>[!NOTE]
>
> AEM guías proporciona cuadros de diálogo que se pueden mover y cambiar de tamaño. Se puede cambiar el tamaño de los cuadros de diálogo que tienen dos líneas cruzadas en la esquina inferior derecha. A continuación se muestran las líneas cruzadas del cuadro de diálogo Carácter especial.

![](images/insert-special-char.png){width="550" align="left"}

En el cuadro de diálogo Insertar carácter especial, puede buscar un carácter especial con su nombre. Todos los caracteres especiales se almacenan en varias categorías. Utilice la lista desplegable Seleccionar categoría y seleccione una categoría. Se muestran los caracteres especiales disponibles en la categoría seleccionada. Puede navegar por la lista de caracteres especiales utilizando las teclas de flecha o hacer clic en el carácter que desee insertar. El Nombre y el Código hexadecimal del carácter especial seleccionado se muestran debajo de la lista. Haga clic en Insertar para insertar el carácter seleccionado en el documento.

**Insertar palabra clave** - ![](images/Keyword_icon.svg)

Inserte la palabra clave definida en el mapa DITA. Haga clic en el icono Insertar palabra clave para abrir el cuadro de diálogo Referencia de clave .

![](images/insert-keyword.png){width="550" align="left"}

Las palabras clave se enumeran en orden alfabético y también puede buscar palabras clave\(s\) escribiendo una cadena de búsqueda en el cuadro Buscar. El resultado de la búsqueda devolverá las palabras clave que contienen la cadena en ID o valor. Las palabras clave definidas en el mapa DITA se enumeran en este cuadro de diálogo. Elija la palabra clave que desee insertar y haga clic en **Insertar**.

También puede cambiar los atributos de la palabra clave insertada haciendo clic con el botón derecho en la palabra clave y seleccionando la opción Atributos . Se abre el cuadro de diálogo Atributos para palabra clave :

![](images/attributes-for-keyword.png){width="550" align="left"}

Puede cambiar los atributos de la palabra clave o agregar un nuevo atributo a la palabra clave.

**Insertar fragmento** - ![](images/insert-snippet-icon.svg)

Inserte un fragmento en la ubicación actual o en la siguiente ubicación válida. Para que esta función funcione, debe tener fragmentos definidos en el sistema. Para obtener más información sobre cómo añadir un fragmento, consulte la **Fragmento** descripción de la función en el [Panel izquierdo](web-editor-features.md#id2051EA0M0HS) para obtener más información.

Al hacer clic en el icono Insertar fragmento, se muestra el catálogo Insertar fragmento. El catálogo distingue entre contextos, lo que indica que solo mostrará los fragmentos si se permiten en la ubicación actual.

El siguiente ejemplo muestra dos fragmentos preconfigurados: Warning y Error que se pueden insertar en la ubicación actual del documento.

![](images/insert-snippet.png){width="300" align="left"}

Al elegir un fragmento de la lista, éste se inserta en la ubicación actual o siguiente válida del documento. La siguiente captura de pantalla muestra el fragmento de error insertado en el documento:

![](images/error-snippet.png){width="400" align="left"}

**Insertar/Editar mapa de imagen** - ![](images/imagemap-rectangle.svg)

Inserta un mapa de imagen en la imagen seleccionada. Una imagen con áreas en las que se puede hacer clic y que se vincula a temas o páginas web se denomina mapa de imagen.

Seleccione una imagen en el tema actual y haga clic en el icono Insertar/Editar mapa de imagen para abrir el cuadro de diálogo Insertar mapa de imagen .

![](images/insert-image-map.png){width="650" align="left"}

Elija la forma preferida Rectángulo ![](images/imagemap-rectangle-toolbar.png), Círculo ![](images/imagemap-circle-toolbar.png)o Polígono ![](images/imagemap-polygon-toolbr.png) para definir un área sobre una imagen que desea utilizar como vínculo. Después de definir un área, aparece el cuadro de diálogo Referencia donde debe especificar el vínculo al contenido interno o externo:

![](images/reference-dialog.png){width="650" align="left"}

Si las áreas se superponen, puede traer la forma hacia adelante o enviarla hacia atrás haciendo clic en el icono correspondiente de la barra de herramientas. También puede eliminar un área seleccionándola y haciendo clic en el icono Eliminar . Al hacer doble clic en un área, se abre el cuadro de diálogo Referencia, donde puede cambiar el vínculo de destino. Una vez que haya marcado las áreas requeridas en la imagen, guarde los cambios haciendo clic en Listo.

**Bloquear/desbloquear** - ![](images/LockClosed_icon.svg)/ ![](images/LockOpen_icon.svg)

Bloquea o desbloquea el archivo actual. Bloquear \(o extraer\) un archivo proporciona al usuario acceso de escritura exclusivo en el archivo. Cuando el archivo está desbloqueado \(o marcado\), los cambios se guardan en la versión actual del archivo.

Si está en la vista Mapa y expande el mapa principal, puede bloquear todos los archivos del mapa con un solo clic. Simplemente expanda el archivo de mapa principal y seleccione el archivo principal, lo que resulta en seleccionar todos los archivos dentro del mapa. A continuación, puede hacer clic en el icono Bloquear para obtener el bloqueo de todos los archivos del mapa.

**Alternar vista de etiquetas** - ![](images/Label_icon.svg)

Las etiquetas son indicaciones visuales que indican los límites de un elemento. Un límite de elemento marca el principio y el final de un elemento. A continuación, puede utilizar estos límites como señal visual para colocar el punto de inserción o seleccionar el texto dentro de un límite. Si desea insertar otro elemento antes o después de un elemento en el documento, puede colocar el punto de inserción antes o después del límite de apertura o cierre del elemento.

La siguiente captura de pantalla muestra un documento con la vista de etiquetas activada:

![](images/tags-view.png){width="650" align="left"}

Las siguientes operaciones se pueden realizar en un documento con la vista de etiquetas activada:

- **Seleccionar un elemento**: Haga clic en la etiqueta de apertura o cierre de un elemento para seleccionar su contenido.

- **Expandir o contraer etiquetas**: Haga clic en el signo + o - en una etiqueta para expandirla o contraerla.

- **Uso del menú contextual**: El menú contextual proporciona opciones para cortar, copiar o pegar el elemento seleccionado. También puede insertar un elemento antes o después del elemento seleccionado. Las otras opciones permiten generar ID o abrir el panel Propiedades para el elemento seleccionado.

- **Arrastrar y soltar elementos**: Seleccione la etiqueta de un elemento y arrástrela y suéltela fácilmente en el documento. Si la ubicación de colocación es una ubicación válida donde el elemento está permitido, el elemento se coloca en la ubicación de colocación.


>[!NOTE]
>
> Si un usuario habilita la Vista de etiquetas desde el Editor web, permanecerá habilitada incluso en las sesiones. Esto significa que no tiene que volver a habilitar la vista de etiquetas para acceder a ella más adelante. El valor predeterminado de la vista de etiquetas para la sesión de un nuevo usuario viene determinado por la propiedad tagsView del archivo ui\_config.json. Para obtener más información, consulte la *Configuración del valor predeterminado para la vista de etiquetas* en Instalar y configurar las guías de Adobe Experience Manager as a Cloud Service.

**Habilitar/Deshabilitar el seguimiento de cambios** ![](images/track-change-icon.svg)

Puede realizar un seguimiento de todas las actualizaciones realizadas en un documento activando el modo Seguimiento de cambios . Después de habilitar el seguimiento de cambios, todas las inserciones y eliminaciones se capturan en el documento. Todo el contenido eliminado se resalta mediante tachado y todas las inserciones se resaltan en el texto en color verde. Además, también se obtienen las barras de cambio en el borde de la página de temas. De nuevo, se muestra una barra roja para el contenido eliminado y una barra verde para el contenido añadido. En caso de que haya adición y eliminación en la misma línea, se mostrarán barras verdes y rojas.

La siguiente captura de pantalla resalta el contenido eliminado e insertado junto con las barras de cambios:

![](images/track-changes-content.png){width="650" align="left"}

Un caso de uso típico para realizar el seguimiento de cambios en un documento puede ser la revisión entre pares. Puede habilitar el seguimiento de cambios y compartir el documento para su revisión. A continuación, el revisor realizará cambios con el seguimiento de cambios activado. Cuando reciba el documento, deberá disponer de un mecanismo para ver las actualizaciones sugeridas, así como una forma conveniente de aceptar o rechazar los cambios.

AEM guías proporciona la función Cambios rastreados que contiene información sobre las actualizaciones realizadas en el documento. La función Cambios rastreados proporciona información sobre qué actualizaciones se realizaron, quién las realizó y a qué hora. Con la función Cambios rastreados también puede aceptar o rechazar fácilmente las actualizaciones sugeridas en el documento.

Para acceder a la función, haga clic en el icono Cambios rastreados en el panel derecho.

![](images/changes-panel_cs.png){width="300" align="left"}

Al hacer clic en un cambio, se selecciona el contenido modificado en el documento. Puede aceptar un cambio seleccionando el icono Aceptar cambio o rechazarlo seleccionando el botón Rechazar cambio.

Si desea aceptar o rechazar todos los cambios con un solo clic, seleccione **Aceptar todo** o **Rechazar todo**.

>[!NOTE]
>
> El modo Vista previa permite ver el documento con o sin las marcas del contenido modificado. Para obtener más información, consulte la [Vista previa](web-editor-views.md#preview-mode-id19AAGL00163) en el menú contextual.

**Combinar** - ![](images/merge-icon.svg)

Cuando trabaja en un entorno de varios autores, resulta difícil rastrear qué cambios han realizado los otros autores en un tema o mapa. La función Combinar permite controlar mejor no solo la visualización de los cambios, sino también los cambios que se conservan en la última versión del documento.

**Combinar archivos de tema**

Para combinar los cambios en un tema, realice los pasos siguientes:

1. Abra un tema en el Editor web.

1. Haga clic en **Combinar**.

   Aparecerá el cuadro de diálogo Combinar.

   ![](images/merge-changes-in-topic.png){width="550" align="left"}

1. *\(Opcional\)* También puede examinar y seleccionar un nuevo archivo desde otra ubicación de su repositorio.

1. Seleccione una versión del archivo con la que desea comparar la versión actual del archivo.

1. En Opciones, elija:

   - **Seguimiento de cambios desde la versión seleccionada**: Esta opción muestra todas las actualizaciones de contenido en forma de seguimiento de cambios. A continuación, puede optar por aceptar o rechazar cambios en el documento de uno en uno o de todos en uno.

   - **Revertir a la versión seleccionada**: Esta opción revierte la versión actual del documento a la versión seleccionada. Esta opción no le da ningún control sobre qué contenido se acepta o rechaza.

1. Haga clic en **Listo**.

1. Si seleccionó la variable **Seguimiento cambiado desde la versión seleccionada** , todos los cambios de la versión seleccionada se mostrarán en la función Cambios rastreados del panel derecho.

   Puede optar por aceptar o rechazar todos los comentarios del panel Cambios rastreados o aceptar o rechazar comentarios individuales.


**Combinar archivos de mapa**

Para combinar los cambios en un archivo de asignación, realice los siguientes pasos:

1. Abra un mapa en el Editor web.

1. Haga clic en **Combinar**.

   Aparecerá el cuadro de diálogo Combinar.

   ![](images/merge-changes-in-map.png){width="550" align="left"}

1. *\(Opcional\)* También puede examinar y seleccionar un nuevo archivo desde otra ubicación de su repositorio.

1. Seleccione una versión del archivo con la que desea comparar la versión actual del archivo.

1. En Opciones, elija:

   - **Seguimiento de cambios desde la versión seleccionada**: Esta opción muestra todas las actualizaciones de contenido en forma de seguimiento de cambios. A continuación, puede optar por aceptar o rechazar cambios en el documento de uno en uno o de todos en uno.

   - **Revertir a la versión seleccionada**: Esta opción revierte la versión actual del documento a la versión seleccionada. Esta opción no le da ningún control sobre qué contenido se acepta o rechaza.

1. Haga clic en **Listo**.

   1. Si seleccionó la variable **Seguimiento cambiado desde la versión seleccionada** , todos los cambios de la versión seleccionada se mostrarán en el panel de cambios rastreados \(a la derecha\).

      Puede optar por aceptar o rechazar todos los cambios del panel Cambios rastreados o aceptar o rechazar cambios individuales en el archivo de asignación.


**Historial de versiones** - ![](images/version-history-web-editor-ico.svg)

AEM guías proporciona varias formas de ver las versiones creadas para los archivos de temas y también maneras de revertir a una versión específica. Sin embargo, la mayoría de estas funciones están disponibles fuera del Editor web.

La función Historial de versiones del Editor web permite no solo comprobar las versiones y etiquetas disponibles en el tema activo, sino que también le ofrece la flexibilidad de volver a cualquier versión desde el editor en sí.

Para acceder al historial de versiones y volver a una versión específica del tema, realice los pasos siguientes:

1. Abra un tema en el Editor web.

1. Haga clic en **Historial de versiones**.

   Aparecerá el cuadro de diálogo Historial de versiones.

   ![](images/version-history-dialog-web-editor.png){width="550" align="left"}

1. Elija una versión del tema al que desee volver en la **Seleccionar versión** lista desplegable.

   >[!NOTE]
   >
   > Si una versión tiene etiquetas aplicadas, también se muestran \(entre corchetes\) junto con el número de versión.

   Una vez que elija una versión en la lista desplegable, aparecerá disponible la opción Revertir a la versión seleccionada . La ventana de vista previa muestra las diferencias entre la versión actual y la versión seleccionada del tema.

   ![](images/version-history-revert-diff-dialog-web-editor.png){width="550" align="left"}

1. Haga clic en **Revertir a la versión seleccionada** para revertir la copia de trabajo con la versión seleccionada del tema.

   Aparecerá el cuadro de diálogo Revertir versión .

   ![](images/version-history-revert-dialog-save-working-copy.png){width="550" align="left"}

1. \(*Opcional*\) Proporcione un motivo para volver a una versión anterior. También puede crear una nueva versión de la copia de trabajo activa del tema.

1. Haga clic en **Confirme.**

   La copia de trabajo del archivo se revierte a la versión seleccionada. Si elige crear una nueva versión de la copia de trabajo activa, también se creará una nueva versión del archivo con todos los cambios de trabajo.


Al volver a una versión anterior, se muestra una señal visual que indica que la versión en la que está trabajando no es la versión más reciente.

![](images/older-version-visual-cue.png){width="800" align="left"}

**Administración de etiquetas de versión** -  ![](images/version-label-icon.svg)

Las etiquetas le ayudan a identificar la fase en la que un tema en particular se encuentra en el DLC \(Ciclo de vida de desarrollo de documentos\). Por ejemplo, cuando está trabajando en un tema, puede establecer la etiqueta como &quot;Aprobado&quot;. Una vez que se publica un tema y se pone a disposición de los clientes, se puede asignar la etiqueta &quot;Publicado&quot; a ese tema.

AEM guías le permite especificar etiquetas en un formato de texto de forma libre o utilizar un conjunto de etiquetas predefinidas. La etiqueta personalizada permitiría a cualquier autor del sistema especificar una etiqueta según su elección. Esto proporciona flexibilidad; sin embargo, introduce etiquetas incoherentes en el sistema. Para superar este problema, los administradores pueden configurar un conjunto de etiquetas predefinidas. Para obtener más información sobre la configuración de etiquetas predefinidas, consulte *Configuración y personalización del Editor web XML* en el as a Cloud Service Instalar y configurar guías de Adobe Experience Manager .

Estas etiquetas se muestran en forma de lista desplegable a los autores, dondequiera que necesiten especificar una etiqueta. Esto garantiza que solo se utilicen etiquetas predefinidas y coherentes en el sistema.

Existen distintos métodos para aplicar etiquetas a los temas: [Historial de versiones](web-editor-use-label.md#) en la interfaz de usuario de Assets, [Líneas de base](/help/tutorials/user-guide/generate-output-use-baseline-for-publishing.md#id184KD0T305Z) IU y Editor web. La función Etiqueta de versión del Editor web ofrece a los autores una forma rápida y sencilla de asignar etiquetas a sus temas.

Para agregar etiquetas al tema desde el Editor web, realice los siguientes pasos:

1. Abra un tema en el Editor web.

1. Haga clic en **Etiqueta de versión**.

   Aparecerá el cuadro de diálogo Administración de etiquetas de versión.

   ![](images/version-label-management-dialog.png){width="650" align="left"}

   El cuadro de diálogo Administración de etiquetas de versión se divide en dos partes: el panel izquierdo tiene una lista de versiones disponibles para el tema junto con la lista desplegable de etiquetas \ (o un cuadro de texto para introducir una etiqueta\) y el panel derecho con una vista previa del tema.

1. Seleccione una versión en la que desee aplicar etiquetas.

   Cuando elige una versión diferente del tema en la lista de versiones, el panel de vista previa muestra los cambios entre la versión actual y la versión seleccionada del tema

   >[!NOTE]
   >
   > Si ya se ha aplicado una etiqueta a una versión, esta se muestra junto al número de versión en la lista desplegable y debajo de la lista Seleccionar versión . Para eliminar una etiqueta existente, haga clic en el botón \(**x**\) junto a la etiqueta.

1. Si el administrador ha definido una lista de etiquetas, se le mostrará una lista desplegable de las etiquetas desde donde puede elegir las etiquetas que desea aplicar. Puede seleccionar varias etiquetas en la lista desplegable.

   De lo contrario, se le mostrará un cuadro de texto en el que podrá introducir las etiquetas que desee agregar al tema.

   >[!NOTE]
   >
   > No se puede aplicar la misma etiqueta en varias versiones de un tema. Si intenta asociar una etiqueta existente, se le da una opción para eliminarla de la versión existente y aplicarla en la versión seleccionada del tema.

1. Haga clic en **Agregar etiqueta**.

1. En el mensaje de confirmación Aplicar etiqueta , seleccione la opción **Mover etiqueta** para mover las etiquetas de una versión existente a la versión seleccionada. Si no selecciona esta opción y hay etiquetas asignadas a una versión diferente del tema, no se mueven a la versión del tema seleccionado. Estas etiquetas se ignoran en el proceso de aplicación de etiquetas.


**Crear tarea de revisión** -  ![](images/create-review-task-icon.svg)

Puede crear una tarea de revisión del tema actual o del archivo de asignación directamente desde el Editor web. Abra el archivo para el que desea crear la tarea de revisión y haga clic en Crear tarea de revisión para iniciar el proceso de creación de la revisión.

>[!NOTE]
>
> También puede crear una tarea de revisión desde el panel Revisión \(a la derecha\).

Siga las instrucciones indicadas en la [Revisión de temas o mapas](review.md#) para obtener más información.

## Panel izquierdo {#id2051EA0M0HS}

El panel izquierdo es un panel persistente. Puede expandirla o contraerla haciendo clic en el icono Expandir barra lateral \(![](images/sidebar-expand-icon.svg)\). En la vista expandida, muestra los nombres de los iconos que aparecen como información sobre herramientas en la vista contraída.

>[!NOTE]
>
> Se puede cambiar el tamaño del panel izquierdo. Para cambiar el tamaño del panel, coloque el cursor en el límite del panel, el cursor cambiará a una flecha de doble punta, haga clic y arrastre para cambiar el tamaño del panel.

El panel izquierdo le permite acceder a las siguientes funciones:

**Favoritos** -  ![](images/favorite-collections.svg)

Si trabaja en un conjunto de archivos o carpetas, puede agregarlos a su lista favorita para acceder rápidamente a ellos. La lista Favoritos muestra la lista de documentos que ha agregado y otra lista de documentos favoritos a disposición del público de los demás usuarios.

Para crear una lista o colección de favoritos, haga clic en el icono + situado junto al panel Favoritos para que aparezca el registro de la colección nueva :

![](images/favorite-new-collection.PNG){width="300" align="left"}

Introduzca un título y una descripción para la colección favorita que desea crear. Si selecciona **Público**, este favorito también se muestra a otros usuarios.

Para agregar un archivo a su colección favorita, utilice cualquiera de los siguientes métodos:

- Vaya al archivo o la carpeta necesarios en la vista Repositorio, haga clic en el botón *Opciones* para abrir el menú contextual y elija **Agregar a favoritos**. En el cuadro de diálogo Agregar a favoritos, puede elegir agregar el archivo o la carpeta a un favorito existente o crear uno nuevo.

   ![](images/favorite-add-file-folder.png){width="300" align="left"}

- Haga clic con el botón derecho en la ficha de un archivo en el editor para abrir el menú contextual. Choose **Agregar A \> Favoritos** para agregar el archivo a la lista de favoritos.

   ![](images/favorite-add-from-file-context-menu_cs.png){width="400" align="left"}


>[!NOTE]
>
> Para quitar un elemento de la lista de favoritos, haga clic en el icono Opciones situado junto al archivo o carpeta en la lista Favoritos y elija **Eliminar de Favoritos**.

**Vista del repositorio** - ![](images/Repository_icon.svg)

Al hacer clic en el icono Vista de repositorio, se obtiene una lista de archivos y carpetas disponibles en DAM.

Se cargan 75 archivos a la vez. Cada vez que haga clic en **Cargar más**... se cargan 75 archivos y el botón deja de mostrarse cuando se han enumerado todos los archivos. Esta carga por lotes es eficiente y puede acceder a los archivos más rápido en comparación con la carga de todos los archivos existentes en una carpeta.

Puede desplazarse fácilmente al archivo requerido dentro de DAM y abrirlo en el Editor web. Si tiene el acceso necesario para editar el archivo, puede hacerlo.

También puede hacer clic y reproducir un archivo de audio o vídeo en el Editor web. Puede cambiar el volumen o la vista del vídeo. En el menú de accesos directos también tiene las opciones para descargar, cambiar la velocidad de reproducción o ver la imagen en imagen.



Al hacer doble clic en un archivo de mapa, se abre en la **Vista Mapa**. Para obtener más información, consulte la **Vista Mapa** descripción de la función en el [Panel izquierdo](web-editor-features.md#id2051EA0M0HS) para obtener más información. Al hacer doble clic en un archivo de tema, se abre en la [Área de edición de contenido](#id2051EB000UI). Al poder navegar y abrir un archivo directamente desde el Editor web, se ahorra tiempo y aumenta la productividad.

**Filtrar búsqueda**

El Editor web proporciona filtros mejorados para buscar texto. Haga clic en el filtro Buscar \(![](images/filter-search-icon.svg)\)para abrir el panel de filtros. Puede buscar un texto en los archivos presentes en la ruta seleccionada del repositorio de AEM. Por ejemplo, se busca &quot;propósito general&quot; en la siguiente captura de pantalla.

![](images/repository-filter-search.png){width="400" align="left"}

También tiene las siguientes opciones para filtrar los archivos y limitar la búsqueda en el repositorio de AEM:

- **Archivos DITA**: Puede buscar todo **Temas DITA** y **Mapas DITA** presentes en la ruta seleccionada.
- **Archivos no DITA**: Puede buscar **Archivos de imagen**, **Multimedia** y **Documentos** en la ruta seleccionada.
- **Elementos DITA**: También puede buscar valores específicos en los atributos de los elementos DITA especificados.
- **Protegido por**: Puede buscar archivos que el usuario especificado haya extraído.
- **Última modificación**: Puede buscar archivos que se hayan modificado por última vez después de una fecha seleccionada pero antes de una fecha seleccionada. También puede buscar archivos que hayan sido modificados por última vez en las últimas 2 horas, la última semana, el último mes o el último año.
- **Etiquetas**: Puede buscar archivos que tengan etiquetas específicas aplicadas a ellos. Puede escribir la etiqueta o seleccionarla en la lista desplegable.

**Nota:** El administrador del sistema también puede configurar los filtros de texto y mostrar u ocultar otros filtros. Para obtener más información, consulte *Configurar filtros de texto* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.

Se muestra la lista de archivos filtrados que contienen el texto buscado. Por ejemplo, en la captura de pantalla anterior, se muestran los archivos que contienen el texto &quot;propósito general&quot;. Puede seleccionar varios archivos de la lista filtrada para arrastrarlos y soltarlos en un mapa abierto para la edición.

**Menú Opciones**

Además de abrir archivos desde el panel izquierdo, también puede realizar muchas acciones utilizando la variable

Menú Opciones disponible en la vista Repositorio. Verá diferentes opciones, dependiendo de si elige una carpeta, un archivo de tema o un archivo de medios.

**Opciones de una carpeta**

Puede realizar las siguientes acciones utilizando el menú Opciones disponible para un *carpeta* en la vista Repositorio:

![](images/options-menu-folder_cs.PNG){width="550" align="left"}


- **Crear**: Cree un nuevo tema DITA, un mapa DITA o una carpeta. Para obtener más información, consulte la  **Crear temas desde la vista Repositorio** en el [Panel izquierdo](web-editor-features.md#id2051EA0M0HS) para obtener más información.



- **Cargar recursos**: Cargue un archivo desde el sistema local a la carpeta seleccionada en AEM repositorio. También puede arrastrar y soltar archivos del sistema local en el tema de trabajo actual. Esto resulta muy útil si desea insertar imágenes de su sistema local en el tema.

   ![](images/upload-assets.png){width="550" align="left"}

   Puede seleccionar una carpeta en la que desee cargar el archivo y también se mostrará una previsualización de la imagen. Si desea cambiar el nombre del archivo, puede hacerlo en el cuadro de texto del nombre del archivo. Haga clic en cargar para completar el proceso de carga de archivos. Si ha arrastrado y soltado un archivo de imagen en un tema, el archivo de imagen se añade en el artículo y también se carga.

   Si el administrador ha activado la opción UUID en *XMLEditorConfig*, podrá ver el UUID de la imagen cargada en el **Fuente** propiedad.

   ![](images/uuid-in-source-upload-image_cs.png){width="800" align="left"}

- **Buscar archivos en la carpeta**: Mueve el foco a la búsqueda del repositorio, donde puede introducir el término de búsqueda. La búsqueda se realiza en la carpeta seleccionada del repositorio. También puede aplicar un filtro para devolver archivos DITA, archivos de imagen o ambos.

   ![](images/find-files-in-folders-repo-view_cs.png){width="400" align="left"}

   También puede buscar utilizando el UUID de un archivo. En ese caso, los resultados de la búsqueda muestran el título del archivo DITA/XML y, en el caso de que el archivo sea un archivo de imagen, se muestra el UUID del archivo. En el siguiente ejemplo de búsqueda, se busca el UUID de un archivo de imagen y los resultados de la búsqueda muestran el UUID del archivo de imagen original y el título del tema del archivo en el que se hace referencia a esa imagen.

   ![](images/uuid-repo-search-image-topic-file_cs.png){width="300" align="left"}

- **Contraer todo**: Contrae todas las carpetas abiertas en el repositorio y muestra solamente las carpetas de nivel raíz.

   >[!NOTE]
   >
   > Utilice la variable **\>** junto a una carpeta para expandirla.

- **Agregar a favoritos**: Agrega la carpeta seleccionada a los favoritos. Puede elegir agregarla a una colección de favoritos existente o nueva.

- **Actualizar**: Obtenga una nueva lista de archivos y carpetas del repositorio.
- **Ver en la interfaz de usuario de Assets**: Muestre el contenido de la carpeta en la interfaz de usuario de Assets.

**Opciones de un archivo**

Verá diferentes opciones en el menú Opciones en función de si selecciona un archivo multimedia o un archivo DITA. Algunas opciones comunes disponibles para archivos multimedia y DITA son:

- Duplicar
- Cierre de compra/Registro
- Vista previa
- Eliminar
- Copiar
- Contraer todo
- Agregar a favoritos
- Propiedades
- Ver en la interfaz de usuario de Assets

![](images/options-menu-repo-view-file-level.png){width="550" align="left"}

A continuación se explican las distintas opciones del menú Opciones:

- **Editar**: Abra el archivo para editarlo. Si se trata de un archivo .ditamap/.bookmap, se abre en la variable [Editor de mapas avanzado](map-editor-advanced-map-editor.md#) para editar.

- **Duplicar**: Utilice esta opción para crear un duplicado o una copia del archivo seleccionado. También tiene la opción de cambiar el nombre del archivo duplicado en la solicitud de Duplicate Asset. De forma predeterminada, el archivo se crea con un sufijo \(como filename\_1.extension\). El título del archivo sigue siendo el mismo que el archivo de origen y el nuevo archivo comienza con la versión 1.0. Todas las referencias, etiquetas y metadatos se copian mientras que las líneas de base no se copian en el archivo duplicado.
- **Comprobar**: Obtenga un bloqueo en el archivo seleccionado para editarlo. Para un archivo bloqueado, esta opción cambia a **Proteger**.

   >[!NOTE]
   >
   > Si un usuario bloquea o extrae un archivo, al pasar el puntero del ratón sobre el icono de bloqueo, se mostrará al usuario \(nombre\) que ha bloqueado el archivo.

- **Vista previa**: Obtenga una vista previa rápida del archivo \(.dita/.xml\) sin abrirlo.

   ![](images/quick-preview_cs.png){width="800" align="left"}

- **Eliminar**: Utilice esta opción para eliminar el archivo seleccionado. Se muestra un mensaje de confirmación antes de eliminar el archivo.

   - Se muestra un mensaje de confirmación antes de eliminar el archivo.
   - Si no se hace referencia al archivo desde ningún otro archivo, este se elimina y se muestra un mensaje de éxito.
   - Si el archivo está desprotegido, no puede eliminarlo y aparecerá un mensaje de error.

      >[!NOTE]
      >
      > Si el administrador no ha podido eliminar los archivos desprotegidos, solo se mostrará el mensaje de error. Para obtener más información, consulte *Impedir la eliminación de archivos desprotegidos* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.

   - Si el archivo se agrega a una colección favorita, la variable **Forzar eliminación** y puede eliminarlo a la fuerza.
   - Si se hace referencia al archivo desde cualquier otro archivo, **Forzar eliminación** con el mensaje de confirmación se muestra y puede eliminar el archivo a la fuerza:

      ![](images/options-menu-force-delete.png){width="550" align="left"}

      >[!NOTE]
      >
      > Si el administrador ha concedido el permiso de eliminación de archivos, **Forzar eliminación** está activada. Si no, **Forzar eliminación** se desactiva y aparece un mensaje que indica que no tiene permiso para eliminar los archivos a los que se hace referencia. Para obtener más información, consulte *Impedir la eliminación de archivos a los que se hace referencia* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.

   - Si elimina un tema referenciado y ha abierto el archivo que contiene referencias para edición, se mostrará el vínculo roto para el archivo referenciado.
   >[!NOTE]
   >
   > También puede eliminar el archivo seleccionado de forma similar utilizando la tecla Supr del teclado.

- **Copiar**: Puede elegir entre las siguientes opciones:

   - **Copiar UUID**: Copie el UUID del archivo seleccionado en el Portapapeles.

   - **Copiar ruta**: Copie la ruta completa del archivo seleccionado en el Portapapeles.

- **Contraer todo**: Contraer todos los archivos del repositorio. Solo se muestran las carpetas de nivel superior del repositorio.
- **Agregar a**: Puede elegir entre las siguientes opciones:
   - **Favoritos**: Agrega el archivo seleccionado a los favoritos. Puede elegir agregarla a una colección de favoritos existente o nueva.

   - **Contenido reutilizable**: Agrega el archivo seleccionado a la lista Contenido reutilizable del panel izquierdo.

- **Propiedades**: Utilice esta opción para abrir la página de propiedades del archivo seleccionado. También se puede acceder a esta página de propiedades desde la interfaz de usuario de Assets seleccionando un archivo y haciendo clic en el icono Propiedades de la barra de herramientas.

- **Abrir tablero de mapas**: Si el archivo seleccionado es un mapa DITA, esta opción abre el tablero de asignación.

- **Ver en la interfaz de usuario de Assets**: Utilice esto para mostrar una previsualización de un archivo .dita/.xml en la interfaz de usuario de Assets. En el caso de un archivo .ditamap/.bookmap, todos los archivos de temas dentro del mapa se muestran en una sola vista unificada página por página.

- **Generación rápida**: Genere el resultado del archivo seleccionado. La salida solo se puede generar para archivos que formen parte de un ajuste preestablecido de salida. Para obtener más información, consulte [Publicación basada en artículos desde el Editor web](web-editor-article-publishing.md#id218CK0U019I).


**Crear temas desde la vista Repositorio**

Puede elegir crear un nuevo tema, asignación o carpeta desde el icono + situado junto al panel Repositorio o desde el menú contextual de una carpeta en la vista Repositorio.

***Crear un tema***

Cuando elija *crear un tema nuevo* en el menú, aparece el cuadro de diálogo siguiente:

![](images/create-topic-dialog.png){width="300" align="left"}

En el **Crear nuevo tema** , proporcione los siguientes detalles:

- Una plantilla en la que se basará el tema. Por ejemplo, para una configuración predeterminada, puede elegir entre las plantillas en blanco, concepto, DITAVAL, referencia, tarea, tema y resolución de problemas.

   Si la carpeta tiene un perfil de carpeta configurado, solo verá aquellas plantillas de tema que estén configuradas en el perfil de carpeta.

- Ruta donde desea guardar el archivo del tema. De forma predeterminada, la ruta de la carpeta seleccionada actualmente en el repositorio se muestra en el campo Path .
- Título para el tema.

- *\(Opcional\)* El nombre de archivo del tema. El nombre del archivo se sugiere automáticamente en función del título del tema.

   Si el administrador ha habilitado los nombres de archivo automáticos en función de la configuración de UUID, no verá el campo Nombre como se muestra en la siguiente captura de pantalla:

   ![](images/new-topic-without-filename.PNG){width="300" align="left"}


Al hacer clic en **Crear**, el tema se crea en la ruta especificada. Además, el tema se abre en el Editor web para su edición.

***Creación de un mapa DITA***

Cuando elija *crear un nuevo mapa DITA*, aparece el siguiente cuadro de diálogo:

![](images/create-map-dialog.png){width="300" align="left"}

En el **Crear nuevo mapa** , proporcione los siguientes detalles:

- Una plantilla en la que se basará el mapa. Por ejemplo, para una configuración predeterminada, puede elegir entre las plantillas de asignación de Bookmap o DITA.

- Ruta donde desea guardar el archivo de asignación. De forma predeterminada, la ruta de la carpeta seleccionada actualmente en el repositorio se muestra en el campo Path .
- A **Título** para el mapa.

- *\(Opcional\)* El nombre de archivo del mapa. El nombre del archivo se sugiere automáticamente en función del Título del mapa.

   Si el administrador ha habilitado los nombres de archivo automáticos en función de la configuración de UUID, no verá el campo Nombre .


Al hacer clic en **Crear**, el mapa se crea y se añade dentro de la carpeta especificada en el campo Path . Además, el mapa se abre en la vista Mapa. Puede abrir el archivo de mapa en el Editor de mapas y agregarle tema. Para obtener más información sobre cómo agregar temas a un archivo de asignación, consulte [Creación de un mapa](map-editor-create-map.md#).

***Crear una carpeta***

Cuando elija *crear una carpeta nueva*, obtendrá el **Crear nueva carpeta** diálogo:

![](images/new-folder-dialog_cs.png){width="300" align="left"}

Escriba un **Título** para la carpeta, que se convierte automáticamente en el nombre de la carpeta. La ruta es donde desea guardar el archivo de asignación. De forma predeterminada, la ruta de la carpeta seleccionada actualmente en el repositorio se muestra en el campo Path . Al hacer clic en **Crear**, la carpeta se crea y se añade dentro de la carpeta desde la que se ejecutó la opción crear carpeta.

**Vista Mapa** -  ![](images/map-view-icon.svg)

Al hacer clic en el icono Vista de mapa, obtendrá una lista de temas dentro del archivo de mapa. Si no ha abierto ningún archivo de asignación, la vista de mapa aparecerá en blanco. Al hacer doble clic en cualquier archivo de mapa, se abre el archivo de mapa en esta vista. Puede hacer doble clic en cualquier archivo del mapa para abrirlo en el Editor web. Cuando se abre un mapa en la vista del mapa, el título del mapa actual se muestra en el centro de la barra de herramientas principal. Si el título es demasiado largo, se muestra un punto suspensivo y también puede situarse sobre el título para ver el título completo en la información del objeto. Si tiene derechos de edición en los archivos de mapa, también podrá editar los archivos. Para obtener más información sobre cómo abrir y editar un tema a través de un mapa DITA, consulte [Editar temas a través de un mapa DITA](map-editor-advanced-map-editor.md#id17ACJ0F0FHS).

Puede realizar las siguientes acciones utilizando el menú Opciones del archivo de mapa:

![](images/options-menu-map-view_cs.png){width="550" align="left"}

- **Editar**: Abra el archivo de mapa para editarlo en el Editor de mapas avanzado.

- **Seleccionar todo**: Seleccione todos los archivos del mapa.

- **Borrar selección**: Anule la selección de los archivos seleccionados en el mapa.

- **Cierre de compra y bloqueo**: Cierre la compra y obtenga un bloqueo en los archivos seleccionados en el mapa.

- **Cancelar cierre de compra y desbloquear**: Desbloquea el archivo de mapa y lo pone a disposición para su edición. No revierte los cambios a la versión anterior.

- **Guardar como nueva versión y desbloquear**: Cree una versión más reciente y libere el bloqueo de los archivos seleccionados en el mapa.

- **Vista previa**: Abra una previsualización del archivo de mapa. En esta vista, todos los archivos de temas dentro del mapa se muestran en una sola vista unificada página por página.

- **Copiar**: Puede elegir entre las siguientes opciones:
   - **Copiar UUID**: Copie el UUID del archivo de asignación al Portapapeles.
   - **Copiar ruta**: Copie la ruta completa del archivo de asignación al Portapapeles.

- **Localizar en el repositorio**: Muestra la ubicación del archivo de asignación en el repositorio \(o DAM\).

- **Agregar a**: Puede elegir entre las siguientes opciones:
   - **Favoritos**: Agrega el archivo de asignación a favoritos. Puede elegir agregarla a una colección de favoritos existente o nueva.

   - **Contenido reutilizable**: Agrega el archivo de asignación a la lista Contenido reutilizable del panel izquierdo.

- **Propiedades**: Utilice esta opción para abrir la página de propiedades del archivo de asignación. También se puede acceder a esta página de propiedades desde la interfaz de usuario de Assets seleccionando un archivo y haciendo clic en el icono Propiedades de la barra de herramientas.

- **Abrir tablero de mapas**: Abra el tablero de mapas.

- **Ver en la interfaz de usuario de Assets**: Utilice esta opción para mostrar una previsualización del archivo de asignación en la interfaz de usuario de Assets. En esta vista, todos los archivos de temas dentro del mapa se muestran en una sola vista unificada página por página.

- **Generación rápida**: Genere la salida para el archivo de mapa seleccionado. La salida solo se puede generar para archivos que formen parte de un ajuste preestablecido de salida. Para obtener más información, consulte [Publicación basada en artículos desde el Editor web](web-editor-article-publishing.md#id218CK0U019I).
- **Cerrar**: Cierra el archivo de asignación.

La siguiente captura de pantalla muestra el menú Opciones de un archivo en la vista Mapa DITA:

![](images/options-menu-file_cs.PNG){width="550" align="left"}

Puede realizar las siguientes acciones mediante el menú Opciones:

- **Editar**: Abra el archivo para editarlo. Si se trata de un archivo .ditamap/.bookmap, se abre en la variable [Editor de mapas avanzado](map-editor-advanced-map-editor.md#) para editar.

- **Comprobar**: Compruebe el archivo seleccionado. Para un archivo desprotegido, esta opción cambia a **Proteger**.

   >[!NOTE]
   >
   > Si un usuario bloquea o extrae un archivo, al pasar el puntero del ratón sobre el icono de bloqueo, se mostrará al usuario \(nombre\) que ha bloqueado el archivo.

- **Vista previa**: Obtenga una vista previa rápida del archivo \(.dita/.xml\) sin abrirlo.
- **Copiar**: Puede elegir entre las siguientes opciones:
   - **Copiar UUID**: Copie el UUID del archivo seleccionado en el Portapapeles.
   - **Copiar ruta**: Copie la ruta completa del archivo seleccionado en el Portapapeles.

- **Localizar en el repositorio**: Muestra la ubicación del archivo seleccionado en el repositorio \(o DAM\).
- **Expandir todo**: Expanda todos los temas en los archivos de asignación.

- **Contraer todo**: Contraer todos los temas que forman parte del archivo de asignación actual.

- **Agregar a**: Puede elegir entre las siguientes opciones:
   - **Favoritos**: Agrega el archivo seleccionado a los favoritos. Puede elegir agregarla a una colección de favoritos existente o nueva.

   - **Contenido reutilizable**: Agrega el archivo seleccionado a la lista Contenido reutilizable del panel izquierdo.

- **Propiedades**: Utilice esta opción para abrir la página de propiedades del archivo seleccionado. También se puede acceder a esta página de propiedades desde la interfaz de usuario de Assets seleccionando un archivo y haciendo clic en el icono Propiedades de la barra de herramientas.

- **Ver en la interfaz de usuario de Assets**: Utilice esto para mostrar una previsualización de un archivo .dita/.xml en la interfaz de usuario de Assets. En el caso de un archivo .ditamap/.bookmap, todos los archivos de temas dentro del mapa se muestran en una sola vista unificada página por página.

- **Generación rápida**: Genere el resultado del archivo seleccionado. La salida solo se puede generar para archivos que formen parte de un ajuste preestablecido de salida. Para obtener más información, consulte [Publicación basada en artículos desde el Editor web](web-editor-article-publishing.md#id218CK0U019I).

>[!NOTE]
>
> También puede abrir y editar las propiedades de los temas seleccionados en un mapa DITA desde el **Más opciones** en la parte inferior de la vista Mapa.

**Vista Esquema** -  ![](images/outline-icon.svg)

Al hacer clic en el icono Vista de esquema, se obtiene la vista jerárquica de los elementos utilizados en el documento.

![](images/outline-view_cs.png){width="300" align="left"}

La vista Esquema ofrece las siguientes funciones:

- Una vista de árbol de todos los elementos utilizados en el documento.

- Si un elemento tiene un ID, un atributo y un texto, puede verlos junto con el elemento .

- Acceda a la vista Esquema en las vistas Autor y Origen.

- Utilice la lista desplegable de filtros para mostrar todos los elementos o solo las referencias rotas:

- Al hacer clic en un elemento en la vista Esquema se selecciona el contenido del elemento en la vista Autor o Origen. La vista Esquema permanece sincronizada con la vista Autor y Origen. Si realiza cambios en cualquier vista, puede verlos en la vista Esquema. Por ejemplo, si agrega un párrafo o actualiza un elemento en la vista Autor, se mostrará en la vista Esquema.

   ![](images/select-element-content-outline-view_cs.png){width="650" align="left"}

- Arrastrar y soltar elementos. Puede reemplazar fácilmente un elemento soltando otro elemento en él. Si arrastra y suelta un elemento sobre otro elemento y ve un cuadro cuadrado alrededor del elemento, indica que el elemento se reemplazará. Reemplaza el elemento en el que se coloca el elemento.

   ![](images/replace-element-outline-view_cs.png){width="300" align="left"}

   Si arrastra y suelta un elemento, un rectángulo discontinuo indica que el elemento se puede colocar en la ubicación actual. Si la función de arrastrar y soltar no es válida, se muestra un mensaje de error para indicar que la operación no está permitida.

   ![](images/drop-element-outline-view_cs.png){width="300" align="left"}

- La variable **Opciones** en el *Vista Esquema* permite realizar operaciones genéricas como cortar, copiar, eliminar, generar ID, insertar elemento antes o después del elemento actual, cambiar el nombre o reemplazar un elemento, desajustar un elemento y crear un fragmento a partir del elemento seleccionado.

>[!NOTE]
>
>Para obtener más información sobre Generar ID, Insertar elemento antes o después del elemento actual y Desajustar un elemento, consulte [Otras funciones del Editor web](web-editor-other-features.md#).

**Opciones de vista para el panel Vista de esquema**

Con la lista desplegable Opciones de vista , puede elegir ver lo siguiente si el elemento los tiene:

- **Mostrar ID**: Muestra el id del elemento.
- **Mostrar atributo**: Muestra el atributo junto con su valor.
- **Mostrar texto**: Muestra el texto. Si el texto supera los 20 caracteres, se muestra un punto suspensivo.

Si un elemento de bloque tiene su propio texto, se muestra junto con ese elemento de bloque. Si no tiene su propio texto, el texto del primer elemento secundario se muestra junto con ese elemento de bloque.

![](images/outline-view-block-element.png){width="550" align="left"}

Si el administrador ha creado un perfil para los atributos, obtendrá esos atributos junto con sus valores configurados. También puede asignar atributos de visualización configurados por el administrador en la sección **Atributos de visualización** en la configuración del editor. Los atributos definidos para un elemento se muestran en las vistas Presentación y Esquema.


Para obtener más información, consulte la *Atributos de visualización* dentro de la variable *Configuración del editor* descripción de la función en el [Panel izquierdo](web-editor-features.md#id2051EA0M0HS) para obtener más información.

**Función de búsqueda**
Con la función de búsqueda, puede buscar un elemento por su nombre, id, texto o valor de atributo.

La búsqueda no distingue entre mayúsculas y minúsculas y coincide exactamente con la cadena. Los resultados de la búsqueda se ordenan según la posición del elemento en el documento.

Puede buscar una cadena en el elemento si se muestra en el panel Vista de esquema. Por ejemplo, si la cadena &quot;Adobe&quot; está presente en el texto del elemento y se muestra en el panel Vista de esquema (tal como ha seleccionado) **Mostrar texto** en la lista desplegable Opciones de vista ), se filtra el elemento que lo contiene. Pero si el texto no se muestra en el panel Vista de esquema (tal y como no ha seleccionado) **Mostrar texto** en la lista desplegable Opciones de vista ), el elemento que lo contiene no se filtra. Del mismo modo, encontrará la cadena en el ID o los atributos si los ha seleccionado.



**Contenido reutilizable** -  ![](images/content-reuse-icon.png)

Una de las características principales de DITA es la capacidad de reutilizar contenido. El panel Contenido reutilizable puede almacenar sus archivos DITA desde donde normalmente inserta contenido reutilizable. Una vez añadidos, los archivos DITA permanecen en el panel Contenido reutilizable entre sesiones. Esto significa que no tiene que volver a añadir los archivos DITA para acceder a ellos más adelante.

Puede arrastrar y soltar contenido reutilizable desde el panel hasta el tema actual y se inserta fácilmente y rápidamente. También puede obtener una vista previa del contenido antes de insertarlo en el documento.

Para agregar un archivo DITA al panel Contenido reutilizable, utilice cualquiera de los siguientes métodos:

- Haga clic en el icono + situado junto a Contenido reutilizable para abrir el cuadro de diálogo Examinar archivo. Seleccione el archivo que desea agregar y haga clic en **Agregar** para completar el proceso.

   ![](images/reuse-content-add-dita-file_cs.png){width="650" align="left"}

- En la vista Repositorio, haga clic en el icono Opciones del archivo deseado y elija **Agregar a contenido reutilizable** en el menú contextual.

- Haga clic con el botón derecho en la ficha de un archivo en el editor para abrir el menú contextual y elija **Agregar a contenido reutilizable**.


Una vez agregado el archivo, puede ver todos los elementos de contenido reutilizables del archivo en el panel Contenido reutilizable . El contenido reutilizable se muestra con sus ID y nombres de elemento.

Cuando agrega un archivo a la lista Contenido reutilizable, se muestra el título del archivo en lugar del UUID del archivo. Para comprobar el UUID del archivo, pase el ratón sobre el título del archivo y el UUID del archivo se mostrará en la información del objeto.

![](images/uuid-reusable-content-file-title_cs.png){width="300" align="left"}

>[!NOTE]
>
> Puede agregar varios archivos a la lista de contenido reutilizable. A continuación, puede insertar el contenido deseado del panel Contenido reutilizable en el documento.

**Actualizar**: Revisa todo el contenido reutilizable y muestra una nueva lista de contenido reutilizable.

Para insertar contenido desde el panel Contenido reutilizable, utilice cualquiera de los siguientes métodos:

- Pase el puntero del ratón sobre un elemento que desee insertar, haga clic en el icono Opciones y elija **Insertar contenido reutilizable**.

   ![](images/insert-reusable-content_cs.png){width="400" align="left"}

   >[!NOTE]
   >
   > Nota: La variable **Vista previa** también está disponible en el menú contextual, que le proporciona una vista previa rápida del elemento antes de insertarlo.

- Arrastre y suelte el elemento de contenido reutilizable desde el panel en la ubicación deseada del documento.


**Glosario** -  ![](images/glossary.svg)

AEM guías le permite crear y utilizar fácilmente documentos de tipo glosario. Puede crear archivos de temas del glosario y luego incluirlos en un mapa de glosario común. Una vez agregado este mapa como su mapa raíz, las entradas del glosario se muestran en el panel Glosario.

![](images/glossary-panel.png){width="650" align="left"}

Para insertar un término del glosario, simplemente arrastre y suelte la entrada del panel en la ubicación deseada del tema. El menú Opciones de un término de glosario le permite obtener información rápida **Vista previa** del término de entrada, **Copiar ruta** del archivo de términos de entrada, o busque el archivo de términos de entrada en el repositorio.

Siga estos pasos para buscar términos de texto y sustituirlos por abreviaciones de glosario:

1. Abra el tema o mapa DITA en el que desee buscar y convertir el texto o los términos.
1. Seleccione el panel del glosario para ver los términos del glosario presentes en el mapa raíz. Puede arrastrar y soltar estos términos para agregarlos al tema abierto.
1. Seleccione el **Zona interactiva** herramienta \( ![](images/hotspot-icon.svg)\) en el panel Glosario para buscar y convertir términos de texto específicos a abreviaciones de glosario vinculadas. Además, viceversa puede utilizarla para buscar abreviaciones del glosario y convertirlas en términos de texto.

![](images/glossary-hotspot-tool.png){width="300" align="left"}

Puede configurar las siguientes opciones de la herramienta Zona interactiva:

![](images/Glossary-search-keys.png){width="300" align="left"}

- **Claves de glosario**: Seleccione las teclas de glosario del mapa DITA que desee utilizar para la búsqueda en el tema seleccionado. A continuación se muestran las claves seleccionadas. Para quitar una clave seleccionada, haga clic en el botón **Eliminar** icono.

- **Temas**: Elija la **Tema actual** abierto en el Editor web, todas las **Temas abiertos** en el mapa actual, o **Mapa actual** se está editando en el Editor de mapas para buscar los términos.
- **Filtrar temas por estado**: Puede elegir limitar la búsqueda a temas que tengan el estado de documento seleccionado. Los temas pueden estar en estado Borrador, Editar, Revisión, Aprobado, Revisado, Hecho o en cualquiera de los estados configurados por la organización.
- **Acción**: Puede elegir si buscar en las claves del glosario **Manualmente para cada tema** o **Automáticamente para todos los temas**. Si elige **Manualmente para cada tema**, le pedirá que confirme antes de convertir cada término en cada tema. Si elige **Automáticamente para todos los temas**, convierte automáticamente todos los términos de todos los temas.
- **Convertir**: Puede convertir una búsqueda **Texto a término de glosario** o **Término del glosario en texto.**
- **Opciones**: Puede seleccionar entre las siguientes opciones:
   - **Coincidencia que distingue entre mayúsculas y minúsculas**: Busca un término para encontrar la coincidencia que tiene la misma carcasa. Por ejemplo, &quot;USB&quot; no coincidirá con &quot;usb&quot;.
   - **Convertir solo la primera instancia**: Si hay varias instancias del término buscado en un tema, solo se convierte la primera instancia.
   - **Comprobar archivo antes de conversión**: El archivo buscado se extrae antes de que se conviertan los términos.
   - **Crear una nueva versión después de la conversión**: Se crea una nueva versión del tema una vez completada la conversión de términos.
- **Siguiente** aparece si selecciona **Manualmente para cada tema** . Haga clic en **Siguiente** para convertir los términos de cada tema según la configuración seleccionada. Solicita la conversión de términos en cada tema y pasa al siguiente archivo. Puede elegir convertir un término o omitirlo y pasar al siguiente término.

   ![](images/manual-convert-skip.png){width="300" align="left"}

- **Convertir** aparece si selecciona **Automáticamente para todos los temas** . Select **Convertir** para convertir todos los términos encontrados en el documento en abreviaciones de glosario vinculadas.

Una lista de **Temas actualizados** con los términos convertidos y **Temas con error** se muestra. Pase el ratón sobre el \( ![](images/info-icon.svg)\) cerca de Temas con error para ver los detalles del error.

![](images/glossary-converted-terms-error.png){width="300" align="left"}

>[!NOTE]
>
> Actualice el tema para ver los términos convertidos.

**Condiciones** -  ![](images/conditions-icon.svg)

El panel Condiciones muestra los atributos condicionales definidos por el administrador en el perfil global o de nivel de carpeta. Puede agregar condiciones al contenido simplemente arrastrando y soltando la condición deseada en el contenido. El contenido condicional se resalta con el color definido para la condición de que sea más fácil identificarlo.

También puede aplicar varias condiciones en un elemento arrastrando y soltando varias condiciones en un elemento. Cuando se aplican varias condiciones a un elemento, el panel Propiedades muestra las condiciones aplicadas separadas por una coma.

![](images/multiple-conditions-applied_cs.png){width="800" align="left"}

Sin embargo, en la vista Código, las condiciones se separan con un delimitador de espacio. Cuando agregue o edite una condición en la vista Código, asegúrese de que las condiciones múltiples se separen con un espacio.

>[!IMPORTANT]
>
> La siguiente captura de pantalla es de un usuario con privilegios administrativos. Como usuario con privilegios administrativos, puede agregar, editar y eliminar condiciones. De lo contrario, como autor normal, solo obtendrá la opción de aplicar condiciones.

![](images/conditional-content-through-panel_cs.png){width="800" align="left"}

Para añadir o definir una condición, haga clic en el icono + situado junto al panel Condiciones para que aparezca el cuadro de diálogo Definir condición :

![](images/conditional-panel-create-cond.png){width="400" align="left"}

En la lista Atributo, seleccione el atributo condicional que desea definir, introduzca un valor para la condición y, a continuación, especifique la etiqueta que se muestra en el panel Condiciones. También puede definir un color para la condición. Este color se establece como el color de fondo del contenido en el que se aplica la condición

Para editar una condición, elija **Editar** en el menú Opciones. Aparecerá el cuadro de diálogo Editar condición:

![](images/conditional-panel-edit-cond.png){width="400" align="left"}

Especifique los detalles del mismo modo que se configuró al definir una nueva condición.

**Asunto** -  ![](images/subject_scheme_panel-icon.svg)

Los mapas de esquemas de sujetos son una forma especializada de mapas DITA que se utilizan para definir sujetos taxonómicos y valores controlados. Según sus necesidades, puede crear un mapa de esquema de temas y hacer referencia a él dentro del archivo de asignación raíz. AEM guías le permite definir la jerarquía de nivel anidado de las definiciones de asunto en su esquema de temas.

Puede crear y, a continuación, utilizar fácilmente el esquema de temas en un mapa de esquemas de temas. Una vez agregado este mapa como mapa raíz, el esquema de temas se muestra en el panel Esquema de temas. El panel Esquema de temas muestra el esquema de temas disponible de forma anidada o jerárquica.

AEM guías también admite mapas de esquemas de temas de nivel anidado, y puede tener varios esquemas de temas definidos en el mapa de esquemas de temas raíz.

El siguiente ejemplo muestra cómo utilizar el esquema de temas en AEM guías.

1. Cree un archivo de esquema de temas en la herramienta que elija. El siguiente código XML crea un esquema de asunto que enlaza valores para la variable `platform` atributo.

   ```XML
   <?xml version="1.0" encoding="UTF-8"?>
   <!DOCTYPE subjectScheme PUBLIC "-//OASIS//DTD DITA Subject Scheme Map//EN" "subjectScheme.dtd">
   <subjectScheme id="GUID-4f942f63-9a20-4355-999f-eab7c6273270">
       <title>rw</title>
       <!-- Define new OS values that are merged with those in the unixOS scheme -->
       <subjectdef keys="os">
           <subjectdef keys="linux">    </subjectdef>
           <subjectdef keys="mswin">    </subjectdef>
           <subjectdef keys="zos">    </subjectdef>
       </subjectdef>
       <!-- Define application values -->
       <subjectdef keys="app" navtitle="Applications">
           <subjectdef keys="apacheserv">    </subjectdef>
           <subjectdef keys="mysql">    </subjectdef>
       </subjectdef>
       <!-- Define an enumeration of the platform attribute, equal to       each value in the OS subject. This makes the following values       valid for the platform attribute: linux, mswin, zos -->
       <enumerationdef>
           <attributedef name="platform">    </attributedef>
           <subjectdef keyref="os">    </subjectdef>
       </enumerationdef>
       <!-- Define an enumeration of the otherprops attribute, equal to       each value in the application subjects.       This makes the following values valid for the otherprops attribute:       apacheserv, mysql -->
       <enumerationdef>
           <attributedef name="otherprops">    </attributedef>
           <subjectdef keyref="app">    </subjectdef>
       </enumerationdef>
   </subjectScheme>
   ```

   ![](images/subject-scheme-panel.png){width="300" align="left"}

1. Guarde el archivo con la extensión a.ditamap y cárguelo en cualquier carpeta de DAM.

   >[!NOTE]
   >
   > Puede añadir una referencia al archivo de esquema de asunto en el mapa DITA principal.

   ![](images/subject-scheme-root-map.png){width="550" align="left"}

1. Establezca el mapa principal como el mapa raíz en la variable **Preferencias de usuario**. Una vez agregado este mapa como mapa raíz, el esquema de temas se muestra en el panel Esquema de temas.

   ![](images/subject-scheme-user-preferences.png){width="400" align="left"}

1. En el Editor web, abra el archivo en el que desea utilizar las definiciones de esquema de asunto.
1. Aplique el esquema de temas a su contenido simplemente arrastrando y soltando el esquema de temas deseado en su contenido. A continuación, el contenido se resalta en el color definido.

   ![](images/subject-scheme-apply.png){width="650" align="left"}


**Menú desplegable Atributos**

También puede cambiar el valor del esquema de asunto mediante la lista desplegable Atributo del panel Propiedades de contenido en la vista Autor. Para cambiar el valor, seleccione un valor en la lista desplegable Atributo .

![](images/subject-scheme-attribute-dropdown.png){width="300" align="left"}

También puede aplicar valores a un atributo seleccionando varios valores en la lista desplegable.

**Vista de origen**

También puede cambiar los valores desde la lista desplegable del atributo en la vista de origen. La vista de origen también impide que se agregue cualquier valor incorrecto.

![](images/subject-scheme-code-error.png){width="550" align="left"}

**Ver y aplicar el esquema de temas desde el panel Condiciones**

También puede ver y aplicar el esquema de temas desde el panel Condiciones .

Para ver el esquema de temas en el panel Condiciones , el administrador del sistema debe seleccionar la opción **Mostrar esquema de sujeto en el panel Condiciones** en la ficha Condición de Configuración del editor. Para obtener más información, consulte [Pestaña Condición](#id21BMNE0602V).

El panel Condiciones muestra la estructura vertical plana de las definiciones de asunto dentro del esquema de temas.

![](images/subject-scheme-condtions-panel.png){width="300" align="left"}

Puede agregar condiciones al contenido arrastrando y soltando la condición deseada en el contenido. El contenido condicional se resalta con el color definido para la condición.

**Fragmentos** -  ![](images/insert-snippet-icon.svg)

Los fragmentos de código son fragmentos de contenido pequeños que se pueden reutilizar en varios temas del proyecto de documentación. El panel Fragmentos muestra una colección de fragmentos de contenido que ha creado. Para insertar un fragmento, arrástrelo y suéltelo desde el panel hasta la ubicación deseada en el tema. El panel Fragmentos permite añadir, editar, eliminar, previsualizar e insertar un fragmento.

>[!IMPORTANT]
>
> La siguiente captura de pantalla es de un usuario con privilegios administrativos. Como usuario con privilegios administrativos, puede agregar, editar y eliminar fragmentos. De lo contrario, como autor normal, solo obtendrá las opciones para obtener una vista previa e insertar un fragmento.

![](images/snippets-panel_cs.png){width="400" align="left"}

Para agregar un fragmento, utilice cualquiera de los siguientes métodos:

- Haga clic en el icono + situado junto a Fragmentos para abrir el cuadro de diálogo Nuevo fragmento.

   ![](images/snippet-new-dialog.png){width="550" align="left"}

   En el cuadro de diálogo Nuevo fragmento, proporcione un título que aparezca en el panel Fragmentos, una descripción y un código XML del contenido de fragmento que desea crear. Haga clic en **Crear** para guardar y crear el fragmento.

- En el área de edición de contenido, haga clic con el botón derecho en la ruta de exploración del elemento que desee utilizar como fragmento y elija **Crear fragmento** en el menú contextual. El cuadro de diálogo Nuevo fragmento aparece con el código XML del elemento seleccionado rellenado en la variable **Contenido** campo . Introduzca la variable **Título** y **Descripción** para el fragmento y haga clic en **Crear** para guardar el fragmento.

- En el área de edición de contenido, haga clic con el botón derecho en cualquier lugar del contenido que desee utilizar como fragmento y elija **Crear fragmento** en el menú contextual. El cuadro de diálogo Nuevo fragmento aparece con el código XML del elemento seleccionado rellenado en la variable **Contenido** campo . Introduzca la variable **Título** y **Descripción** para el fragmento y haga clic en **Crear** para guardar el fragmento.

   La siguiente captura de pantalla resalta la ruta de exploración y el área de contenido desde la que puede invocar el menú contextual.

   ![](images/snippet-create-from-breadcrumb-content.png){width="350" align="left"}


Para insertar un fragmento, utilice cualquiera de los siguientes métodos:

- Seleccione un fragmento del panel Fragmentos y arrástrelo y suéltelo en la ubicación que desee en el tema.

- Sitúe el punto de inserción donde desee insertar el fragmento, en el menú Opciones del fragmento requerido, seleccione Insertar fragmento.


>[!NOTE]
>
> Desde el menú contextual de una entrada de fragmento, también puede elegir entre Editar, Eliminar, obtener una vista previa o Insertar un fragmento.

**Plantillas** -  ![](images/templates-icon.svg)

El panel Plantillas solo está disponible para administradores. El uso de este panel y el administrador pueden crear y administrar fácilmente plantillas que luego puedan utilizar los autores. De forma predeterminada, las plantillas se clasifican en *Mapa* y *Tema* plantillas de tipo .

![](images/templates-panel_cs.png){width="550" align="left"}

Para crear una plantilla, haga clic en el icono + situado junto a Plantillas y seleccione la plantilla que desee crear. Si selecciona **Plantilla de tema**, aparece el cuadro de diálogo Crear nueva plantilla de tema :

![](images/create-new-topic-template.PNG){width="400" align="left"}

Elija el tipo de plantilla que desea crear desde la **Plantilla** lista desplegable. Proporcione la variable **Título**, que aparece en el panel Plantillas . La variable **Nombre** de la plantilla se sugiere automáticamente en función del título, sin embargo, puede proporcionar un nombre de archivo diferente.

>[!NOTE]
>
> Si el administrador ha habilitado los nombres de archivo automáticos en función de la configuración de UUID, no verá el campo Nombre .

Una vez creada la plantilla, debe agregarla al perfil global o de nivel de carpeta. Una vez añadida la plantilla, los autores empezarán a ver la nueva plantilla en el proceso de creación de tema/asignación.

Con el menú Opciones de una plantilla existente, puede elegir **Editar** o **Duplicar** es así. En caso de duplicación, se conserva la estructura y el tipo de plantilla \(de documento\) y se puede reutilizar para crear otra plantilla a partir de ella.

**Buscar y reemplazar** -  ![](images/FindAndReplace_icon.svg)

El icono Buscar y reemplazar se encuentra en la parte inferior del panel izquierdo. El panel Buscar y reemplazar le permite buscar y reemplazar texto entre archivos en un mapa o en una carpeta dentro del repositorio. Puede encontrar y reemplazar en todos los temas de un mapa, así como temas presentes en los submapas dentro del mapa.

![](images/map-find-replace.png){width="800" align="left"}

Para realizar la búsqueda global y reemplazar, realice los siguientes pasos:

1. Abra la **Buscar y reemplazar** panel.
1. Haga clic en el **Buscar** en el menú desplegable, seleccione una de las siguientes opciones para realizar la búsqueda.
   - **Mapa actual**: Para buscar en el mapa abierto actualmente

      >[!NOTE]
      >
      > Esta opción aparece si ya ha abierto un mapa para editarlo.

   - **Ruta**: Para buscar en la ruta seleccionada
   - **Seleccionar mapa**: Para buscar en el mapa seleccionado

1. Puede hacer clic en el botón **Opciones** y elija entre las siguientes opciones:

   - **Archivo de cierre de compra antes de reemplazar**: Seleccione esta opción si desea extraer un archivo automáticamente antes de reemplazar el término de búsqueda. Esta configuración es más relevante en caso de que el administrador haya habilitado la configuración para extraer un archivo antes de editarlo. Con la configuración del servidor habilitada, debe seleccionar esta opción. Evitará que el cuadro de diálogo de cierre de compra de archivos le pida que cierre la compra de cada archivo antes de realizar cualquier cambio. Si no selecciona esta opción, aparecerá un mensaje antes de abrir un archivo para editarlo.
   - **Palabra completa solamente**: Seleccione esta opción si desea buscar toda la cadena de búsqueda. Por ejemplo, si se introduce en la cadena de búsqueda, el resultado de la búsqueda devolverá todos los archivos que contengan palabras como información general y sobre. Si desea restringir la búsqueda para que devuelva el término exacto introducido, seleccione esta opción.
   - **Crear nueva versión después de reemplazar**: Seleccione esta opción si desea crear una nueva versión del tema en la que elija reemplazar el texto. También puede proporcionar comentarios de versión que se añadirán con cada archivo actualizado.

      Si no selecciona esta opción, los cambios se guardan en la versión actual del tema y no se crea ninguna versión nueva.

   - **Incluir referencia indirecta**: Seleccione esta opción si desea buscar la cadena en las referencias indirectas también dentro del mapa DITA. De forma predeterminada, esto está desactivado, por lo que la búsqueda se realiza únicamente en las referencias directas.

1. Escriba el término de búsqueda o el texto que desee encontrar.
1. Introduzca el texto con el que desea reemplazar el término de búsqueda.
1. Pulse Intro o seleccione **Buscar** icono \( ![](images/search-icon.svg)\) para realizar la búsqueda.
1. Seleccione un archivo de la lista de resultados de la búsqueda. El archivo se abre en el área de edición de contenido con el término buscado resaltado en el contenido.
1. Abra la **Buscar y reemplazar** panel.
1. Haga clic en el **Buscar** en el menú desplegable, seleccione una de las siguientes opciones para realizar la búsqueda.

   - **Mapa actual**: Para buscar en el mapa abierto actualmente

      >[!NOTE]
      >
      > Esta opción aparece si ya ha abierto un mapa para editarlo.

   - **Ruta**: Para buscar en la ruta seleccionada
   - **Seleccionar mapa**: Para buscar en el mapa seleccionado

1. Puede hacer clic en el botón **Opciones** y elija entre las siguientes opciones:

   - **Archivo de cierre de compra antes de reemplazar**: Seleccione esta opción si desea extraer un archivo automáticamente antes de reemplazar el término de búsqueda. Esta configuración es más relevante en caso de que el administrador haya habilitado la configuración para extraer un archivo antes de editarlo. Con la configuración del servidor habilitada, debe seleccionar esta opción. Evitará que el cuadro de diálogo de cierre de compra de archivos le pida que cierre la compra de cada archivo antes de realizar cualquier cambio. Si no selecciona esta opción, aparecerá un mensaje antes de abrir un archivo para editarlo.

   - **Palabra completa solamente**: Seleccione esta opción si desea buscar toda la cadena de búsqueda. Por ejemplo, si se introduce en la cadena de búsqueda, el resultado de la búsqueda devolverá todos los archivos que contengan palabras como información general y sobre. Si desea restringir la búsqueda para que devuelva el término exacto introducido, seleccione esta opción.

   - **Crear nueva versión después de reemplazar**: Seleccione esta opción si desea crear una nueva versión del tema en la que elija reemplazar el texto. También puede proporcionar comentarios de versión que se añadirán con cada archivo actualizado.

      Si no selecciona esta opción, los cambios se guardan en la versión actual del tema y no se crea ninguna versión nueva.

   - **Incluir referencia indirecta**: Seleccione esta opción si desea buscar la cadena en las referencias indirectas también dentro del mapa DITA. De forma predeterminada, esto está desactivado, por lo que la búsqueda se realiza únicamente en las referencias directas.

1. Escriba el término de búsqueda o el texto que desee encontrar.

1. Introduzca el texto con el que desea reemplazar el término de búsqueda.

1. Pulse Intro o seleccione **Buscar** icono \( ![](images/search-icon.svg)\) para realizar la búsqueda.
1. Seleccione un archivo de la lista de resultados de la búsqueda. El archivo se abre en el área de edición de contenido con el término buscado resaltado en el contenido.

1. Haga clic en **Reemplazar incidencia única** \( ![](images/replace-icon.svg)\) para reemplazar el término de búsqueda resaltado actualmente en el tema o haga clic en Coincidencia siguiente ![](images/next-match-in-search.png) o ![](images/previous-match-in-search.png) Coincidencia anterior para desplazarse a la siguiente o anterior incidencia del texto.

1. Haga clic en **Reemplazar todo en el archivo** \( ![](images/replace-all-in-file-icon.svg)\)para reemplazar todas las ocurrencias del término buscado en un solo archivo con el término de reemplazo en un solo clic. Se le mostrará una notificación después de reemplazar todas las ocurrencias en el archivo seleccionado.

   >[!NOTE]
   >
   > Pase el ratón sobre un archivo de la lista de resultados de la búsqueda para ver el icono Reemplazar todo en el archivo a su derecha. También puede obtener el icono Ignorar archivo para eliminar el archivo del resultado de la búsqueda. Los archivos que ignora se eliminan de la lista y el término buscado no se reemplaza en ellos.

1. Haga clic en **Reemplazar todo** \( ![](images/replace-all-in-file-icon.svg)\) en la parte superior derecha de la lista para reemplazar todas las ocurrencias del término buscado en todos los archivos con el término de reemplazo en un solo clic.

   >[!NOTE]
   >
   > Para habilitar la variable **Reemplazar todo** , el administrador del sistema debe seleccionar la opción **Habilitar Reemplazar todo** en el **General** en **Configuración del editor**.


Sólo se puede realizar una operación de reemplazo en todo el sistema a la vez, y hasta que se realice la operación, verá el estado &quot;Reemplazar todo en curso&quot;. También puede cancelar la operación de reemplazo de todas entre o ver el informe de registro. Si interrumpe la operación, recibirá una notificación al respecto en la Bandeja de entrada. Se le mostrará una notificación de éxito después de reemplazar todas las ocurrencias en el archivo seleccionado.

![](images/replace-all-in-progress.png){width="400" align="left"}

También puede usar la variable **Buscar en Mapa** de la **Opciones** de un mapa para buscar y reemplazar texto en un mapa. Esta opción aparece para un mapa abierto en el panel del repositorio o en la vista del mapa.

![](images/map-options-menu.png){width="550" align="left"}

## Área de edición de contenido {#id2051EB000UI}

El área de edición de contenido es donde se muestra el contenido del tema o del mapa. Se realizan todas las ediciones de contenido en esta área. Proporciona una vista WYSIWYG del contenido que está editando. Puede tener varios temas abiertos al mismo tiempo, que se muestran en sus fichas respectivas. Debajo de la pestaña del archivo, se encuentra la ruta del elemento en la ubicación actual del cursor. En la esquina superior derecha del área de edición de contenido, se muestra el número de versión del tema actual.

![](images/content-editing-area.png){width="650" align="left"}

## Panel derecho {#id2051EB003YK}

El panel derecho es un panel persistente que contiene información sobre el documento seleccionado actualmente.

>[!NOTE]
>
> Se puede cambiar el tamaño del panel derecho. Para cambiar el tamaño del panel, coloque el cursor en el límite del panel, el cursor cambiará a una flecha de doble punta, haga clic y arrastre para cambiar el tamaño del panel.

El panel derecho le permite acceder a las siguientes funciones:

**Propiedades de contenido** -  ![](images/content-properties-icon.svg)

Para acceder a la función Propiedades de contenido , haga clic en el icono Propiedades de contenido del panel derecho. El panel Propiedades de contenido contiene información sobre el tipo de elemento seleccionado actualmente en el documento y sus atributos. También puede agregar atributos seleccionando el atributo en la lista desplegable y especificando el valor de un atributo.

>[!NOTE]
>
> Incluso si el tema contiene contenido referenciado, puede añadir atributos en él mediante el panel de propiedades.

Si el administrador ha creado un perfil para los atributos, obtendrá esos atributos junto con sus valores configurados. Con el panel de propiedades de contenido, puede elegir esos atributos y asignarlos al contenido relevante de su tema. De esta forma, también puede crear contenido condicional, que se puede utilizar para crear resultados condicionales. Para obtener más información sobre la generación de resultados mediante ajustes preestablecidos condicionales, consulte [Usar ajustes preestablecidos de condición](generate-output-use-condition-presets.md#).

![](images/properties-tab-attributes_cs.png){width="300" align="left"}

**Propiedades del archivo** -  ![](images/topic-properties-icon.svg)

Para ver las propiedades del archivo seleccionado, haga clic en el icono Propiedades del archivo en el panel derecho. Las Propiedades del archivo tienen las dos secciones siguientes:

**General**

La sección General le permite acceder a las siguientes funciones:

![](images/file-properties-general.png){width="300" align="left"}

- **Nombre**: Muestra el nombre de archivo del tema seleccionado. El nombre de archivo está hipervinculado a la página de propiedades del archivo seleccionado.
- **ID**: Muestra el ID del tema seleccionado.
- **Etiquetas de metadatos**: Estas son las etiquetas de metadatos del tema. Se establecen desde el campo etiquetas de la página de propiedades.
- **Idioma**: Muestra el idioma del tema. Se establece desde el campo de idioma de la página de propiedades.
- **Creado el**: Muestra la fecha y la hora en que se creó el tema.
- **Protegido por**: Muestra el usuario que retiró el tema.
- **Estado del documento**: Puede seleccionar y actualizar el estado del documento del tema abierto actualmente. Para obtener más información, consulte [Estado del documento ](web-editor-document-states.md#)*.*

**Nota:** Puede copiar los valores de atributo de los distintos campos de las propiedades de archivo en el portapapeles.

**Referencias**

La sección Referencias le permite acceder a las siguientes funciones:

![](images/file-properties-references.png){width="300" align="left"}

- **Se usa en**: El campo Utilizado en referencias enumera los documentos en los que se remite o utiliza el archivo actual.
- **Vínculos de salida:** Los vínculos salientes enumeran los documentos a los que se hace referencia en el documento actual.

Pase el ratón sobre la referencia del archivo y obtenga la ruta del archivo y el UUID del archivo en la información del objeto.

**Nota:** Todas las referencias utilizadas en y salientes están hipervinculadas a los documentos. Puede abrir y editar fácilmente los documentos vinculados.

Además de abrir archivos, también puede realizar muchas acciones utilizando la variable **Opciones** en la sección Referencias . Algunas de las acciones que puede realizar son: editar, previsualizar, copiar UUID, copiar ruta, agregar a favoritos, propiedades y abrir tablero de mapas.

**Consulte** -  ![](images/review-icon.svg)

Al hacer clic en el icono Revisar se abre el panel de revisión, donde puede crear una tarea de revisión para el documento abierto actualmente.

![](images/review-panel-before-opening.png){width="300" align="left"}

Si ha creado varios proyectos de revisión, puede seleccionar uno en la lista desplegable y acceder a los comentarios de revisión.

Con el panel de revisión, puede ver y publicar respuestas a los comentarios sobre el tema. Puede aceptar o rechazar los comentarios uno por uno.

Para obtener más información, consulte [Comentarios de revisión de direcciones](review-address-review-comments.md#).

**Cambios rastreados** -  ![](images/track-change-icon.svg)

Con la función Cambios rastreados del panel derecho, puede ver la información de todas las actualizaciones realizadas en un documento. También puede buscar cualquier actualización específica realizada en el documento.

>[!NOTE]
>
> La función Cambios rastreados muestra todas las actualizaciones que se han rastreado con la función Habilitar/Deshabilitar seguimiento de cambios de la barra de herramientas principal. Para obtener más información, consulte [Habilitar/Deshabilitar el seguimiento de cambios](#id205DF0203Y4).

**Tema principal:**[ Trabajar con el Editor web](web-editor.md)
