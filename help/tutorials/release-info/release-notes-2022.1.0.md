---
title: Notas de la versión para [!DNL AEM Guides], versión de enero de 2022
description: Versión de enero de [!DNL Adobe Experience Manager Guides] as a Cloud Service
exl-id: b2da77fa-f17c-440b-be59-acaafcd9a57c
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '2429'
ht-degree: 3%

---

# Versión de enero de [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Actualización a la versión de enero

Actualice su [!DNL Adobe Experience Manager Guides] as a Cloud Service (posteriormente denominado [!DNL AEM Guides] as a Cloud Service) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
1. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2022.1.78.
1. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la versión de enero de [!DNL AEM Guides] as a Cloud Service.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por [!DNL AEM Guides] Versión as a Cloud Service de enero de 2022.

### FrameMaker y FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| No compatible | Actualización 4 y posterior de 2020 |
|  |  |


### Conector de oxígeno

| [!DNL AEM Guides] Versión en nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022.1.0 | 2.4.0 | 2.4.0 | 2.2 | 2.2 |
|  |  |  |  |  |


## Nuevas funciones y mejoras

### Publicación basada en artículos

Con la versión de enero, hemos introducido una función de publicación basada en artículos integrada en el Editor web. Puede utilizar la función de publicación basada en artículos para generar de forma incremental resultados de uno o más temas o publicar el contenido en una plataforma de base de conocimientos.

Esta función permite a los usuarios crear el mapa DITA de forma aditiva y publicar temas a medida que estén listos. Una vez que haya publicado el mapa, utilice la función de publicación basada en artículos para lograr la publicación incremental solo para los artículos actualizados.

![Publicación basada en artículos](assets/article-based-publishing.png)

Además de AEM, puede usar esta característica única para publicar sus artículos en cualquier portal de la base de conocimiento, como Salesforce. Esta función también incluye una plantilla de contenido OOTB, creada sobre AEM componentes principales, que permite crear un repositorio basado en el conocimiento del contenido técnico. Lo bueno de esta plantilla es que es totalmente personalizable para adaptarse a sus necesidades organizativas y también puede admitir casos de uso como portales de intranet corporativos.
También puede filtrar los artículos en función de su estado de documento y de la hora de modificación.

Esta publicación de artículos basada en la necesidad sobre la marcha no solo le proporciona control total sobre la publicación de contenido, sino que también reduce el tiempo total para publicar el contenido actualizado.
Al publicar los artículos con esta plantilla, también puede pasar los metadatos a las páginas publicadas.
Para obtener más información, consulte *Publicación basada en artículos desde el Editor web* en la Guía del usuario.

### Editor web mejorado

En el Editor web se introducen muchas mejoras y nuevas funciones:

* También se ha añadido compatibilidad con el esquema de temas en el Editor web. Ahora puede crear y utilizar el esquema de asunto mediante el panel Esquema de asunto . Con la adición del esquema de temas, ahora puede utilizar metadatos corporativos y taxonomía propios.

![Asunto](assets/subject-scheme-panel.png)

* En esta versión se ha introducido una nueva herramienta de puntos interactivos de glosario para administrar los glosarios de forma masiva. Con esta herramienta, puede convertir rápidamente el texto en glosario y glosario en términos de forma masiva para un mapa seleccionado o para temas abiertos.

![Zona interactiva del glosario](assets/glossary-hotspot-tool.png)

* Se ha agregado funcionalidad de actualización en el panel Contenido reutilizable que le permite actualizar rápidamente el contenido reutilizable en los archivos de referencia.
* El nuevo indicador de copia de trabajo le muestra si su archivo actual (copia de trabajo) está sincronizado con la versión guardada o no.

![Indicador de versión](assets/version-update-indicator.png)

* El filtro de búsqueda en el panel Repositorio y el cuadro de diálogo de exploración de archivos se han mejorado para ofrecer más opciones de filtrado, que se pueden personalizar aún más.

![Filtros de búsqueda en el repositorio](assets/repository-filter-search.png)

* Ahora puede cargar archivos .docx desde el Editor web.

### Autor con FrameMaker

Ahora puede crear y publicar sus documentos en FrameMaker. FrameMaker se envía con un conector incorporado a Adobe Experience Manager. En FrameMaker obtiene una interfaz fácil de usar que le permite mantener versiones de sus documentos en un entorno distribuido y colaborativo.

