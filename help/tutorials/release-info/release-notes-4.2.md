---
title: Notas de versión | Versión de Adobe Experience Manager Guides 4.2
description: Última versión de Adobe Experience Manager Guides
exl-id: 8a7fef77-63af-462f-89c5-054ab31e079b
source-git-commit: 890d64aed5f4005e3f4d3143bc35804e39036ad3
workflow-type: tm+mt
source-wordcount: '3668'
ht-degree: 2%

---

# Versión 4.2 de las guías de Adobe Experience Manager (febrero de 2023)

Esta nota de la versión cubre las instrucciones de actualización, nuevas funciones y mejoras de la versión 4.2 de las guías de Adobe Experience Manager (más adelante denominadas *AEM Guías de*).

## Actualice a la última versión

AEM Puede actualizar fácilmente su versión actual de Guías de la a la versión 4.2. AEM Antes de continuar con la actualización a la versión 4.2 de las guías del usuario, debe tener en cuenta los siguientes puntos:
* Si utiliza las versiones 4.0, 4.1 o 4.1.x, puede actualizar directamente a la versión 4.2.
* Si utiliza la versión 3.8.5, debe actualizar a la versión 4.0 antes de actualizar a la versión 4.2.
* Si su versión es anterior a la 3.8.5, consulte la *AEM Guías de actualización* de la guía de instalación específica del producto.

>[!NOTE]
>
>AEM AEM Debe instalar el paquete de servicio de antes de actualizar la versión de las guías de usuario.

Para obtener más información, consulte [Instrucciones de actualización](assets/Adobe-Experience-Manager-Guides-Upgrade-Instructions-EN.pdf).

## 4,2 | Notas de la versión

## Matriz de compatibilidad

AEM En esta sección se enumera la matriz de compatibilidad para las aplicaciones de software compatibles con la versión 4.2 de las Guías de la aplicación para la administración de aplicaciones (Guides).

### Adobe Experience Manager

**No UUID**
Paquete de servicio 15, 14, 13 o 12 de la versión 6.5

**UUID**
Paquete de servicio 15, 14, 13 o 12 de la versión 6.5

Para obtener más información, consulte la *Requisitos técnicos* de la guía Instalar y configurar guías de Adobe Experience Manager.

### FrameMaker y FrameMaker Publishing Server

| Edición | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.2 (no UUID) | 2022 o superior | 2020.2 o superior* | 2022 o superior | 2020.3 o superior |
| 4.2 (UUID) | 2022 o superior | 2020.2 o superior* | 2022 o superior | 2020.4 o superior |
|  |  |  |  |

AEM *La línea de base y las condiciones creadas en la versión de FMPS a partir de 2020.2 son compatibles con las versiones de FMPS.

### Conector de oxígeno

| Edición | Ventanas de conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.2 (no UUID) | 2.1-regular-4 | 2.1-regular-4 | 1.6 | 1.6 |
| 4.2 (UUID) | 2.8-uuid-8 | 2.8-uuid-8 | 2.3 | 2.3 |
|  |  |  |


## Nuevas funciones y mejoras

AEM Las guías de la versión de ofrecen muchas mejoras y nuevas funciones en la versión 4.2:

### Generar informes desde el editor web

AEM Las guías de usuario incluyen una función en el editor web que permite comprobar la integridad general de los documentos técnicos y generar informes para ellos.
Puede ver la lista de temas y administrar los metadatos de todas las referencias para el mapa actual desde el
**Informes** en el Editor Web.

**Generar la vista Lista de temas**

Puede generar la Lista de temas que proporciona información detallada sobre los temas, como el tipo de referencia, el estado del documento y el autor. También puede generar el CSV para descargar la instantánea actual de los temas en el mapa DITA.

**Administrar metadatos y cambiar el estado del documento**

