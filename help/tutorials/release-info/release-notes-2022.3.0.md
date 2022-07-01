---
title: Notas de la versión para [!DNL AEM Guides], versión de marzo de 2022
description: Versión de marzo de [!DNL Adobe Experience Manager Guides] as a Cloud Service
exl-id: 885edbb5-dfe4-4bdc-bb66-0df64addb094
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 2%

---

# Versión de marzo de [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Actualización a la versión de marzo

Actualice su [!DNL Adobe Experience Manager Guides] as a Cloud Service (posteriormente denominado *[!DNL AEM Guides]as a Cloud Service*) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2022.3.123.
3. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la versión de marzo de [!DNL AEM Guides] as a Cloud Service.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por [!DNL AEM Guides] as a Cloud Service versión de marzo de 2022.

### FrameMaker y FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| No compatible | Actualización 4 y posterior de 2020 |
|  |  |


### Conector de oxígeno

| [!DNL AEM Guides] Versión en nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac |
| --- | --- | --- |
| 2022.3.0 | 2.4.0 | 2.4.0 |
|  |  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

## Nuevas funciones y mejoras

### Nuevo panel de línea de base

[!DNL AEM Guides] La versión as a Cloud Service de marzo proporciona la función de línea de base integrada en el Editor web. Ahora puede crear líneas de base desde el Editor web y utilizarlas para publicar o traducir temas de distintas versiones.

Nota: Para actualizar el sistema, actualice la última **ui_config.json** para Perfil de carpeta.

Utilice esta función para crear una línea de base con una versión específica de los temas disponibles en una fecha y hora específicas. Además, se ofrece compatibilidad con la API para crear o actualizar una línea de base con una etiqueta definida para una versión de los temas.

![ficha de gestión de línea de base](assets/baseline-manage.png)

Puede buscar en los archivos en función de sus nombres o ubicación. También puede filtrar los temas que desea mostrar en la ventana de edición de la línea base y ordenarlos en función de columnas específicas.

![ficha de gestión de línea de base](assets/baseline-filter.png)

Se ha seguido mejorando el rendimiento del proceso de creación de la línea de base. El proceso para crear líneas de base es asíncrono, por lo que puede seguir editando otros archivos en el Editor web mientras se crea la línea de base. Para obtener más información, consulte *Crear y administrar líneas de base desde el Editor web* en la Guía del usuario.

Nota: La pestaña Línea de base en el panel del mapa está oculta de forma predeterminada. El administrador puede activar la ficha Línea de base en el panel de asignación.

### Comportamiento de actualización del Editor web mejorado

Ahora están disponibles las siguientes mejoras con la operación de actualización del explorador en el Editor web:

* Ahora obtendrá asistencia para actualizar el navegador mientras edita el contenido en el Editor web. Si pulsa el icono de actualización del explorador mientras se abren para editar uno o varios archivos con cambios no guardados, se le pedirá que guarde los archivos o cancele la acción de actualización.

* Incluso al actualizar el navegador, se conservan las vistas del panel izquierdo y del panel derecho.

* El tema activo o el mapa DITA se vuelve a abrir en el área de edición de contenido.

### Mejoras en la publicación

El proceso de publicación se ha mejorado aún más con la versión de marzo de [!DNL AEM Guides] as a Cloud Service:

* Se han respetado las líneas de base para los metadatos de AEM salida del sitio. También puede procesar las propiedades de una versión de línea de base como metadatos. Si no se define ninguna línea de base, las propiedades de la última versión se procesan como metadatos.

* La variable **Nombre del archivo** y **Argumentos de la línea de comandos DITA-OT** se han añadido opciones para los ajustes preestablecidos de salida HTML5, EPUB y Personalizado. Ahora puede especificar el nombre del archivo con el que desea guardar la salida. También puede especificar los argumentos adicionales que desea que procese DITA-OT durante la generación de resultados.

## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* No se pueden agregar elementos de materia principal y de materia secundaria en un mapa de libros mediante la vista Autor del Editor web. (7652)
* El árbol de referencia se rompe tras eliminar un tema y realizar una operación de movimiento. (8804)
* Se recibe una excepción al ver el contenido después de cargar un recurso. (3638)
* El error se produce cuando los archivos cuya carpeta principal tiene caracteres especiales en el nombre del archivo se abren en Oxygen (utilizando la variable **Editar en oxígeno** ). (8918)
* La variable **Localizar en repositorio** no encuentra ni resalta el mapa DITA en el Editor XML. (8796)
* El filtrado no muestra los resultados adecuados cuando se añaden varios atributos al contenido en el Editor XML. (8795)
* Se produce un error al añadir un usuario como administrador en el perfil de carpetas cuando el ID de usuario es numérico. (8908)

## Problemas conocidos

El Adobe ha identificado el siguiente problema conocido en el [!DNL AEM Guides] Versión as a Cloud Service de marzo.

* Al eliminar las etiquetas de las referencias directas también se eliminan las etiquetas de las referencias indirectas.

* No se puede reflejar el título de la línea base actualizada sin actualizar manualmente el panel de la línea base.

* La función de vista previa de versiones del panel Historial de versiones no muestra la vista previa de un tema seleccionado.