Una vez creado el contenido, FrameMaker permite publicar los documentos en diferentes formatos: PDF, HTML5, EPUB y DITA. También puede realizar diversas operaciones de administración de archivos como cierre de compra, cierre de compra con dependientes, ingreso, actualización, etc.
Para crear con FrameMaker en [!DNL AEM Guides] Utilice de forma as a Cloud Service la versión 2020.4 y superior de FrameMaker.

### Nuevo panel de traducción

Se ha introducido un nuevo panel de traducción en el Editor web con las siguientes funciones:

* Ordenar, buscar y filtrar la lista de temas.
* Filtrar contenido por tipo de referencia: referencias directas o indirectas.
* Navegación sencilla para encontrar un proyecto existente al iniciar una solicitud de traducción.
* Se ha introducido un mecanismo de traducción en varios idiomas para evitar la creación de varios proyectos para cada idioma cuando se inicia una solicitud de traducción para más de un idioma.
* Se ha introducido una configuración para ocultar la pestaña de traducción en el panel de mapas. De forma predeterminada, está visible. Puede elegir traducir contenido mediante el panel de asignación o el Editor web.

![Panel de traducción](assets/translation-from-web-editor.png)

### Publicación mejorada

* Los autores ahora pueden pasar metadatos a nivel de mapa y tema a la publicación de DITA-OT. Esto resulta útil cuando las plantillas de PDF personalizadas están diseñadas para utilizar propiedades de metadatos de archivo como etiquetas, autor, estado del documento, etc.

![Metadatos DITA-OT](assets/custom-meta-data-output-preset.png)

* Se ha añadido una nueva configuración para permitir a los usuarios conservar o eliminar las versiones de los temas que se eliminan al **Eliminar y crear** se utiliza en la generación de salida del sitio AEM.

### Administración de archivos mejorada

Ahora se pueden ver las siguientes mejoras al trabajar con archivos en AEM Assets:
* Se ha introducido una nueva experiencia de carga de archivos y un nuevo cuadro de diálogo para elegir una estrategia de resolución de conflictos.

![Conflicto de carga de archivos](assets/file-upload-name-conflict.png)

* Capacidad para crear una nueva versión de un archivo cargado con la capacidad de evitar sobrescribir un archivo extraído.
* Ahora puede ver una vista previa de imágenes directamente desde la vista Historial de versiones. Además, para los archivos DITA y no DITA, el Historial de versiones muestra la información de la versión actual por separado.

![Miniatura del historial de versiones](assets/version-history-preview-image.png)

* Siempre que el usuario crea un archivo DITA, el nombre de archivo predeterminado aparece en minúsculas para estar en línea con el escenario de creación de carpetas nativas de AEM.

### Nueva función de exportación de informes

Los informes son muy útiles para identificar el estado del contenido. [!DNL AEM Guides] as a Cloud Service proporciona varios informes para controlar el contenido. Ahora, no solo puede ver los informes, sino que también puede exportar los datos del informe en un archivo CSV para verlo y compartirlo con el equipo mayor. Los datos de los informes pueden darle una mirada rápida a los vínculos rotos o a las imágenes que faltan.

![Exportación de informes](assets/export-report.png)

### Experiencia de actualización de Oxygen DAM mejorada

Al actualizar archivos desde AEM Servidor en Oxygen, se muestra un mensaje de advertencia si tiene archivos sin guardar en su sesión actual de Oxygen. Puede optar por cancelar la operación de actualización para guardar los archivos sin guardar. Sin esta función, los usuarios perdían cualquier información no guardada en sus documentos.


### Otras mejoras de las funciones

* Ahora puede crear una **Proyecto Dita** plantilla en el **/apps/projects/templates** ruta.
* Ahora descargue el valor predeterminado **ui_config.json** de sus perfiles de carpeta. Esto se puede usar para combinar los cambios personalizados de los **ui_config.json** al actualizar.
* No es necesario borrar la caché del explorador incluso cuando hay nuevas versiones de archivos JS presentes.

## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

### Editor web

