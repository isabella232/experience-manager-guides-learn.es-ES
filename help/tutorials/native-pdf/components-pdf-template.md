---
title: Función de publicación de PDF nativo | Componentes de una plantilla de PDF
description: Conozca los distintos componentes de una plantilla de PDF y cómo personalizarlos y configurarlos.
hide: true
hidefromtoc: true
exl-id: 0ddb3b81-42ca-4a66-be7d-051a5175d53a
source-git-commit: 563a301e4db20cd8076eaffd970d53b7a8743449
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 0%

---

# Componentes de una plantilla de PDF {#components-pdf-template}

Una plantilla de PDF tiene cuatro componentes: Diseños de página, hojas de estilo, recursos y configuración. Puede crear una plantilla personalizando estos componentes individuales y asociándola con un ajuste preestablecido de salida mientras genera una salida de PDF. Las secciones siguientes tratan en detalle estos componentes y su proceso de personalización.


## Crear y personalizar diseños de página {#create-customize-page-layout}

La configuración del componente Diseños de página permite diseñar la estructura de una página definiendo el encabezado, el pie de página y el área de contenido de una página. Con el editor de diseño de página WYSIWYG, se puede crear un diseño de página para diferentes secciones de un PDF, como las portadas frontal y posterior, el capítulo, la tabla de contenido (TOC), el índice, la página en blanco, la lista de figuras (LOF), la lista de tablas (LOT), el glosario o crear un diseño para una página personalizada. En Configuración de plantilla de PDF, puede asignar un diseño de página con diferentes secciones dentro de un PDF, que luego se utilizan para generar el resultado del PDF.

### Crear un nuevo diseño de página {#create-page-layout}

>[!NOTE]
>
>Existen diseños de página de ejemplo que se envían fuera de la caja. Puede personalizarlos o crear nuevos diseños de página.

1. En el Editor web, vaya a la **Salida** pestaña .
1. Expanda la barra lateral izquierda y haga clic en **Plantillas**.
1. Abra la plantilla con la que desee trabajar.
   >[!NOTE]
   >
   >Puede abrir una plantilla haciendo doble clic en su nombre o haciendo clic en el icono > situado junto a su nombre.
1. Para crear un nuevo diseño de página, siga uno de estos procedimientos:
   * Pase el ratón **Diseños de página** y haga clic en (*Opciones* icono) **...** y elija **Nuevo diseño de página**.
   * En el **Plantillas** , haga clic en el **+** junto a **Plantillas** y elija **Diseño de página** en el menú contextual.

      Se abrirá el cuadro de diálogo Agregar diseño .

      <img src="assets/add-layout-2.png" alt="Cuadro de diálogo Agregar diseño" width="250">
1. Especifique un nombre para el nuevo diseño de página.
   >[!NOTE]
   >
   >Evite utilizar caracteres especiales al dar nombre a un diseño de página. Un espacio en el nombre se sustituye por un guión bajo &quot;_&quot;.
1. Haga clic en **Listo**.

   El nuevo diseño se crea y se agrega en Diseños de página.

### Duplicación de un diseño de página {#duplicate-page-layout}

1. En el **Plantillas** de la plantilla que desea duplicar, haga doble clic en **Diseños de página** o haga clic en el botón **>** icono antes **Diseños de página**.

   Esto muestra la lista de diseños de página dentro de la plantilla.

1. Pase el ratón sobre el diseño de página que desee duplicar y haga clic en (*Opciones* icono) **...** y seleccione **Duplicar** en el menú contextual.

1. En el _Duplicar diseño_ , escriba un nombre para el diseño de página.

1. Haga clic en **Listo**.
Se crea y se agrega una copia del diseño de página seleccionado en Diseños de página.

### Personalización de un diseño de página {#customize-page-layout}

1. En el **Plantillas** de la plantilla que desea editar, haga doble clic en **Diseños de página** o haga clic en el botón **>** icono antes **Diseños de página**.

   Esto muestra la lista de diseños de página dentro de la plantilla.
1. Para personalizar cualquier diseño de página, realice una de las acciones siguientes:
   * Haga doble clic en cualquier diseño de página.
   * Pase el ratón sobre cualquier diseño de página y haga clic en (*Opciones* icono) **...** y seleccione **Editar** en el menú contextual.

   Se abre el editor de diseño de página para personalizarlo.
