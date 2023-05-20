---
title: Informe de mapa DITA del editor web
description: Obtenga información sobre cómo asignar informes DITA desde el editor web
exl-id: b1011cec-6374-4026-bf1c-54a1981c760e
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '1608'
ht-degree: 0%

---

# Informe de mapa DITA del editor web {#id231HF0Z0NXA}

AEM Las guías de usuario incluyen una función en el editor web que permite comprobar la integridad general de las referencias y generar informes para ellas.

Puede ver la lista de temas, administrar los metadatos de todas las referencias y ver la lista multimedia del mapa actual desde el **Informes** en el Editor Web.

## Genere un CSV desde la vista Lista de temas

El **Lista de temas** La vista proporciona información detallada sobre los temas, como el tipo de referencia, el estado del documento y el autor.

Puede crear un informe de los temas realizando los siguientes pasos:

1. En el **Repositorio** , abra el fichero de mapa DITA en la vista Mapa.
1. Haga clic en **Administrar** pestaña.
1. Doble clic **Lista de temas** a la izquierda. Se mostrará la lista de temas presentes en el mapa DITA.

   ![](images/web-editor-topiclist-panel.png){width="800" align="left"}

1. Desde el **Filtros** Panel: puede filtrar los temas en función de la variable **Tipo de referencia** \(directo o indirecto\), **Estado del documento** \(estado actual de los temas. Por ejemplo, si los temas están en estado Editar, En revisión o Revisado, se muestran\) o el **Autor** del tema.

1. También puede utilizar las siguientes opciones de filtrado de temas para elegir mostrar las siguientes columnas en la lista:

   - **Tema** El título del tema se especifica en el mapa DITA. Puede hacer clic en el tema para editarlo.
   - **Nombre de archivo** Nombre del archivo.
   - **UUID** El identificador único universal \(UUID\) del archivo.
   - **Ubicación del archivo** Ruta de acceso completa del tema.
   - **Tipo de referencia** El tipo de referencia: directa o indirecta.
   - **Estado del documento** Estado actual del tema.
   - **Autor** El usuario que trabajó por última vez en el tema.
   - **Mapa principal** La lista de todos los mapas en los que se hace referencia directamente al tema.

   >[!NOTE]
   >
   > Clic **Actualizar** para obtener una nueva lista de temas y ver los cambios en el archivo de asignación o si se actualiza alguna referencia en el archivo de temas.

1. Clic **Descargar CSV** para descargar la instantánea actual de los temas del mapa DITA. El archivo CSV contiene las columnas seleccionadas y los temas filtrados en la **Lista de temas** vista. A continuación, puede abrir este archivo CSV de lista de temas en cualquier editor CSV.

**Administrar metadatos por lotes desde el informe Metadatos**

AEM Guías de le permite etiquetar contenido DITA desde el editor web. Puede aplicar etiquetas a un tema individual o utilizar la función de etiquetado masivo para aplicar varias etiquetas a varios temas, a un mapa DITA o a un submapa. También puede cambiar el estado del documento de todos los temas seleccionados al siguiente estado común posible del documento.

## Ver metadatos

Para ver los metadatos de las referencias en el mapa DITA actual, realice los siguientes pasos:

1. En el panel Repositorio, abra el fichero de mapa DITA en la vista Mapa.
1. Haga clic en **Administrar** pestaña.
1. Doble clic **Metadatos** a la izquierda. Se mostrará la lista de metadatos de todas las referencias del mapa DITA. Esto incluye también las referencias de medios.

   ![](images/web-editor-metadata-panel.png){width="800" align="left"}

