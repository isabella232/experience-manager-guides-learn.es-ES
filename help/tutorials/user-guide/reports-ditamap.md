---
title: Informe de mapa DITA desde el panel de mapas
description: Obtenga información sobre cómo asignar DITA informe desde el panel de mapas
source-git-commit: 8a104cfe17778a71915e3700f49fc6892493ccd0
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---


# Informe de mapa DITA desde el panel de mapas {#id205BB800EEN}

AEM guías proporciona a los administradores las capacidades de creación de informes para comprobar la integridad general de la documentación antes de publicarla o ponerla a disposición de los usuarios finales. El informe de mapa DITA del panel de mapas de AEM guías proporciona información valiosa como los temas que faltan, los temas con elementos que faltan, el UUID de temas referenciados y archivos multimedia, y el estado de revisión de cada tema. Un informe detallado de nivel de tema también proporciona información relacionada con contenido DITA, como referencias de contenido y falta de imágenes o referencias cruzadas.

>[!NOTE]
>
> AEM guías actualiza este informe sobre todos los eventos que producen un cambio en el archivo de asignación o cuando se actualiza cualquier referencia dentro del archivo de tema.

Realice los siguientes pasos para ver el informe Mapa DITA:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación DITA para el que desea ver el informe y haga clic en él.

1. Haga clic en **Informes**.

   ![](images/reports-page-uuid.png)

   La página Informes se divide en dos partes:

   - **Resumen del tema:**

      Muestra el resumen general del archivo de asignación seleccionado. Al consultar el Resumen, puede conocer rápidamente el número total de temas en el mapa, los temas que faltan, el número de temas que carecen de elementos, el estado de los temas: en borrador, en revisión o en estado revisado.

   - **Detalles:**

      Al hacer clic en un tema, se muestra un informe detallado del tema seleccionado.

      ![](images/detailed-report-uuid.png)

      Elementos resaltados en **A**, **B**, **C** y **D** se describen a continuación:

      - **Tema**: Título del tema especificado en el mapa DITA. Si pasa el puntero del ratón sobre el título del tema, se mostrará la ruta completa del tema. Si hay problemas en el tema, como la falta de referencias o imágenes, se muestra un punto rojo antes del título del tema.

      - **Nombre del archivo**: Nombre del archivo.

      - **UUID**: Identificador único universal \(UUID\) del archivo.

      - **Autor**: Usuario que trabajó último en este tema.

      - **Estado del documento**: Estado actual del documento: borrador, revisión o revisión.

      - **Temas faltantes \(B\)**: Si hay temas con referencias rotas, esos temas se enumeran en la lista de temas que faltan.

      - **Elementos que faltan**: Muestra el número de imágenes que faltan o de referencias cruzadas rotas, si las hay.

      - **Abrir en Editor \(D\)**: Al hacer clic en este icono, se abre el tema en el Editor web.

   Elementos resaltados en **E** se describen a continuación:

   - **Multimedia**: La ruta de las imágenes utilizadas en el tema se muestra junto con su UUID. Si hace clic en la ruta de la imagen, la imagen correspondiente se abre en una ventana emergente. Los vínculos de imagen rotos aparecen en color rojo.

   - **Referencias de contenido**: La ruta del contenido referido en el tema se muestra junto con su UUID. Si hace clic en el título del contenido de referencia, el tema correspondiente se abre en el modo de vista previa.

   - **Referencia cruzada**: La ruta del contenido de referencia cruzada se muestra junto con su UUID. Si hace clic en el título del contenido de referencia, el tema correspondiente se abre en el modo de vista previa. Las referencias cruzadas rotas se muestran en color rojo.

   - **Consulte**: Muestra el estado de la tarea de revisión del tema. Puede ver el estado \(abrir o cerrar\), la fecha de vencimiento y el usuario asignado para el tema que se está revisando. Si hace clic en el vínculo del tema, se abre el tema en modo de revisión.

   - **Se usa en**: Muestra una lista de otros temas o mapas donde se utiliza el tema. El UUID de todos estos temas y mapas también se enumera.



Además del informe para cada tema individual, los administradores también tienen acceso a información como el historial de publicación de un mapa DITA. Para obtener más información sobre el historial de las salidas generadas, consulte [Ver el estado de la tarea de generación de salida](generate-output-for-a-dita-map.md#viewing_output_history).

## Generar el CSV del informe de asignación DITA

Puede descargar y exportar el CSV de un informe de asignación DITA. El CSV contiene el informe de asignación DITA detallado.

Realice los siguientes pasos para generar el CSV de un informe de asignación DITA:

1. Haga clic en **Generar informe** en la parte superior izquierda para generar el informe de asignación DITA.

   ![](images/generate-DITA-map-report.png)

1. Recibirá una notificación una vez que el informe esté listo para descargarse. Haga clic en **Descargar** para descargar el CSV del informe generado.

   ![](images/download-report-dialog.png)


   También puede descargar el CSV del informe generado más adelante desde la Bandeja de entrada de notificaciones de AEM.

   Haga clic en el informe generado en la bandeja de entrada para descargar el informe.

   ![](images/report-inbox--notification.png)

Una vez descargado el informe en la Bandeja de entrada, también puede seleccionar el informe y utilizar el icono Abrir de la parte superior para abrir el informe seleccionado.

**Tema principal:**[ Informes](reports-intro.md)