Puede aplicar etiquetas a un tema individual o utilizar la función de etiquetado masivo para aplicar varias etiquetas a varios temas, a un mapa DITA o a un submapa. También puede cambiar el estado del documento de todos los temas seleccionados al siguiente estado común posible del documento.

<img src="assets/web-editor-metadata-panel.png" alt="administrar metadatos" width="600">

### Experiencia de usuario modificada para la funcionalidad de revisión

AEM Ahora, las guías de usuario de proporcionan un UX mejorado que le ayuda a revisar los temas compartidos para su revisión. En la experiencia más reciente, la funcionalidad de revisión presenta las siguientes mejoras:

* Interfaz de usuario actualizada
* Panel Condiciones que le permite resaltar el contenido según las condiciones disponibles en el tema.
* Cada comentario del panel de comentarios está vinculado al texto correspondiente del tema actual. Ayuda a identificar el texto comentado.
* Los comentarios se muestran en el orden del texto comentado en el documento.
* El nombre de la tarea de revisión se muestra en el flujo de trabajo de revisión.
* Seleccione el mapa de raíz para la tarea de revisión que se utiliza para resolver todas las referencias clave y los términos del glosario utilizados en el contenido de la revisión.
* Barra de herramientas contextual que le ayuda a resaltar o tachar texto rápidamente.
* Menú Opciones para editar o eliminar sus propios comentarios.
* Para los comentarios obsoletos, tiene acceso a la vista en paralelo que le ayuda a comparar la versión anterior del tema con la versión de revisión actual
* Al utilizar los filtros, los comentarios del panel derecho se filtran según la selección y el número de comentarios del panel izquierdo se actualiza en consecuencia.


<img alt="revisar tarea" src="assets/comment-pop-up-panel.png" width="600">


Para obtener más información, consulte la *Revisar temas o mapas* de la guía Uso de guías de Adobe Experience Manager.

### Mejoras de traducción

Ahora tiene mejoras más fáciles de usar en el panel de traducción que le ayudan a traducir fácilmente sus documentos desde el Editor web.


**Columna Etiqueta de versión añadida al panel de traducción**

En el panel de traducción, también puede ver la columna Etiqueta de versión. Muestra la etiqueta de la versión seleccionada del archivo de origen. Esto puede ayudarle a seleccionar todos los archivos con una etiqueta específica y traducirlos de una sola vez.

**Ver la diferencia de versión de los archivos sin sincronizar en el panel de traducción**

Ahora puede comprobar las diferencias entre la versión seleccionada y la última versión de origen traducida de los temas. También puede optar por traducir el **Fuera de sincronización** archivos basados en los cambios realizados entre las dos versiones de un tema.

<img src="assets/translation-version-diff.png" alt="comité de traducción" width="600">



**Pasar la etiqueta de versión a la versión de destino**

AEM Guías de le permite pasar la etiqueta del archivo de origen al archivo de destino. Esto le ayuda a identificar fácilmente la versión de origen del archivo traducido.

<img alt="etiquetas de traducción" src="assets/translation-pass-source-label.png" width="600">

Por ejemplo, si tiene algunos archivos de origen con la etiqueta de versión Release 1.0 aplicada a ellos, también puede pasar la etiqueta de origen (Versión 1.0) al archivo traducido.

**Forzar sincronización de recursos sin sincronizar**

AEM Si realiza cambios en algunos de los recursos, Guías de recursos los marca como Desincronizados. Puede volver a traducir los recursos modificados o elegir descartar el estado Fuera de sincronización. Por ejemplo, si ha realizado algunos cambios menores que realmente no necesitan traducción, puede marcar su estado como Sincronizado.

**Ver proyectos de traducción en curso de un tema o mapa**

Algunas de las referencias del panel de traducción pueden estar en curso. AEM Ahora, Guías de proporciona una función que le ayuda a ver la lista de todos los proyectos de traducción en curso (junto con el idioma de destino) que contienen la referencia seleccionada.

Para obtener más información, consulte la *Traducir documentos desde el editor web* de la guía Uso de guías de Adobe Experience Manager.

