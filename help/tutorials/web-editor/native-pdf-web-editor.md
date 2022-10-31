---
title: PDF nativo | Generación de salida de PDF
description: Generar salida de PDF en las guías de Adobe Experience Manager as a Cloud Service
exl-id: ec3d59b7-1dda-4fd1-848e-21d8a36ff5e4
source-git-commit: e7fe44f6d0c0ce08d5f94140474212c280b41f52
workflow-type: tm+mt
source-wordcount: '2297'
ht-degree: 1%

---

# Salida del PDF de publicación

Con AEM guías, puede generar PDF de temas individuales o un archivo de mapa completo. Puede publicar el contenido en formato de PDF mediante uno de los tres métodos siguientes:

* **DITA-OT**

Utilice este método para generar una salida de PDF para un mapa desde el panel de mapas. Puede establecer las propiedades de publicación antes de generar el PDF creando un ajuste preestablecido de salida para el mapa que está abierto en el panel de mapas. Para crear o editar un ajuste preestablecido de salida, la variable *Explicación de los ajustes preestablecidos de salida* en la sección [Guía del usuario as a Cloud Service de AEM Guías](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/cs-apr-22/XML-Documentation-for-Adobe-Experience-Manager_CS_User-Guide_EN.pdf).

Para obtener más información sobre la generación de un PDF mediante el método DITA-OT, consulte [Generación de un PDF con DITA-OT](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-pdf.html).

* **FrameMaker Publishing Server (FMPS)**

Utilice este método para generar una salida de PDF no solo a partir del contenido DITA, sino también de los documentos FrameMaker (.book y .fm) disponibles en el repositorio de AEM. El PDF se puede crear configurando un ajuste preestablecido de salida y publicándolo mediante FrameMaker Publishing Server (FMPS). Puede diseñar y configurar el aspecto de la salida para el PDF y otros formatos y almacenarla en un archivo de configuración (.sts). FMPS utiliza este archivo de configuración para generar resultados para un mapa DITA o un archivo .book. Para crear o editar un ajuste preestablecido de salida, consulte la  *Explicación de los ajustes preestablecidos de salida* en la sección [Guía del usuario as a Cloud Service de AEM Guías](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/cs-apr-22/XML-Documentation-for-Adobe-Experience-Manager_CS_User-Guide_EN.pdf).

Para obtener más información sobre la configuración de FMPS, consulte [Generar salida de documentos de FrameMaker](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Ffm-output-generatation.html).

* **Publicación del PDF nativo**

Utilice este método para generar una salida de PDF con numerosas funciones basada en los estándares de medios paginados W3C CSS3 y CSS. Con la publicación de PDF nativos, puede usar plantillas para definir el diseño y el estilo del contenido y aplicar diversas configuraciones para ajustar el PDF. Además, puede modificar y crear sus propias plantillas con el editor de plantillas.