1. Desde el **Filtros** panel, puede filtrar los temas en función de la variable **Estado del documento** \(estado actual de los temas. Por ejemplo, si los temas están en estado Editar, En revisión o Revisado, se muestran\), **Referencias** \(directo o indirecto\), **Tipo de archivo** \(Mapa, Tema e Imagen\) de la referencia.
1. También puede elegir ver solo la variable **Archivos sin etiquetas** o también elegir etiquetas específicas de la **Etiquetas** filtre para ver los archivos asociados a ellos.
   1. También puede utilizar las siguientes opciones de filtrado de temas para elegir mostrar las siguientes columnas en la lista de metadatos:
      - **Título** \(seleccionado de forma predeterminada\) El título del fichero al que se hace referencia se especifica en el mapa DITA. Puede hacer clic en el archivo para editarlo.También puede hacer clic en un archivo de audio o vídeo y reproducirlo en el Editor Web. Puede cambiar el volumen o la vista del vídeo. En el menú contextual también tiene las opciones para descargar, cambiar la velocidad de reproducción o ver la imagen en la imagen.

         >[!NOTE]
         >
         > También aparece un icono de desprotección cerca del título de un archivo desprotegido. Puede pasar el ratón sobre el icono para ver el nombre del usuario.

      - **Nombre de archivo** Nombre del archivo.
      - **Ubicación del archivo** Ruta de acceso completa del archivo.
      - **Etiquetas** \(seleccionado de forma predeterminada\) Etiquetas aplicadas al archivo.

         >[!NOTE]
         >
         > De forma predeterminada, puede ver dos etiquetas para un archivo. Para ver más etiquetas, haga clic en **Mostrar más**. Clic **Mostrar menos** para volver a contraer la lista.

      - **Tipo de referencia** El tipo de referencia: directa o indirecta
      - **Estado del documento** \(seleccionado de forma predeterminada\) Estado actual del archivo de referencia.
      - **Tipo de archivo** \(seleccionado de forma predeterminada\) Tipo de archivo de origen. Las opciones disponibles son Mapa, Tema e Imagen.
      - **Extraído por** El usuario que ha desprotegido el archivo.
1. Clic **Descargar CSV** para descargar la instantánea actual de las referencias en el mapa DITA. El CSV contiene las columnas seleccionadas y las referencias filtradas en la vista Lista de temas. A continuación, puede abrir este archivo CSV de metadatos en cualquier editor CSV.

**Actualización de metadatos**

1. Para actualizar los metadatos, seleccione los archivos que desea actualizar.

   >[!NOTE]
   >
   > No puede seleccionar ningún archivo desprotegido. También aparece un icono de desprotección cerca del título de un archivo desprotegido. Puede pasar el ratón sobre el icono para ver el nombre del usuario.

1. Seleccionar **Administrar** desde arriba.

   ![](images/web-editor-manage-metadata.png){width="350" align="left"}

1. Si desea añadir nuevas etiquetas, seleccione nuevas etiquetas en la lista desplegable para aplicarlas a todos los temas seleccionados. También puede eliminar cualquier etiqueta haciendo clic en el icono en forma de cruz situado cerca de la etiqueta.

   >[!NOTE]
   >
   > Se muestran las etiquetas comunes aplicadas en todos los temas seleccionados.

1. Seleccione un nuevo estado de documento si desea cambiar el estado del documento de todas las referencias seleccionadas. La lista desplegable muestra el estado posible común de todos los temas seleccionados. Por ejemplo, si el estado actual de los temas es En revisión, podrá ver los estados Borrador, Aprobado o Revisado.
1. Clic **Actualizar** para actualizar los metadatos. Se muestra un mensaje de confirmación para los metadatos, tanto si se actualizan correctamente como si tienen actualizaciones fallidas. También puede hacer clic en **Descargar informe** para descargar el CSV de metadatos desde el cuadro de diálogo de confirmación. Este CSV contiene los detalles del estado de actualización de las referencias seleccionadas.

## Generación de un informe multimedia

El **Multimedia** Este informe proporciona información detallada sobre los archivos multimedia utilizados en el mapa, como el título, el tipo \(audio, vídeo e imágenes\), los archivos en los que se utiliza multimedia y el tipo de referencia de los archivos en los que se han utilizado. También puede ver el UUID y la ubicación del contenido multimedia dentro del repositorio. Puede crear un informe del contenido multimedia realizando los siguientes pasos:

1. En el **Repositorio** , abra el fichero de mapa DITA en la vista Mapa.
1. Haga clic en **Administrar** pestaña.
1. Doble clic **Multimedia** a la izquierda. Se mostrará la lista de elementos multimedia presentes en el mapa DITA.
1. Desde el **Filtros** panel puede ordenar la lista por multimedia o por los nombres de utilizados en las referencias.

   - Cuando realiza un pedido por **Multimedia**, el **** del contenido multimedia se muestra en la primera columna y, a continuación, los nombres de todas las referencias en las que se han utilizado se muestran en otra columna de la misma fila. Por ejemplo, la siguiente captura de pantalla muestra el archivo multimedia WarmCoolForC.gif en la primera columna y las tres referencias en las que se utiliza se muestran en la tercera columna de la misma fila.

      ![](images/multimedia-report-file-order.png){width="650" align="left"}

   - Si realiza un pedido por **Utilizado en** columna, verá la vista transpuesta en la que los nombres de las referencias en las que se ha utilizado multimedia se enumeran en la primera columna, mientras que los nombres multimedia se enumeran en otra columna en filas separadas. Por ejemplo, la siguiente captura de pantalla muestra los nombres de tres referencias \(Ajuste de la temperatura del asiento, Cambio de la visualización de la temperatura del asiento y Área de tripulación\) en la primera columna y el archivo multimedia WarmCoolForC.gif se muestra en la tercera columna en tres filas independientes.

      ![](images/multimedia-report-used-in-order.png){width="650" align="left"}

1. Puede filtrar su contenido multimedia en función de las **Tipo multimedia**, y **Tipo de referencia**. La lista de archivos multimedia se muestra en función de su selección en la lista desplegable. Por ejemplo, se puede elegir mostrar sólo las referencias de audio en el mapa DITA y un fichero sólo muestra las referencias de audio utilizadas en él.

   >[!NOTE]
   >
   > Según el tipo de multimedia que se use en el mapa, la imagen, el vídeo y el audio se enumeran en la **Tipo multimedia** y Directas o Indirectas aparecen en la lista desplegable de. **Tipo de referencia** desplegable.

1. También puede utilizar las siguientes opciones de filtrado para elegir mostrar las siguientes columnas en la lista:

   - **Multimedia** \(seleccionado de forma predeterminada\) El título del contenido multimedia se especifica en el mapa DITA. Puede hacer clic en el contenido multimedia para editarlo.
   - **Ubicación multimedia** La ruta completa del contenido multimedia.
   - **UUID multimedia** El identificador único universal \(UUID\) del archivo.
   - **Tipo multimedia** \(seleccionado de forma predeterminada\) Tipo de multimedia. Las opciones disponibles son Audio, Vídeo o Imagen.
   - **Utilizado en** \(seleccionado de forma predeterminada\) Las referencias en las que se ha utilizado el contenido multimedia. Puede hacer clic en la referencia para editarla.
   - **Tipo de referencia** \(seleccionado de forma predeterminada\) El tipo de referencia: directo o indirecto.

   >[!NOTE]
   >
   > Clic **Actualizar** para obtener una lista nueva de contenido multimedia y ver los cambios realizados en el archivo de mapa o si se ha actualizado algún contenido multimedia del mapa DITA.

1. También puede hacer clic en un archivo de audio o vídeo y reproducirlo en el Editor Web. Puede cambiar el volumen o la vista del vídeo. En el menú contextual también tiene las opciones para descargar, cambiar la velocidad de reproducción o ver la imagen en la imagen.

   ![](images/video-web-editor.png){width="800" align="left"}

1. Clic **Descargar CSV** para descargar la instantánea actual del contenido multimedia en el mapa DITA. El CSV contiene las columnas seleccionadas y el contenido multimedia filtrado en la **Multimedia** vista. A continuación, puede abrir este archivo CSV multimedia en cualquier editor CSV.

**Tema principal:**[ Informes](reports-intro.md)
