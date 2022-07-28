---
title: Función de publicación de PDF nativo | Diseño de un diseño de página
description: 'Aprenda a diseñar el diseño de la página para presentar información en diferentes secciones de la salida del PDF. '
hide: true
hidefromtoc: true
source-git-commit: 77256556d9222ffd096a599e5875c94108ebb8ed
workflow-type: tm+mt
source-wordcount: '3300'
ht-degree: 0%

---

# Diseño de un diseño de página

Al crear un documento de PDF, tendría diferentes secciones para presentar diferentes tipos de información. Por ejemplo, un documento de PDF comenzaría desde una portada o portada, que tendría el logotipo de su empresa, el título del libro o la información de la versión. Luego habría capítulos, apéndices o páginas del glosario. Cada sección de un documento PDF tiene un aspecto diferente y se logra creando y personalizando el diseño de página.

Al diseñar el diseño de la página, puede definir los distintos elementos que la componen. Por ejemplo, puede definir el tamaño de página, los márgenes, el encabezado y pie de página, la orientación y otras especificaciones de página en una página. La función Publicación de PDF nativos le permite diseñar su página según los estándares de medios pagados de CSS. La mayoría de los ajustes que se tratan en los medios pagados de CSS se pueden personalizar fácilmente mediante la interfaz de usuario de la función PDF nativo. Para algunos otros formatos de nivel avanzado, puede utilizar la vista Origen para escribir su propio código CSS.

Una vez que haya diseñado los diseños de página, debe asociar estos diseños con sus secciones respectivas en la configuración de Diseño de página del PDF. Consulte la _Crear y personalizar diseños de página_ para obtener más información sobre cómo crear y abrir un diseño de página para su personalización.

## Tipos de diseños de página y sus variantes

Un documento de PDF generalmente contiene las siguientes secciones:

* Portada
* Tabla de contenido
* Alza de cifras
* Alza de tablas
* Páginas de capítulo o tema
* Glosario
* Índice
* Página de fondo

Estas secciones necesitarían un diseño de página correspondiente para presentar la información en un formato específico. Además, también puede tener una página en blanco que se utilice como usuario que rellena para iniciar un nuevo capítulo desde una página impar o par. En ese caso, necesitará un diseño de página en blanco.

La configuración de los diseños de página de la sección **Plantilla > Configuración** permite definir qué plantilla se utilizará para las diferentes secciones del PDF. Cada diseño de página puede tener combinaciones de página de inicio, derecha o izquierda diferentes. Estas se rigen por las reglas definidas en el *Medios de página CSS* estándares.

## Cree los diseños de la primera página, derecha o izquierda

Los diferentes diseños de página de la plantilla de PDF se pueden personalizar aún más si se tienen diferentes diseños de página de primer, derecho o izquierdo. Puede diseñar estas páginas de forma diferente utilizando el diseñador de diseño de página.

> **Nota**: Si desea tener un diseño de página único para una sección del libro, no es necesario crear los diseños de página primero, derecho o izquierdo.

Tenga en cuenta los siguientes puntos al crear los diseños de página:

* Si desea utilizar un diseño de página único para todas las páginas de un capítulo, solo debe crear un diseño de página de capítulo único.
* Si desea tener un aspecto diferente para la primera página de los capítulos de su libro, debe crear un diseño de primera página para los capítulos.
* Si desea tener un aspecto diferente para cada página izquierda y derecha del libro, debe crear las variantes del lado izquierdo y derecho para el diseño de la página del capítulo.
* Si desea que los capítulos comiencen desde una página impar o par, deberá crear un diseño de página en blanco. Este diseño de página se utiliza para llenar el espacio entre dos capítulos a fin de garantizar que el capítulo comience desde la página par o impar deseada.

El siguiente ejemplo le guiará por el proceso de creación de variantes de un diseño de página:

1. Cree un diseño de página de &quot;capítulo&quot; siguiendo los pasos indicados en *Crear un nuevo diseño de página* procedimiento.

   Se crea y se agrega un diseño de página de capítulo en blanco en los diseños de página.

   De forma predeterminada, al crear un diseño de página, también se abre para su edición. La siguiente captura de pantalla muestra un diseño de página en blanco (predeterminado):

   <img src="./assets/default-blank-page-layout.png" height="400">

   El encabezado, pie de página y área de contenido de una plantilla se crean de forma predeterminada. Puede personalizar fácilmente estas áreas mediante las herramientas, las propiedades de página y las propiedades de contenido que se proporcionan en la interfaz de usuario. Para una configuración avanzada, puede usar la vista Origen y agregar el HTML personalizado y el código CSS.

1. Para crear una variante para el diseño de página del capítulo:

   1. Sitúe el ratón encima de **Capítulo** diseño y haga clic en **Opciones** para mostrar el menú contextual.

   1. Haga clic o pase el ratón por encima **Agregar variante de diseño** y elija el diseño de página que desee crear (Primero, Izquierda o Derecha).

   El diseño de página seleccionado se crea mediante una copia del diseño de capítulo base. Esto significa que si ha realizado cambios en el diseño predeterminado de la página del capítulo, los mismos cambios se replicarán en el diseño de la página de la variante.

## Trabajar con imágenes en un diseño de página

Según sus necesidades, es posible que desee agregar una imagen que aparezca en cada primera página de un resultado de capítulo (PDF). La variable <u>**Agregar imagen**</u> en el editor de diseño de página se utiliza para insertar imágenes en un diseño de página.

Por ejemplo, si desea insertar una imagen en el área del encabezado de la primera página del resultado del capítulo, realice los siguientes pasos:

1. Abra el diseño de página necesario para editarlo.

   > **Nota**: Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. Haga clic en Editar encabezado (<img src="./assets/header-icon.svg" width="25">) para colocar el cursor en el área del encabezado.

1. Haga clic en Inert Image (<img src="./assets/insert-image-icon.svg" width="25"> ) icono.

   Aparecerá la ventana emergente Seleccionar ruta.

1. Vaya a la ubicación de la imagen y haga clic en Seleccionar para insertarla en el área del encabezado.

   La siguiente captura de pantalla muestra una imagen de ejemplo añadida en el área del encabezado.

   <img src="./assets/image-in-header-area.png" width="500">

   Una vez insertada la imagen, puede modificar sus atributos para darle el aspecto que desee. La forma más sencilla de cambiar el aspecto de una imagen o cualquier otro elemento del diseño de la página, utilice el panel Propiedades de contenido para hacerlo. Consulte _Trabajo con el panel Propiedades del contenido_ para las distintas propiedades disponibles a través de la interfaz de usuario para personalizar.

## Trabajar con campos

Los campos son muy útiles cuando desea insertar un fragmento de información predefinido. Por ejemplo, puede incluir un campo Título del capítulo en el área del encabezado del capítulo que se sustituya por el título del capítulo real cuando se publique.

Existen las siguientes categorías para los campos que puede insertar en el diseño de página:

* Fecha
* Hora
* Título del tema
* Título de proyecto
* Número de página
* Página Total
* Título del capítulo
* Número de capítulo
* Metadatos

Cada una de estas categorías de campos contiene diferentes variaciones en las que se puede insertar la información del campo. Por ejemplo, un campo de fecha puede tener diferentes variaciones, como `YYYY-MM-DD`, `MM/DD/YY`, `MM/DD/YYYY` y así sucesivamente.

En el siguiente ejemplo, insertaremos un número de página y un título de tema en el área de pie de página de nuestro diseño de página.

1. Abra el diseño de página necesario para editarlo.

   Nota: Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. Haga clic en Editar pie de página (![](./assets/footer-icon.svg)) para colocar el cursor en el área del pie de página.

1. Insertar un elemento de párrafo haciendo clic en Insertar elementos de HTML <img src="./assets/insert-html-element-2.svg" width="25"> y seleccione Párrafo en la lista de elementos.

1. Haga clic en Insertar campos ( ![](./assets/insert-fields-icon.svg)).

   Aparecerá la ventana emergente Campos.