### Generar resultados en varios formatos desde el editor web

Ahora puede generar fácilmente el resultado de sus temas o mapa DITA desde el Editor Web. AEM Puede configurar varios ajustes preestablecidos de salida, como Sitio de la aplicación, PDF, HTML 5, JSON (un formato de salida sin encabezado) y salida personalizada. Utilícelos para generar los resultados correspondientes. Puede definir atributos en los temas DITA y, a continuación, utilizar el ajuste preestablecido de condición para aplicar una condición al publicar la salida. También se puede utilizar la función de publicación Línea base para publicar selectivamente una versión específica del tema o mapa DITA.

**Administrar ajustes preestablecidos de salida del perfil global y de carpeta**

AEM Las guías de proporcionan la función para crear y administrar ajustes preestablecidos de salida para los Perfiles global y de carpeta. A continuación, puede utilizar fácilmente estos ajustes preestablecidos de salida para generar resultados para todas las asignaciones relacionadas con ese perfil global o de carpeta.

<img alt="añadir ajuste preestablecido" src="assets/add-global-output-preset.png" width="400">


Estos ajustes preestablecidos globales aparecen en **Output** de todas las asignaciones relacionadas. Puede utilizarlas para generar la salida de todas las asignaciones relacionadas. Puede seleccionar el ajuste preestablecido como ajuste preestablecido por defecto del PDF para generar la salida del PDF. También puede **Editar**, **Cambiar nombre**, **Duplicar**, o **Eliminar** un ajuste preestablecido de salida existente del **Opciones** menú.

>[!NOTE]
>
>Solo los usuarios administrativos de nivel de carpeta pueden crear ajustes preestablecidos de Perfil global y de carpeta.

### Buscar y reemplazar el texto en el nivel de mapa

Ahora puede buscar archivos dentro de un mapa que contengan texto específico. El texto buscado se resalta en los archivos. También puede reemplazar la palabra o frase buscada por otra palabra o frase dentro de los archivos. Seleccione el **Reemplazar una sola incidencia** para reemplazar la incidencia actual y el **Reemplazar todo en archivo** para reemplazar todas las ocurrencias en el archivo seleccionado. Puede seleccionar **Reemplazar todo** para reemplazar todas las ocurrencias del término buscado en todos los archivos.

<img src="assets/map-find-replace.png" alt="mapa buscar reemplazar" width="600">


De forma predeterminada, las opciones **Archivo de retirada antes de reemplazar** y **Crear nueva versión tras reemplazar** están seleccionados, por lo que se extrae un archivo antes de reemplazar el texto y se crea una nueva versión después de reemplazar el texto. También se puede buscar la cadena en las referencias indirectas dentro del mapa DITA. De forma predeterminada, esta opción está desactivada, por lo que la búsqueda solo se realiza en las referencias directas.

### Vista Presentación en el editor de mapas


Ahora puede ver el diseño completo de un mapa DITA en el Editor de mapas. Cuando se abre un mapa para editarlo, se abre la vista Presentación del Editor de mapas. En esta vista, puede ver la jerarquía de mapas en una vista de árbol. También puede editar y organizar o estructurar los temas en un mapa.

<img src="assets/layout-view-map.png" alt=" vista de diseño del mapa" width="600">

La vista Presentación contiene una barra de herramientas independiente que le ayuda a realizar muchas tareas sobre los temas presentes en un mapa.
Puede insertar referencias de temas, grupos de temas y definiciones de claves en un mapa. Puede reorganizar los temas presentes en un mapa moviéndolos hacia arriba, hacia abajo, a la izquierda o a la derecha. También puede arrastrar y soltar los temas para moverlos en un mapa. El editor de mapas también proporciona los iconos para bloquear o desbloquear archivos, comprobar el historial de versiones y realizar una administración de etiquetas de versión.


