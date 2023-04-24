---
title: Descargar archivos
description: Obtenga información sobre cómo descargar archivos
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Descargar archivos {#id216MC0H0BE8}

Puede descargar recursos, incluidos archivos DITA y no DITA. Existen varias formas de descargar recursos, algunos métodos son nativos de AEM y otros son compatibles con las guías de AEM. Para obtener información de descarga de recursos AEM nativos, consulte [Descargar recursos de Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/download-assets-from-aem.html) en AEM documentación. En la siguiente sección se explica el mecanismo de descarga de archivos a través de la consola de asignación DITA en AEM guías.

## Exportación de un archivo de mapa DITA

Una vez que tenga el archivo de mapa DITA en el repositorio de AEM, puede descargar el archivo de mapa junto con sus dependientes. Esto le ofrece la flexibilidad de compartir el archivo de asignación completo para editar, validar, revisar o simplemente crear una copia de seguridad sin conexión.

Realice los siguientes pasos para descargar un archivo de asignación DITA junto con sus archivos dependientes:

1. En la interfaz de usuario de Assets, vaya al mapa DITA que desea descargar.

1. Haga clic en el mapa DITA para abrirlo en la consola de asignación DITA.

1. Seleccione el **Temas** para ver una lista de los temas disponibles en el mapa de DITA.

1. En la barra de herramientas principal, haga clic en **Descargar mapa**.

   Aparecerá el cuadro de diálogo Descargar mapa.

   ![](images/download-map.png){width="300" align="left"}

1. Haga clic en **Descargar**. En el cuadro de diálogo Descargar mapa, puede elegir las siguientes opciones:

   - **Usar línea de base**: Seleccione esta opción para obtener una lista de líneas de base creadas para el mapa DITA. Si desea descargar el archivo de mapa y su contenido en función de una línea de base específica, seleccione Línea de base en la lista desplegable. Para obtener más información sobre cómo trabajar con líneas de base, consulte [Trabajo con línea de base](generate-output-use-baseline-for-publishing.md#).
   - **Acoplar jerarquía de archivos**: Seleccione esta opción para guardar todos los temas y archivos multimedia a los que se hace referencia en una sola carpeta.

   >[!NOTE]
   >
   > También puede descargar el archivo de mapa sin seleccionar ninguna opción. En ese caso, se descarga la última versión persistente de los temas a los que se hace referencia y los archivos multimedia.

1. Después de hacer clic en el botón **Descargar** , la solicitud de descarga del mapa se pone en cola. Recibirá la siguiente notificación una vez que el mapa esté listo para descargarse.

   ![](images/download-map-prompt.png){width="550" align="left"}

   - Haga clic en **Descargar** para descargar el archivo de asignación en formato .zip.

   - Haga clic en **Descargar más tarde** para descargar el archivo de mapa más tarde. Se puede acceder al vínculo de descarga desde la bandeja de entrada de notificaciones de AEM. Haga clic en la notificación de asignación generada en la bandeja de entrada para descargar el mapa en formato .zip.
   >[!NOTE]
   >
   > De forma predeterminada, los mapas descargados permanecen durante cinco días en la Bandeja de entrada de notificaciones de AEM.

![](images/download-map-inbox.png){width="300" align="left"}

Una vez descargado el mapa, puede seleccionar el mapa y utilizar el icono Abrir de la parte superior para abrir el informe seleccionado.

**Tema principal:**[ Administrar contenido](authoring.md)