1. Seleccione el **Número de página** de la lista Campo, la categoría **default(1)** formato de número de página de la lista Formato y haga clic en **Insertar**.

   <img src="./assets/insert-page-number-field.svg" width="400">

   > **Nota**: También puede editar el formato de todos los campos, excepto el formato predeterminado. Para ello, haga clic en el icono Editar junto al formato que desea editar, realice cambios y haga clic en Aceptar.

   El campo de número de página predeterminado se inserta en el área de pie de página del diseño de página.

   <img src="./assets/page-number-field-in-footer.png" width="400">

   La ruta de exploración superior enumera los elementos en los que se almacena la información.

1. Introduzca un espacio en blanco después del campo de número de página y haga clic en el botón **Insertar campos** icono.

1. Seleccione el **Título del tema** de la lista Campo, la categoría **Chapter.ptl** formato de título de la lista Formato y haga clic en Insertar.

   La variable `Chapter.ptl` , que se rellena con el título del tema en el momento de la publicación, se inserta en el área de pie de página. En este momento, los campos número de página y título del tema están separados por un espacio.

   <img src="./assets/page-number-topic-title-near-footer.png" width="400">

1. Para alinear a la derecha el título del tema, realice los siguientes pasos:

   1. Haga clic en el elemento Campo de la ruta de exploración para seleccionar el campo de título del tema.

   1. En el panel derecho, haga clic en Propiedades de contenido del HTML.

      <img src="./assets/right-pane-content-properties.png" width="350">

   1. Expanda el **Diseño** propiedades y establezca la variable **Flotante** valor de propiedad a **right**.

      <img src="./assets/float-prop-html-content.png" width="350">

      El campo del título del tema se alinea hacia la derecha del pie de página.

      <img src="./assets/topic-title-moved-right-footer.png" width="500">

> **Lado del desarrollador:**  ![](./assets/developer-corner-icon.svg)

Si desea trabajar directamente con el CSS y el código del HTML, también puede conseguirlo yendo la vista Origen del diseño de página y realizando cambios en el código. El siguiente fragmento de código muestra la misma configuración de pie de página realizada a través del código:

```md
…
<div data-region="footer">
	<p>
		<span data-field="page-number" data-format="default">1</span>
		<span data-field="title" data-format="default" style="float: right">Chapter.plt</span>
	</p>
</div>
…
```

## Agregar una tabla de contenido de capítulo

Un capítulo o una mini tabla de contenido sirve como referencia rápida para que los lectores sepan qué hay en el capítulo. Normalmente, se añade una tabla de contenido de capítulo al principio de un capítulo. Por lo tanto, si desea utilizar una tabla de contenido de capítulo, puede agregarla al diseño de página de capítulo principal o al diseño de primera página de un capítulo.

En el siguiente ejemplo, insertaremos una tabla de contenido de capítulo en el diseño de primera página de un capítulo:

1. Abra el diseño de página necesario para editarlo.

   Nota: Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. Coloque el cursor en el área de contenido del diseño de página.
1. Haga clic en la tabla de contenido del capítulo (<img src="./assets/chapter-toc-icon.svg">) icono.

   La tabla de contenido del capítulo predeterminada se inserta en el área de contenido.

   <img src="./assets/chapter-toc-default.png" width="400">

   > **Nota**: La tabla de contenido del capítulo predeterminado contiene los encabezados del 1 al 4. En este caso, el encabezado 1 es el propio título del capítulo. Por lo tanto, es posible que no desee volver a incluir el título del capítulo en la tabla de contenido o que desee aumentar el nivel de encabezados que desee en la tabla de contenido. Puede personalizar la tabla de contenido cambiando las propiedades.

1. Abra el panel Propiedades de contenido del HTML para personalizar los niveles de encabezado de la tabla de contenido.

   Por ejemplo, si desea comenzar desde el encabezado 2, cambie la primera lista desplegable para que comience desde 2.

   <img src="./assets/customize-chapter-toc.png" width="400">

   Del mismo modo, si desea que los encabezados lleguen hasta el nivel 5, cambie la segunda lista desplegable a 5. La tabla de contenido actualizada se verá como se muestra a continuación:

   <img src="./assets/chapter-toc-updated.png" width="400">

   > **Nota**: El PDF publicado finalmente solo mostrará las entradas de la tabla de contenido en función del contenido de sus capítulos. Si no tiene encabezados de nivel 5 en un capítulo, no se mostrarán en el resultado final.