La vista Presentación también proporciona el **Opciones de vista** para mostrar u ocultar el número de línea, mostrar u ocultar la casilla de verificación, o mostrar el nombre de archivo o el título de los temas de un mapa.
También puede ver los temas en función de los filtros condicionales aplicados.

Además de organizar los temas en el archivo de asignación, también puede agregar, mover, copiar, pegar o eliminar referencias utilizando **Opciones** menú disponible para un elemento en la vista Presentación.

<img src="assets/layout-inline-attributes.png" alt=" atributos de diseño de mapa" width="600">


El panel derecho muestra las Propiedades de contenido y las Propiedades de mapa en la vista Diseño del Editor de mapas. Ahora también puede establecer la información de metadatos para los temas o el mapa. Puede definir el título de navegación, el texto de vínculo, la descripción breve y las palabras clave para el tema o el mapa seleccionado.

Para obtener más información, consulte *Vista Presentación* de la guía Uso de guías de Adobe Experience Manager.

### Panel Generación rápida

AEM Ahora, Guías de proporciona el panel Generación rápida, que le ayuda a generar y ver rápidamente la salida de los ajustes preestablecidos creados para su mapa DITA.

<img src="assets/quick-generate-map-view.png" alt=" generar panel rápidamente" width="600">

En el **Generación rápida** , puede ver la lista de todos los ajustes preestablecidos de salida creados para el mapa DITA. También puede ver rápidamente el resultado generado para los ajustes preestablecidos. Al finalizar la generación de resultados, aparece un mensaje de éxito o error. También puede ver el registro de errores que contiene detalles del error que se produjo en el proceso de generación.

### Crear una línea base dinámica basada en etiquetas

AEM Ahora, Guías de le proporciona la función para crear líneas de base dinámicas basadas en etiquetas. Si genera una línea de base, descarga una línea de base o crea un proyecto de traducción utilizando una línea de base, los archivos se seleccionan dinámicamente en función de las etiquetas actualizadas. Esta función resulta útil, ya que no es necesario modificar la línea de base al actualizar las etiquetas.

<img src="assets/dynamic-baseline.png" alt=" línea base dinámica" width="400">

### Eliminar y duplicar archivos del panel del repositorio

Ahora puede eliminar fácilmente archivos (de uno en uno) de la **Opciones** menú del archivo seleccionado del panel repositorio. Se muestra un mensaje de confirmación antes de eliminar el archivo. Si no se hace referencia al archivo desde ningún otro archivo, se elimina y se muestra un mensaje de éxito.

<img src="assets/options-menu-repo-view-file-level.png" alt="menú opciones de archivo " width="500">

También puede crear un duplicado o una copia del archivo seleccionado. De forma predeterminada, el archivo se crea con un sufijo (como filename_1.extension).


### Otras mejoras del editor web

* AEM En Guías de la, puede realizar algunas operaciones comunes para imágenes y archivos multimedia mediante el menú contextual. Ahora también puede localizar la imagen o el medio seleccionado en el repositorio o ver la vista previa del archivo en la interfaz de usuario de Assets.

* El nombre del perfil de carpeta actual se muestra como una etiqueta para el icono Preferencias de usuario en la barra de herramientas principal. Esto le ayuda a identificar el perfil de carpeta en el que está trabajando.

* Cuando se abre un mapa en la vista de mapa, el título del mapa actual se muestra en el centro de la barra de herramientas principal. Esto resulta útil para que los usuarios sepan qué mapa está abierto actualmente.

### Depuración de versiones seleccionadas de archivos

A medida que crea y mantiene el contenido, es posible que se creen muchas versiones para los archivos DITA en el repositorio. AEM Guías de permite depurar versiones anteriores de los archivos DITA del repositorio y liberar espacio en disco.

<img src="assets/preview-purge-report.png" alt="Previsualizar informe de depuración" width="500">

