---
title: Función de publicación de PDF nativo | Personalización y configuración de la función PDF nativo
description: Aprenda a personalizar y configurar los distintos componentes de la función de PDF nativo.
source-git-commit: bd62afd85ddbcf5f305b18b9a9c226a4790d383a
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# plantilla de PDF

El uso de una plantilla garantiza la coherencia en el diseño y la estructura del contenido. Como las plantillas están predefinidas, puede evitar cualquier modificación en el formato de los problemas que se presenten en cada proyecto o actualización nuevos. Las plantillas le permiten diseñar diseños de página, aplicar estilo al contenido y aplicar diversas configuraciones para personalizar el PDF.

Aunque los autores pueden utilizar los ajustes preestablecidos de PDF para generar resultados, los desarrolladores pueden crear sus propias plantillas. Existen plantillas de ejemplo enviadas de fábrica que los desarrolladores pueden personalizar o duplicar según sus necesidades organizativas.


## Creación de una nueva plantilla de PDF {#create-pdf-template}

Puede crear plantillas de PDF personalizadas con diseños de página específicos y definir el formato para los componentes de diseño de página (como TDC, índice, glosario) o los componentes DITA (como encabezado, párrafo o lista) mediante hojas de estilo. Puede crear una nueva plantilla desde cero o crearla con una plantilla de ejemplo.

Para crear una nueva plantilla de PDF, siga los pasos a continuación:
1. En el Editor web, vaya a la **Salida** pestaña .
1. Expanda la barra lateral izquierda y haga clic en **Plantillas**.
<img src="assets/create-pdf-template.png" alt="Crear plantilla de PDF" width="400">
1. En el panel **Plantillas**, haga clic en el icono **+** situado junto a **Plantillas** y seleccione **Plantilla de PDF**.
1. Especifique un nombre para la plantilla en el cuadro de diálogo **Nueva plantilla**.
1. Haga clic en **Listo**.

La nueva plantilla se crea y se añade en la variable *Plantillas* panel.

## Duplicación de una plantilla de PDF

Si desea crear una plantilla nueva con los mismos diseños de página y formato que los de una plantilla existente, puede crear una copia. Una vez duplicada una plantilla, puede personalizar aún más sus componentes según sea necesario.

Para duplicar una plantilla de PDF existente, siga los pasos a continuación:
1. En el Editor web, vaya a la **Salida** pestaña .
1. Expanda la barra lateral izquierda y haga clic en **Plantillas**.

   Se abrirá el panel Plantillas .
1. Pase el ratón sobre la plantilla que desee duplicar y seleccione la (*Opciones* icono) **...** y elija **Duplicar** en el menú contextual.

   Se abrirá el cuadro de diálogo Duplicar plantilla .\
   <img src="assets/duplicate-template.png" alt="Duplicar plantilla de PDF" width="250">
1. Especifique un nombre para el teamplte.

   La variable **Nombre** se rellena previamente como una copia del mismo nombre que la plantilla de origen.

1. Para especificar un nombre preferido, elimine el nombre rellenado previamente y especifique un nombre.
1. Haga clic en **Listo**.

   Se crea y se agrega una plantilla duplicada en Plantillas.

## Personalización de una plantilla de PDF

Las plantillas se pueden personalizar modificando los componentes de la plantilla y aplicando formatos de estilo mediante hojas de estilo.

Para personalizar una plantilla de PDF, siga los siguientes pasos:
1. En el Editor web, vaya a la ficha Salida .
1. Expanda la barra lateral izquierda y haga clic en Plantillas.

   Se abrirá el panel Plantillas .
1. Para ver los componentes de una plantilla, realice una de las acciones siguientes:

   * Haga clic en el icono > situado junto a una plantilla o haga doble clic en el nombre de la plantilla.
   * Pase el ratón sobre cualquier plantilla, haga clic en ... (icono Opciones) y seleccione Editar en el menú contextual.

      De forma predeterminada, se abre el panel Configuración en el editor de plantillas.
   <img src="assets/customize-pdf-template.png" alt="Personalizar tutoriales de PDF" width="350">

   Los distintos componentes de plantilla que puede personalizar se clasifican en las siguientes secciones:
   * Diseños de página: Un PDF típico contiene páginas diferentes, como portada o página de título, tabla de contenido, capítulo, índice, etc. La sección Diseños de página le permite diseñar la apariencia de diferentes páginas que formarían su PDF. Además del aspecto, también puede definir la organización de elementos de página, como el encabezado, el pie de página y las áreas de contenido de una página. Para obtener más información sobre la personalización del diseño de una página, consulte ***Crear y personalizar diseños de página***.
   * Hojas de estilo: La configuración de la sección Hojas de estilo le permite personalizar el aspecto de los componentes del diseño de página, como la tabla de contenido, el índice, el glosario y mucho más. Además, también puede personalizar los estilos del contenido DITA como encabezados, párrafos, listas, etc. Para obtener más información sobre el uso de las hojas de estilo, consulte ***Utilice hojas de estilo para personalizar el PDF***.
   * Recursos: Almacene archivos de recursos que necesitaría personalizar o diseñar plantillas de PDF. Los recursos como logotipos, fuentes personalizadas, imágenes de fondo y mucho más se almacenan en Recursos. Para obtener más información sobre la utilización de los recursos, consulte ***Trabajar con recursos***.
   * Configuración: Configure los ajustes de salida para generar un PDF con la plantilla . Esta sección le permite definir la asignación de plantillas para varias páginas en un PDF, en la página de inicio de capítulos, en los marcadores de impresión, etc. Para obtener más información sobre cómo aplicar la configuración, consulte ***Configuración avanzada del PDF***.
1. Para personalizar un componente de plantilla, haga doble clic en un componente de plantilla o haga clic en el icono > antes de hacerlo.

   Por ejemplo, haga doble clic en *Diseños de página* o haga clic en el botón *>* icono antes *Diseños de página* para ver los diseños de página disponibles.
1. Una vez que haya realizado los cambios deseados, haga clic en *Guardar todo* (o `Ctrl+S`).