## Trabajar con diseño de página de varias columnas

Los diseños de página de varias columnas son muy comunes en la publicación de revistas o índices en un libro. La función de publicación de PDF nativo permite dividir fácilmente el documento en varias columnas. Si utiliza diferentes diseños de página, puede elegir mantener solamente una sección específica dividida en varias columnas, mientras mantiene las demás secciones en un único diseño de columna (o normal).

Para crear un diseño de página con varias columnas, realice los pasos siguientes:

1. Abra el diseño de página necesario para editarlo.

   > **Nota**: Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. Como el diseño de varias columnas se aplica al contenido, excluyendo el área de encabezado y pie de página, debe seleccionar el elemento de contenido en la ruta de exploración.

   Una vez seleccionada la ruta de exploración del contenido, el panel Propiedades del contenido del HTML mostrará las propiedades de Varias columnas.

   <img src="./assets/multiple-columns-properties.png" width="400">

1. Utilice las propiedades de varias columnas para personalizar el diseño de página de varias columnas:

   * **Recuento de columnas:** Especifique el número de columnas para dividir la página. Utilice los iconos de flecha arriba y abajo o introduzca un número para establecer el número de columnas.

   * **Anchura de columna:** Especifique el ancho de una columna en una presentación de varias columnas. De forma predeterminada, el tamaño se establece en píxeles (px); también se puede especificar en pt, rem, em, % o en unidades.

      >**Nota:** Si no especifica un tamaño, las columnas se ajustan automáticamente al tamaño de los márgenes de página dados.

   * **Diferencia entre columnas** : Especifique el espacio entre columnas individuales.

   * **Intervalo de columna** : Si desea que cualquier elemento del diseño de la página abarque varias columnas, debe utilizar esta propiedad. Esto se logra modificando el estilo del elemento deseado mediante las hojas de estilo; para obtener más información, consulte _\&lt;section explaining=&quot;&quot; style=&quot;&quot; customization=&quot;&quot;>_.

   En el diseño de página, si desea que un determinado texto aparezca en la primera página de todos los diseños de página de capítulo, puede agregarlo a la variante Primera página del diseño de página de capítulo.

   Como se muestra en el ejemplo siguiente, la propiedad Columna de expansión del texto del encabezado se establece en todo. Esto garantiza que, aunque el documento sea de varias columnas, el encabezado abarque todas las columnas.

   <img src="./assets/element-span-across-columns.png" width="400">

   >[**IMPORTANTE**]
   Puede aplicar la propiedad Columna de expansión a cualquier elemento DITA.

   * **Relleno de columna** : Especifique cómo rellena el contenido las columnas. De forma predeterminada, se establece en Balance , que rellena cada columna con la misma cantidad de contenido.

   * **Regla de columna** : Si desea tener una línea entre columnas, utilice esta propiedad para definir los estilos de línea o de regla. Especifique los valores de Estilo, Color y Ancho de la regla para agregar una línea entre columnas.


## Uso de las propiedades de página para una orientación de página diferente**

Al diseñar un diseño de página, es esencial tener control sobre las distintas propiedades de página. La función PDF nativo encapsula todas las propiedades de página principales en el panel Propiedades de página . El panel Propiedades de página proporciona acceso a varias propiedades en las siguientes secciones:

* **Tamaño de página**: Especifique el tamaño de página que desee usar para el diseño de página. La lista desplegable Tamaño de la página le permite elegir entre más de 15 tamaños de página.

* **Orientación**: Especifique la orientación de página que se utilizará para el diseño de página. Puede elegir entre las orientaciones de página Vertical u Horizontal. Tenga en cuenta que puede elegir que se apliquen distintas orientaciones a distintas variantes de página en un diseño de página. Por ejemplo, puede definir la orientación vertical en la primera página y el horizontal en los diseños de página izquierda y derecha.