* Los conrefs aparecen en color rojo incluso cuando no están rotos. (8239)
* El valor del atributo condicional no se rellena automáticamente cuando se selecciona Añadir todas las propiedades en el editor DITAVAL. (8234)
* Los autores no pueden insertar una imagen en un tema mediante una ruta relativa. (8112)
* La página de la tarea de revisión no muestra los archivos multimedia si hay espacios en el nombre del archivo. (8111)
* La conref de Ph añadida en la celda de la tabla se muestra en color rojo. (8083)
* Los vínculos en la tarea de revisión no se actualizan cuando se mueven los archivos en revisión. (8080)
* El Editor web no procesa correctamente las imágenes que tienen la propiedad de escalado establecida en el 75% o superior. (8073)
* Las imágenes de GIF se representan como imágenes estáticas en el Editor web. (8024)
* Una referencia clave en un elemento de nota no se muestra en la vista previa del Editor web o en la salida. (8006)
* xref a un elemento que en sí es una conref no se resuelve en el editor. (7933)
* El título que tiene clave no se representa correctamente en la vista previa del editor ni en el panel Repositorio. (7909)
* Los fragmentos con caracteres especiales no se almacenan correctamente. (7908)
* Guardar un tema después de dar formato a las ecuaciones MathML provoca un error. (7954)
* keydef Having (tm) no se procesa correctamente en el editor y la salida del sitio AEM contenía símbolos TM duplicados. (7859)
* Arrastrar y soltar un fragmento no funciona según los DTD. (7758)
* El HTML ignora las dimensiones definidas personalizadas para los gráficos. (7718)
* el atributo conrefend no se actualiza cuando se mueve el archivo de origen. (7698)
* Trabajar con documentos de tipo de tema de referencia conlleva varios problemas de IU. (7656)
* Los archivos DITAVAL no se muestran cuando el autor agrega ditavalf en un mapa. (7594)
* Espacio inesperado en cada espacio en blanco `<entry>` elemento cuando el atributo outputclass se agrega a `<tgroup>` elemento. (7532)
* El botón de origen no funciona para los temas abiertos mediante el panel de asignación. (7465)
* La impresión bonita inserta líneas en blanco y espacios que se pueden ver cuando el archivo se abre en FrameMaker o Oxygen. (7408)
* Los mapas con href=&quot;/&quot; en cualquiera de los temas no se publican en AEM sitios. (7405)
* Problemas de rendimiento encontrados en el editor cuando el mapa raíz tiene un gran número de keydefs. (7400)
* El estado del documento de un mapa con plantilla personalizada no se hereda de su perfil de estados correspondiente. (7359)
* `<tm>` elemento procesado incorrectamente como elemento de bloque. (7286)
* Las plantillas duplicadas se muestran en el panel Plantillas de editor cuando se crea una nueva plantilla. (5814)
* Las plantillas definidas en ui_config para imágenes para configurar atributos adicionales no son aplicables para casos de arrastrar y soltar. (5713)
* Aparición predeterminada incorrecta de uicontrol en la menucascada. (5483)
* Las plantillas personalizadas para tema/mapa no muestran un nombre nuevo en la interfaz de usuario. Muestra el nombre como &quot;Tema&quot;/&quot;Mapa&quot; en lugar de mostrar el nombre configurado. (4958)
* Posibilidad de borrar la hoja de ruta de la configuración de preferencias del usuario. (8534)
* No se muestra una colección de mapas recién creada, ni siquiera después de actualizar la página.(8603)
* No se puede cerrar el tema desbloqueado. (8545)
* El cambio entre el modo de origen y de autor marca el tema como sucio y requiere que el contenido se guarde de nuevo.(8524)
* Reutilizar el panel de contenido se bloquea al buscar caracteres especiales `[` o `*` .(8279)
* El cursor no se muestra en la barra de búsqueda cuando se abre el cuadro de diálogo Insertar elemento con el atajo de teclado Alt+Intro.(7912)
* La opción de búsqueda solo busca en los nombres de archivo y no en el contenido. (7784)


### Conector de oxígeno

* Los archivos cuya carpeta principal tiene caracteres especiales dan error al cargar en Oxygen. (8054)
* Cuando se abre un documento recién creado en Oxygen, aparece el error &quot;No se puede encontrar el GUID&quot;. (7856)
* La opción de protección se desactiva una vez que el archivo se ha extraído de AEM mediante Editar en Oxygen. (7471)


### Revisión

* La sincronización en tiempo real no funciona para los comentarios. (7661)

### Mapa del tablero

* No se puede ver el contenido conref en el título de un tema en la pestaña de informes o temas del tablero de asignación. (8263)
* Salida de AEM Sites | jcr:title de la página del sitio generada no se actualiza cuando se actualiza el título del tema DITA. (8131)
* Download MAP no descarga los archivos de vídeo utilizados dentro de los temas. (8070)
* Los archivos multimedia no se descargan cuando el objeto Tag se utiliza a través de la API de descarga de bookmap. (8057)
* El informe incorrecto se muestra en la ficha Informes si algún tema tiene referencia a un archivo cuyo título comienza por conref. (4698)
* El cuadro de diálogo Aplicar etiquetas de la ficha Línea de base no muestra las etiquetas en la lista desplegable. (8455)

