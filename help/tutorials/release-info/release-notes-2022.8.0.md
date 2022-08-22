---
title: Notas de la versión | Guías de Adobe Experience Manager as a Cloud Service, versión de agosto de 2022
description: Última versión de las guías de Adobe Experience Manager as a Cloud Service
source-git-commit: 7cc33e4621c2bfbf08a720f173e8e419c5424a6c
workflow-type: tm+mt
source-wordcount: '1156'
ht-degree: 2%

---

# Última versión de las guías de Adobe Experience Manager as a Cloud Service

## Actualice a la última versión

Actualice las guías actuales de Adobe Experience Manager as a Cloud Service (más adelante, *Guías AEM as a Cloud Service*) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2022.8.167.
3. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la última versión de AEM guías as a Cloud Service.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por AEM Guías as a Cloud Service para la versión de agosto de 2022.

### FrameMaker y FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| No compatible | Actualización 4 y posterior de 2020 |
|  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

### Conector de oxígeno

| AEM guías como una versión en la nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac |
| --- | --- | --- |
| 2022.8.0 | 2,7,5 | 2,7,5 |
|  |  |  |


## Nuevas funciones y mejoras

AEM guías as a Cloud Service proporciona muchas mejoras y nuevas funciones en la última versión:

### Vista Diseño en el Editor de mapas

Ahora puede ver el diseño completo de un mapa DITA en el Editor de mapas. Cuando se abre un mapa para editarlo, se abre la variable **Diseño** vista del Editor de mapas. En esta vista, puede ver la jerarquía del mapa en una vista de árbol y también organizar o estructurar los temas en un mapa.

![vista de diseño](assets/layout-view-map.png)

La vista Diseño contiene una barra de herramientas independiente que le ayuda a realizar muchas tareas sobre los temas presentes en un mapa.
Puede insertar referencias de temas, grupos de temas y definiciones de claves en un mapa. Puede reorganizar los temas presentes en un mapa moviéndolos hacia arriba, hacia abajo, hacia la izquierda o hacia la derecha. También puede arrastrar y soltar los temas para moverlos en un mapa. El Editor de mapas también proporciona los iconos para bloquear o desbloquear archivos, comprobar el historial de versiones y realizar una administración de etiquetas de versiones.


La vista Diseño también proporciona la variable **Opciones de vista** para mostrar u ocultar el número de línea, muestre u oculte la casilla de verificación o muestre el nombre o título del archivo para los temas de un mapa.


![opciones de vista](assets/view-options.png)

También puede ver los temas en función de los filtros condicionales aplicados a ellos.

Además de organizar los temas en el archivo de mapa, también puede agregar, mover, copiar, pegar o eliminar referencias utilizando la variable **Opciones** para un elemento en la vista Presentación. También puede arrastrar y soltar un tema o un mapa desde el panel del repositorio al mapa abierto en el Editor de mapas.

El panel derecho muestra las Propiedades de contenido y las Propiedades de mapa en la vista Diseño del Editor de mapas. Los Atributos en línea definidos para el tema seleccionado se muestran en relación con el tema en la vista Diseño. Por ejemplo, puede encontrar rápidamente todos los temas que tengan el atributo platform definido como `IOS`.

Ahora también puede establecer la información de metadatos para los temas o el mapa. Puede definir el título de navegación, el texto del vínculo, la descripción corta y las palabras clave para el tema o mapa seleccionado.

![vista de diseño panel derecho](assets/layout-inline-attributes.png)

Para obtener más información, consulte *Vista Diseño* en Uso de las guías de Adobe Experience Manager as a Cloud Service.

### Atributos en línea en la configuración del editor

AEM guías ahora permite la configuración de **Atributos en línea** por su administrador de **Configuración del editor**. También puede agregar nuevos atributos en línea o eliminar los existentes del **Atributos en línea** en la Configuración del editor.
Los Atributos en línea configurados definidos para un tema se muestran en relación con el tema en la vista Diseño.

