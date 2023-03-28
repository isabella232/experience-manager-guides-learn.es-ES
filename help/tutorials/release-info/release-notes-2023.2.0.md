---
title: Notas de la versión | Guías de Adobe Experience Manager as a Cloud Service, versión de febrero de 2023
description: Versión de febrero de las guías de Adobe Experience Manager as a Cloud Service
exl-id: c639b136-11ed-4a8b-a595-4bb5da879747
source-git-commit: ee520ab86ea41df7556a1f40d7bfc5e3617b34ae
workflow-type: tm+mt
source-wordcount: '2178'
ht-degree: 2%

---

# Versión de febrero de las guías de Adobe Experience Manager as a Cloud Service

## Actualización a la versión de febrero

Actualice las guías actuales de Adobe Experience Manager as a Cloud Service (más adelante, *Guías AEM as a Cloud Service*) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2023.2.235.
3. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la versión de febrero de AEM Guías as a Cloud Service.

## Pasos para indexar el contenido existente (solo si está en una versión anterior a la versión de septiembre de AEM Guías as a Cloud Service)

Realice los siguientes pasos para indexar el contenido existente y utilice el nuevo texto de buscar y reemplazar en el nivel del mapa:

* Ejecute una solicitud de POST al servidor (con autenticación correcta): `http://<server:port>/bin/guides/map-find/indexing`.
(Opcional: Puede pasar rutas específicas de los mapas para indexarlos, de forma predeterminada todos los mapas se indexarán || Ejemplo: `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* La API devolverá un jobId. Para comprobar el estado del trabajo, puede enviar una solicitud de GET con id de trabajo al mismo punto final: `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por ejemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Una vez completado el trabajo, la solicitud de GET anterior responderá con éxito y mencionará si se han producido errores en los mapas. Los mapas indexados correctamente se pueden confirmar desde los registros del servidor.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por AEM Guías as a Cloud Service para la versión de febrero de 2023.

### FrameMaker y FrameMaker Publishing Server

| AEM guías como una versión en la nube | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.02.0 | No compatible | 2022 o posterior |
|  |  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

### Conector de oxígeno

| AEM guías como una versión en la nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.02.0 | 2.8-uuid-8 | 2.8-uuid-8 | 2.3 | 2.3 |
|  |  |  |  |


## Nuevas funciones y mejoras

AEM guías as a Cloud Service proporciona mejoras y nuevas funciones en la versión de febrero:

### Generar informes desde el Editor web

AEM guías incluye una función en el Editor web que permite comprobar la integridad general de los documentos técnicos y generar informes para ellos.
Puede ver la lista de temas, administrar los metadatos y ver el contenido multimedia utilizado en todas las referencias para el mapa actual desde el
**Informes** en el Editor web.

**Generar la vista Lista de temas**

Puede generar la lista de temas, que proporciona información detallada sobre sus temas, como el tipo de referencia, el estado del documento y el autor. También puede generar el CSV para descargar la instantánea actual de los temas en el mapa de DITA.

**Administrar metadatos y cambiar el estado del documento**

Puede aplicar etiquetas en un tema individual o utilizar la función de etiquetado masivo para aplicar varias etiquetas en varios temas, un mapa DITA o un submapa. También puede cambiar el estado del documento de todos los temas seleccionados al siguiente estado de documento común posible.

<img src="assets/web-editor-metadata-panel.png" alt="administrar metadatos" width="600">

**Generar el informe Multimedia**

Puede generar el informe multimedia que contiene información detallada sobre el contenido multimedia utilizado en sus referencias dentro del mapa actual. Tiene la flexibilidad de filtrar y ordenar los archivos multimedia enumerados en el informe.
También puede generar el CSV para descargar la instantánea actual del contenido multimedia utilizado en el mapa de DITA.

<img src="assets/web-editor-reports-multimedia.png" alt="informe multimedia" width="600">

### Experiencia de usuario mejorada para la funcionalidad de revisión

Ahora, AEM guías proporciona una experiencia de usuario mejorada que le ayuda a revisar los temas compartidos para su revisión. En la última experiencia, la funcionalidad de revisión presenta las siguientes mejoras:

* Interfaz de usuario actualizada
* Panel Condiciones que permite resaltar el contenido según las condiciones disponibles en el tema
* Cada comentario del panel de comentarios está vinculado al texto correspondiente del tema actual. Ayuda a identificar el texto comentado.
* Los comentarios se muestran en el orden del texto comentado en el documento.
* El nombre de la tarea de revisión se muestra en el flujo de trabajo de revisión.
* Seleccione la hoja de ruta para la tarea de revisión que se utiliza para resolver todas las referencias clave y los términos del glosario utilizados en el contenido de revisión.
* Barra de herramientas contextual que ayuda a resaltar o tachar rápidamente el texto
* Menú Opciones para editar o eliminar sus propios comentarios
* Para comentarios obsoletos, tiene acceso a la vista en paralelo que le ayuda a comparar la versión anterior del tema con la versión de revisión actual.
* Al utilizar los filtros, los comentarios del panel derecho se filtran según la selección y el número de comentarios del panel izquierdo se actualiza en consecuencia.


   <img alt="revisar tarea" src="assets/comment-pop-up-panel.png" width="600">



### Mejoras de traducción

Ahora tiene mejoras más fáciles de usar en el panel Traducción que le ayudan a traducir fácilmente sus documentos desde el Editor web.

**Pasar la etiqueta de versión a la versión de destino**

AEM guías le permite pasar la etiqueta del archivo de origen al archivo de destino. Esto le ayuda a identificar fácilmente la versión de origen del archivo traducido.

<img alt="etiquetas de traducción" src="assets/translation-pass-source-label.png" width="600">

Por ejemplo, si tiene algunos archivos de origen con la etiqueta de versión Versión 1.0 aplicada a ellos, también puede pasar la etiqueta de origen (Versión 1.0) al archivo traducido.

**Forzar sincronización para activos fuera de sincronización**

Si realiza cambios en algunos de los recursos, las guías de AEM las marcan como no sincronizadas. Puede volver a traducir los recursos modificados o elegir rechazar el estado de falta de sincronización. Por ejemplo, si ha realizado algunos cambios menores que realmente no necesitan una traducción, puede marcar su estado como In Sync.

<img src="assets/translation-version-diff.png" alt="tarjeta de traducción" width="600">

**Ver proyectos de traducción en curso para un tema o mapa**

Es posible que algunas de las referencias del panel de traducción estén en curso. Ahora, AEM guías proporciona una función que le ayuda a ver la lista de todos los proyectos de traducción en curso (junto con el idioma de destino) que contienen la referencia seleccionada.


### Generar salida en varios formatos desde el Editor web

Ahora puede generar fácilmente el resultado para sus temas o mapa DITA desde el Editor web. Puede configurar varios ajustes preestablecidos de salida, como AEM sitio, PDF, HTML5, JSON (un formato de salida sin encabezado) y resultados personalizados. A continuación, puede utilizarlos para generar los respectivos resultados.

Puede definir atributos en los temas de DITA y, a continuación, utilizar el ajuste preestablecido de condición para aplicar una condición al publicar la salida. También puede utilizar la función Publicación de línea de base para publicar selectivamente una versión específica de su mapa o tema de DITA.


### Buscar y reemplazar el texto en el nivel del mapa

AEM guías le permite buscar archivos dentro de un mapa que contengan texto específico. El texto buscado se resalta en los archivos. Ahora también puede reemplazar la palabra o frase buscada con otra palabra o frase dentro de todos los archivos. Puede seleccionar **Reemplazar todo** a la derecha de la parte superior de la lista para reemplazar todas las ocurrencias del término buscado en todos los archivos.

<img src="assets/map-find-replace.png" alt="buscar reemplazar" width="600">

### Eliminar y duplicar archivos del panel del repositorio

Ahora puede crear fácilmente un duplicado o una copia de un archivo desde el **Opciones** del archivo seleccionado en el panel repositorio. De forma predeterminada, el archivo se crea con un sufijo (como `filename_1.extension`).

<img src="assets/options-menu-repo-view-file-level.png" alt="menú de opciones de archivo " width="500">


### Otras mejoras del Editor web

* En AEM guías, puede realizar algunas operaciones comunes para imágenes y archivos multimedia mediante el menú contextual. Ahora también puede localizar la imagen o los medios seleccionados en el repositorio o ver la previsualización del archivo en la interfaz de usuario de Assets.

* El nombre del perfil de carpeta actual se muestra como una etiqueta para el icono Preferencias de usuario en la barra de herramientas principal. Esto le ayuda a identificar el perfil de carpeta en el que está trabajando.

* Cuando se abre un mapa en la vista del mapa, el título del mapa actual se muestra en el centro de la barra de herramientas principal. Esto es útil para informar a los usuarios qué mapa está abierto actualmente.


### Ver título en lugar de UUID en el Editor de oxígeno

Ahora AEM guías le permite elegir **Uso del título en el Editor y el Administrador de mapas** en Configuración. Si selecciona esta opción, el título del archivo se muestra en la ficha del archivo cuando se abre en el Editor o en el Administrador de mapas DITA. Si no selecciona esta opción, el UUID del archivo se muestra en la pestaña del archivo.

### Publicación basada en microservicios para guías AEM as a Cloud Service

El nuevo microservicio de publicación le permite ejecutar grandes cargas de trabajo de publicación simultáneamente en AEM guías as a Cloud Service y aprovechar la plataforma sin servidor líder en el sector de Adobe I/O Runtime.

Para cada solicitud de publicación, AEM guías as a Cloud Service ejecuta un contenedor independiente que se escala horizontalmente según las solicitudes del usuario. Esto le permite ejecutar varias solicitudes de publicación y obtener un rendimiento mejorado.

Para obtener más información, consulte [Configuración de la nueva publicación basada en microservicios para AEM guías as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/knowledge-base/publishing/configure-microservices.md).

### PDF nativo | Agregar un marcador personalizado en la salida del PDF

Ahora puede agregar un marcador personalizado a un contenido en particular en la salida del PDF final para facilitar la navegación. Esto se agregaría a la tabla de contenido que se crea a partir de los títulos de temas o secciones del mapa DITA.

### PDF nativo | Aplicar estilo personalizado en entradas de TDC y contenido del tema

AEM guías proporciona la función para aplicar estilo personalizado en las entradas de la tabla de contenido o en un tema concreto de la salida del PDF. Por ejemplo, puede cambiar el color del texto en la tabla de contenido y el título del tema. También puede aplicar estilos a todo el contenido dentro del tema.


### PDF nativo | Estilo del marcador de página en el componente de nota al pie

Ahora puede aplicar estilo al marcador de página en las notas de pie de página. Por ejemplo, puede añadir corchetes o cambiar su color. Estos estilos ayudan a los usuarios a identificar fácilmente los marcadores de página del documento.

### PDF nativo | Cambiar barra para indicar los temas modificados en la Tabla de contenido

AEM guías ahora le permite identificar rápidamente los temas modificados en la tabla de contenido de la salida del PDF.  Muestra una barra de cambios a la izquierda de los temas modificados en la tabla de contenido. Puede hacer clic en el tema de la tabla de contenido y ver los cambios detallados.

<img src="assets/change-marker-toc.png" alt="Cambiar marcador en TDC " width="500">

## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

### Creación

* Los cambios en el HTML del Editor web causan problemas con `<dl>` y `<dlentry>`. (11024)
* Algunos atributos no se tratan como condicionales y causan problemas. (10895)
* Tres niveles o más anidados `<indexterm>` no están anidados en la exportación de PDF nativo. (10799)
* El contenido desaparece en el cuerpo de una tarea al pasar de la vista Autor a la vista Origen. (10735)
* Los comentarios de revisión no se colocan correctamente en una tarea de revisión. (10625)
* **Deshacer** o **Rehacer** no funciona correctamente en algunos archivos. (10373)
* Los metadatos personalizados no se retienen al copiar y pegar. (10367)
* La opción Deshacer del Editor XML lleva al usuario a la parte superior de la página. (10091)
* Las propiedades de nodo se eliminan después de copiar y pegar el funcionamiento de un recurso. (10053)
* mimeType está codificado para la creación y actualización de recursos DITA. (8979)
* El nombre del creador de versiones en el Historial de versiones es &quot;fmdita-service-user&quot; para los archivos cargados a través de la interfaz de usuario de Assets. (8910)
* Los fragmentos de contenido no se pueden copiar ni pegar cuando AEM guías está instalada en la nube. (11315)
* El navegador (Editor web) se bloquea al cargar contenido con esquema personalizado. (11211)

### Administración

* Copiar un recurso de mapa DITA (desde la interfaz de usuario de Asset ) provoca líneas de base erróneas en el recurso copiado. (11218)
* El mensaje de advertencia no se muestra en la carga de un archivo que sea mayor que el límite permitido en AEM (2 GB de forma predeterminada). (10817)
* Editor web: línea de base | El comportamiento de la última columna es diferente en el nuevo panel de línea de base del Editor web. (10808)
* Traducción | El trabajo de traducción no se inicia debido a que /libs/fmdita/i18n/ja.json no es válido. (10543)
* Traducción | Se produce un error en un proyecto de traducción de ámbitos creado desde el panel de traducción (Traducción humana). (10526)
* Traducción | El procesamiento posterior está bloqueado para toda la carpeta de idiomas cuyos recursos están presentes en un proyecto de traducción activo. (10332)
* Si la versión se cambia y se guarda en el editor de línea de base, aparecen varias ventanas emergentes para cualquier recurso. (10399)
* La fuga de sesión se produce en `com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver(QueryBuilderImpl.java:210)`. (10279)

### Publicación

* La regeneración del tema no funciona en algunos escenarios. (10635)
* Publishlistener no muestra los datos solicitados en los registros de información y también contiene algunos registros no deseados.( 10567)
* PDF nativo | Al crear un ajuste preestablecido de salida con la opción &quot;Añadir a perfil de carpeta&quot;, la generación del PDF falla con una excepción de puntero nulo. (10950)
* PDF nativo | Se producen problemas al girar el encabezado Tabla. (10555)
* PDF nativo | Anidado `<indexterm>` no están anidados en la exportación de PDF nativo. (10521)
* PDF nativo | El topicref anidado en los apéndices se transforma en h1 en el HTML temporal. (10454)
* La publicación de línea de base falla para el PDF generado con FrameMaker Publishing Server 2020. (10551)
* PDF nativo | Añadir `xref` en una imagen no representa la imagen en el PDF generado. (11346)
* PDF nativo | La etiqueta de imagen añade un atributo display-inline a todas las imágenes. (10653)
* PDF nativo | Los comentarios de borrador están ocultos de forma predeterminada en la salida generada. (10560)
* PDF nativo | navtitle no es compatible con topichead. (10509)
