---
title: Notas de la versión | Versión de las guías de Adobe Experience Manager 4.2
description: Última versión de las guías de Adobe Experience Manager
source-git-commit: 2fb46bdfb7f42fd9b3ef19343700009818c5b4f2
workflow-type: tm+mt
source-wordcount: '3681'
ht-degree: 2%

---

# 4.2 versión de las guías de Adobe Experience Manager (febrero de 2023)

Esta nota de la versión cubre las instrucciones de actualización, las nuevas funciones y las mejoras de la versión 4.2 de las guías de Adobe Experience Manager (más adelante denominadas *Guías AEM*).

## Actualice a la última versión

Puede actualizar fácilmente su versión actual de AEM guías a la versión 4.2. Antes de continuar con la actualización a la versión 4.2 de AEM guías, debe tener en cuenta los siguientes puntos:
* Si utiliza las versiones 4.0, 4.1 o 4.1.x, puede actualizar directamente a la versión 4.2.
* Si utiliza la versión 3.8.5, debe actualizar a la versión 4.0 antes de actualizar a la versión 4.2.
* Si está en una versión anterior a la 3.8.5, consulte la *Actualizar guías AEM* en la guía de instalación específica del producto.

>[!NOTE]
>
>Debe instalar AEM service pack antes de actualizar AEM versión de las guías.

Para obtener más información, consulte [Instrucciones de actualización](assets/Adobe-Experience-Manager-Guides-Upgrade-Instructions-EN.pdf).

## 4,2 | Notas de la versión

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software compatibles con AEM versión de Guías 4.2.

### Adobe Experience Manager

**No UUID**
Versión 6.5 Service Pack 15, 14, 13 o 12

**UUID**
Versión 6.5 Service Pack 15, 14, 13 o 12

Para obtener más información, consulte la *Requisitos técnicos* en la guía Instalar y configurar guías de Adobe Experience Manager .

### FrameMaker y FrameMaker Publishing Server

| Edición | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.2 (no UUID) | 2022 o posterior | 2020.2 o posterior* | 2022 o posterior | 2020.3 o superior |
| 4.2 (UUID) | 2022 o posterior | 2020.2 o posterior* | 2022 o posterior | 2020.4 o superior |
|  |  |  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

### Conector de oxígeno

| Edición | Ventanas del conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.2 (no UUID) | 2.1-regular-4 | 2.1-regular-4 | 1.6 | 1.6 |
| 4.2 (UUID) | 2.8-uuid-8 | 2.8-uuid-8 | 2.3 | 2.3 |
|  |  |  |


## Nuevas funciones y mejoras

AEM guías proporciona muchas mejoras y nuevas funciones en la versión 4.2:

### Generar informes desde el Editor web

AEM guías incluye una función en el Editor web que permite comprobar la integridad general de los documentos técnicos y generar informes para ellos.
Puede ver la lista de temas y administrar los metadatos de todas las referencias para el mapa actual desde el
**Informes** en el Editor web.

**Generar la vista Lista de temas**

Puede generar la lista de temas, que proporciona información detallada sobre sus temas, como el tipo de referencia, el estado del documento y el autor. También puede generar el CSV para descargar la instantánea actual de los temas en el mapa de DITA.

**Administrar metadatos y cambiar el estado del documento**

Puede aplicar etiquetas en un tema individual o utilizar la función de etiquetado masivo para aplicar varias etiquetas en varios temas, un mapa DITA o un submapa. También puede cambiar el estado del documento de todos los temas seleccionados al siguiente estado de documento común posible.

<img src="assets/web-editor-metadata-panel.png" alt="administrar metadatos" width="600">

### Experiencia de usuario mejorada para la funcionalidad de revisión

Ahora, AEM guías proporciona una experiencia de usuario mejorada que le ayuda a revisar los temas compartidos para su revisión. En la última experiencia, la funcionalidad de revisión presenta las siguientes mejoras:

* Interfaz de usuario actualizada
* Panel Condiciones que permite resaltar el contenido según las condiciones disponibles en el tema.
* Cada comentario del panel de comentarios está vinculado al texto correspondiente del tema actual. Ayuda a identificar el texto comentado.
* Los comentarios se muestran en el orden del texto comentado en el documento.
* El nombre de la tarea de revisión se muestra en el flujo de trabajo de revisión.
* Seleccione la hoja de ruta para la tarea de revisión que se utiliza para resolver todas las referencias clave y los términos del glosario utilizados en el contenido de revisión.
* Barra de herramientas contextual que le ayuda a resaltar o tachar rápidamente el texto.
* Menú Opciones para editar o eliminar sus propios comentarios.
* Para comentarios obsoletos, tiene acceso a la vista en paralelo que le ayuda a comparar la versión anterior del tema con la versión de revisión actual
* Al utilizar los filtros, los comentarios del panel derecho se filtran según la selección y el número de comentarios del panel izquierdo se actualiza en consecuencia.