1. Una vez que haya realizado los cambios deseados, haga clic en *Guardar todo* (o `Crl+S`).

   Para obtener más información sobre la definición de elementos de diseño individuales, como encabezado, pie de página, número de página, título, etc., consulte [Diseño de un diseño de página](design-page-layout.md).

## Utilice hojas de estilo para personalizar el PDF {#stylesheet-customization}

La configuración del componente Hojas de estilo le permite aplicar estilo a los componentes de diseño de página y al contenido DITA mediante el editor WYSIWYG o trabajar directamente con el archivo CSS. Puede crear sus propios estilos o personalizar las propiedades de estilo predeterminadas. El editor WYSIWYG le permite acceder a la mayoría de las propiedades que necesitaría para aplicar estilo al diseño de la página o al contenido DITA. Para personalizaciones avanzadas, puede trabajar directamente en la vista Origen.

### Crear una nueva hoja de estilo {#create-stylesheet}

Aunque los archivos CSS se proporcionan para el contenido y el diseño, puede crear una nueva hoja de estilo para aplicar varias personalizaciones a un tipo de estilo específico que luego se puede aplicar a un componente de destino. De forma predeterminada, los archivos CSS de muestra están agrupados dentro del producto. Estos archivos CSS están pensados para ayudarle a organizar la información de estilo entre contenido y diseños. Puede combinar estos estilos en un solo archivo CSS o en varios archivos.

De forma predeterminada, cada vez que crea un nuevo diseño de página, la variable `layout.css` se incluye en el nuevo diseño de página. Si desea que el diseño de página contenga estilos de un archivo CSS diferente, simplemente puede arrastrar y soltar el archivo CSS deseado en el área de edición de contenido del nuevo diseño de página. Para validar si el archivo CSS se ha incrustado en el diseño de página, cambie a la vista Origen y encontrará un vínculo al archivo CSS en la `<head>` elemento.


Para crear una hoja de estilo, siga los siguientes pasos:
1. En el **Plantillas** realice una de las siguientes acciones:
   * Pase el ratón sobre la **Hojas de estilo** y haga clic en la pestaña *Opciones* icono) **...** y elija **Nueva hoja de estilo**.
   * Haga clic en el **+** junto a **Plantillas** y elija **Hoja de estilo** en el menú contextual.

   Se abrirá el cuadro de diálogo Agregar hoja de estilo .

   <img src="assets/add-stylesheet.png" alt="Agregar hoja de estilo" width="250">
1. Especifique un nombre para la nueva hoja de estilo.
1. Haga clic en **Listo**.

   Se crea y agrega una nueva hoja de estilo en la sección Hojas de estilo .

### Crear un nuevo estilo {#create-style}

De forma predeterminada, los archivos CSS contienen estilos para encabezado, párrafo, carácter, hipervínculo, imagen, tabla, div, página y otros estilos. Puede anular el formato de estilo predeterminado o crear un nuevo estilo.

Normalmente, creará un nuevo estilo cuando desee asociar un estilo personalizado para cualquier elemento DITA. Para que funcionen estos estilos personalizados, debe asegurarse de que está asociando el nombre de clase del estilo con el atributo outputclass del elemento DITA.


Para crear un nuevo estilo, siga los pasos a continuación:
1. Haga clic con el botón derecho en cualquier estilo y seleccione Nuevo estilo en el menú contextual.

   Se abrirá el cuadro de diálogo Agregar estilo .

   <img src="assets/add-style.png" alt="Agregar nuevo estilo" width="300"/>
1. En el **Etiqueta** , elija una etiqueta para la que desee crear un nuevo estilo.
1. Especifique un **Clase** nombre.

   Este nombre de clase debe estar asociado con el atributo outputclass de la etiqueta en el contenido de origen.
1. Seleccione un **Pseudo Clase** para un estilo mejorado del elemento.
1. Haga clic en **Listo**.

   Se crea y se añade un nuevo estilo bajo el estilo base.

### Personalización de un estilo nuevo o predefinido {#customize-style}

Una vez que haya creado un nuevo archivo CSS con estilos predeterminados o desee personalizar estilos en un archivo CSS existente, puede utilizar el editor de estilos para hacerlo.

Para personalizar un estilo, siga los siguientes pasos:
1. Haga doble clic en **Hojas de estilo** o haga clic en el botón **>** icono antes **Hojas de estilo**.

   Muestra los archivos CSS predeterminados (Contenido y Diseño) y personalizados.