AEM Guías no elimina la primera versión del archivo o una versión que se incluye en una línea de base, ni tiene una etiqueta aplicada. La operación de purga ni siquiera elimina los archivos que se incluyen en una traducción o en un flujo de trabajo de revisión. Puede elegir el número de versiones que desea conservar y también decidir eliminar los archivos que sean anteriores al número de días definido.

Antes de iniciar la operación de depuración, puede obtener una vista previa del informe para ver las versiones que se van a purgar. A continuación, puede decidir iniciar o cancelar la operación de depuración.

<img src="assets/download-purge-report.png" alt="Informe de purga de PDownload" width="500">

Una vez finalizada la operación de depuración, puede comprobar el informe de depuración para ver los archivos depurados.

### Ver el título en lugar del UUID en el editor de oxígeno

AEM Ahora, Guías de le permite elegir **Uso del título en el editor y el administrador de mapas** en Configuración. Si selecciona esta opción, el título del fichero se mostrará en la ficha del fichero cuando se abra en el Editor o en el Administrador de mapas DITA. Si no selecciona esta opción, el UUID del archivo se muestra en la pestaña del archivo.

### IU de metadatos disponible para ajustes preestablecidos de PDF

Puede definir los metadatos a partir del ajuste preestablecido de salida de un mapa DITA. Puede establecer los metadatos de Título, Autor, Asunto y Palabras clave. Estos metadatos se asignan a los metadatos de las propiedades de archivo del PDF de salida. Estos metadatos anulan los metadatos definidos en el nivel de libro. Puede definir los metadatos específicamente en cada ajuste preestablecido de salida y pasarlos al PDF de salida.

### PDF nativo | PDF con barra de cambios que muestra la diferencia entre las versiones del documento

Ahora puede crear un PDF que muestre las diferencias de contenido entre dos versiones con la barra de cambios. Puede elegir comparar la versión actual con una línea base de la versión anterior o comparar entre las dos versiones de línea base seleccionadas.

<img src="assets/pdf-change-version.png" alt="pdf-change-version" width="600">

Aparecerá una barra de cambios en el PDF para indicar el contenido modificado, insertado o eliminado. También tiene las opciones para hacer lo siguiente:
* Mostrar el contenido insertado en color verde y subrayado
* Mostrar el contenido eliminado en color rojo y marcado con un tachado

### PDF nativo | Compatibilidad de variables con ruta de salida y nombre de archivo del PDF

Ahora también puede utilizar las siguientes variables integradas para definir la ruta de salida y el archivo del PDF. Puede utilizar una sola variable o una combinación de ellas para definir estas opciones:
* `${map_filename}`
* `${map_title}`
* `${preset_name}`
* `${language_code}`
* `${map_parentpath}` (Solo para la ruta de salida)
* `${path_after_langfolder}` (Solo para la ruta de salida)

### PDF nativo | Generación de una tabla de contenido para mapas DITA y reordenación de diseños de página

Ahora también se puede generar la tabla de contenido en mapas DITA utilizando un ajuste de PDF avanzado de la plantilla. Puede elegir habilitar o deshabilitar la visualización de los distintos diseños de página y también reordenar su posición.

### PDF nativo | Añadir un marcador personalizado en la salida del PDF

Ahora puede agregar un marcador personalizado a un contenido en particular en la salida final del PDF para facilitar la navegación. Se añadirá al índice creado a partir de los títulos de temas o secciones del mapa DITA.

### PDF nativo | Aplicar estilo personalizado en entradas del índice y contenido del tema

AEM Guías de proporciona la función para aplicar un estilo personalizado en las entradas de la tabla de contenido o en un tema concreto de la salida del PDF. Por ejemplo, puede cambiar el color del texto de la tabla de contenido y el título del tema. También puede aplicar estilos a todo el contenido dentro del tema.




## Problemas solucionados

A continuación se enumeran los errores corregidos en varias áreas:

### Creación