<img alt="revisar tarea" src="assets/comment-pop-up-panel.png" width="600">


Para obtener más información, consulte *Revisión de temas o mapas* en la guía Uso de guías de Adobe Experience Manager .

### Mejoras de traducción

Ahora tiene mejoras más fáciles de usar en el panel Traducción que le ayudan a traducir fácilmente sus documentos desde el Editor web.


**Columna Etiqueta de versión agregada al panel de traducción**

En el panel de traducción, también puede ver la columna Etiqueta de versión . Se mostrará la etiqueta de la versión seleccionada del archivo de origen. Esto puede ayudarle a seleccionar todos los archivos con una etiqueta específica y traducirlos de una sola vez.

**Ver la diferencia de versión de los archivos fuera de sincronización desde el panel de traducción**

Ahora puede comprobar las diferencias entre la versión seleccionada y la última versión de origen traducida de los temas. También puede optar por traducir la variable **Sin sincronización** archivos basados en los cambios realizados entre las dos versiones de un tema.

<img src="assets/translation-version-diff.png" alt="tarjeta de traducción" width="600">



**Pasar la etiqueta de versión a la versión de destino**

AEM guías le permite pasar la etiqueta del archivo de origen al archivo de destino. Esto le ayuda a identificar fácilmente la versión de origen del archivo traducido.

<img alt="etiquetas de traducción" src="assets/translation-pass-source-label.png" width="600">

Por ejemplo, si tiene algunos archivos de origen con la etiqueta de versión Versión 1.0 aplicada a ellos, también puede pasar la etiqueta de origen (Versión 1.0) al archivo traducido.

**Forzar sincronización para activos fuera de sincronización**

Si realiza cambios en algunos de los recursos, las guías de AEM las marcan como no sincronizadas. Puede volver a traducir los recursos modificados o elegir rechazar el estado de falta de sincronización. Por ejemplo, si ha realizado algunos cambios menores que realmente no necesitan una traducción, puede marcar su estado como In Sync.

**Ver proyectos de traducción en curso para un tema o mapa**

Es posible que algunas de las referencias del panel de traducción estén en curso. Ahora, AEM guías proporciona una función que le ayuda a ver la lista de todos los proyectos de traducción en curso (junto con el idioma de destino) que contienen la referencia seleccionada.

Para obtener más información, consulte *Traducción de documentos desde el Editor Web* en la guía Uso de guías de Adobe Experience Manager .

### Generar salida en varios formatos desde el Editor web

Ahora puede generar fácilmente el resultado para sus temas o mapa DITA desde el Editor web. Puede configurar varios ajustes preestablecidos de salida, como AEM sitio, PDF, HTML5, JSON (un formato de salida sin encabezado) y resultados personalizados. Utilícelos para generar los respectivos resultados. Puede definir atributos en los temas de DITA y, a continuación, utilizar el ajuste preestablecido de condición para aplicar una condición al publicar la salida. También puede utilizar la función Publicación de línea de base para publicar selectivamente una versión específica de su mapa o tema de DITA.

**Administrar ajustes preestablecidos de salida de Perfil de carpetas y global**

AEM guías le proporcionan la función de crear y administrar ajustes preestablecidos de salida para los Perfiles globales y de carpeta. A continuación, puede utilizar fácilmente estos ajustes preestablecidos de salida para generar resultados para todos los mapas relacionados con ese perfil Global o Folder.

<img alt="agregar ajuste preestablecido" src="assets/add-global-output-preset.png" width="400">


Estos ajustes preestablecidos globales aparecen en la sección **Salida** de todos los mapas relacionados. Puede utilizarlos para generar el resultado de todos los mapas relacionados. Puede seleccionar el ajuste preestablecido como ajuste preestablecido de PDF predeterminado para generar la salida del PDF. También puede **Editar**, **Cambiar nombre**, **Duplicar** o **Eliminar** un ajuste preestablecido de salida existente de la variable **Opciones** para abrir el Navegador.