1. Abra una hoja de estilo para editarla.

   Para abrir la hoja de estilo y editarla, realice una de las acciones siguientes:
   * Haga doble clic en el nombre de la hoja de estilo.
   * Pase el ratón sobre el nombre de la hoja de estilo, haga clic en (icono Opciones) ... y seleccione Editar.

   Se abrirá la hoja de estilo para editarla y se mostrará la lista de estilos en el panel Estilos.

   <img src="assets/customize-style.png" alt="Personalizar estilo" width="450">

1. Para personalizar un estilo, haga doble clic en un estilo o haga clic en el icono > antes de un estilo para verlo y personalizarlo con el editor Estilos.

para obtener más información sobre cómo trabajar con los estilos más comunes, consulte [Trabajar con estilos de contenido comunes](stylesheet.md)

## Trabajar con recursos {#work-with-resources}

Es un contenedor para todos los recursos utilizados para diseñar una plantilla. Puede considerarla una carpeta que contiene recursos como imágenes de fondo, fuentes personalizadas, logotipos y mucho más. Cada vez que se añade un recurso en la plantilla, este se carga o se desprotege en la carpeta de recursos. A continuación, puede utilizar estos recursos para personalizar o diseñar las plantillas de PDF.

Para agregar un archivo de recursos a la carpeta Recursos, siga los siguientes pasos:
1. Pase el ratón sobre la ficha Carpeta de recursos , haga clic en (icono Opciones ) ... y seleccione Importar.

   Se abrirá el cuadro de diálogo Cargar recursos .

   <img src="assets/resources-import-assets.png" alt="Carga de recursos" width="300">

   La ruta en la que se cargará el archivo de recursos se muestra en la **Seleccionar carpeta de recursos** campo .
   >[!NOTE]
   >
   >No puede cambiar la ruta para cargar recursos. De forma predeterminada, todos los recursos se almacenan en la sección `/content/dam/dita-templates/pdf/<PDF-template-name>` carpeta.

1. Haga clic en **Elegir archivos** para examinar el archivo de recursos desde el equipo local

1. Haga clic en **Cargar**.
El archivo seleccionado se importa y se muestra en la carpeta Recursos .

## Configuración avanzada del PDF {#advanced-pdf-settings}

Utilice la sección Configuración para definir la configuración avanzada del diseño de página del PDF, empezando por el PDF de página impar o par, los formatos de las referencias cruzadas y permitiendo la impresión de marcas en el PDF final que se genera con la plantilla.

Para configurar, haga clic en **Configuración** en el **Plantillas** para ver las siguientes opciones:

**General**

Defina los ajustes básicos de configuración para iniciar un capítulo desde una página impar o par, la estructura de la tabla de contenido y el formato de línea de encabezado para las entradas de la tabla de contenido. Puede definir la siguiente configuración:

* **Iniciar capítulo siempre desde**: Permite definir cómo se publica cada capítulo en el PDF final. Puede elegir entre una **Nueva página**, **Página impar** o **Página par** opciones. Si elige iniciar un capítulo nuevo desde una página impar, se inserta una página en blanco después de un capítulo que termina en una página impar. Por ejemplo, si el capítulo termina en la página 15, el proceso de publicación insertará un 16 en blanco<sup>th</sup> para que el nuevo capítulo pueda comenzar desde la página 17<sup>th</sup> página.

* **Iniciar cada tema desde una página nueva**: Si desea que cada tema del capítulo comience desde una página nueva, seleccione **Iniciar cada tema desde una página nueva** . Si desea mantener los temas en continuación sin espacios en la página, anule la selección de esta opción.

* **Estructura de TDC**: Permite personalizar la jerarquía de la Tabla de contenido. Utiliza los siguientes ajustes adicionales:

   * **Usar encabezados hasta el nivel**: Permite ajustar el número de niveles de encabezado que se mostrarán en la estructura de TDC de su PDF.
   * **No mostrar el número de página del primer nivel en la tabla de contenido**: Seleccione esta opción para ocultar los números de página correspondientes para todos los capítulos que contienen temas anidados o secundarios. Considere el siguiente ejemplo en el que se crea una salida sin seleccionar esta opción.

   <img src="assets/page-number-in-toc.png" alt="Carga de recursos" width="250">

   En el ejemplo anterior, Configuración avanzada de PDF, Apéndice y Legal son los encabezados de tema de primer nivel o títulos de capítulo. Se asigna un número de página a todos estos encabezados.

   Ahora, si selecciona esta opción y genera el resultado, obtendrá la siguiente tabla de contenido:
   <img src="assets/page-number-missing-in-toc.png" alt="Carga de recursos" width="250">

   Aquí puede observar que la configuración del primer capítulo de PDF avanzado no tiene número de página, ya que contiene temas anidados o secundarios. Mientras que un número de página si se asigna a Apéndice y Legal porque son temas independientes sin ningún tema secundario.

