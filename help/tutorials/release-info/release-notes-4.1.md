---
title: Notas de la versión | Versión de las guías de Adobe Experience Manager 4.1
description: Última versión de las guías de Adobe Experience Manager
exl-id: c70b3bbc-3332-4626-bc30-641034f8fd06
source-git-commit: f74126c1eb7bccf0c9464cbe9b1138af5bd4938f
workflow-type: tm+mt
source-wordcount: '3275'
ht-degree: 3%

---

# Versión 4.1.x de las guías de Adobe Experience Manager

En estas notas de la versión se tratan las instrucciones de actualización, las nuevas funciones y las mejoras de la versión 4.1.x de las guías de Adobe Experience Manager (más adelante, las *Guías AEM*).

## Actualice a la última versión

Puede actualizar fácilmente su versión actual de AEM guías a la versión 4.1.2. Antes de continuar con la actualización a la versión 4.1.2 de las guías AEM, debe tener en cuenta los siguientes puntos:
* Si utiliza la versión 4.1 o 4.1.x, puede actualizar directamente a la versión 4.1.2.
* Si utiliza la versión 4.0.x, deberá actualizar a la versión 4.1 o 4.1.x antes de actualizar a la versión 4.1.2.
* Si utiliza la versión 3.8.5, deberá actualizar a la versión 4.0.x antes de actualizar a la versión 4.1.
* Si está en una versión anterior a la 3.8.5, consulte la sección actualización en la guía de instalación específica del producto.

Para obtener más información, consulte [Instrucciones de actualización](assets/Adobe-Experience-Manager-Guides-Upgrade-Instructions-EN.pdf).

## 4.1.2 | Notas de la versión

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software compatibles con AEM versión 4.1.2 de las guías.

### Adobe Experience Manager

**No UUID**
Versión 6.5 Service Pack 13, 12, 11 o 10

**UUID**
Versión 6.5 Service Pack 13, 12, 11 o 10

Para obtener más información, consulte la sección Requisitos técnicos en la guía Instalar y configurar guías de Adobe Experience Manager .


### FrameMaker y FrameMaker Publishing Server

| Edición | FMPS 2020 | FMPS 2019 | Fm 2020 | Fm 2019 |
| --- | --- | --- | --- | --- |
| 4.1.2 (no UUID) | 2020.2 o posterior* | 2019 | 2020.3 o superior | 2019.8 (última actualización) |
| 4.1.2 (UUID) | 2020.2 o posterior* | No compatible | 2020.4 o superior | No compatible |
|  |  |  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

### Conector de oxígeno

| Edición | Ventanas del conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.1.2 (no UUID) | 2,0 | 2,0 | 1,6 | 1,6 |
| 4.1.2 (UUID) | 2.7 | 2,7 | 2.3 | 2,3 |
|  |  |  |


## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* Al seleccionar todos los perfiles de carpeta, aparece un perfil de carpeta invisible (que es incorrecto). (10393)
* La creación de la línea de base no elige la versión más reciente, cuando la zona horaria del usuario es diferente de la del servidor. (10336)
* El método abreviado Control+F no abre el modo de búsqueda del explorador en la consola Recursos después de la instalación de AEM guías 4.1. (10339)
* Se produce un error de creación de línea de base para el tema que tiene la referencia a una carpeta. (10383)
* La pestaña Ajustes preestablecidos de salida muestra una pantalla en blanco de forma intermitente y, en algunos casos, se muestran ajustes preestablecidos no editables. (10390)
* La administración de espacios clave está generando excepciones y errores. (10449)

### Problemas conocidos con la solución alternativa

* La línea de base exportada durante la traducción no se carga en la pestaña de línea de base del editor.

   **Solución alternativa**: Utilice la pestaña de línea de base del panel de asignación DITA.

## 4,1 | Notas de la versión

En estas notas de la versión se tratan las instrucciones de actualización, las nuevas funciones y las mejoras de la versión 4.1.x de las guías de Adobe Experience Manager (más adelante, las *Guías AEM*).

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software compatibles con AEM versión 4.1 de las guías.

### Adobe Experience Manager

