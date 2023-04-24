---
title: Informe de mapa DITA del Editor web
description: Obtenga información sobre cómo asignar DITA informe desde el Editor web
source-git-commit: 895d9bd3587c871d5223df5b71403d10bdc3d762
workflow-type: tm+mt
source-wordcount: '1608'
ht-degree: 0%

---


# Informe de mapa DITA del Editor web {#id231HF0Z0NXA}

AEM guías incluye una función en el Editor web que permite comprobar la integridad general de las referencias y generar informes para ellas.

Puede ver la lista de temas, administrar los metadatos de todas las referencias y ver la lista multimedia del mapa actual desde el **Informes** en el Editor web.

## Generar un CSV desde la vista Lista de temas

La variable **Lista de temas** la vista proporciona información detallada sobre sus temas, como el tipo de referencia, el estado del documento y el autor.

Puede crear un informe de los temas siguiendo estos pasos:

1. En el **Repositorio** , abra el archivo de asignación DITA en la vista Mapa.
1. Haga clic en el **Administrar** pestaña .
1. Hacer doble clic **Lista de temas** a la izquierda. Se muestra la lista de temas presentes en el mapa DITA.

   ![](images/web-editor-topiclist-panel.png)

1. En el **Filtros** El panel le permite filtrar los temas en función de la variable **Tipo de referencia** \(directo o indirecto\), **Estado del documento** \ (estado actual de los temas). Por ejemplo, si los temas están en estado Editar, En revisión o Revisado, se enumeran\) o **Autor** del tema.
1. También puede utilizar las siguientes opciones de filtrado de temas para elegir mostrar las siguientes columnas en la lista:

   - **Tema** El título del tema se especifica en el mapa DITA. Puede hacer clic en el tema para editarlo.
   - **Nombre del archivo** Nombre del archivo.
   - **UUID** Identificador único universal \(UUID\) del archivo.
   - **Ubicación del archivo** Ruta completa del tema.
   - **Tipo de referencia** Tipo de referencia: directa o indirecta.
   - **Estado del documento** Estado actual del tema.
   - **Autor** El usuario que trabajó último en el tema.
   - **Mapa principal** Lista de todos los mapas donde se hace referencia directa al tema.

   >[!NOTE]
   >
   > Haga clic en **Actualizar** para obtener una nueva lista de temas y ver cualquier cambio en el archivo de mapa o si se actualiza cualquier referencia dentro del archivo de temas.

1. Haga clic en **Descargar CSV** para descargar la instantánea actual de los temas en el mapa de DITA. El CSV contiene las columnas seleccionadas y los temas filtrados en la variable **Lista de temas** vista. A continuación, puede abrir este archivo CSV de lista de temas en cualquier editor CSV.

**Administrar metadatos de forma masiva desde el informe Metadatos**

AEM guías le permite etiquetar contenido DITA desde el editor web. Puede aplicar etiquetas en un tema individual o utilizar la función de etiquetado masivo para aplicar varias etiquetas en varios temas, un mapa DITA o en un submapa. También puede cambiar el estado del documento de todos los temas seleccionados al siguiente estado de documento común posible.

## Ver metadatos

Para ver los metadatos de las referencias en el mapa DITA actual, realice los siguientes pasos:

1. En el panel Repositorio, abra el archivo de asignación DITA en la vista Mapa.
1. Haga clic en el **Administrar** pestaña .
1. Hacer doble clic **Metadatos** a la izquierda. Se muestra la lista de metadatos de todas las referencias del mapa DITA. Esto incluye también las referencias de medios.

   ![](images/web-editor-metadata-panel.png)