>[!NOTE]
>
>Solo los usuarios administrativos de nivel de carpeta pueden crear ajustes preestablecidos de Perfil global y de carpeta .

### Buscar y reemplazar el texto en el nivel del mapa

Ahora puede buscar archivos dentro de un mapa que contengan texto específico. El texto buscado se resalta en los archivos. También puede reemplazar la palabra o frase buscada con otra palabra o frase dentro de los archivos. Seleccione el **Reemplazar incidencia única** para reemplazar la incidencia actual y la variable **Reemplazar todo en archivo** para reemplazar todas las ocurrencias del archivo seleccionado. Puede seleccionar **Reemplazar todo** para reemplazar todas las ocurrencias del término buscado en todos los archivos.

<img src="assets/map-find-replace.png" alt="buscar reemplazar" width="600">


De forma predeterminada, las opciones **Archivo de cierre de compra antes de reemplazar** y **Crear nueva versión después de reemplazar** están seleccionadas, por lo que se desprotege un archivo antes de reemplazar el texto y se crea una nueva versión después de reemplazar el texto. También puede buscar la cadena en las referencias indirectas dentro del mapa de DITA. De forma predeterminada, esto está desactivado, por lo que la búsqueda se realiza únicamente en las referencias directas.

### Vista Diseño en el Editor de mapas


Ahora puede ver el diseño completo de un mapa DITA en el Editor de mapas. Cuando se abre un mapa para editarlo, se abre la vista Diseño del Editor de mapas. En esta vista, puede ver la jerarquía del mapa en una vista de árbol. También puede editar y organizar o estructurar los temas en un mapa.

<img src="assets/layout-view-map.png" alt=" vista de diseño del mapa" width="600">

La vista Diseño contiene una barra de herramientas independiente que le ayuda a realizar muchas tareas sobre los temas presentes en un mapa.
Puede insertar referencias de temas, grupos de temas y definiciones de claves en un mapa. Puede reorganizar los temas presentes en un mapa moviéndolos hacia arriba, hacia abajo, hacia la izquierda o hacia la derecha. También puede arrastrar y soltar los temas para moverlos en un mapa. El Editor de mapas también proporciona los iconos para bloquear o desbloquear archivos, comprobar el historial de versiones y realizar una administración de etiquetas de versiones.


La vista Diseño también proporciona la variable **Opciones de vista** para mostrar u ocultar el número de línea, mostrar u ocultar la casilla de verificación, o mostrar el nombre o título del archivo para los temas de un mapa.
También puede ver los temas en función de los filtros condicionales aplicados a ellos.

Además de organizar los temas en el archivo de mapa, también puede agregar, mover, copiar, pegar o eliminar referencias utilizando la variable **Opciones** para un elemento en la vista Presentación.

<img src="assets/layout-inline-attributes.png" alt=" atributos de diseño del mapa" width="600">


El panel derecho muestra las Propiedades de contenido y las Propiedades de mapa en la vista Diseño del Editor de mapas. Ahora también puede establecer la información de metadatos para los temas o el mapa. Puede definir el título de navegación, el texto del vínculo, la descripción corta y las palabras clave para el tema o mapa seleccionado.

Para obtener más información, consulte *Vista Diseño* en la guía Uso de guías de Adobe Experience Manager .

### Panel de generación rápida

Ahora, AEM guías proporciona el panel Generación rápida , que le ayuda a generar y ver rápidamente los resultados de los ajustes preestablecidos creados para su mapa DITA.

<img src="assets/quick-generate-map-view.png" alt=" panel generar rápido" width="600">

En el **Generación rápida** , puede ver la lista de todos los ajustes preestablecidos de salida creados para su mapa DITA. También puede ver rápidamente el resultado generado para los ajustes preestablecidos. Se muestra un mensaje de éxito o de error al finalizar la generación de salida. También puede ver el registro de errores que contiene detalles del error que se produjo en el proceso de generación.

### Crear una línea de base dinámica basada en etiquetas

Ahora, AEM guías le proporciona la función de crear líneas de base dinámicas basadas en etiquetas. Si genera una línea de base, descarga una línea de base o crea un proyecto de traducción con una línea de base, los archivos se seleccionan dinámicamente en función de las etiquetas actualizadas. Esta función es útil, ya que no es necesario modificar la línea de base al actualizar las etiquetas.

<img src="assets/dynamic-baseline.png" alt=" línea de base dinámica" width="400">

### Eliminar y duplicar archivos del panel del repositorio