**No UUID**
Versión 6.5 Service Pack 13, 12, 10 o 11

**UUID**
Versión 6.5 Service Pack 13, 12, 10 o 11

Para obtener más información, consulte la sección Requisitos técnicos en la guía Instalar y configurar guías de Adobe Experience Manager .




### FrameMaker y FrameMaker Publishing Server

| Edición | FMPS 2020 | FMPS 2019 | Fm 2020 | Fm 2019 |
| --- | --- | --- | --- | --- |
| 4.1 (no UUID) | 2020.2 o posterior* | 2019 | 2020.3 o superior | 2019.8 (última actualización) |
| 4.1 (UUID) | 2020.2 o posterior* | No compatible | 2020.4 o superior | No compatible |
|  |  |  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

### Conector de oxígeno

| Edición | Ventanas del conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.1 (no UUID) | 2,0 | 2,0 | 1,6 | 1,6 |
| 4.1 (UUID) | 2,7 | 2,7 | 2,3 | 2,3 |
|  |  |  |


## Nuevas funciones y mejoras

AEM guías proporciona muchas mejoras y nuevas funciones en la versión 4.1:

### Editor web mejorado

* **Resolución de clave mejorada**

Una referencia de clave de contenido DITA inserta una parte del contenido de un tema en otro. Utiliza una clave para localizar el contenido. Es necesario resolver las referencias clave asociadas a un tema DITA. El mapa raíz seleccionado tiene la prioridad más alta para resolver las referencias clave.

![cuadro de diálogo preferencias de usuario](assets/user-preferences.png)

Ahora las referencias clave se resuelven sobre la base del mapa raíz configurado en el siguiente orden de prioridad:

1. Preferencias de usuario
2. Panel Vista Mapa
3. Perfil de carpeta

Para obtener más información, consulte *Resolución de referencias clave* en la guía Uso de guías de Adobe Experience Manager .

* **Agregar un panel personalizado en el panel izquierdo**

Ahora puede agregar un panel personalizado en el panel izquierdo del Editor web. Puede utilizar un panel personalizado para varios fines, como proporcionar ayuda o realizar pruebas en un proyecto. Si se ha configurado un panel personalizado, también aparece en la lista de paneles dentro del **Configuración del editor**. Puede alternar el conmutador para mostrar u ocultar el panel personalizado.

* **Posibilidad de cambiar el estado del documento de los temas en un mapa DITA**

Ahora puede cambiar fácilmente el estado del documento de temas seleccionados dentro de un mapa DITA. También puede abrir y editar las propiedades de los temas seleccionados en un mapa DITA desde el **Más opciones** en la parte inferior del panel Vista de mapa .

![propiedades de tema seleccionadas](assets/map-view-properties.png)

* **Información de la versión mostrada en el modo de vista previa**

El Editor web le ayuda a administrar sus versiones. Ahora también puede ver la versión del tema activo o del mapa DITA en la esquina superior derecha de la ficha del tema en el modo de vista previa de un tema.

![versión de vista previa](assets/preview-version.png)


* **Comportamiento de actualización del Editor web mejorado**

Ahora están disponibles las siguientes mejoras con la operación de actualización del explorador en el Editor web:

* Ahora obtendrá asistencia para actualizar el navegador mientras edita el contenido en el Editor web. Si pulsa el icono de actualización del explorador mientras se abren para editar uno o varios archivos con cambios no guardados, se le pedirá que guarde los archivos o cancele la acción de actualización.

* Incluso al actualizar el navegador, se conservan las vistas del panel izquierdo y del panel derecho.

* El tema activo o el mapa DITA se vuelve a abrir en el área de edición de contenido.

* **Crear mapas basados en plantillas personalizadas**

Ahora obtiene la potente función para crear plantillas de mapa personalizadas. Puede utilizarlos para crear mapas DITA junto con las plantillas de tema y las plantillas de asignación a las que se hace referencia en la plantilla de asignación.

![plantillas de datos](assets/dita-templates.png)

También puede consultar otras plantillas de asignación y plantillas de tema desde la plantilla de asignación personalizada. Las plantillas de mapa a las que se hace referencia pueden hacer referencia a varias plantillas de mapa, plantillas de temas, temas, mapas, imágenes, vídeos y otros recursos.