* El panel izquierdo se rompe al añadir una pestaña. (11126)
* Los cambios en el HTML del editor web causan problemas con `<dl>` y `<dlentry>`. (11024)
* Algunos atributos no se tratan como condicionales y causan problemas. (10895)
* Tres niveles o más anidados `<indexterm>` no están anidadas en la exportación de PDF nativa. (10799)
* El contenido desaparece en el cuerpo de una tarea al cambiar de la vista Autor a Fuente. (10735)
* Los comentarios de revisión no se colocan correctamente en una tarea de revisión. (10625)
* `<conref>` una nota dentro de una etiqueta para no se muestra en el modo de vista previa. (10559)
* Al pulsar Retroceso al final de un elemento de la lista, se elimina toda la lista. (10540)
* La pantalla se muestra en blanco en Chrome v106 al arrastrar y soltar cualquier elemento de la interfaz de usuario (por ejemplo, del panel Condiciones ). (10524)
* Falta el botón Sangría automática en la barra de herramientas de **Origen** vista. (10448)
* El primer carácter de un elemento de lista se pierde a veces cuando la lista se crea en el editor.( 10447)
* **Deshacer** o **Rehacer** no funciona correctamente en algunos archivos. (10373)
* Los metadatos personalizados no se conservan en la acción de copiar y pegar. (10367)
* Se produce un error al realizar una copia (ctrl+c) y pegar (ctrl+v) del contenido. (10304)
* El panel Esquema no muestra contenido cuando se cambia del modo Autor al Modo Origen. (10296)
* El submapa no se crea cuando hace referencia a un mapa principal en las plantillas DITA. (10231)
* Los problemas de navegación se producen en el Editor Web después de la actualización 4.0. (10159)
* La opción Deshacer del Editor XML lleva al usuario al principio de la página. (10091)
* Las propiedades del nodo se eliminan después de la operación de copiar y pegar de un recurso. (10053)
* Los ficheros de SVG añadidos a los temas DITA no se muestran en el modo de vista previa del editor. (10010)
* Los resultados de búsqueda para buscar y reemplazar dentro del Editor Web no se pueden leer en el modo Oscuro. (9978)
* No existe ningún cargador al crear un mapa a partir de la plantilla de mapa. (9891)
* La referencia en la plantilla de tema no funciona y el ID de hash copiado no se actualiza en la copia de contenido. (9890)
* No se muestra ninguna opción para examinar los temas o la plantilla de asignación dentro de las subcarpetas del tema o la carpeta de asignación. (9889)
* No hay opción para crear una nueva plantilla en las subcarpetas de temas o mapas. (9888)
* El Editor XML no actualiza las imágenes de los temas. (9500)
* mimeType está codificado para la creación y actualización de recursos DITA. (8979)
* Se inserta un guión normal al seleccionar Guión de no separación en la **Insertar carácter especial** diálogo. (8919)
* El nombre del creador de la versión en el Historial de versiones es &quot;fmdita-serviceuser&quot; para los archivos cargados mediante la interfaz de usuario de Assets. (8910)
* La opción Editar no funciona para imágenes mientras se trabaja en la vista de columna de la interfaz de usuario de Recursos. (8758)
* El tema DITA no se actualiza automáticamente con los cambios realizados en **Propiedades** página. (8745)
* Al mover elementos dentro del tema en el editor web, los ID asignados en los elementos se sobrescriben con los ID asignados automáticamente. (7895)

### Administración