### Publicación

* La creación de PDF falla por primera vez cuando se selecciona Activar versiones . (8053, 8294)
* El carácter de espacio en blanco se agrega automáticamente después de &quot;tm; en AEM salida del sitio. (7964)
* No se pueden ver los vídeos de YouTube en AEM salida del sitio. (7401)
* El filtro por etiqueta falla para el contenido al que se hace referencia después de que el usuario haga clic en examinar todos los temas de la ficha de línea de base del panel de asignación. (7388)
* Publicar tema con elemento `<tm>` tener un valor de propiedad SM o reg se muestra incorrectamente en la salida generada. (7239)
* La publicación de línea de base con imagen no está seleccionando la última versión de la imagen en la salida publicada. (7231)
* Los temas a los que se puede hacer referencia se muestran en la pestaña de la línea base. (5424)
* La publicación incremental de un tema con conkeyref en su título no funciona como se espera. (4474)
* El título de la página no se utiliza para la generación de direcciones URL de salida aunque esté marcado. (8257)
* Publicación de línea de base seleccionando la versión actual de las imágenes en lugar del nodo congelado. Esto también se observa si una imagen tiene espacio o caracteres especiales en el nombre del archivo. (8274, 8322)
* La publicación incremental falla en el mapa DITA con el esquema de sujeto de tipo que tiene mapref. (8218)
* Se agrega nulo cada vez que se agrega un mapa al tablero de publicación masiva. (8695)
* Al usar la publicación de línea de base con imagen como referencia en el tema, la imagen no se publica en la salida. (8564)
* La publicación falla con una excepción si se elimina la línea de base utilizada en AEM publicación del sitio. (8572)
* La regeneración del tema no funciona. (8091)
* Existen problemas con la publicación de notas al pie en tablas. (4709)

### AEM Assets

* Se han encontrado problemas de rendimiento al realizar la selección/eliminación en grandes conjuntos de contenido en la interfaz de usuario de Assets. (8238)
* La función de búsqueda guardada (colección inteligente) se rompe si el predicado DITA se agrega a los filtros de búsqueda. (8048)
* No funciona la reversión de la imagen a una versión anterior. (DXML-7903)
* La opción Eliminar también está visible para los autores que no tienen permiso para eliminarla. (7322)
* La superposición de CCMS para el Editor de recursos rompe la representación de la opción Eliminar. (8093)
* El perfil del documento no se va a eliminar. (8604)
* Las referencias rompen al realizar &quot;Seleccionar todo&quot; y mover el contenido multimedia/digital a otra carpeta. (8621)
* Las referencias incorrectas se producen en el origen al mover los recursos. (8627)
* La vista de lista fija no se carga. (8542)

### Importación de contenido

* Conversión de HTML a DITA | La tabla con entradas &quot;tr&quot; vacías &quot;td&quot; genera filas adicionales en la salida. (8132)
* Conversión de HTML a DITA | El HTML que tiene una tabla con varios cuerpos falla con excepción. (7940)
* Conversión de HTML a DITA | se produce un error si el HTML de origen tiene comentarios. (7937)
* La importación de archivos DITA 1.3 DITA hace que algunos href se transformen en vínculos con formato incorrecto. (8019)

## Problemas conocidos

Adobe ha identificado los siguientes problemas conocidos para [!DNL AEM Guides] Versión as a Cloud Service de enero de 2022.


### Problemas conocidos con la solución alternativa

Utilice la solución dada para los siguientes problemas conocidos:

* La autenticación web no funciona para el conector Oxygen en Mac.
   **Solución alternativa**: Utilice el conector Oxygen en Windows por ahora.

* En el navegador Firefox, los comentarios de revisión no se pueden importar sin abrir la vista en paralelo.
   **Solución alternativa**: Utilice el navegador Chrome por ahora.

* Las referencias rompen al mover las imágenes o archivos multimedia que tienen espacio en los nombres de archivo.
   **Solución alternativa**: Cambie el nombre del archivo y elimine los espacios del nombre del archivo antes de moverlos.

* El tablero de mapas no se carga de forma intermitente en la última versión del navegador Chrome.
   **Solución alternativa**: Actualice la página del tablero de asignación.

### Otros problemas conocidos

* Si el oxígeno está conectado con [!DNL AEM Guides] mediante autenticación web, el cierre de sesión falla.
* Las tareas de revisión no se pueden reasignar a los usuarios.
* Hay problemas presentes en la interfaz de usuario de la colección Map como si el texto estuviera distorsionado y **Seleccionar todo** no funciona correctamente.