![Configuración del editor](assets/editor-settings-inline-attributes.png)


### Filtros adicionales en la vista Repositorio

Ahora la búsqueda de filtros en la vista del repositorio se ha vuelto más poderosa. Dos nuevos criterios de búsqueda, **Última modificación** y **Etiquetas** para filtrar los archivos y limitar la búsqueda en el repositorio de AEM:
* **Última modificación**: Puede buscar archivos que se hayan modificado por última vez después de una fecha seleccionada pero antes de una fecha seleccionada. También tiene la opción de usar los criterios predefinidos y buscar archivos que hayan sido modificados por última vez en las últimas 2 horas, la última semana, el último mes o el último año.
* **Etiquetas**: También puede buscar archivos que tengan etiquetas específicas aplicadas a ellos. Puede escribir la etiqueta o seleccionarla en la lista desplegable.

![Filtros de vista del repositorio](assets/repo-filter-search.png)


## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* El índice Lucene obsoleto se utiliza en /core/article-publish/src/main/java/com/adobe/dxml/article/publish/util/DoxUtils.java (9291)
* Node.js actualizado no se utiliza para la publicación. (9835)
* El tema DITA no se actualiza automáticamente con los cambios realizados en la variable **Propiedades** página. (8745)
* El elemento de materia frontal cuando se añade a un mapa de datos DITA no funciona correctamente. (9507)
* PDF nativo | Se genera un PDF en blanco al usar **Generación rápida** para varios archivos cuando se selecciona un elemento vacío. (9822)
* PDF nativo | El apéndice se publica como capítulo en la salida del PDF. (9829)
* PDF nativo | Cuando se edita una imagen de SVG, no se muestra actualizada en el diseño de página. (9069)
* Se inserta un carácter de guión normal al `Nonbreaking Hyphen` se inserta utilizando **Insertar carácter especial** diálogo. (8919)
* El Editor XML no muestra imágenes actualizadas en los temas si se han editado. (9500)
* Al publicar la salida a través del Editor, los ajustes preestablecidos no se pueden eliminar de la variable **Salida** pestaña . (9100)
* Los submapas de un mapa DITA no se extraen usando la variable **Seleccionar todo** en el menú elipsis. (9814)
* No se pueden arrastrar y soltar plantillas de asignación o tema desde el **Plantillas** a la plantilla de asignación personalizada en el editor web. (9846)
* No se puede crear un nuevo tema o plantilla de asignación en la subcarpeta de una plantilla de mapa o tema. (9888)
* No hay ninguna opción presente para examinar los temas o mapas presentes dentro de las subcarpetas de un mapa o plantilla de tema. (9889)
* Cuando se actualiza y guarda un archivo de esquema junto con el archivo DITA, no se muestra el panel derecho (si el archivo DITA rompe las validaciones presentes en el archivo de esquema). (9986)
* Se puede crear un nuevo ajuste preestablecido de salida duplicado si su nombre es el mismo que un ajuste preestablecido existente. (9997)
* Las imágenes SVG se dañan y no se publican correctamente al generar la salida del HTML. (9949)


## Problemas conocidos

Adobe ha identificado los siguientes problemas conocidos de AEM Guías as a Cloud Service para la versión de agosto de 2022.

### Problemas conocidos con la solución alternativa

Utilice la solución dada para los siguientes problemas conocidos:

* La vista Diseño no está visible en el Editor de mapas.

   **Solución alternativa**: Actualice ui_config.json en el perfil de carpeta.

* Symbols.json está anulado, por lo que se produce el problema 8919.

   **Solución alternativa**: Los símbolos.json actualizados deben combinarse con símbolos.json anulados.

### Otros problemas conocidos

* Si se seleccionan varios archivos de la sección de resultados mostrada al realizar una búsqueda en el repositorio y después arrastrados en la vista de autor, solo se añade un solo archivo.