1. En el **Filtros** , puede filtrar los temas en función de la variable **Estado del documento** \ (estado actual de los temas). Por ejemplo, si los temas están en estado Editar, En revisión o Revisado, se enumeran\), **Referencias** \(directo o indirecto\), **Tipo de archivo** \(Mapa, Tema e Imagen\) de la referencia.
1. También puede elegir ver solo la variable **Archivos sin etiquetas** o también elija etiquetas específicas en la **Etiquetas** para ver los archivos asociados a ellos.
   1. También puede utilizar las siguientes opciones de filtrado de temas para elegir mostrar las siguientes columnas en la lista de metadatos:
      - **Título** \(seleccionado de forma predeterminada\) El título del archivo al que se hace referencia se especifica en el mapa DITA. Puede hacer clic en el archivo para editarlo. También puede hacer clic y reproducir un archivo de audio o vídeo en el Editor web. Puede cambiar el volumen o la vista del vídeo. En el menú de accesos directos también tiene las opciones para descargar, cambiar la velocidad de reproducción o ver la imagen en imagen.

         >[!NOTE]
         >
         > También aparece un icono de desprotección cerca del título de un archivo extraído. Puede situarse sobre el icono para ver el nombre del usuario.

      - **Nombre del archivo** Nombre del archivo.
      - **Ubicación del archivo** Ruta de acceso completa del archivo.
      - **Etiquetas** \(seleccionado de forma predeterminada\) Etiquetas aplicadas al archivo.

         >[!NOTE]
         >
         > De forma predeterminada, puede ver dos etiquetas para un archivo. Para ver más etiquetas, haga clic en **Mostrar más**. Haga clic en **Mostrar menos** para volver a contraer la lista.

      - **Tipo de referencia** Tipo de referencia: directa o indirecta
      - **Estado del documento** \(seleccionado de forma predeterminada\) El estado actual del archivo de referencia.
      - **Tipo de archivo** \(seleccionado de forma predeterminada\) Tipo del archivo de origen. Las opciones disponibles son Mapa, Tema e Imagen.
      - **Protegido por** El usuario que ha extraído el archivo.
1. Haga clic en **Descargar CSV** para descargar la instantánea actual de las referencias en el mapa DITA. El CSV contiene las columnas seleccionadas y las referencias filtradas en la vista Lista de temas. A continuación, puede abrir este archivo CSV de metadatos en cualquier editor CSV.

**Actualización de metadatos**

1. Para actualizar los metadatos, seleccione los archivos para los que desea actualizar.

   >[!NOTE]
   >
   > No puede seleccionar ningún archivo extraído. También aparece un icono de desprotección cerca del título de un archivo extraído. Puede situarse sobre el icono para ver el nombre del usuario.

1. Select **Administrar** desde arriba.

   ![](images/web-editor-manage-metadata.png)

1. Si desea agregar nuevas etiquetas, seleccione nuevas etiquetas en la lista desplegable para aplicarlas a todos los temas seleccionados. También puede eliminar cualquier etiqueta haciendo clic en el icono de cruz situado cerca de la etiqueta .

   >[!NOTE]
   >
   > Se muestran las etiquetas comunes aplicadas a todos los temas seleccionados.

1. Seleccione un nuevo estado de documento si desea cambiar el estado del documento de todas las referencias seleccionadas. La lista desplegable muestra el estado común posible de todos los temas seleccionados. Por ejemplo, si el estado actual de los temas es Revisión, puede ver el estado Borrador, Aprobado o Revisado.
1. Haga clic en **Actualizar** para actualizar los metadatos. Se muestra un mensaje de confirmación para los metadatos, tanto si se ha actualizado correctamente como si hay actualizaciones fallidas. También haga clic en **Descargar informe** para descargar el CSV de metadatos desde el cuadro de diálogo de confirmación. Este CSV contiene los detalles del estado de actualización de las referencias seleccionadas.

## Generar un informe multimedia

La variable **Multimedia** El informe proporciona información detallada sobre el contenido multimedia que se utiliza en el mapa, como el título, el tipo \(audio, vídeo e imágenes\), los archivos en los que se utiliza contenido multimedia y el tipo de referencia de los archivos, en los que se han utilizado. También puede ver el UUID y la ubicación del contenido multimedia dentro del repositorio. Puede crear un informe del contenido multimedia siguiendo estos pasos:

1. En el **Repositorio** , abra el archivo de asignación DITA en la vista Mapa.
1. Haga clic en el **Administrar** pestaña .
1. Hacer doble clic **Multimedia** a la izquierda. Se muestra la lista de multimedia presente en el mapa DITA.
1. En el **Filtros** puede ordenar la lista por contenido multimedia o por los nombres de usados en referencias.

   - Cuando realiza el pedido **Multimedia**, el nombre****del contenido multimedia se muestra en la primera columna y, a continuación, los nombres de todas las referencias en las que se han utilizado, se muestran en otra columna de la misma fila. Por ejemplo, la siguiente captura de pantalla muestra el WarmCoolForC.gif multimedia en la primera columna y tres referencias en las que se utiliza, se muestran en la tercera columna de la misma fila.

      ![](images/multimedia-report-file-order.png)

   - Si realiza el pedido por **Se usa en** , verá la vista transpuesta donde los nombres de las referencias en las que se han utilizado multimedia se enumeran en la primera columna, mientras que los nombres multimedia se enumeran en otra columna en filas independientes. Por ejemplo, la siguiente captura de pantalla muestra los nombres de las tres referencias \(Ajuste de la temperatura del asiento, Cambio de la visualización de la temperatura del asiento y Área de la tripulación\) en la primera columna y el elemento multimedia WarmCoolForC.gif se muestra en la tercera columna en tres filas independientes.

      ![](images/multimedia-report-used-in-order.png)

1. Puede filtrar el contenido multimedia en función de la variable **Tipo multimedia** y **Tipo de referencia**. La lista de archivos multimedia se muestra en función de su selección en la lista desplegable . Por ejemplo, puede elegir mostrar solo las referencias de audio en el mapa DITA, y un archivo muestra solamente las referencias de audio utilizadas en él.

   >[!NOTE]
   >
   > Según el tipo de multimedia utilizado en el mapa, las imágenes, los vídeos y el audio se enumeran en la **Tipo multimedia** y Directo o Indirecto aparecen en la lista desplegable **Tipo de referencia** lista desplegable.

1. También puede utilizar las siguientes opciones de filtrado para elegir mostrar las columnas siguientes en la lista:

   - **Multimedia** \(seleccionado de forma predeterminada\) El título del contenido multimedia se especifica en el mapa DITA. Puede hacer clic en el contenido multimedia para editarlo.
   - **Ubicación multimedia** Ruta completa del contenido multimedia.
   - **UUID multimedia** Identificador único universal \(UUID\) del archivo.
   - **Tipo multimedia** \(seleccionado de forma predeterminada\) Tipo del contenido multimedia. Las opciones disponibles son Audio, Vídeo o Imagen.
   - **Se usa en** \(seleccionado de forma predeterminada\) Las referencias en las que se ha utilizado el contenido multimedia. Puede hacer clic en la referencia para editarla.
   - **Tipo de referencia** \(seleccionado de forma predeterminada\) El tipo de referencia: directa o indirecta.

   >[!NOTE]
   >
   > Haga clic en **Actualizar** para obtener una nueva lista de multimedia y ver cualquier cambio en su archivo de mapa o si se actualiza cualquier multimedia dentro de su mapa DITA.
1. También puede hacer clic y reproducir un archivo de audio o vídeo en el Editor web. Puede cambiar el volumen o la vista del vídeo. En el menú de accesos directos también tiene las opciones para descargar, cambiar la velocidad de reproducción o ver la imagen en imagen.
   ![](images/video-web-editor.png)

1. Haga clic en **Descargar CSV** para descargar la instantánea actual del contenido multimedia en el mapa de DITA. El CSV contiene las columnas seleccionadas y el contenido multimedia filtrado en la variable **Multimedia** vista. A continuación, puede abrir este archivo CSV multimedia en cualquier editor CSV.

**Tema principal:**[ Informes](reports-intro.md)