* **Formato del encabezado**: Utilice la lista desplegable para seleccionar las líneas de encabezado Punteado, Sólido o Espacio para conectar los niveles de encabezado con sus números de página correspondientes.
Para aplicar estructura de TDC y niveles de encabezado de estilo, consulte [Agregar una tabla de contenido de capítulo](design-page-layout.md#add-chapter-toc).

   >[!NOTE]
   >
   >Si es desarrollador de CSS, también puede definir el formato de encabezado directamente en el archivo CSS.
* **Usar marcador de continuación de tabla**: Seleccione esta opción para definir marcadores para tablas largas que se extienden por varias páginas. <!--For more information on using table continuation markers, see Use table continuation markers.-->

**Diseños de página**

La configuración de Diseños de página le permite controlar por completo la especificación del diseño de página que se utilizará para una sección específica del documento. Por ejemplo, para seleccionar un diseño para la Tabla de contenido, haga clic en el menú desplegable en el campo TDC y seleccione el diseño que ha diseñado para generar la TDC.

Si no ha creado un diseño para una sección en particular del documento, simplemente puede elegir un diseño que sirva como diseño predeterminado para esas secciones o temas. El diseño de página predeterminado se aplica a todas las secciones que no tengan un diseño de página dedicado.

Del mismo modo, si desea una portada y una página anterior, debe tener un diseño de página creado y aplicado en la configuración. De lo contrario, el PDF no contendrá las páginas de portada y de atrás.


Para obtener más información sobre los diseños de página, consulte [Diseño de un diseño de página](design-page-layout.md).

**Imprimir**

Configure los ajustes de producción de impresión para asignar marcas de impresora, seleccionar modelos de color y especificar propiedades relacionadas con la impresión de la salida del PDF.

* **Marcas de impresora**: Al preparar un documento para la producción de impresión, se agregan marcas de impresora a los límites de la página para facilitar la correcta alineación, recorte y selección de color durante la impresión. Al seleccionar una marca de impresora, el límite de la página se amplía para dar cabida a la marca, que se recorta durante la impresión. Puede elegir mostrar las siguientes marcas de impresora en la salida del PDF:
   * **Marcas de recorte**: Seleccione la opción para colocar una marca en cada esquina del área de recorte para indicar dónde debe recortarse el papel después de imprimir.
   * **Marcas de sangrado**: Seleccione para colocar una marca en cada esquina del cuadro de sangrado para indicar el área de recorte de la imagen extendida.
   * **Marcas de registro**: Seleccione esta opción para colocar una marca fuera del área de recorte y alinear las distintas separaciones en un documento de color.
   * **Barras de color**: Seleccione esta opción para añadir una banda de colores fuera del área de recorte para mantener la coherencia del color y ajustar la densidad de tinta al imprimir.

   Defina las dimensiones de las marcas de impresora seleccionadas utilizando la variable **Ancho de línea**, **Color de línea** y **Ancho del cuadro de sangrado** opciones.

* **Tamaño del cuadro de medios**: Es el tamaño general de la página, incluido el área extendida ocupada por las marcas de impresora. Utilice la opción desplegable para seleccionar el tamaño de la página de salida del PDF o crear su propio tamaño personalizado.

* **Espacio de color**: Se le da la opción de elegir entre espacios de color RGB o CMYK para imprimir el documento PDF. Elija RGB para mostrar el PDF generado digitalmente y CMYK para impresión física. Los colores definidos en el documento se convierten al espacio de color elegido.
   >[!NOTE]
   >
   >Es necesario un perfil de color ICC para la creación de PDF/A si se utiliza espacio de color CMYK.

   <!--For more information on applying these print settings, see *Printing preferences*.-->

**Referencias cruzadas**

Utilice la pestaña Cross-reference para definir cómo se publican las referencias cruzadas en el PDF. Puede dar formato a las referencias cruzadas para el título del tema, tablas, figuras y mucho más. <!--For more information, see *Format cross-references*.-->