* La copia de un recurso de mapa DITA (desde la IU de recursos ) provoca líneas de base erróneas en el recurso copiado. (11218)
* AEM El mensaje de advertencia no se muestra en la carga de un archivo que supere el límite permitido en el (2 GB de forma predeterminada). (10817)
* Editor web: línea de base | El comportamiento de la columna Última es diferente en el nuevo tablero de línea de base dentro del Editor Web. (10808)
* Traducción | El trabajo de traducción no se ha iniciado debido a un /libs/fmdita/i18n/ja.json no válido. (10543)
* Traducción | Se produce un error en un proyecto de traducción de ámbito creado desde el panel de traducción (traducción humana). (10526)
* Traducción | El procesamiento posterior está bloqueado para toda la carpeta de idioma cuyos recursos están presentes en un proyecto de traducción activo. (10332)
* Traducción| Los metadatos y las etiquetas no se propagan a las copias traducidas. (4696)
* Aparecen varias ventanas emergentes para cualquier recurso si se cambia la versión y se guarda en el Editor de líneas de base. (10399)
* La pérdida de sesión se produce en com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver(QueryBuilderImpl.java:210). (10279)
* El archivo de vídeo no aparece en la línea de base si la carpeta principal contiene espacio en el nombre. (10031)

### Publicación

* La regeneración de temas no funciona para algunos escenarios. (10635)
* La publicación del PDF no consigue generar la salida para un ajuste preestablecido duplicado (de un ajuste preestablecido existente). (10584)
* El botón Ver registro no funciona en caso de que falle la generación del PDF para un ajuste preestablecido. (10576)
* Publishlistener no muestra los datos solicitados en los registros de información y también contiene algunos registros no deseados.( 10567)
* PDF nativo | La generación del PDF falla con una excepción de puntero nulo. (10950)
* PDF nativo | conkeyref no se está resolviendo en la salida generada. (10564)
* PDF nativo | Se producen problemas con los metadatos de un mapa al que hay que hacer referencia en la salida del PDF.( 10556)
* PDF nativo | Se producen problemas al girar el encabezado de tabla. (10555)
* PDF nativo | Se producen problemas al eliminar temas que tienen un rol de procesamiento=&#39;resource-only&#39;. (10554)
* PDF nativo | Las referencias clave vacías se muestran en la salida del PDF. (10553)
* PDF nativo | Anidado `<indexterm>` no están anidadas en la exportación de PDF nativa. (10521)
* PDF nativo | El PDF nativo utiliza un estilo en línea en lugar del nombre de clase para las etiquetas generadas. (10498)
* PDF nativo | El tema anidado en los apéndices se transforma en h1 en el HTML temporal.( 10454)
* PDF nativo | No se pueden ocultar los temas de la primera línea de contenido de la tabla de contenido. (10355)
* PDF nativo | Atributo de marco de tabla no propagado al HTML temporal (como clase). (10353)
* PDF nativo | Los archivos temporales del HTML agregan las clases colsep y rowsep a <td> y <th> incluso si su valor es 0 en el DITA de origen. (10352)
* PDF nativo | Al reiniciar los números de página en el diseño del capítulo, la numeración se inicia aleatoriamente desde el final del capítulo anterior. (10154)
* PDF nativo | Las referencias clave para los keydefs con vínculos de imagen o externos no se resuelven. (10063)
* PDF nativo | El apéndice se muestra como un capítulo en el PDF generado. (9829)
* La pestaña Plantilla del editor xml no se muestra a los administradores de perfil de carpeta. (10266)
* La publicación de línea de base falla para el PDF generado mediante FrameMaker Publishing Server 2020. (10551)
* Error de aplicación al hacer clic en el botón Editar después de seleccionar todos los ajustes preestablecidos mediante la casilla de verificación Ajustes preestablecidos de salida en la ventana emergente Generación rápida. (10388)
* Si la pestaña Salida del editor web tiene más ajustes preestablecidos, la sección de ajustes preestablecidos no se puede desplazar verticalmente y no muestra todos los ajustes preestablecidos disponibles. (9787)
* No se pueden eliminar los ajustes preestablecidos del flujo de trabajo de salida al publicar mediante el editor. (9100)
* El vínculo de igual a igual se representa como texto normal en lugar de como vínculo en la página generada. (7774)

### Problema conocido

El Adobe AEM de ha identificado el siguiente problema conocido de la versión 4.2 de las Guías de usuario de:

* Los usuarios pueden realizar operaciones de revisión incluso después de completar la tarea de revisión.