Ahora puede eliminar fácilmente los archivos (un solo archivo a la vez) del **Opciones** del archivo seleccionado desde el panel del repositorio. Se muestra un mensaje de confirmación antes de eliminar el archivo. Si no se hace referencia al archivo desde ningún otro archivo, este se elimina y se muestra un mensaje de éxito.

<img src="assets/options-menu-repo-view-file-level.png" alt="menú de opciones de archivo " width="500">

También puede crear un duplicado o una copia del archivo seleccionado. De forma predeterminada, el archivo se crea con un sufijo (como filename_1.extension).


### Otras mejoras del Editor web

* En AEM guías, puede realizar algunas operaciones comunes para imágenes y archivos multimedia mediante el menú contextual. Ahora también puede localizar la imagen o los medios seleccionados en el repositorio o ver la previsualización del archivo en la interfaz de usuario de Assets.

* El nombre del perfil de carpeta actual se muestra como una etiqueta para el icono Preferencias de usuario en la barra de herramientas principal. Esto le ayuda a identificar el perfil de carpeta en el que está trabajando.

* Cuando se abre un mapa en la vista del mapa, el título del mapa actual se muestra en el centro de la barra de herramientas principal. Esto es útil para informar a los usuarios qué mapa está abierto actualmente.

### Depuración de versiones seleccionadas de archivos

A medida que crea y mantiene el contenido, es posible que se creen muchas versiones para sus archivos DITA en el repositorio. AEM guías le permite depurar versiones anteriores de sus archivos DITA del repositorio y liberar espacio en disco.

<img src="assets/preview-purge-report.png" alt="Previsualizar informe de depuración" width="500">

AEM guías no elimina la primera versión del archivo o una versión que esté incluida en una línea de base, ni se le aplica una etiqueta. La operación de depuración ni siquiera elimina los archivos que se incluyen en una traducción o un flujo de trabajo de revisión. Puede elegir el número de versiones que desea conservar y también decidir eliminar los archivos anteriores al número definido de días.

Antes de iniciar la operación de depuración, puede obtener una vista previa del informe para ver las versiones que se purgarán. A continuación, puede decidir iniciar o cancelar la operación de depuración.

<img src="assets/download-purge-report.png" alt="Informe de depuración de PDdownload" width="500">

Una vez finalizada la operación de depuración, puede consultar el informe de depuración para ver los archivos depurados.

### Ver título en lugar de UUID en el Editor de oxígeno

Ahora AEM guías le permite elegir **Uso del título en el Editor y el Administrador de mapas** en Configuración. Si selecciona esta opción, el título del archivo se muestra en la ficha del archivo cuando se abre en el Editor o en el Administrador de mapas DITA. Si no selecciona esta opción, el UUID del archivo se muestra en la pestaña del archivo.

### IU de metadatos disponible para ajustes preestablecidos de PDF

Puede establecer los metadatos desde el ajuste preestablecido de salida de un mapa DITA. Puede definir los metadatos Título, Autor, Asunto y Palabras clave. Estos metadatos se asignan a los metadatos en las Propiedades del archivo del PDF de salida. Estos metadatos anulan los metadatos definidos a nivel de libro. Puede definir los metadatos específicamente en cada ajuste preestablecido de salida y pasarlos al PDF de salida.

### PDF nativo | PDF con barra de cambios que muestra la diferencia entre las versiones del documento

Ahora puede crear un PDF que muestre las diferencias de contenido entre dos versiones con la barra de cambios. Puede elegir comparar la versión actual con una línea de base de la versión anterior o comparar las dos versiones de línea de base seleccionadas.

<img src="assets/pdf-change-version.png" alt="pdf-change-version" width="600">

Aparece una barra de cambios en el PDF para indicar el contenido modificado, insertado o eliminado. También tiene las opciones para hacer lo siguiente:
* Mostrar el contenido insertado en color verde y subrayado
* Mostrar el contenido eliminado en color rojo y marcado con tachado

### PDF nativo | Compatibilidad de variables para Ruta de salida y nombre de archivo del PDF

Ahora también puede utilizar las siguientes variables predeterminadas para definir la ruta de salida y el archivo de PDF. Puede utilizar una o una combinación de variables para definir estas opciones:
* ${map_filename}
* ${map_title}
* ${preset_name}
* ${language_code}
* ${map_parentpath} (solo para la ruta de salida)
* ${path_after_langfolder} (solo para la ruta de salida)