![crear plantillas de datos](assets/create-dita-template.png)

La plantilla de mapa personalizada puede ayudarle a replicar fácilmente las plantillas de mapa y toda la estructura de carpetas referida. Estas plantillas personalizadas son especialmente útiles para crear y recrear múltiples mapas que tienen estructuras y referencias recursivas.

* **Compatibilidad con schematron**
&quot;Esquatrón&quot; se refiere a un lenguaje de validación basado en reglas que se utiliza para definir pruebas para un archivo XML. Con un archivo de Esquatrón puede definir ciertas reglas y después validarlas para un tema DITA o un mapa. El editor web es compatible con los archivos de esquema. Puede importar los archivos de Esquema y editarlos también en el Editor web. La compatibilidad con Esquemas en el Editor web ayuda a validar los archivos con un conjunto de reglas y a mantener la coherencia y la exactitud en los temas.

![validar esquema](assets/schematron-validate.png)

* **Cuadro de diálogo mejorado en el cierre de archivos**

AEM guías le pedirá que guarde los cambios y que desbloquee los archivos bloqueados cuando intente cerrar un archivo abierto en el Editor web. Los mensajes se muestran en función de la variable **Solicitar el registro de entrada al cerrar** y **Solicitar una nueva versión al cerrar** configuración del administrador.

Según la configuración, tiene la opción de guardar los cambios y crear una nueva versión del documento. O bien, también puede proteger el archivo y guardar los cambios en la versión actual.

![Cierre de archivos](assets/file-close-save-changes-unlock.png)

Para obtener más información, consulte *Situaciones de cierre y guardado de archivos* en la guía Uso de guías de Adobe Experience Manager .* El **Insertar palabra clave** se ha mejorado. Ahora puede encontrar más fácilmente una palabra clave para insertarla, ya que las palabras clave se enumeran en orden alfabético. También puede buscar palabras clave escribiendo una cadena de búsqueda en el cuadro Buscar.

![insertar palabra clave](assets/insert-keyword.png)

* **Compatibilidad con documentos Markdown**
Markdown es un lenguaje de marcado ligero que puede ayudarle a agregar elementos de formato a documentos de texto sin formato. El Editor web permite utilizar documentos Markdown (.md) junto con documentos DITA. Puede crear y previsualizar fácilmente un documento Markdown en el Editor web y también agregarlo en el archivo de mapa a través del editor de mapas DITA.  Para obtener más información, consulte 
*Creación de documentos Markdown desde el Editor web* en la guía Uso de guías de Adobe Experience Manager .

![markdown de soporte](assets/create-markdown-dita-topic.png)

* **Capacidad para configurar una vista de etiquetas predeterminada**
Si un usuario habilita la Vista de etiquetas desde el Editor web, permanecerá habilitada incluso en las sesiones.  Esto significa que no tiene que volver a habilitar la vista de etiquetas para acceder a ella más adelante. El administrador puede configurar el estado predeterminado de la vista de etiquetas en el Editor web. El valor predeterminado de la vista de etiquetas para la sesión de un nuevo usuario viene determinado por la propiedad tagsView del archivo ui_config.json.

* Ahora, en la vista del repositorio, los archivos se cargan en lotes. Todos los archivos presentes en el principal o `/content/dam folder` se muestran. Pero desde el siguiente nivel o la carpeta secundaria se cargan 75 archivos a la vez. Esta carga por lotes es eficiente y puede acceder a los archivos más rápido en comparación con la carga de todos los archivos existentes en una carpeta.

![cargar más archivos](assets/load-more-files.png)

### Nuevo panel de línea de base

AEM versión 4.1 de las guías proporciona la función de línea de base integrada en el Editor web. Ahora puede crear líneas de base desde el Editor web y utilizarlas para publicar o traducir temas de distintas versiones.

**Nota**: Para actualizar el sistema, actualice la última **ui_config.json** para Perfil de carpeta.

Utilice esta función para crear una línea de base con una versión específica de los temas disponibles en una fecha y hora específicas. Además, se ofrece compatibilidad con la API para crear o actualizar una línea de base con una etiqueta definida para una versión de los temas.

