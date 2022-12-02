---
title: Notas de la versión | Guías de Adobe Experience Manager as a Cloud Service, versión de noviembre de 2022
description: Última versión de las guías de Adobe Experience Manager as a Cloud Service
exl-id: 9f329ec1-dd74-47cc-8567-3fadd962584a
source-git-commit: 0663ed4434fdf583a9446891f944d94b85f375c6
workflow-type: tm+mt
source-wordcount: '1372'
ht-degree: 2%

---

# Última versión de las guías de Adobe Experience Manager as a Cloud Service

## Actualice a la última versión

Actualice las guías actuales de Adobe Experience Manager as a Cloud Service (más adelante, *Guías AEM as a Cloud Service*) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2022.11.198.
3. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la última versión de AEM guías as a Cloud Service.

## Pasos para indexar el contenido existente (solo si está en una versión anterior a la versión de septiembre de AEM Guías as a Cloud Service)

Realice los siguientes pasos para indexar el contenido existente y utilice el nuevo texto de buscar y reemplazar en el nivel del mapa:

* Ejecute una solicitud de POST al servidor (con autenticación correcta): `http://<server:port>/bin/guides/map-find/indexin`.
(Opcional: Puede pasar rutas específicas de los mapas para indexarlos, de forma predeterminada todos los mapas se indexarán || Ejemplo: `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* La API devolverá un jobId. Para comprobar el estado del trabajo, puede enviar una solicitud de GET con id de trabajo al mismo punto final: `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por ejemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Una vez completado el trabajo, la solicitud de GET anterior responderá con éxito y mencionará si se han producido errores en los mapas. Los mapas indexados correctamente se pueden confirmar desde los registros del servidor.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por AEM Guías as a Cloud Service para la versión de noviembre de 2022.

### FrameMaker y FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| No compatible | Actualización 4 y posterior de 2020 |
|  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

### Conector de oxígeno

| AEM guías como una versión en la nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022.11.0 | 2,7,13 | 2,7,13 | 2.3 | 2,3 |
|  |  |  |  |


## Nuevas funciones y mejoras

AEM guías as a Cloud Service proporciona mejoras y nuevas funciones en la última versión:


### Eliminar archivos del panel del repositorio

Ahora puede eliminar fácilmente los archivos (un solo archivo a la vez) del **Opciones** del archivo seleccionado desde el panel del repositorio.
<img src="assets/repository-delete-file.png" alt="Eliminar del repositorio" width="500">

Se muestra un mensaje de confirmación antes de eliminar el archivo. Si no se hace referencia al archivo desde ningún otro archivo, este se elimina y se muestra un mensaje de éxito.

Si el archivo seleccionado está desprotegido, no puede eliminarlo y aparecerá un mensaje de error. Si el archivo seleccionado se agrega a una colección favorita o se hace referencia a él desde cualquier otro archivo, AEM guías comprueba la confirmación y le da la opción de eliminarla a la fuerza. Si elimina un tema referenciado y ha abierto el archivo que contiene referencias para edición, se mostrará el vínculo roto para el archivo referenciado.

**Nota**: También puede eliminar el archivo seleccionado mediante la tecla Supr del teclado.


### Depuración de versiones seleccionadas de archivos

A medida que crea y mantiene el contenido, es posible que se creen muchas versiones para sus archivos DITA en el repositorio. AEM guías le permite depurar versiones anteriores de sus archivos DITA del repositorio y liberar espacio en disco.

<img src="assets/preview-purge-report.png" alt="Previsualizar informe de depuración" width="500">


AEM guías no elimina la primera versión del archivo o una versión que esté incluida en una línea de base, ni se le aplica una etiqueta. La operación de depuración ni siquiera elimina los archivos que se incluyen en una traducción o un flujo de trabajo de revisión. Puede elegir el número de versiones que desea conservar y también decidir eliminar los archivos anteriores al número definido de días.

Antes de iniciar la operación de depuración, puede obtener una vista previa del informe para ver las versiones que se purgarán. A continuación, puede decidir iniciar o cancelar la operación de depuración.

<img src="assets/download-purge-report.png" alt="Informe de depuración de PDdownload" width="500">

Una vez finalizada la operación de depuración, puede consultar el informe de depuración para ver los archivos depurados.

### Administrar ajustes preestablecidos de salida de Perfil de carpetas y global

AEM guías le proporcionan la función de crear y administrar ajustes preestablecidos de salida para los Perfiles globales y de carpeta. A continuación, puede utilizar fácilmente estos ajustes preestablecidos de salida para generar resultados para todos los mapas relacionados con ese perfil Global o Folder.

<img src="assets/add-global-output-preset.png" alt="Añadir perfil global" width="400">

**Nota** Solo los usuarios administrativos de nivel de carpeta pueden crear ajustes preestablecidos de Perfil global y de carpeta .

Estos ajustes preestablecidos globales aparecen en la sección **Salida** de todos los mapas relacionados. Puede utilizarlos para generar el resultado de todos los mapas relacionados. Puede seleccionar el ajuste preestablecido como ajuste preestablecido de PDF predeterminado para generar la salida del PDF. También puede **Editar**, **Cambiar nombre**, **Duplicar** o **Eliminar** un ajuste preestablecido de salida existente de la variable **Opciones** para abrir el Navegador.

### Columna Etiqueta de versión agregada al panel de traducción

En el panel de traducción, también puede ver la columna Etiqueta de versión . Se mostrará la etiqueta de la versión seleccionada del archivo de origen. Esto puede ayudarle a seleccionar todos los archivos con una etiqueta específica y traducirlos de una sola vez.

<img src="assets/send-translation.png" alt="enviar para traducción" width="600">


### PDF nativo | PDF con barra de cambios que muestra la diferencia entre las versiones del documento

Ahora puede crear un PDF que muestre las diferencias de contenido entre dos versiones con la barra de cambios. Puede elegir comparar la versión actual con una línea de base de la versión anterior o comparar las dos versiones de línea de base seleccionadas.

<img src="assets/pdf-change-version.png" alt="spdf-change-version" width="600">

Aparece una barra de cambios en el PDF para indicar el contenido modificado, insertado o eliminado. También tiene las opciones para hacer lo siguiente:
* Mostrar el contenido insertado en color verde y subrayado
* Mostrar el contenido eliminado en color rojo y marcado con tachado

### PDF nativo | Compatibilidad de variables para Ruta de salida y nombre de archivo del PDF

Ahora también puede utilizar las siguientes variables predeterminadas para definir la ruta de salida y el archivo de PDF. Puede utilizar una o una combinación de variables para definir estas opciones:
* `${map_filename}`
* `${map_title}`
* `${preset_name}`
* `${language_code}`
* `${map_parentpath}` (solo para la ruta de salida)
* `${path_after_langfolder}` (solo para la ruta de salida)


### PDF nativo | Generar tabla de contenido para mapas DITA y reordenar diseños de página

Ahora también puede generar el TOC en los mapas DITA utilizando una configuración de PDF avanzada de la plantilla. Puede optar por habilitar o deshabilitar la visualización de los distintos diseños de página y también reordenar su posición.

## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* PDF nativo | `conkeyref` no se resuelve en la salida del PDF generado. (10564)
* PDF nativo | Se producen problemas al acceder a los metadatos de un mapa en la salida del PDF. (10556)
* PDF nativo | El estilo en línea se utiliza para generar etiquetas en lugar del nombre de clase.  (10498)
* El Editor web carga la página en blanco de forma intermitente. (10678)
* La publicación del PDF falla si se crea un ajuste preestablecido mediante la duplicación de un ajuste preestablecido existente. (10584)
* **Ver registro** no funciona cuando falla la generación del PDF para un ajuste preestablecido. (10576)
* Tenga en cuenta que dentro de una etiqueta para que sea una conref no se muestra en la vista previa. (10559)
* Al pulsar Retroceso al final de un elemento de lista, se elimina toda la lista. (10540)
* Al utilizar un PDF nativo, exporte el anidado `<indexterm>` no están anidadas en el índice. (10521)
* **Sangría automática** falta en la vista de origen. (10448)
* El primer carácter de un elemento de lista se pierde mientras la lista se crea en el editor. (10447)
* Se muestran varias ventanas emergentes si se cambia cualquier versión de recurso DITA y se guarda en la ventana de edición de línea de base. (10399)
* El error de la aplicación se produce al hacer clic **Editar** después de seleccionar todos los ajustes preestablecidos de salida del panel Generación rápida . (10388)
* Los metadatos personalizados para el tema DITA no se conservan cuando se realiza una acción de copiar y pegar desde la interfaz de usuario de Assets. (10367)
* El procesamiento posterior está bloqueado para toda la carpeta de idiomas cuyos recursos están presentes en un proyecto de traducción activo. (10332)
* La ficha Plantilla del Editor XML no está visible para los administradores de perfiles de carpetas. (10266)
* Los problemas de navegación se producen en el Editor web después de la actualización a la versión 4.0. (10159)
* Los archivos SVG no se muestran en el modo Vista previa. (10010)
* Si la ficha Salida del editor contiene más ajustes preestablecidos, la sección de ajustes preestablecidos no se puede desplazar y no se mostrarán todos. (9787)
* **Editar** y **Anotar** las opciones de una imagen no funcionan correctamente en la vista de columna. (8758)
* El vínculo del mismo nivel no se resuelve y aparece como texto normal en la salida generada. (7774)
