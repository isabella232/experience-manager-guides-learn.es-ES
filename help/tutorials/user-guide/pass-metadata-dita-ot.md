---
title: Pasa los metadatos a la salida utilizando DITA-OT
description: Aprenda a pasar los metadatos a la salida utilizando DITA-OT
source-git-commit: 8b6294425c6e60d1c5b37d98e99114014a104ee6
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# Pasa los metadatos a la salida utilizando DITA-OT {#id21BJ00QD0XA}

Los metadatos son información adicional sobre el resultado. En AEM guías puede pasar los metadatos existentes o crear etiquetas de metadatos personalizadas. Puede transferir metadatos a AEM, PDF, HTML5, EPUB y salidas de formato personalizado mediante la publicación DITA-OT.

Realice los siguientes pasos para pasar los metadatos a la salida mediante la publicación DITA-OT:

1. En el **IU de recursos**, navegue hasta el archivo de asignación DITA para el que desea pasar los metadatos a DITA-OT y haga clic en él.
1. Seleccione y edite un ajuste preestablecido de salida al que desee pasar los campos de metadatos. Por ejemplo, seleccione el ajuste preestablecido de salida del PDF.
1. Select **DITA-OT** en Generar &lt;output> Uso de la opción en el ajuste preestablecido de salida seleccionado.

   ![](images/custom-meta-data-output-preset.png)

1. En el menú desplegable Propiedades , seleccione los metadatos que desea pasar a la publicación DITA-OT.

   La lista desplegable Propiedades muestra las propiedades personalizadas y las predeterminadas. Por ejemplo, en la captura de pantalla anterior, el autor es la propiedad personalizada mientras `dc:description`, `dc:language`, `dc:title`y `docstate` son las propiedades predeterminadas.

   >[!NOTE]
   >
   > Estas propiedades se eligen del archivo metadataList disponible en la siguiente ubicación:`/libs/fmdita/config/metadataList`. De forma predeterminada, hay cuatro propiedades enumeradas en este archivo: `dc:description`, `dc:language`, `dc:title`y `docstate`.

   Este archivo se puede superponer en: `/apps/fmdita/config/metadataList`.

   Para pasar una propiedad personalizada para la que ya haya definido los valores, consulte [Utilizar metadatos de AEM en la salida del PDF DITA-OT](https://experienceleaguecommunities.adobe.com/t5/xml-documentation-discussions/use-aem-metadata-in-dita-ot-pdf-output/td-p/411880).

1. En el **Propiedades** , seleccione las propiedades personalizadas y predeterminadas necesarias. Por ejemplo, seleccione `author`, `dc:title`y `dc:description`. Son las `metadata/properties` que se crea una vez que creamos un archivo. Las propiedades seleccionadas se muestran debajo del cuadro desplegable.

   ![](images/selected-metadata-properties.png)

1. Haga clic en **Listo** en la parte superior izquierda para guardar los cambios.
1. Genere la salida.

Las propiedades de metadatos seleccionadas se pasarán a la salida generada mediante DITA-OT.

**Tema principal:**[ Generación de resultados](generate-output.md)