* **Ver rotación**: Especifique la vista o la dirección en la que se coloca el contenido de la página. Puede elegir entre 90 grados en el sentido de las agujas del reloj, 90 en el sentido de las agujas del reloj o 180 grados en el sentido de las agujas del reloj. Esto resulta muy útil en una situación en la que desea utilizar una combinación de diseños verticales y horizontales en la salida. Por ejemplo, se puede usar vertical como diseño de página genérico y definir el diseño de página horizontal para capturar tablas largas. En ese caso, puede elegir mostrar el contenido de la tabla en el sentido de las agujas del reloj 90 grados. De este modo, la página se orientará en horizontal y el contenido se girará 90 grados para mantener la continuidad de la vista. Más adelante en esta sección veremos cómo se logra esto como ejemplo.

* **Reiniciar numeración desde**: Especifique el número de página desde el que comenzará la numeración de este diseño de página. Por ejemplo, puede crear un diseño de página para la sección Apéndice de su libro y configurar la numeración para que se reinicie desde 1.

* **Diseño**: Especifique los márgenes de la página junto con el relleno para los lados superior, inferior, izquierdo y derecho.

* **Contexto**: Incluya una imagen como imagen de fondo en el diseño de página. Puede especificar la altura y la anchura de la imagen junto con las propiedades de repetición y posición.

* **Nota al pie**: Especifique las propiedades para mostrar las notas al pie en la salida. Puede elegir especificar los márgenes y las propiedades de relleno junto con un estilo de borde.

Veamos un ejemplo en el que se utiliza una combinación de orientación de página vertical y horizontal y propiedades de rotación de vista. En este ejemplo, crearemos un PDF con orientación vertical predeterminada, pero una tabla se procesará en orientación horizontal con contenido en vista de 90 grados en sentido horario. El resultado final tendrá un aspecto similar al siguiente:

<img src="./assets/portrait-landscape-page-layouts.png" height="800">

En la salida anterior, la información de la Lista de contactos se presenta en modo horizontal con contenido también rotado en 90 grados. El contenido restante se muestra en el modo vertical normal.

Para lograr este tipo de salida, se deben realizar las siguientes tareas principales:

1. Cree un diseño de página con orientación horizontal.
1. Cambie la propiedad Ver rotación para representar el contenido en 90 grados en el sentido de las agujas del reloj.
1. Cree un estilo personalizado para usar el nuevo diseño de página.
1. Añada el estilo en la definición de salida de la tabla que queremos procesar en el diseño de página horizontal.

Siga estos pasos para realizar las tareas anteriores:

1. Cree un diseño de página con orientación horizontal.
   1. Cree un diseño de página &quot;horizontal&quot; siguiendo los pasos descritos en el procedimiento &quot;Crear un nuevo diseño de página&quot;.

   1. En el panel derecho, haga clic en **Propiedades de página**.

      <img src="./assets/page-properties-panel.png" width="300">
   1. Cambie el **Orientación** a **Horizontal**.

1. Cambie la propiedad Ver rotación para representar el contenido en 90 grados en el sentido de las agujas del reloj.

   1. Select **90° en el sentido de las agujas del reloj** en la lista desplegable Ver rotación .

   1. Haga clic en **Guardar todo** para guardar las propiedades actualizadas del diseño de página.

1. Cree un estilo personalizado para usar el nuevo diseño de página.
   1. Expanda la barra lateral izquierda y haga doble clic en la plantilla en la que desea crear el estilo.

   1. Expanda la sección Hojas de estilo .

   1. Pase el ratón sobre la hoja de estilo Diseño y haga clic en el icono (_Opciones_ icono) **...** y elija **Editar**.

      La hoja de estilo Presentación se abre para su edición.

   1. Haga clic con el botón derecho en **Otros estilos** y elija **Nuevo estilo**.

      <img src="./assets/stylesheet-other-new-style.png" width="300">

   1. En el **Agregar estilo** ventana emergente, introduzca `landscape-style` en el **Clase** campo name .

      <img src="./assets/stylesheet-new-landscape-style.png" width="400">

   1. Haga clic en **Listo**.

      Un nuevo estilo llamado `.landscape-style` se crea y agrega al final de **Otros estilos** lista.

   1. Haga doble clic en el `.landscape-style` para abrirlo y editarlo.

   1. Expanda el **Paginación** propiedad.

   1. Entrar `Landscape` en el **Diseño de página** propiedad.

      <img src="./assets/new-style-with-landscape-layout.png" width="500">

