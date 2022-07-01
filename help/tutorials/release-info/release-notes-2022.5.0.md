---
title: Notas de la versión | Guías de Adobe Experience Manager as a Cloud Service, versión de mayo de 2022
description: Última versión de las guías de Adobe Experience Manager as a Cloud Service
exl-id: 7928a300-5ec9-492c-b9be-02b6f87638c6
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '1874'
ht-degree: 4%

---

# Última versión de las guías de Adobe Experience Manager as a Cloud Service

## Actualice a la última versión

Actualice las guías actuales de Adobe Experience Manager as a Cloud Service (más adelante, *Guías AEM as a Cloud Service*) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2022.5.144.
3. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la última versión de AEM guías as a Cloud Service.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por AEM Guías as a Cloud Service de la versión de mayo de 2022.

### FrameMaker y FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| No compatible | Actualización 4 y posterior de 2020 |
|  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

### Conector de oxígeno

| AEM guías como una versión en la nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac |
| --- | --- | --- |
| 2022.5.0 | 2.6.9 | 2.6.9 |
|  |  |  |


## Nuevas funciones y mejoras

AEM guías as a Cloud Service proporciona muchas mejoras y nuevas funciones en la última versión:

### Editor web mejorado

* **Crear mapas basados en plantillas personalizadas**

Ahora obtiene la potente función para crear plantillas de mapa personalizadas. Puede utilizarlos para crear mapas DITA junto con las plantillas de tema y las plantillas de asignación a las que se hace referencia en la plantilla de asignación.

![plantillas de datos](assets/dita-templates.png)

También puede consultar otras plantillas de asignación y plantillas de tema desde la plantilla de asignación personalizada. Las plantillas de mapa a las que se hace referencia pueden hacer referencia a varias plantillas de mapa, plantillas de temas, temas, mapas, imágenes, vídeos y otros recursos.

![crear plantillas de datos](assets/create-dita-template.png)

La plantilla de mapa personalizada puede ayudarle a replicar fácilmente las plantillas de mapa y toda la estructura de carpetas referida. Estas plantillas personalizadas son especialmente útiles para crear y recrear múltiples mapas que tienen estructuras y referencias recursivas.

* La variable **Insertar palabra clave** se ha mejorado. Ahora puede encontrar más fácilmente una palabra clave para insertarla, ya que las palabras clave se enumeran en orden alfabético. También puede buscar palabras clave escribiendo una cadena de búsqueda en el cuadro Buscar.

![insertar palabra clave](assets/insert-keyword.png)

* Ahora, en la vista del repositorio, los archivos se cargan en lotes. Se cargan 75 archivos a la vez. Esta carga por lotes es eficiente y puede acceder a los archivos más rápido en comparación con la carga de todos los archivos existentes en una carpeta.

![cargar más archivos](assets/load-more-files.png)

* Puede procesar imágenes SVG que incluyan datos incrustados o vínculos en todas las pantallas del editor XML, incluidas, entre otras, la vista previa y la vista del autor.

* El XSD/DTD predeterminado se puede actualizar a la última versión

### Proceso de traducción mejorado

* **Capacidad para crear un proyecto de traducción de ámbitos**
Si necesita crear solo el ámbito para traducir un proyecto, puede seleccionar 
**Crear un nuevo proyecto de traducción de ámbitos**. Esto no enviará las copias para su traducción y se mantiene el estado de traducción original de los archivos.

![proyecto de traducción de creación de ámbitos](assets/scoping-translation-project.png)

* Si rechaza la traducción de uno o más temas de un trabajo de traducción, el estado de traducción en curso de todos los temas rechazados vuelve a su estado original.

* La variable **Idiomas** muestra las carpetas de idioma junto con sus códigos de idioma. Por ejemplo, francés (fr) y alemán (de).

* La función de traducción ahora también admite el código de idioma que incluye el país y el idioma. Por ejemplo, `fr-fr`, `en-us`.

![idioma de traducción](assets/translation-languages.png)

* Al cargar un mapa DITA que está fuera de la carpeta del idioma, no se registra ninguna excepción en el servidor.

Para obtener más información sobre la traducción, consulte *Traducción de documentos desde el Editor Web* en Uso de las guías de Adobe Experience Manager as a Cloud Service.


### Publicación mejorada

* También puede acceder al **Publicar tablero** en la pestaña Outputs mientras genera la salida desde el panel de mapas. En el panel Publicar encontrará una lista de todas las tareas de publicación activas.

![resultados en cola](assets/queued-output.png)