![ficha de gestión de línea de base](assets/baseline-manage.png)

Puede buscar en los archivos en función de sus nombres o ubicación. También puede filtrar los temas que desea mostrar en la ventana de edición de la línea base y ordenarlos en función de columnas específicas.

![ficha de gestión de línea de base](assets/baseline-filter.png)

Se ha seguido mejorando el rendimiento del proceso de creación de la línea de base. El proceso para crear líneas de base es asíncrono, por lo que puede seguir editando otros archivos en el Editor web mientras se crea la línea de base. Para obtener más información, consulte *Crear y administrar líneas de base desde el Editor web* en la guía Uso de guías de Adobe Experience Manager .

Nota: La pestaña Línea de base en el panel del mapa está oculta de forma predeterminada. El administrador puede activar la ficha Línea de base en el panel de asignación.

* El parámetro de línea de base en las API para descargar mapa ahora utiliza el título de la línea de base para recuperar el contenido con versiones.

### Proceso de traducción mejorado

* **Capacidad para crear un proyecto de traducción de ámbitos**
Si necesita crear solo el ámbito para traducir un proyecto, puede seleccionar 
**Crear un nuevo proyecto de traducción de ámbitos**. Esto no enviará las copias para su traducción y se mantiene el estado de traducción original de los archivos.

![proyecto de traducción de creación de ámbitos](assets/scoping-translation-project.png)

* La variable **Idiomas** muestra las carpetas de idioma junto con sus códigos de idioma. Por ejemplo, francés (fr) y alemán (de).

![idioma de traducción](assets/translation-languages.png)

Para obtener más información sobre la traducción, consulte *Traducción de documentos desde el Editor Web* en la guía Uso de guías de Adobe Experience Manager .


### Publicación mejorada

* También puede acceder al **Publicar tablero** en la pestaña Outputs mientras genera la salida desde el panel de mapas. En el panel Publicar encontrará una lista de todas las tareas de publicación activas.

![resultados en cola](assets/queued-output.png)

* Desde el panel de mapas puede seleccionar varios archivos DITAVAL para generar contenido condicional. Puede mantener el orden de los archivos añadiendo o eliminando archivos. También puede pasar el ratón sobre el nombre del archivo para ver la ruta en el repositorio de AEM donde se almacena el archivo.

* Se han respetado las líneas de base para los metadatos de AEM salida del sitio. También puede procesar las propiedades de una versión de línea de base como metadatos. Si no se define ninguna línea de base, las propiedades de la última versión se procesan como metadatos.

* La variable **Nombre del archivo** y **Argumentos de la línea de comandos DITA-OT** se han añadido opciones para los ajustes preestablecidos de salida HTML5, EPUB y Personalizado. Ahora puede especificar el nombre del archivo con el que desea guardar la salida. También puede especificar los argumentos adicionales que desea que procese DITA-OT durante la generación de resultados.

### Mapa del tablero

Cuando selecciona descargar el mapa DITA, la solicitud se pone en cola y recibe una notificación una vez que el mapa está listo para descargarse. Puede elegir descargar el archivo de mapa inmediatamente o descargarlo más tarde desde el vínculo proporcionado en la bandeja de entrada de notificaciones de AEM.

![Descarga de mapas](assets/download-map-prompt.png)

### Otras mejoras de las funciones

* AEM guías ahora es compatible con Oxygen XML Author versión 24.1.
* El parámetro de línea de base en las API para descargar mapa ahora utiliza el título de la línea de base para recuperar el contenido con versiones.

### Función obsoleta

AEM guías ya no admite la generación del formato de salida DITA para documentos FrameMaker. Esta opción DITA también se ha eliminado de los ajustes preestablecidos de salida del panel Mapa.

## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* La compatibilidad con la creación no está disponible como alternativa para las referencias basadas en rutas de archivos para la publicación. (8076)
* DITA Add on package evita la detección de activos duplicados DAM. (8417)
* Después de registrar un documento de Oxygen a AEM, el contenido japonés del documento se reemplaza por signos de interrogación (????). (9124)
* La actualización de los archivos desprotegidos no funciona en el registro con autenticación web en Oxygen. (9179)
* El archivo no se extrae cuando se abre en Oxygen. (9192)
* Después de registrar un documento de Oxygen a AEM, el contenido japonés del documento se reemplaza por signos de interrogación (????). (9276)
* La autenticación web no funciona en Oxygen. (9296)
* La recarga falla en Oxygen cuando los archivos ya existen en AEM en la misma ubicación. (9328)
* La opción no está disponible para sincronizar contenido de forma forzada entre AEM y el sistema local. (9439)
* El ID no se genera automáticamente para el elemento añadido mediante **Insertar contenido reutilizable** de la barra de herramientas secundaria. (5826)
* No se muestra ningún cuadro de diálogo de confirmación al cargar una imagen con el mismo nombre que un archivo existente, a través del editor. (6011)
* Un espacio de no separación no disponible en la paleta de caracteres. (7523)
* La lista de elementos (Alt+Intro) aparece atenuada en el tema oscuro/más oscuro. (7913)
* La versión no se actualiza al guardar la revisión de un tema desde la barra de herramientas del panel de asignación. (8228)
* xref no se puede insertar ni siquiera en ubicaciones válidas. (8354)
* La operación &#39;getversionlabels&#39; tiene limitaciones y no proporciona el rendimiento esperado. (8513)
* Los problemas se producen con el cuadro de diálogo de confirmación al cerrar un archivo bloqueado o editado que no se abre actualmente en el editor. (8692)
* Se produce un error al añadir un usuario como administrador en el perfil de carpetas cuando el ID de usuario es numérico. (8908)
* El panel Traducción está visible incluso al abrir el mapa DITA en el Editor de mapas. (9053)
* El código de idioma no se muestra con el idioma en el panel Traducción . (9108)
* Las pestañas Traducción y Línea de base están visibles durante algún tiempo en el panel Mapa. (9146)
* Cuando la traducción termina, se crea una versión adicional para el recurso traducido. (9310)
* La traducción aprobada no se integra en el idioma de destino cuando el código de idioma de destino contiene cinco caracteres como `fr_ca`. (9357)
* El contenido traducido se rompe cuando el código de idioma de destino creado se menciona como `fr-fr, `, `en-us`. (9527)
* Al cargar un mapa DITA que está fuera de la carpeta del idioma, se registra una excepción en el servidor.(9543)
* No se puede crear el archivo DITA utilizando la plantilla DITA personalizada del editor. (7262)
* El mapa DITA se pierde al publicar un mapa UUID DITA a través de FMPS. (7278)
* AEM guías no copia las propiedades no únicas de un recurso cuando se copia y se pega un recurso. (8241)
* El nombre de archivo del mapa DITA no se convierte a minúsculas en la creación. (8383)
* La descripción de la tarea de revisión no aparece en la notificación por correo electrónico que se envía cuando se asigna una nueva tarea de revisión. (8507)
* Descargar API de asignación | Las carpetas temporales no se limpian en caso de que se produzcan errores en el proceso de descarga. (8523)
* `columnpreview.jsp` depende de SP.  (8543)
* Los trabajos de salida con estado &quot;En espera&quot; o &quot;En ejecución&quot; no se limpian en el panel de publicación.  (8569)
* Icono predeterminado seleccionado al generar un informe mediante el botón Generar , incluso cuando se define la propiedad icon . (8573)
* Se producen problemas en el proceso de revisión al actualizar de 3.8.X a 4.0. (8788)
* En el panel Revisión del Editor web, si un nombre de usuario es largo, los iconos para aceptar/rechazar no se muestran claramente. (8793)
* El árbol de referencia se rompe tras eliminar un tema y realizar una operación de movimiento. (8804)
* El DTD personalizado definido por el usuario no tiene prioridad sobre el DTD DITA estándar incrustado en DITA-OT. (9104)
* La posición del resaltado es incorrecta en la vista en paralelo. (9305)
* La nota al pie de página de uso por referencia no se desplaza a la sección de notas al pie de AEM salida del sitio. (9061)
* El orden de las notas al pie es incorrecto en la salida AEM del sitio. (9327)
* Los recursos DITA recién creados siempre los desprotege otro usuario. (9387)
* El error siempre se registra en la creación de contenido nuevo. (9388)
* La tercera pantalla del proceso de creación de la tarea de revisión no muestra la lista de glosarios. (4558)
* Referencias UUID incorrectas asignadas al cargar varios archivos desde el conector FrameMaker/Oxygen. (8269)
* La notificación por correo electrónico no se envía cuando se vuelve a asignar una tarea de revisión en la Bandeja de entrada. (8376)
* El segundo usuario administrador no se puede agregar como el primer usuario administrador a una carpeta. (8430)
* **Aplicar etiquetas** en la ficha Línea de base no muestra etiquetas en la lista desplegable. (8455)
* Al usar la publicación de línea de base con imagen como referencia en el tema, la imagen no se publica en la salida. (8564)
* La función de depuración de salida falla si hay un gran número de nodos del historial de salida sobrantes presentes. (8568)
* En el panel del historial de versiones, la sección de la versión actual muestra una marca de tiempo incorrecta y la información la modifica. (8765)
* La línea de base no se actualiza en función de la etiqueta definida. (8799)
* El error se produce cuando los archivos cuya carpeta principal tiene caracteres especiales en el nombre del archivo se abren en Oxygen (utilizando la variable **Editar en oxígeno** ). (8918)
* La carga de archivos desde Oxygen a AEM falla. (9157)
* El mapa de descarga con la línea de base no funciona si el contenido se mueve a otra carpeta. (9331)
* Oxygen comprueba una versión incorrecta de un tema después de que una versión vuelva a aparecer en AEM. (9411)
* La búsqueda en el panel Repositorio y el cuadro de diálogo de exploración de referencia tope bloquea la pantalla cuando el contenido es grande. (9432)
* Si la configuración **Crear nueva versión para el archivo cargado** está activada, se crea una nueva versión al revertir y guardar en cualquier nodo congelado. (9473)
* En la interfaz de usuario de Assets se muestran diferencias incorrectas en la marca de tiempo al revertir una versión de archivo. (9480)
* Los archivos se desprotegen automáticamente al revertir a cualquier versión. (9482)
* El icono Bloquear se muestra en la vista del repositorio incluso cuando el archivo se protege desde el editor.  (5756)
* No se pueden agregar elementos de materia principal y de materia secundaria en un mapa de libros mediante la vista Autor del Editor web. (7652)
* El modo de Vista previa no es compatible `deliveryTarget` atributo de procesamiento condicional en DITA. (7685)
* Al abrir un tema del glosario en el editor XML, AEM obliga a guardarlo aunque no se haya modificado. (8105)
* El cuadro de diálogo Insertar referencias se abre al añadir el asunto ref a un mapa mediante la interfaz de usuario. (8212)
* Reutilizar el panel de contenido se bloquea al buscar caracteres especiales `[` o `*` .(8279)
* Al crear Glossentry, el Editor web muestra el contenido como una nota. (8384)
* El Editor XML elimina la nueva línea del bloque de código. (8522)
* El cambio entre el modo de origen y de autor marca el tema como sucio y requiere que el contenido se guarde de nuevo.(8524)
* No se puede cerrar un tema desbloqueado. (8545)
* No existe ninguna opción para elegir la ruta de la base de conocimiento en los ajustes preestablecidos de publicación basados en artículos. (8636)
* Faltan atributos al añadir un capítulo a un mapa de marcadores mediante Arrastrar y soltar desde la vista Favoritos. (8746)
* El cuadro de diálogo Insertar palabra clave no tiene la capacidad de búsqueda y las palabras clave no se enumeran en orden ordenado. (9094)
* Al realizar una búsqueda en el Editor XML, la página se bloquea. (9452)
* Faltan sitios en AEM ajustes preestablecidos en la ficha Salida . (9567)
* Las imágenes de SVG que no se representan correctamente en los modos de autor del Editor XML. (9426)
* No se respeta la línea de base al publicar mediante salesforce. (8953)
* No está presente la capacidad para borrar la asignación de ruta de la configuración de preferencias de usuario. (8534)