### PDF nativo | Generar tabla de contenido para mapas DITA y reordenar diseños de página

Ahora también puede generar el TOC en los mapas DITA utilizando una configuración de PDF avanzada de la plantilla. Puede optar por habilitar o deshabilitar la visualización de los distintos diseños de página y también reordenar su posición.

### PDF nativo | Agregar un marcador personalizado en la salida del PDF

Ahora puede agregar un marcador personalizado a un contenido en particular en la salida del PDF final para facilitar la navegación. Esto se agregaría a la tabla de contenido que se crea a partir de los títulos de temas o secciones del mapa DITA.

### PDF nativo | Aplicar estilo personalizado en entradas de TDC y contenido del tema

AEM guías proporciona la función para aplicar estilo personalizado en las entradas de la tabla de contenido o en un tema concreto de la salida del PDF. Por ejemplo, puede cambiar el color del texto en la tabla de contenido y el título del tema. También puede aplicar estilos a todo el contenido dentro del tema.




## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

### Creación

* El panel izquierdo se rompe al añadir una pestaña. (11126)
* Los cambios en el HTML del Editor web causan problemas con `<dl>` y `<dlentry>`. (11024)
* Algunos atributos no se tratan como condicionales y causan problemas. (10895)
* Tres niveles o más anidados `<indexterm>` no están anidados en la exportación de PDF nativo. (10799)
* El contenido desaparece en el cuerpo de una tarea al pasar de la vista Autor a la vista Origen. (10735)
* Los comentarios de revisión no se colocan correctamente en una tarea de revisión. (10625)
* `<conref>` la nota dentro de una etiqueta para no se muestra en el modo de vista previa. (10559)
* Al pulsar Retroceso al final de un elemento de lista, se elimina toda la lista. (10540)
* La pantalla aparece en blanco en Chrome v106 al arrastrar y soltar cualquier elemento de la interfaz de usuario (por ejemplo, en el panel Condiciones ). (10524)
* Falta el botón Sangría automática en la barra de herramientas de la **Fuente** vista. (10448)
* El primer carácter de un elemento de lista se pierde a veces cuando la lista se crea en el editor.( 10447)
* **Deshacer** o **Rehacer** no funciona correctamente en algunos archivos. (10373)
* Los metadatos personalizados no se retienen al copiar y pegar. (10367)
* Se produce un error al realizar una copia (ctrl+c) y pegar (ctrl+v) del contenido. (10304)
* El panel Esquema no muestra el contenido cuando se cambia del modo Autor al Origen. (10296)
* El submapa no se crea cuando hace referencia a un mapa principal en plantillas DITA. (10231)
* Los problemas de navegación se producen en el Editor web después de la actualización a la versión 4.0. (10159)
* La opción Deshacer del Editor XML lleva al usuario a la parte superior de la página. (10091)
* Las propiedades de nodo se eliminan después de copiar y pegar el funcionamiento de un recurso. (10053)
* Los archivos SVG añadidos a los temas DITA no se muestran en el modo de vista previa del editor. (10010)
* Los resultados de búsqueda para buscar y reemplazar dentro del Editor web no se pueden leer en modo Oscuro. (9978)
* No existe ningún cargador al crear un mapa a partir de la plantilla de mapa. (9891)
* La conref en la plantilla de tema no funciona y el ID de hash copiado no se actualiza en la copia de contenido. (9890)
* No se muestra ninguna opción para examinar los temas o la plantilla de asignación dentro de las subcarpetas del tema o de la carpeta de asignación. (9889)
* No hay opción para crear una nueva plantilla en las subcarpetas de temas o mapas. (9888)
* El Editor XML no actualiza las imágenes en los temas. (9500)
* mimeType está codificado para la creación y actualización de recursos DITA. (8979)
* Se inserta un guión normal al seleccionar Guión no separable en la sección **Insertar carácter especial** diálogo. (8919)
* El nombre del creador de versiones en el Historial de versiones es &quot;fmdita-service-user&quot; para los archivos cargados a través de la interfaz de usuario de Assets. (8910)
* La opción Editar no funciona para imágenes mientras se trabaja en la vista Columna de la interfaz de usuario de Assets. (8758)
* El tema de DITA no se actualiza automáticamente con los cambios realizados en **Propiedades** página. (8745)
* Al mover elementos dentro del tema en el Editor web, las ID asignadas a elementos se sobrescriben con las ID asignadas automáticamente. (7895)

### Administración