1. Añada el estilo en la definición de salida de la tabla que queremos procesar en el diseño de página horizontal.

   1. En el Editor web, abra el archivo donde desee aplicar el nuevo diseño de página.

   1. Busque la `<table>` elemento, que se va a procesar en modo horizontal.

   1. En la ruta de exploración, haga clic en la `table` para seleccionar la tabla.

      <img src="./assets/new-style-table-element.png" width="400">

   1. En el panel derecho, haga clic en y abra el **Propiedades de contenido** panel.

   1. En el **Propiedades de contenido** , agregue `outputclass` propiedad con `landscape-style` como valor de propiedad.

      <img src="./assets/new-style-table-outputclass.png" height="400">

   1. Haga clic en **Guardar todo** para guardar el archivo actualizado.

   1. Genere la salida del PDF.

El PDF final tendrá el contenido de la tabla representado en modo horizontal, como se muestra al principio del ejemplo.

## Trabajo con el panel Propiedades del contenido

El panel Propiedades de contenido permite actualizar fácilmente el aspecto de los elementos en el diseño de página. Las propiedades del panel Propiedades del contenido se dividen en las siguientes secciones:

>**Nota**: Para obtener más información sobre el uso de estas propiedades, consulte la documentación de W3C CSS Page Media Standards .

* **Atributos**: Contiene las propiedades ID, Class y Translate. Si establece la propiedad Translate en no, el contenido de ese elemento específico no se traduce.

* **Fuente**: Contiene propiedades relacionadas con fuentes. Puede definir Familia de fuentes, Peso, Tamaño, Decoración de texto (como subrayado, subrayado, contorno, interlineado), Estilo de texto (como negrita, cursiva, etc.), Alineación de texto (como izquierda, derecha, centro o justificado), Administrar espacios en blanco (como formato predefinido, sin ajuste, espacio de interrupción, etc.), Altura de línea, Espaciado entre letras y Sangría de texto.

* **Borde**: Contiene propiedades para agregar y dar formato a un borde de un elemento en el diseño de página. Puede definir Borde lateral (como todo, arriba, abajo, derecha o izquierda), Estilo de borde (como Sólido, Discontinuo, Trazado, etc.), Color de borde, Ancho y Radio para tener borde curvo. En el ejemplo siguiente, se ha añadido un borde curvo en el área de encabezado de la página.

   <img src="./assets/border-properties.png" width="500">

* **Diseño**: Contiene propiedades para configurar el diseño de un elemento en el diseño de página. Puede definir Alto, Ancho, Márgenes y Relleno (para arriba, abajo, izquierda o derecha), Horizontal o Vertical alignment, Flotante (como Izquierda, Derecha o Ninguno), Borrar (como izquierda, derecha, ambos o ninguno), Posición del elemento (como absoluta, fija, relativa o más), Visualización (como bloque, contenido, corrección o más), Índice Z, Transparencia, Transformación (mediante rotación o escala) y Transformar origen (por X y desplazamiento Y).

* **Contexto**: Contiene propiedades para incluir una imagen de fondo o un tono de color. Puede configurar el tamaño de la imagen (estableciendo Alto o Ancho), Repetir el fondo (como repetición, no repetición, redondo o más) y Posición de fondo (como arriba izquierda, centro derecho, centro inferior o más).

* **Múltiples columnas**: Contiene propiedades para configurar propiedades de varias columnas para la página o cualquier elemento específico, como la tabla de contenido del capítulo. Para obtener más información sobre las propiedades y cómo utilizarlas, consulte _Trabajar con diseño de página de varias columnas_.