* Desde el panel de mapas puede seleccionar varios archivos DITAVAL para generar contenido condicional. Puede mantener el orden de los archivos añadiendo o eliminando archivos. También puede pasar el ratón sobre el nombre del archivo para ver la ruta en el repositorio de AEM donde se almacena el archivo.

* **Función obsoleta**
AEM as a Cloud Service ya no admite la generación del formato de salida DITA para documentos FrameMaker. Esta opción DITA también se ha eliminado de los ajustes preestablecidos de salida del panel Mapa.

### Publicación basada en artículos mejorada

El Editor XML permite asignar más de una categoría de producto a un artículo mientras se publica en un perfil de Salesforce.

### Otras mejoras de las funciones

* El modo de vista previa también es compatible `deliveryTarget` atributo de procesamiento condicional en DITA. Está disponible como opción en el filtro desplegable junto con **audiencia**, **platform**, **producto**, props, **otherprops**.
* Se ha proporcionado la opción de sincronización forzada entre el servidor de AEM en Oxygen y el sistema local.

## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* En el panel de revisión del Editor web, el usuario no puede responder a los comentarios de revisión. (9667)
* La aplicación se queda en blanco al hacer clic en una carpeta en blanco después de actualizarla mediante el menú Opciones . (9639)
* Se está creando una nueva versión cuando **Guardar y cerrar** el archivo registrado. (9638)
* El botón Cerrar no se muestra cuando **Guardar como nueva versión** está activada. (9637)
* El PDF correcto no se publica si primero se publica mediante un PDF independiente para cada capítulo y, a continuación, un archivo de PDF único (la opción Crear archivos de PDF independientes está desactivada). (9632)
* El tablero de mapa está arrojando un problema de metadatos para los usuarios que no son administradores. (9620)
* Una vez creada una línea de base, el estado se establece en failed en la interfaz de usuario (la llamada get status está fallando) si el servidor tiene más de 10 000 archivos. (9608)
* El almacenamiento de datos grandes en propiedades provoca un error de publicación, ya que falla el flujo de trabajo de publicación dividido. (9586)
* El estado de los filtros de atributos condicionales no se conserva al cambiar entre la vista previa y el modo de vista previa. (9553)
* El nombre del mapa de marcadores se queda en blanco en la vista Repositorio en caso de que no se proporcione ningún nombre a través del `mainbooktitle` etiqueta. (9538)
* El error HTTP 400 se produce al abrir un archivo cargado con Oxygen. (9535)
* Los ajustes preestablecidos de un mapa abierto anteriormente permanecen visibles en la pestaña Salida al abrir un mapa sin ajustes preestablecidos definidos. (9523)
* La funcionalidad de búsqueda de Etiquetas y atributos no funciona en el panel Esquema. (9506)
* La colección recién creada no estará visible hasta que el explorador se actualice. (9505)
* Las etiquetas de Atributos condicionales (no los valores) aparecen en el modo de origen al añadir todas las condiciones mediante la opción &quot;Añadir todas las props&quot;. (9501)
* Los archivos se desprotegen automáticamente al revertir a cualquier versión. (9482)
* En la interfaz de usuario de Assets se muestran diferencias incorrectas en la marca de tiempo al revertir una versión de archivo. (9480)
* Se agregan varios elementos de los resultados de búsqueda al insertar elementos en el elemento topicref del mapa DITA. (9474)
* Si la configuración **Crear nueva versión para el archivo cargado** está activada, se crea una nueva versión al revertir y guardar en cualquier nodo congelado. (9473)
* El texto de visualización de Referencia clave y Referencia clave de contenido no se mantiene al cambiar la dirección URL del vínculo si no se agrega el texto de visualización al definir la referencia clave. (9458)
* En el Historial de versiones, el número de versión y la etiqueta no se muestran para la versión actual. (9446)
* El editor se bloquea cuando se abren ciertos archivos de contenido en el editor. (9443)
* La búsqueda en el panel Repositorio y el cuadro de diálogo de exploración de referencia tope bloquea la pantalla cuando el contenido es grande. (9432)
* Los metadatos que se pasan a AEM salida del sitio no respetan la línea de base del contenido. (9416)
* Oxygen comprueba una versión incorrecta de un tema después de que una versión vuelva a aparecer en AEM. (9411)
* La línea de base fallida deshabilita la edición en la ficha Ajuste preestablecido del panel de asignación. (9403)
* El error siempre se registra en la creación de contenido nuevo. (9388)
* Los recursos DITA recién creados siempre los desprotege otro usuario. (9387)
* Cambiar el nombre del elemento no funciona correctamente al convertir topicref a glossref. (9380)
* La etiqueta de versión no aparece como lista desplegable en **Guardar como nueva versión** diálogo. (9379)
* Las condiciones no se aplican al cambiar entre versiones diferentes de **Mostrar diferencia** lista desplegable. (9366)
* Se producen varios problemas al usar los filtros de vista previa. (9365)
* No se pueden insertar recursos que no sean DITA y DITAVAL en topicref. (9363)
* La traducción aprobada no se integra en el idioma de destino cuando el código de idioma de destino contiene cinco caracteres como `fr_ca`. (9357)
* No se pueden buscar archivos utilizando **Buscar archivos en la carpeta** de la variable **Más opciones** y la aplicación deja de responder. (9337)
* El cuadro de diálogo Examinar se bloquea si hay un gran número de claves presentes. (9332)
* Los archivos DITAVAL no funcionan al publicar artículos. (9330)
* El orden de las notas al pie es incorrecto en la salida AEM del sitio. (9327)
* La búsqueda no se realiza automáticamente cuando se cambia la ruta de acceso seleccionada. (9323)
* Cuando la traducción termina, se crea una versión adicional para el recurso traducido. (9310)
* No se pueden eliminar los usuarios administradores en el perfil de carpetas. (9306)
* El mapa raíz actualizado desde la Referencia de clave de contenido no se establece hasta que se actualiza la página. (9302)
* La autenticación web no funciona en Oxygen. (9296)
* Los vínculos web con caracteres codificados no funcionan correctamente. (9227)
* El archivo no se extrae cuando se abre en Oxygen. (9217)
* La actualización de los archivos desprotegidos no funciona en el registro con autenticación web en Oxygen. (9179)
* Las pestañas Traducción y Línea de base están visibles durante algún tiempo en el panel Mapa. (9146)
* La experiencia o las características se producen al volver a cargar el perfil de carpeta. (9103)
* Al eliminar el editor de diseño de página, no se cierra desde el panel central de la vista Autor. (9087)
* El error de validación se produce en el Editor web al quitar una imagen y, a continuación, al guardar la nueva versión del documento. (8985)
* No se pueden ver todas las variables `glossrefs` en el panel Glosario (específico del contenido). (8886)
* `xref` sin texto no se muestra en la salida de publicación basada en artículos. (8764)
* Las referencias rompen en imágenes móviles o archivos multimedia que tienen un espacio en los nombres de archivo. (8624)
* Las referencias rompen al elegir `Select All` y moviendo los archivos multimedia o el contenido DITA a otra carpeta. (8622)
* Los trabajos de salida con estado &quot;En espera&quot; o &quot;En ejecución&quot; no se limpian en el panel de publicación.  (8569)
* La función de depuración de salida falla si hay un gran número de nodos del historial de salida sobrantes presentes. (8568)
* DITA Add on package evita la detección de activos duplicados DAM. (8417)
* Crear botón de tarea de revisión habilitado para archivos que no sean DITA. (8401)
* El cuadro de diálogo Insertar referencias se abre al añadir el asunto ref a un mapa mediante la interfaz de usuario. (8212)
* Espacio inesperado encontrado en cada espacio en blanco `entry` elemento cuando el atributo outputclass se agrega a `tgroup` elemento. (7532)
* El panel Repositorio no muestra los iconos de bloqueo de archivos registrados o desprotegidos en cuanto se completa la acción. (5817)
* El icono Bloquear se muestra en la vista del repositorio incluso cuando el archivo se protege desde el editor.  (5756)
* Faltan sitios en AEM ajustes preestablecidos en la ficha Salida . (9567)
* El Editor XML se bloquea al intentar editar algunos archivos DITA. (9537)
* Al realizar una búsqueda en el Editor XML, la página se bloquea. (9452)
* El mapa de descarga con la línea de base no funciona si el contenido se mueve a otra carpeta. (9331)
* La recarga falla en Oxygen cuando los archivos ya existen en AEM en la misma ubicación. (9328)
* La posición del resaltado es incorrecta en la vista en paralelo. (9305)
* Después de registrar un documento de Oxygen a AEM, el contenido japonés del documento se reemplaza por signos de interrogación (????). (9276)
* La carga de archivos desde Oxygen a AEM falla. (9157)
* La notificación por correo electrónico no se envía cuando se vuelve a asignar una tarea de revisión en la Bandeja de entrada. (8376)

## Problemas conocidos

La página en blanco se muestra de forma intermitente al abrir el editor.
