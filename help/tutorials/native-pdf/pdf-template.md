---
title: Creación y personalización de plantillas de PDF nativas
description: Obtenga información sobre cómo crear y personalizar plantillas de PDF nativas.
exl-id: 7660da8e-8a1e-4493-b99b-9b5de9a7483f
source-git-commit: 49fa930483f48cafd057002ee26c9499ce967c60
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# plantilla de PDF {#PDF-template}

El uso de una plantilla garantiza la coherencia en el diseño y la estructura del contenido. Como las plantillas están predefinidas, puede evitar volver a trabajar en los problemas de formato que surgen para cada proyecto nuevo o actualización. Las plantillas permiten diseñar diseños de página, aplicar estilos al contenido y aplicar diversas configuraciones para personalizar el PDF.

Aunque los autores pueden utilizar los ajustes preestablecidos de PDF para generar resultados, los desarrolladores pueden crear sus propias plantillas. Hay plantillas de muestra listas para usar, que los desarrolladores pueden personalizar o duplicar aún más según sus requisitos organizativos.


## Creación de una nueva plantilla de PDF {#create-pdf-template}

Puede crear plantillas de PDF personalizadas con diseños de página específicos y definir el formato para los componentes del diseño de página (como TDC, índice, glosario) o los componentes DITA (como encabezado, párrafo, lista) mediante hojas de estilo. Puede crear una nueva plantilla desde cero o crearla con una plantilla de ejemplo.

Para crear una nueva plantilla de PDF, siga los siguientes pasos:
1. En el Editor Web, vaya a **Output** pestaña.
1. Expanda la barra lateral izquierda y seleccione **Plantillas**.
<img src="assets/create-pdf-template.png" alt="Crear plantilla de PDF" width="400">
1. En el panel **Plantillas**, seleccione el icono **+** situado junto a **Plantillas** y elija **Plantilla de PDF **.
1. Especifique un nombre para la plantilla en el cuadro de diálogo **Nueva plantilla**.
1. Haga clic en **Listo**.

La nueva plantilla se crea y se agrega en *Plantillas* panel.

## Duplicación de una plantilla de PDF {#duplicate-pdf-template}

Si desea crear una nueva plantilla con los mismos diseños de página y formato que los de una plantilla existente, puede crear una copia. Una vez duplicada una plantilla, puede personalizar aún más sus componentes según sea necesario.

Para duplicar una plantilla de PDF existente, siga los siguientes pasos:
1. En el Editor Web, vaya a **Output** pestaña.
1. Expanda la barra lateral izquierda y seleccione **Plantillas**.

   Se abrirá el panel Plantillas.
1. Pase el ratón sobre la plantilla que quiera duplicar y seleccione la opción (*Opciones* icon) **...** y elija **Duplicar** en el menú contextual.

   Se abrirá el cuadro de diálogo Duplicar plantilla.\
   <img src="assets/duplicate-template.png" alt="Duplicar plantilla de PDF" width="250">
1. Especifique un nombre para la plantilla.

   El **Nombre** El campo se rellena previamente como una copia del mismo nombre que la plantilla de origen.

1. Para especificar un nombre preferido, quite el nombre ya rellenado y especifique un nombre.
1. Haga clic en **Listo**.

   Se crea una plantilla duplicada que se añade en Plantillas.

## Personalización de una plantilla de PDF {#customize-pdf-template}

Puede personalizar las plantillas mediante la modificación de los componentes de la plantilla y la aplicación de formatos de estilo mediante hojas de estilo.

Para personalizar una plantilla de PDF, siga los siguientes pasos:
1. En el Editor web, vaya a la pestaña Output.
1. Expanda la barra lateral izquierda y seleccione Plantillas.

   Se abrirá el panel Plantillas.
1. Para ver los componentes de una plantilla, siga uno de estos procedimientos:

   * Seleccione el icono > situado junto a una plantilla o haga doble clic en su nombre.
   * Pase el ratón sobre cualquier plantilla y seleccione el ... (icono Opciones) y elija Editar en el menú contextual.

     De forma predeterminada, se abre el panel Configuración en el editor de plantillas.
   <img src="assets/customize-pdf-template.png" alt="Personalizar plantilla de PDF" width="350">

   >[!NOTE]
   >
   >  El administrador puede descargar las plantillas más recientes desde la siguiente ruta y reemplazar las existentes:
   >
   > `/libs/fmdita/pdf`

   Los distintos componentes de plantilla que puede personalizar se clasifican en las siguientes secciones:
   * Diseños de página: normalmente, un PDF contiene páginas diferentes, como una portada o una página de título, índice, capítulo, índice, citas, etc. La sección Diseños de página permite diseñar el aspecto de las diferentes páginas que compondrían el PDF. Para obtener más información, consulte [Diseños de página](../native-pdf/components-pdf-template.md#page-layouts).

     Además de la apariencia, también puede definir la disposición de los elementos de página, como el encabezado, el pie de página y las áreas de contenido de una página. Para obtener más información sobre cómo personalizar el diseño de una página, consulte [Creación y personalización de diseños de página](components-pdf-template.md#create-customize-page-layout).

   * Hojas de estilo: la configuración de la sección Hojas de estilo permite personalizar el aspecto de los componentes del diseño de página, como la TDC, el índice, el glosario, las citas, etc. Además, también se pueden personalizar estilos para el contenido DITA como encabezados, párrafos, listas, etc. Para obtener más información sobre el uso de las hojas de estilo, consulte [Uso de hojas de estilo para personalizar el PDF](components-pdf-template.md#stylesheet-customization).
   * Recursos: Almacene los archivos de recursos que necesite para personalizar o diseñar plantillas de PDF. Los recursos, como logotipos, fuentes personalizadas, imágenes de fondo y mucho más, se almacenan en Recursos. Para obtener más información sobre el uso de los recursos, consulte [Trabajo con recursos](components-pdf-template.md#work-with-resources).
   * Settings: configure los ajustes de salida para generar un PDF con la plantilla. Esta sección le permite definir la asignación de plantillas para varias páginas de un PDF, la página de inicio del capítulo, los marcadores de impresión, las citas, etc.
También puede organizar el orden en que deben aparecer en la salida final del PDF.
Para obtener más información sobre la aplicación de la configuración, consulte [Configuración avanzada del PDF](components-pdf-template.md#advanced-pdf-settings).


1. Para personalizar un componente de plantilla, haga doble clic en un componente de plantilla o seleccione el icono > que hay antes.

   Por ejemplo, haga doble clic en *Diseños de página* o seleccione la opción *>* icono antes *Diseños de página* para ver los diseños de página disponibles.
1. Cuando haya realizado los cambios deseados, seleccione *Guardar todo* (o `Ctrl+S`).
