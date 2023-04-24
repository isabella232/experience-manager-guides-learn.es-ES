---
title: Informe de reutilización de contenido
description: Descubra más información sobre el informe de reutilización de contenido
source-git-commit: bb7a8d49e5425b7fc856277c054558c75394fcb2
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Informe de reutilización de contenido {#id205BB900OQD}

Otro informe útil que puede generar es el informe de reutilización de contenido. Este informe calcula el porcentaje promedio de uso del contenido, lo que resulta muy útil para los administradores de proyectos y propietarios de empresas a la hora de ver la cantidad de contenido que se está reutilizando.

>[!TIP]
>
> Para garantizar el correcto funcionamiento del informe de reutilización de contenido, debe habilitar el flujo de trabajo posterior al procesamiento. Póngase en contacto con el administrador del sistema para activar los flujos de trabajo posteriores al procesamiento.

Siga estos pasos para ver el informe de reutilización de contenido:

1. Haga clic en el vínculo Adobe Experience Manager en la parte superior y elija **Herramientas**.

1. Select **Guías** de la lista de herramientas.

1. Haga clic en el **Informe de reutilización de contenido** mosaico.

1. Haga clic en **Examinar** para elegir una ruta en la que se encuentren los temas o introduzca la ruta manualmente.

   El informe se genera analizando el contenido en las carpetas principales y en todas las carpetas secundarias.

1. Haga clic en **Generar informe** para obtener el informe de reutilización de contenido.

   ![](images/content-reuse-uuid.png)

   La página del informe se divide en dos partes:

   - **Resumen del informe:**

      Enumera la reutilización promedio del contenido, que se calcula como instancias de reutilización del contenido/recuento total de temas. Este informe tiene en cuenta todas las referencias de contenido directo de primer nivel y las referencias de tema para el cálculo. Las instancias de reutilización de contenido se calculan como el total de la suma de valores en el campo Número de veces que se ha reutilizado . El tema que se reutiliza más ampliamente también se enumera en el resumen del informe. Al hacer clic en el vínculo del tema en el tema más reutilizado, se abre la vista previa del tema.

   - **Detalles:**

      La sección Detalles contiene las columnas siguientes:

      - **Título**: Título del tema. Al hacer clic en el vínculo de título del tema, se abre la vista previa del tema.

      - **UUID**: Identificador único universal \(UUID\) del archivo.

      - **Tamaño**: Tamaño de los archivos en bytes.

      - **Estado**: Estado actual del documento: borrador, revisión o revisión.

      - **Número de veces que se reutiliza**: Número de veces que se ha reutilizado el tema correspondiente. Esto se calcula como el total de la suma de las entradas en las columnas a las que se hace referencia menos 1.

      - **Referenciado por**: Temas en los que se hace referencia al tema correspondiente. En este caso, solo se tienen en cuenta las referencias directas \(primer nivel\). Los temas múltiples están separados por coma. El UUID del archivo al que se hace referencia también se menciona entre corchetes. Al hacer clic en el vínculo de título del tema, se abre la vista previa del tema.


>[!NOTE]
>
> También puede exportar el informe de reutilización de contenido en formato CSV. Para ello, haga clic en el vínculo Export to CSV en la esquina superior izquierda de la pantalla y elija una ubicación para guardar el archivo CSV. A continuación, puede abrir este archivo CSV en cualquier editor CSV.

**Tema principal:**[ Informes](reports-intro.md)