Para obtener más información sobre la publicación de PDF nativos, consulte [Uso de la publicación en el PDF nativo](#native-pdf-publishing).


## Uso de la publicación del PDF nativo {#native-pdf-publishing}

Al crear contenido, resulta esencial asegurarse de que el contenido está optimizado para su visualización, edición e impresión. Si utiliza estándares como W3C CSS3 para estilos de contenido y estándares de medios paginados CSS para propiedades de definición de página como tamaño, márgenes, orientación, saltos de página, encabezados, pies de página y numeración de páginas, puede configurar la vista y el diseño del documento PDF para garantizar la coherencia y la facilidad de uso. La función de publicación de PDF nativo utiliza estos estándares para generar un PDF.

Con la publicación nativa del PDF, puede utilizar plantillas predefinidas para garantizar la coherencia en el diseño y la estructura del contenido, aplicar hojas de estilo para modificar el aspecto de la salida, optimizar el PDF, establecer marcas de impresora, permitir la compatibilidad con lectores de pantalla, establecer la conformidad del PDF, incrustar fuentes, etc.

La generación de un PDF mediante la publicación de un PDF nativo tiene dos aspectos:

* Utilice plantillas para aplicar estilo al contenido, definir diseños de página y diversas configuraciones para ajustar el PDF. Los autores pueden elegir utilizar o modificar las plantillas de ejemplo proporcionadas o crear plantillas personalizadas, así como establecer las opciones de configuración avanzadas que utilizan los editores y los desarrolladores.

* Cree o configure un ajuste preestablecido de salida de PDF para controlar la configuración del PDF. Una vez creado un ajuste preestablecido de salida de PDF, puede generar el PDF .

Para obtener más información, consulte [Generar una salida de PDF](#generate-pdf-output).

## Crear un ajuste preestablecido de salida de PDF {#create-output-preset}

El primer paso para generar una salida de PDF es crear un ajuste preestablecido de salida de PDF, que es una colección de propiedades de publicación asignadas a un mapa. Puede crear un ajuste preestablecido de salida para cualquier mapa que esté abierto en el panel Vista de mapa o configurar un ajuste preestablecido existente para generar rápidamente un PDF para el mismo mapa.

Desde el ajuste preestablecido de salida del PDF puede seleccionar una plantilla, aplicar condiciones, establecer restricciones para controlar cómo un usuario interactúa con su PDF, configurar opciones avanzadas como compresión, conformidad, etc.

Para crear o configurar un ajuste preestablecido de salida de PDF:

1. En la ficha Salida , haga clic en **Ajustes preestablecidos** en la barra lateral izquierda.
Se abre el panel Ajuste preestablecido.
   ![panel preestablecido](assets/preset-panel.png)
2. En la salida **Ajustes preestablecidos** realice una de las siguientes acciones:
   * Haga doble clic en un ajuste preestablecido de salida de PDF predefinido para verlo.
   * Haga clic en el icono + con **Ajustes preestablecidos** para añadir un nuevo ajuste preestablecido de salida de **Tipo: PDF**
3. Para definir la configuración de un ajuste preestablecido de PDF existente:
   * Haga clic en el  **Opciones** ![opciones](assets/options.svg) junto al ajuste preestablecido de salida deseado y seleccione **Editar**.
Puede usar las siguientes opciones en la **General**, **Metadatos**, **Diseño**, **Seguridad** y **Avanzadas** para configurar un ajuste preestablecido de salida de PDF:

**General**

Utilice para especificar la configuración básica de salida, como especificar la ruta de salida, el nombre del archivo PDF y mucho más.

| Configuración | Descripción |
| --- | --- |
| **Ruta de salida** | La ruta dentro del repositorio de AEM donde se almacena la salida del PDF. Asegúrese de que la ruta de salida no esté ubicada dentro de la carpeta del proyecto. Si se deja en blanco, la salida se genera en la ubicación de salida de mapa DITA predeterminada. |
| **Archivo PDF** | Especifique un nombre de archivo para guardar el PDF. De forma predeterminada, el nombre del archivo PDF agrega el nombre de asignación DITA junto con el nombre del ajuste preestablecido. Por ejemplo, ditamap es &quot;TestMap&quot; y el nombre del ajuste preestablecido es &quot;preset1&quot;, el nombre predeterminado del pdf será &quot;TestMap_preset1.pdf&quot;. |
| **Aplicar condiciones usando** | Para el contenido condicional, elija entre las siguientes opciones para generar una salida de PDF basada en esas condiciones: <br>* **Ninguno aplicado** Seleccione esta opción si no desea aplicar ninguna condición en el mapa y el contenido de origen. <br> * **Archivo Ditaval** Seleccione un archivo DITAVAL para generar contenido condicional. Para seleccionar, haga clic en con Ajuste preestablecido de condición y busque el archivo. <br> * **Ajuste preestablecido de condición** Seleccione un ajuste preestablecido de condición en la lista desplegable para aplicar una condición al publicar la salida. Esta opción está visible si ha añadido una condición para el archivo de asignación DITA. Los ajustes condicionales están disponibles en la ficha Ajustes preestablecidos de condición de la consola de asignación DITA. Para obtener más información sobre el ajuste preestablecido de condición, consulte [Usar ajustes preestablecidos de condición](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-use-condition-presets.html). <br> |
| **Usar línea de base** | Si ha creado una Línea de base para el mapa DITA seleccionado, seleccione esta opción para especificar la versión que desea publicar. Consulte [Trabajo con línea de base](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-use-baseline-for-publishing.html) para obtener más información. |

**Metadatos**

Los metadatos son la descripción o definición del contenido. Los metadatos ayudan en la administración de contenido y ayudan a buscar archivos en Internet.

Utilice la pestaña Metadatos para definir el título, el autor, el asunto y las palabras clave de la salida del PDF. Estos metadatos se asignan a los metadatos de la ficha Descripción de las Propiedades del documento del PDF de salida.

**Nota**: Estos metadatos anulan los metadatos definidos a nivel de libro.

![ficha metadatos](assets/pdf-metadata.png)

| Configuración | Descripción |
|---|---|
| **Título** | Especifique un título corto y claro para definir el documento. |
| **Autor** | Especifique los nombres de los autores que crearon el documento. |
| **Asunto** | Defina el asunto o la colección con la que está relacionado el documento. |
| **Palabras clave** | Utilice palabras clave relevantes para mejorar la optimización de su motor de búsqueda (SEO) y ayudar a los usuarios a encontrar el contenido relacionado. |

**Diseño**

Utilice para definir los diseños de página y especificar las opciones de vista de página para los resultados del PDF, como Visualización de página y Establecer niveles de zoom.

| Configuración | Descripción |
| --- | --- |
| **Plantilla de PDF** | Las plantillas de PDF proporcionan una estructura clara para definir los diseños de página, el estilo del contenido y la aplicación de diversas configuraciones a la salida del PDF. Seleccione en las opciones desplegables de plantilla de PDF para elegir la plantilla que prefiera. |
| **Visualización de la página** | Utilice la visualización de página para la vista de página que muestra cómo se muestra el PDF cuando se abre. Seleccione en las opciones desplegables Visualización de página (Page Display) para elegir una vista preferida. <br>* **Predeterminado**  Se muestra según la configuración predeterminada del visor del PDF en el equipo de un usuario.  <br> * **Vista de una sola página** Muestra una página a la vez.   <br> * **Desplazamiento en una sola página** Muestra una sola página en una columna vertical continua.  <br> * **Dos vistas de página** Muestra el pliego de dos páginas una al lado de la otra. .<br> * **Desplazamiento de dos páginas** Muestra el desplazamiento de dos páginas en paralelo con el desplazamiento continuo. |
| **Zoom** | Seleccione para cambiar el tamaño de la vista de página que muestra cómo se muestra el PDF cuando se abre.  <br>* **Predeterminado** Se muestra según la configuración predeterminada del visor del PDF en el equipo de un usuario    <br> * **100 %** Hace que la página aparezca en su tamaño real.     <br> * **Ajustar página** Define el ancho y el alto de la página para que se ajusten al panel del documento. .<br> * **Ajustar anchura de página** Define el ancho de la página para que ocupe el ancho del panel del documento.  <br> * **Ajustar altura de página** Hace que la altura de la página se rellene con la altura del panel del documento. |

**Seguridad**

Protect con su PDF añadiendo restricciones para abrir y leer el archivo. Utilice las siguientes opciones para evitar el acceso no autorizado.

| Configuración | Descripción |
| --- | --- |
| **Establecer contraseña para abrir el documento** | Seleccione para agregar una contraseña segura para ver el archivo PDF. Especifique una contraseña en la variable **Contraseña de usuario** campo . Los usuarios solo pueden abrir el PDF introduciendo la contraseña proporcionada en este campo. |
| **Establecer las restricciones del documento** | Seleccione esta opción para restringir la interacción de los usuarios con su PDF. Especifique una contraseña en la variable **Contraseña del propietario** para que funcione la siguiente configuración de restricción.  <br>* **Impresión** Seleccione para permitir que un usuario imprima el PDF. <br> * **Impresión de calidad de borrador** Seleccione esta opción para permitir que un usuario imprima el PDF en una resolución inferior.  <br> * **Copia de contenido** Seleccione para permitir que un usuario copie el contenido del PDF.   <br> * **Anotaciones** Seleccione esta opción para permitir que un usuario añada una nota o comentario en el PDF.  <br> * **Modificaciones del contenido** Seleccione para permitir que un usuario modifique el contenido en el PDF.  <br> * **Copia de contenido para accesibilidad** Seleccione esta opción para permitir que los lectores de pantalla lean y naveguen por el contenido en el PDF.  <br> * **Conjunto de documentos** Seleccione esta opción para permitir a los usuarios insertar páginas en el PDF.  <br> **Nota**: Los usuarios deben introducir la contraseña de propietario para cambiar cualquier restricción de Archivo > Propiedades en Adobe Acrobat. |

**Avanzado**

Utilice las siguientes opciones para especificar la configuración avanzada para combinar PDF, utilizar compresión, seleccionar el estándar de conformidad, etc.

| Configuración | Descripción |
| --- | --- |
| **Crear PDF accesible (etiquetado)** | Seleccione esta opción para generar un PDF con etiquetas. Un PDF etiquetado facilita a los lectores de pantalla la lectura y navegación por contenido, hipervínculos, marcadores, etc. Por ejemplo, si una tabla está etiquetada, el lector de pantalla sabrá que está leyendo la tabla y no solo líneas y texto. |
| **Combinar PDF incluidos en la tabla de contenido** | Seleccione esta opción para combinar los PDF existentes en la salida agregándolos a la Tabla de contenido. Los PDF se insertan en la ubicación representada en la tabla de contenido y las páginas se incrementan en consecuencia. |
| **Incrustar fuentes usadas** | Seleccione esta opción cuando utilice fuentes que no estén instaladas en el equipo del usuario final. Con esta opción seleccionada, las fuentes usadas se incrustan en el PDF, lo que garantiza que el usuario pueda ver el PDF como desea incluso aunque las fuentes no estén instaladas en su equipo. <br> **Nota**: Una fuente solo se puede incrustar si contiene una configuración del proveedor de fuentes que permita su incrustación. Asegúrese de que dispone de la configuración o licencia necesarias antes de incrustar una fuente. |
| **Uso de la división mediante guiones automática** | Con la división mediante guiones automática activada, las palabras al final de las líneas se desglosan en lugares gramaticalmente correctos con un guión. |
| **Habilitar JavaScript** | Active esta opción si tiene un código JavaScript que desee utilizar para transformar el contenido de forma dinámica antes de generar un PDF. |
| **Incrustar archivos multimedia** | Seleccione esta opción para incluir audio, vídeo y contenido interactivo al PDF. |
| **Utilice la compresión completa para optimizar el tamaño del PDF** | Seleccione esta opción si desea comprimir/reducir el tamaño de un PDF grande. Recuerde, la compresión del PDF puede reducir la calidad del archivo. |
| **Utilizar la compresión de imagen para optimizar el tamaño del PDF** | Seleccione esta opción si desea comprimir/reducir el tamaño de las imágenes utilizadas en el PDF. Recuerde, la compresión de una imagen puede reducir la calidad de la imagen. |
| **Utilizar resolución personalizada (píxeles por pulgada)** | Es la resolución de visualización de la página en píxeles por pulgada. Introduzca un valor preferido en el campo que aparece cuando se selecciona esta opción. El valor predeterminado es de 96 píxeles por pulgada. Defina un valor más alto para que quepa más contenido en una pulgada y viceversa, si establece un valor más bajo. |
| **Mostrar marca de agua** | Seleccione esta opción para procesar ecuaciones MathML presentes en el contenido. De lo contrario, se ignorarán las ecuaciones. |
| **Habilitar ecuaciones MathML** | Seleccione esta opción para procesar ecuaciones MathML presentes en el contenido. De lo contrario, las ecuaciones se ignorarán de forma predeterminada. |
| **Conformidad del PDF** | Es el estándar con el que desea guardar al PDF para garantizar que sea compatible. Seleccione en la lista desplegable para elegir entre la lista de estándares de PDF disponibles. Para obtener más información sobre los estándares admitidos, consulte [Acerca de los estándares de PDF](https://helpx.adobe.com/acrobat/using/pdf-conversion-settings.html#about_pdf_x_pdf_e_and_pdf_a_standards). |

## Generar una salida de PDF {#generate-pdf-output}

Una vez configurado el ajuste preestablecido de salida, puede generar resultados desde el panel Ajustes preestablecidos , utilizando el **Generar ajuste preestablecido** función.

1. En el **Autor** , seleccione **Repositorio** Ver.\
   Se abrirá el panel Repositorio .

2. En el panel Repositorio, abra el archivo de asignación DITA en **Vista Mapa**.

3. En el **Salida** , haga clic en **Ajustes preestablecidos** para ver el panel Ajustes preestablecidos .
Para crear o configurar un ajuste preestablecido de salida, consulte [Crear un ajuste preestablecido de salida de PDF](#create-output-preset).
4. Para guardar la configuración, haga clic en el botón **Guardar todo** ![guardar todo](assets/SaveFloppy_icon.svg) en la esquina superior izquierda de la barra de herramientas estándar en la vista Salida.
5. Haga clic en el **Generar ajuste preestablecido** ![generar ajuste preestablecido](assets/generate-output.svg) en la barra superior.
Puede ver una barra de progreso junto al ajuste preestablecido de salida seleccionado en el panel Ajustes preestablecidos de salida.
6. Una vez finalizada la generación de salida, haga clic en  **Ver salida** ![ver salida](assets/view-output.svg) en la barra superior para ver el resultado.\
   A **Correcto** está visible en la esquina inferior derecha de la pantalla.
Si una salida no se realiza correctamente, se muestra el siguiente mensaje de error.
   ![registro de errores](assets/error-log.png)

Para ver el registro de errores, haga clic en **Rechazar**, pase el ratón sobre la ficha preestablecida seleccionada y haga clic en ![opciones](assets/options.svg) **Opciones** > **Ver registro**.