* Copiar un recurso de mapa DITA (desde la interfaz de usuario de Asset ) provoca líneas de base erróneas en el recurso copiado. (11218)
* El mensaje de advertencia no se muestra en la carga de un archivo que sea mayor que el límite permitido en AEM (2 GB de forma predeterminada). (10817)
* Editor web: línea de base | El comportamiento de la última columna es diferente en el nuevo panel de línea de base del Editor web. (10808)
* Traducción | El trabajo de traducción no se inicia debido a que /libs/fmdita/i18n/ja.json no es válido. (10543)
* Traducción | Se produce un error en un proyecto de traducción de ámbitos creado desde el panel de traducción (Traducción humana). (10526)
* Traducción | El procesamiento posterior está bloqueado para toda la carpeta de idiomas cuyos recursos están presentes en un proyecto de traducción activo. (10332)
* Traducción| Los metadatos y las etiquetas no se propagan a las copias traducidas. (4696)
* Si la versión se cambia y se guarda en el editor de línea de base, aparecen varias ventanas emergentes para cualquier recurso. (10399)
* La fuga de sesión se produce en com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver(QueryBuilderImpl.java:210). (10279)
* Falta el archivo de vídeo en la línea de base si la carpeta principal contiene espacio en el nombre. (10031)

### Publicación

* La regeneración del tema no funciona en algunos escenarios. (10635)
* La publicación del PDF falla al generar el resultado de un ajuste preestablecido duplicado (de un ajuste preestablecido existente). (10584)
* El botón Ver registro no funciona en caso de que falle la generación del PDF para un ajuste preestablecido. (10576)
* Publishlistener no muestra los datos solicitados en los registros de información y también contiene algunos registros no deseados.( 10567)
* PDF nativo | La generación del PDF falla con una excepción de puntero nulo. (10950)
* PDF nativo | conkeyref no se está resolviendo en la salida generada. (10564)
* PDF nativo | Los problemas se producen con los metadatos de un mapa al que se debe hacer referencia en la salida del PDF.( 10556)
* PDF nativo | Se producen problemas al girar el encabezado Tabla. (10555)
* PDF nativo | Se producen problemas al eliminar temas que tienen una función de procesamiento=&#39;solo recurso&#39;. (10554)
* PDF nativo | Las claves vacías se muestran en la salida del PDF. (10553)
* PDF nativo | Anidado `<indexterm>` no están anidados en la exportación de PDF nativo. (10521)
* PDF nativo | El PDF nativo utiliza el estilo en línea en lugar del nombre de clase para las etiquetas generadas. (10498)
* PDF nativo | El topicref anidado en los apéndices se transforma en h1 en el HTML temporal.( 10454)
* PDF nativo | No se pueden ocultar los temas principales de la Tabla de contenido. (10355)
* PDF nativo | El atributo de marco de tabla no se propaga al HTML temporal (como clase). (10353)
* PDF nativo | Los archivos HTML temporales añaden las clases de colección y fila a <td> y <th> incluso si su valor es 0 en la DITA de origen. (10352)
* PDF nativo | El reinicio de los números de página en el diseño del capítulo comienza aleatoriamente a partir del final del capítulo anterior. (10154)
* PDF nativo | Las referencias clave para keydefs con vínculos de imagen o externos no se resuelven. (10063)
* PDF nativo | El apéndice se muestra como un capítulo en el PDF generado. (9829)
* La ficha Plantilla del editor xml no se muestra en los administradores de perfil de carpeta. (10266)
* La publicación de línea de base falla para el PDF generado con FrameMaker Publishing Server 2020. (10551)
* El error de la aplicación se produce al hacer clic en el botón Editar después de seleccionar todos los ajustes preestablecidos mediante la casilla de verificación Ajustes preestablecidos de salida en la ventana emergente Generación rápida . (10388)
* Si la ficha Salida del Editor web tiene más ajustes preestablecidos, la sección de ajustes preestablecidos no se puede desplazar verticalmente y no muestra todos los ajustes preestablecidos disponibles. (9787)
* No se pueden eliminar los ajustes preestablecidos del flujo de trabajo de salida al publicar mediante Editor. (9100)
* El vínculo del mismo nivel se representa como texto normal en lugar de como un vínculo en la página generada. (7774)

### Problema conocido

Adobe ha identificado el siguiente problema conocido para AEM versión 4.2 de las guías:

* Los usuarios pueden realizar operaciones de revisión incluso después de completar la tarea de revisión.
