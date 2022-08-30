---
title: Función de publicación de PDF nativo | Diseño de un diseño de página
description: Aprenda a diseñar el diseño de la página para presentar información en diferentes secciones de la salida del PDF.
hide: true
hidefromtoc: true
exl-id: b4d3bdc4-0d01-46eb-b182-540380220485
source-git-commit: f8af7d7180b3d70d17e1410885017212dec721ef
workflow-type: tm+mt
source-wordcount: '4688'
ht-degree: 0%

---


# Diseño de un diseño de página

Al crear un documento de PDF, tendría diferentes secciones para presentar diferentes tipos de información. Por ejemplo, un documento de PDF comenzaría desde una portada o portada, que tendría el logotipo de su empresa, el título del libro o la información de la versión. Luego habría capítulos, apéndices o páginas del glosario. Cada sección de un documento PDF tiene un aspecto diferente y se logra creando y personalizando el diseño de página.

Al diseñar el diseño de la página, puede definir los distintos elementos que la componen. Por ejemplo, puede definir el tamaño de página, los márgenes, el encabezado y pie de página, la orientación y otras especificaciones de página en una página. La función Publicación de PDF nativos le permite diseñar su página según el [Estándares de medios de página](https://www.w3.org/TR/css-page-3/). La mayoría de los ajustes que se tratan en los estándares de medios pagados se pueden personalizar fácilmente mediante la interfaz de usuario de la función Publicación de PDF nativos . Para algunos otros formatos de nivel avanzado, puede utilizar la vista Origen para escribir su propio código CSS.

Una vez que haya diseñado los diseños de página, debe asociar estos diseños con sus secciones respectivas en la configuración de Diseño de página del PDF. Consulte la _Crear y personalizar diseños de página_ para obtener más información sobre cómo crear y abrir un diseño de página para su personalización.

## Tipos de diseños de página

Un documento de PDF generalmente contiene las siguientes secciones:

* Portada
* Tabla de contenido
* Alza de cifras
* Alza de tablas
* Páginas de capítulo o tema
* Glosario
* Índice
* Página de fondo

Estas secciones necesitarían un diseño de página correspondiente para presentar la información en un formato específico. Además, también puede tener una página en blanco que se utilice como usuario que rellena para iniciar un nuevo capítulo desde una página impar o par. En ese caso, puede utilizar el diseño de página predeterminado o crear un diseño de página para una página en blanco. Consulte _Crear un nuevo diseño de página_ para obtener más información.

La configuración de los diseños de página de la sección **Plantilla > Configuración** permite definir el diseño de página que se utilizará para las diferentes secciones del PDF. Cada diseño de página puede tener además diferentes variantes de página: primera, derecha o izquierda.

### Crear las variantes de diseño de la primera página, derecha o izquierda

Los diferentes diseños de página de la plantilla de PDF se pueden personalizar aún más si se tienen diferentes variantes de diseño de página de inicio, derecha o izquierda. Puede diseñar estas páginas de forma diferente utilizando el diseñador de diseño de página.

>[!NOTE]
>
>Si desea tener un diseño de página único para una sección del libro, no es necesario crear los diseños de página Primero, Derecha o Izquierda.

Tenga en cuenta los siguientes puntos al crear los diseños de página:

>[!NOTE]
>
>Los siguientes puntos toman el diseño de página de capítulo como ejemplo. Sin embargo, estos puntos también son válidos para otros diseños de página.

* Si desea utilizar un diseño de página único para todas las páginas de un capítulo, solo debe crear un diseño de página de capítulo único sin ninguna variante.

* Si desea tener un aspecto diferente para la primera página de los capítulos de su libro, debe crear una variante de diseño de primera página para los capítulos.

* Si desea tener un aspecto diferente para cada página izquierda y derecha del libro, debe crear las variantes del lado izquierdo y derecho para el diseño de la página del capítulo.

* Si desea que los capítulos comiencen desde una página impar o par, puede elegir crear un diseño de página para la página en blanco. Este diseño de página se utiliza para llenar el espacio entre dos capítulos a fin de garantizar que el capítulo comience desde la página par o impar deseada.

   >[!NOTE]
   >
   >Si no crea un diseño de página en blanco independiente, se utilizará el diseño de página predeterminado. Para crear un diseño de página, consulte _Crear un nuevo diseño de página_.

El siguiente ejemplo le guiará por el proceso de creación de variantes de un diseño de página:

1. Cree un diseño de página de &quot;Capítulo&quot; siguiendo los pasos descritos en el procedimiento &quot;Crear un nuevo diseño de página&quot;.

   Se crea y se agrega un diseño de página de capítulo en blanco en los diseños de página.

   De forma predeterminada, al crear un diseño de página, también se abre para su edición. La siguiente captura de pantalla muestra un diseño de página en blanco (predeterminado):

   <img src="./assets/default-blank-page-layout.png" width="300">

   El encabezado, pie de página y área de contenido de una plantilla se crean de forma predeterminada. Puede personalizar fácilmente estas áreas mediante las propiedades de página, las propiedades de contenido y varias herramientas (como insertar imágenes, campos, etc.) que se proporcionan en la interfaz de usuario.

   >[!NOTE]
   >
   >Para una configuración avanzada, puede usar la vista Origen y agregar el HTML personalizado y el código CSS.

1. Sitúe el ratón encima de **Capítulo** diseño y haga clic en **Opciones** para mostrar el menú contextual.

1. Haga clic o pase el ratón por encima **Agregar variante de diseño** y elija el diseño de página que desee crear (Primero, Izquierda o Derecha).

El diseño de página seleccionado se crea mediante una copia del diseño de capítulo base. Esto significa que si ha realizado cambios en el diseño predeterminado de la página del capítulo, los mismos cambios se replican en el diseño de la página variante en el momento de la creación del diseño de la página.

## Trabajo con las Propiedades de página de un diseño de página

Al diseñar un diseño de página, es esencial tener control sobre las distintas propiedades de página. La función Publicación de PDF nativo encapsula todas las propiedades de página principales en el panel Propiedades de página . El panel Propiedades de página proporciona acceso a varias propiedades en las siguientes secciones:

>[!NOTE]
>
>El panel Propiedades de página encapsula las propiedades y sigue las reglas definidas en la sección [Estándares de medios de página](https://www.w3.org/TR/css-page-3/).

* **Tamaño de página** : Especifique el tamaño de página que desee usar para el diseño de página. La lista desplegable Tamaño de la página le permite elegir entre más de 15 tamaños de página. También puede crear un diseño de página utilizando un tamaño de página personalizado; consulte **Definir el tamaño de la página** para obtener más información.

* **Orientación** : Especifique la orientación de página que se utilizará para el diseño de página. Puede elegir entre las orientaciones de página Vertical u Horizontal. Tenga en cuenta que puede elegir que se apliquen distintas orientaciones a distintas variantes de página en un diseño de página. Por ejemplo, si el contenido contiene una tabla amplia o una imagen grande, puede crear un diseño de página horizontal y aplicarlo a una tabla o imagen más amplia.

* **Ver rotación** : Especifique el lado o la dirección en que se representa el lado superior original después de la rotación. Puede elegir entre 90 grados en el sentido de las agujas del reloj, 90 en el sentido de las agujas del reloj o 180 grados en el sentido de las agujas del reloj. Esto resulta muy útil en una situación en la que desea utilizar una combinación de diseños verticales y horizontales en la salida. Por ejemplo, se puede usar el retrato como diseño de página genérico y se puede definir un diseño de página horizontal para procesar tablas anchas. En ese caso, puede configurar para mostrar el contenido de la tabla en el sentido de las agujas del reloj 90 grados. De este modo, la página se orientará en horizontal y el contenido se girará 90 grados para mantener la continuidad de la vista. Más adelante en esta sección veremos cómo se logra esto como ejemplo.

* **Reiniciar numeración desde** : Especifique el número de página desde el que comenzará la numeración de este diseño de página. Por ejemplo, puede configurar el número de página para que se reinicie para cada capítulo. En ese caso, debe establecer la propiedad Restart Numerering From en 1 (Reiniciar numeración desde) en la variante First page layout del diseño de la página del capítulo.

* **Diseño** : Especifique los márgenes de la página junto con el relleno para los lados superior, inferior, izquierdo y derecho. En la siguiente ilustración se explica cómo se representan los márgenes, el relleno y los bordes alrededor del contenido. Tenga en cuenta que el margen en la parte superior e inferior de una página contiene el encabezado y el pie de página.

   <img src="./assets/margins-padding-illustration.png" width="300">

* **Contexto** : Incluya una imagen o un color como fondo del diseño de la página. Para una imagen, puede especificar la altura y la anchura de la imagen junto con las propiedades de repetición y posición.

* **Nota al pie** : Especifique las propiedades para mostrar las notas al pie en la salida. Puede elegir especificar los márgenes y las propiedades de relleno junto con un estilo de borde.

### Definir el tamaño de la página

Lo primero que debe definir en un diseño de página es el tamaño de la página. En las Propiedades de página, hay más de 15 tamaños de página que puede elegir para un diseño de página. También puede crear un tamaño de página personalizado siguiendo estos pasos:

1. Abra el diseño de página necesario para editarlo.

   >[!NOTE]
   >
   >Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. En el panel derecho, haga clic en **Propiedades de página**.
1. En el **Tamaño de página** lista desplegable, seleccione **Personalizado**.

   Se muestran los campos Ancho de página y Alto de página .

1. Introduzca las dimensiones de página deseadas en la **Anchura de la página** y **Altura de la página** campos.

   >[!NOTE]
   >
   >Algunas de las unidades más utilizadas son px (píxeles), pt (puntos), rem, em, % (porcentaje) y in (pulgadas).

### Usar la orientación de la página y la rotación de la vista

Veamos un ejemplo en el que se utiliza una combinación de orientación de página vertical y horizontal y propiedades de rotación de vista. En este ejemplo, crearemos un PDF con orientación vertical predeterminada, pero una tabla se procesará en orientación horizontal con contenido en vista de 90 grados en sentido horario. El resultado final tendrá un aspecto similar al siguiente:

<img src="./assets/portrait-landscape-page-layouts.png" width="400">

En la salida anterior, la información de la Lista de contactos se presenta en modo horizontal con contenido también rotado en 90 grados. El contenido restante se muestra en el modo vertical normal.

Para lograr este tipo de salida, se deben realizar las siguientes tareas principales:

1. Cree un diseño de página con orientación horizontal.

1. Cambie el **Ver rotación** para procesar el contenido en 90°.

1. Cree un estilo personalizado para usar el nuevo diseño de página.

1. Añada el estilo en la definición de clase de salida de la tabla que queremos procesar en el diseño de página horizontal.

Siga estos pasos para realizar las tareas anteriores:

1. Cree un diseño de página con orientación horizontal.
   1. Cree un diseño de página &quot;horizontal&quot; siguiendo los pasos descritos en el procedimiento &quot;Crear un nuevo diseño de página&quot;.

   1. En el panel derecho, haga clic en **Propiedades de página**.

      <img src="./assets/page-properties-panel.png" width="300">
   1. Cambie el **Orientación** a **Horizontal**.

1. Cambie la propiedad Ver rotación para representar el contenido en el sentido de las agujas del reloj en 90°.

   1. Select **90° en el sentido de las agujas del reloj** en la lista desplegable Ver rotación .

   <img src="./assets/view-rotation-page-props.png" width="300">

   1. Haga clic en **Guardar todo** para guardar las propiedades actualizadas del diseño de página.

1. Cree un estilo personalizado para usar el nuevo diseño de página.
   1. Expanda la barra lateral izquierda y haga doble clic en la plantilla en la que desea crear el estilo.

   1. Expanda la sección Hojas de estilo .

   1. Pase el ratón sobre la hoja de estilo Diseño y haga clic en el icono (_Opciones_ )... y seleccione Editar.

      La hoja de estilo Presentación se abre para su edición.

   1. Haga clic con el botón derecho en **Otros estilos** y elija **Nuevo estilo**.
      <img src="./assets/stylesheet-other-new-style.png" width="300">

   1. En la ventana emergente Agregar estilo , introduzca **estilo horizontal** en el **classname**.
      <img src="./assets/stylesheet-new-landscape-style.png" width="400">

   1. Haga clic en **Listo**.

      Un nuevo estilo llamado `.landscape-style` se crea y agrega al final de la lista Otros estilos.

   1. Haga doble clic en el `.landscape-style` para abrirlo y editarlo.

   1. Expanda el **Paginación** propiedad.

   1. Entrar `Landscape` en el **Diseño de página** propiedad.

      <img src="./assets/new-style-with-landscape-layout.png" width="500">

   1. Haga clic en **Guardar todo** para guardar las propiedades de estilo actualizadas.

1. Añada el estilo en la variable `outputclass` definición de la tabla que se desea procesar en el diseño de página horizontal.
   1. En un editor de archivos DITA, abra el archivo en el que desea aplicar el nuevo diseño de página.

   1. Busque la `<table>` elemento, que se va a procesar en modo horizontal.

   1. En la ruta de exploración, haga clic en el elemento de tabla para seleccionar la tabla.

      <img src="./assets/new-style-table-element.png" width="400">

   1. En el panel derecho, haga clic en y abra el panel Propiedades de contenido .

   1. En el panel Propiedades del contenido, agregue una **outputclass** propiedad con **estilo horizontal** como valor de propiedad.

      <img src="./assets/new-style-table-outputclass.png" width="300">

1. Haga clic en **Guardar todo** para guardar el archivo actualizado.
1. Genere la salida del PDF.

El PDF final tendrá el contenido de la tabla representado en modo horizontal, como se muestra al principio del ejemplo.

### Agregar una imagen de fondo

Según sus necesidades, es posible que desee agregar una imagen de fondo que aparezca en cada primera página de un resultado de capítulo (PDF). Las propiedades Fondo de las Propiedades de página permiten agregar fácilmente una imagen de fondo. Puede elegir replicar esta imagen en una página y colocar la imagen en cualquier lugar del área superior, inferior o central de la página.

Por ejemplo, para insertar una imagen de fondo en la parte central del área de contenido, realice los siguientes pasos:

1. Abra el diseño de página necesario para editarlo.

   >[!NOTE]
   >
   >Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. Haga clic en cualquier lugar del área de contenido.

1. En el panel derecho, haga clic en **Propiedades de página**.

1. Expanda el **Contexto** para obtener más información.

1. Haga clic en el botón Examinar de la sección **Ruta de imagen** campo location .

1. Busque y seleccione la imagen que desee utilizar como imagen de fondo.

   La imagen se inserta y se duplica para cubrir toda la página.

1. Cambie el tamaño de la imagen ajustando las propiedades de altura y anchura.

   >[!NOTE]
   >
   >Puede introducir cualquiera de las propiedades de altura o anchura, ya que la imagen se escala automáticamente para mantener la relación de aspecto.

1. Defina las demás propiedades para ajustar el modo en que desea que aparezca la imagen de fondo.

   * **Repetición en segundo plano** : Especifique si desea que el fondo se repita o no.

   * **Posición de fondo** : Especifique una posición para la imagen de fondo de la página.

La siguiente captura de pantalla muestra la imagen de fondo con la propiedad Repetir fondo establecida en _no-repeat_ y la propiedad Posición de fondo establecida en _centro_.

<img src="./assets/background-image.png" width="500">

## Trabajar con encabezado y pie de página

Cuando se incluye información en un encabezado o pie de página de un diseño de página, dicha información se repite en todas las páginas que utilizan dicho diseño de página. Normalmente, el área del encabezado se utiliza para el título del capítulo o tema y el área del pie de página se utiliza para mostrar los números de página.

Al crear un nuevo diseño de página, el área de encabezado y pie de página se crea de forma predeterminada. Puede realizar muchas personalizaciones en el área de encabezado y pie de página de un diseño de página. Por ejemplo, puede insertar una imagen (como un logotipo), variables (que contengan información dinámica) o contenido estático.

### Cambiar los márgenes y líneas del encabezado y pie de página

De forma predeterminada, los márgenes de encabezado y pie de página se establecen en 1 pulgada. Puede cambiar este valor predeterminado cambiando la configuración Margen del panel Propiedades de página . Siga estos pasos para cambiar el tamaño del encabezado y del pie de página:

1. Abra el diseño de página necesario para editarlo.

   >[!NOTE]
   >
   >Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. En el panel derecho, haga clic en **Propiedades de página**.
1. Expanda el **Diseño** para obtener más información.
1. Haga clic en el icono de bloqueo situado junto a la **Margen** propiedad.
1. Para cambiar el tamaño del encabezado, introduzca el valor deseado en el campo Top margin .

   >[!NOTE]
   >
   >Algunas de las unidades más utilizadas son px (píxeles), pt (puntos), rem, em, % (porcentaje) y in (pulgadas).

1. Para cambiar el tamaño del pie de página, introduzca el valor deseado en el campo Bottom margin .

Puede diseñar el área de encabezado y pie de página para que contenga varias líneas. Para ello, agregue un&lt;p> mediante Insertar elementos de HTML (<img src="./assets/insert-html-element-2.svg" width="25">) en el área de encabezado o pie de página.

| _Ámbito del desarrollador_: <img src="./assets/developer-corner-icon.svg" width="25"> |
|---|

Si desea trabajar directamente con el CSS y el código del HTML, puede cambiar los valores de los márgenes como se muestra en el siguiente fragmento de código:

```css
…

<meta name="page-style" content="size:A4 portrait;margin-top:3cm;margin-right:30pt;margin-bottom:1in;margin-left:90px;" />

…
```

>[!NOTE]
>
>En el ejemplo anterior, se utilizan distintas unidades para especificar los valores de los márgenes.

### Eliminación del encabezado y el pie de página

La superposición de encabezado y pie de página en los márgenes superior e inferior. Técnicamente, esto significa que si desea tener un encabezado y un pie de página en el diseño de la página, debe reservar el espacio necesario en los márgenes superior e inferior.

Si no desea que un diseño de página tenga un encabezado y un pie de página, hay dos formas de conseguirlo:

* Si desea conservar los márgenes superior e inferior, deje el área del encabezado y pie de página en blanco.
* Si no desea conservar los márgenes superior e inferior (como el diseño de la portada y trasera de una revista), puede quitar los márgenes estableciendo las propiedades de margen superior e inferior en 0. Esto no deja espacio para el encabezado y el pie de página.

### Añadir una imagen o un logotipo en el encabezado

Según sus necesidades, es posible que desee agregar una imagen que aparezca en el área de encabezado (o en cualquier otra parte) del diseño de la página. Existen dos formas de agregar una imagen al diseño de página:

* Utilice una imagen de la plantilla Recursos.
* Utilice el&lt;add image=&quot;&quot;> en el editor de diseño de página.

>[!NOTE]
>
>Se recomienda utilizar la carpeta Recursos para administrar todos los recursos de plantilla, como imágenes o fuentes.

Para insertar una imagen como el logotipo de su empresa en el área del encabezado, realice los pasos siguientes:

1. Abra el diseño de página necesario para editarlo.

>[!NOTE]
>
>Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. Haga clic en Editar encabezado (<img src="./assets/header-icon.svg" width="25">) para colocar el cursor en el área del encabezado.

   O bien, haga clic dentro del área del encabezado.

1. Para agregar una imagen, elija cualquiera de los siguientes métodos:
1. Haga clic en el **Inertar imagen** (<img src="./assets/insert-image-icon.svg" width="25">) en la barra de herramientas; en el **Seleccionar ruta** elemento emergente, busque la ubicación de la imagen y haga clic en **Select** para insertarlo en el área del encabezado.
1. Arrastre y suelte una imagen de la carpeta Recursos en el área de encabezado.

La siguiente captura de pantalla muestra una imagen de ejemplo añadida en el área del encabezado.

<img src="./assets/image-in-header-area.png" width="500">

Una vez insertada la imagen, puede modificar sus atributos para darle el aspecto que desee. La forma más sencilla de cambiar el aspecto de una imagen o cualquier otro elemento del diseño de la página, utilice el panel Propiedades del contenido . Consulte _Trabajo con el panel Propiedades del contenido_ para las distintas propiedades disponibles a través de la interfaz de usuario para personalizar.

### Añadir campos y metadatos

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

Cada una de estas categorías de campos contiene diferentes variaciones en las que se puede insertar la información del campo. Por ejemplo, un campo de fecha puede tener diferentes variaciones, como `YYYY-MM-DD`, `MM/DD/YY`, `MM/DD/YYYY` y así sucesivamente. Del mismo modo, Número de página puede tener variaciones en forma de formatos romanos, decimales o incluso de configuración regional, como _Árabe_, _Devanagari_, _Hebreo_, y más.

Además de los campos predefinidos, también puede añadir información de metadatos como variables o campos en el diseño de página. Estos metadatos se almacenan en el contenido de asignación DITA de origen y se pueden insertar fácilmente en el diseño de página. Para obtener más información, consulte _Trabajar con campos y metadatos_.

En el siguiente ejemplo, insertaremos un número de página y un título de capítulo en el área de pie de página de un diseño de página.

1. Abra el diseño de página necesario para editarlo.

   >[!NOTE]
   >
   >Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. Haga clic en el **Editar pie de página** (![](./assets/footer-icon.svg)) para colocar el cursor en el área del pie de página.

   O bien, haga clic dentro del área del pie de página.

1. Inserte un elemento de párrafo haciendo clic en el botón **Insertar elementos de HTML** (<img src="./assets/insert-html-element-2.svg" width="25">) y seleccione Párrafo en la lista de elementos.

1. Haga clic en el **Insertar campos** (![](./assets/insert-fields-icon.svg)).

   Aparecerá la ventana emergente Campos.

1. Seleccione el **Número de página** de la lista Campo, la categoría **default(1)** formato de número de página de la lista Formato y haga clic en **Insertar**.

   <img src="./assets/insert-page-number-field.svg" width="400">

   >[!NOTE]
   >
   >También puede editar el formato de todos los campos, excepto el formato predeterminado. Para ello, haga clic en el icono Editar junto al formato que desea editar, realice cambios y haga clic en Aceptar. Para obtener más información, consulte _Trabajar con campos y metadatos_.

   El campo de número de página predeterminado se inserta en el área de pie de página del diseño de página.

   <img src="./assets/page-number-field-in-footer.png" width="400">

   La ruta de exploración superior enumera los elementos en los que se almacena la información.

1. Introduzca un espacio en blanco después del campo de número de página y haga clic en el botón **Insertar campos** icono.

1. Seleccione el **Título del capítulo** de la lista Campo, la categoría **Título del capítulo** en la lista Formato y haga clic en **Insertar**.

   La variable _Título del capítulo_ , que se rellena con el título del capítulo en el momento de la publicación, se inserta en el área de pie de página. En este momento, los campos número de página y título del capítulo están separados por un espacio.

   <img src="./assets/page-number-topic-title-near-footer.png" width="400">

1. Para alinear a la derecha el título del capítulo, realice los siguientes pasos:

   1. Haga clic en el elemento Campo de la ruta de exploración para seleccionar el campo Título del capítulo .

   1. En el panel derecho, haga clic en la **Propiedades de contenido** (<img src="./assets/content-properties-icon.png" width="25">) icono.

   1. Expanda el **Diseño** propiedades y establezca la variable **Flotante** valor de propiedad a **right**.
      <img src="./assets/float-prop-html-content.png" width="400">

      El campo Título del capítulo se alinea hacia la derecha del pie de página.
      <img src="./assets/topic-title-moved-right-footer.png" width="500">


| _Ámbito del desarrollador_: <img src="./assets/developer-corner-icon.svg" width="25"> |
|---|

Si desea trabajar directamente con el CSS y el código del HTML, también puede conseguirlo yendo la vista Origen del diseño de página y realizando cambios en el código. El siguiente fragmento de código muestra la misma configuración de pie de página realizada a través del código:

```css
…
<p>

<span data-field="page-number" data-format="default">1</span>

<span data-field="chapter-title" data-format="default" style="float: right">Chapter Title</span>

</p>
…
```

## Trabajo con área de contenido

El área de contenido es el área más grande en términos de espacio de contenido. El área de contenido se rellena con el contenido del tema. En algunos casos especiales, puede añadir contenido repetitivo en el área de contenido. Este contenido se publica en la ubicación especificada en el diseño de página. Por ejemplo, el encabezado de la tabla de contenido, glosario e índice se puede añadir como contenido repetitivo, que se publica &quot;tal cual&quot; en la salida final. Otro ejemplo es la tabla de contenido del capítulo, que generalmente se agrega en la primera página de cada capítulo.

Una de las personalizaciones más utilizadas en el área de contenido es el diseño de varias columnas. Con el potente diseñador de diseños de página, puede personalizar páginas específicas para procesarlas en varias columnas, a la vez que mantiene el contenido en otras páginas en una sola columna.

En las secciones siguientes, se tratan varios escenarios para personalizar el área de contenido.

### Agregar una tabla de contenido de capítulo

Una tabla de contenido de capítulo sirve como referencia rápida para que los lectores sepan qué hay en el capítulo. Normalmente, se añade una tabla de contenido de capítulo al principio de un capítulo. Por lo tanto, si desea utilizar una tabla de contenido de capítulo, puede agregarla al área de contenido del diseño de página de capítulo principal o la primera variante de diseño de página de un capítulo.

En el siguiente ejemplo, insertaremos una tabla de contenido de capítulo en el primer diseño de página de un capítulo:

>[!NOTE]
>
>Para este procedimiento, se da por hecho que se ha creado la variante First page para un diseño de página de capítulo. Para obtener instrucciones sobre cómo crear una variante de página, consulte _Crear las variantes de diseño de la primera página, derecha o izquierda_.

1. Abra el diseño de página necesario para editarlo.

   >[!NOTE]
   >
   >Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. Coloque el cursor en el área de contenido del diseño de página.

1. Haga clic en la tabla de contenido del capítulo (<img src="./assets/chapter-toc-icon.svg">) icono.

   La tabla de contenido del capítulo predeterminada se inserta en el área de contenido.

   <img src="./assets/chapter-toc-default.png" width="400">

   >[!NOTE]
   >
   >La tabla de contenido del capítulo predeterminado contiene los encabezados del 1 al 4. En este caso, el encabezado 1 es el propio título del capítulo. Por lo tanto, es posible que no desee volver a incluir el título del capítulo en la tabla de contenido o que desee aumentar el nivel de encabezados que desee en la tabla de contenido. Puede personalizar la tabla de contenido cambiando las propiedades.

1. Abra el panel Propiedades de contenido para personalizar los niveles de encabezado de la tabla de contenido.

   Por ejemplo, si desea comenzar desde el encabezado 2, cambie la primera lista desplegable para que comience desde 2.

   <img src="./assets/customize-chapter-toc.png" width="400">

   Del mismo modo, si desea que los encabezados lleguen hasta el nivel 5, cambie la segunda lista desplegable a 5. La tabla de contenido actualizada se verá como se muestra a continuación:

   <img src="./assets/chapter-toc-updated.png" width="400">

   >[!NOTE]
   >
   >El PDF publicado finalmente solo mostrará las entradas de la tabla de contenido en función del contenido de sus capítulos. Si no tiene encabezados de nivel 5 en un capítulo, no se mostrarán en el resultado final.

La apariencia de la tabla de contenido predeterminada se puede personalizar mediante las hojas de estilo. El estilo que comienza con `chaptoc-level-#` (like `chaptoc-level-1`, `chaptoc-level-2`, etc.) se utilizan para personalizar los estilos de la tabla de contenido del capítulo. Para obtener más información sobre los elementos de hojas de estilo utilizados en la tabla de contenido y cómo personalizarlos, consulte _Personalización de la TDC de capítulo predeterminada_.

>[!IMPORTANT]
>
>Actualmente, si realiza actualizaciones de estilo en una hoja de estilo, es posible que no se refleje en la vista previa del contenido. Sin embargo, la salida se procesa con los estilos actualizados.

### Trabajar con diseño de página de varias columnas

Los diseños de página de varias columnas son muy comunes en la publicación de revistas o índices en un libro. La función Publicación de PDF nativos permite dividir fácilmente el documento en varias columnas. Si utiliza diferentes diseños de página, puede elegir mantener solamente una sección específica dividida en varias columnas, mientras mantiene las demás secciones en un único diseño de columna (o normal).

Para crear un diseño de página con varias columnas, realice los pasos siguientes:

1. Abra el diseño de página necesario para editarlo.

   >[!NOTE]
   >
   >Consulte _Personalización de un diseño de página_ para abrir un diseño de página para personalizarlo o editarlo.

1. Como el diseño de varias columnas se aplica al contenido, excluyendo el área de encabezado y pie de página, debe seleccionar el elemento de contenido en la ruta de exploración.

   Una vez seleccionada la ruta de exploración del contenido, el panel Propiedades del contenido mostrará las propiedades de Varias columnas.

   <img src="./assets/multiple-columns-properties.png" width="400">

1. Utilice las propiedades de varias columnas para personalizar el diseño de página de varias columnas:

   * **Recuento de columnas:** Especifique el número de columnas para dividir la página. Utilice los iconos de flecha arriba y abajo o introduzca un número para establecer el número de columnas.

   * **Anchura de columna:** Especifique el ancho de una columna en una presentación de varias columnas. De forma predeterminada, el tamaño se establece en píxeles (px); también se puede especificar en pt, rem, em, % o en unidades.

      >[!NOTE]
      >
      >Si no especifica un tamaño, las columnas se dividen uniformemente para que encajen en la página dada. En la mayoría de los casos, no es necesario especificar este valor.

   * **Diferencia entre columnas** : Especifique el espacio entre columnas individuales.

   * **Intervalo de columna** : Si desea que cualquier elemento del diseño de la página abarque varias columnas, debe utilizar esta propiedad. Esto se logra modificando el estilo del elemento deseado mediante las hojas de estilo; para obtener más información, consulte _Sección que explica la personalización de estilos_.

   En el diseño de página, si desea que un determinado texto aparezca en la primera página de todos los diseños de página de capítulo, puede agregarlo a la variante Primera página del diseño de página de capítulo.

   Como se muestra en el ejemplo siguiente, la propiedad Columna de expansión del texto del encabezado se establece en todo. Esto garantiza que, aunque el documento sea de varias columnas, el encabezado abarque todas las columnas.

   <img src="./assets/element-span-across-columns.png" width="400">

   >[!IMPORTANT]
   >
   >Puede aplicar la propiedad Span Column a cualquier elemento DITA utilizando el atributo outputclass .

   * **Relleno de columna** : Especifique cómo rellena el contenido las columnas. De forma predeterminada, se establece en Balance , que rellena cada columna con la misma cantidad de contenido.

   * **Regla de columna** : Si desea tener una línea entre columnas, utilice esta propiedad para definir los estilos de línea o de regla. Especifique los valores de Estilo, Color y Ancho de la regla para agregar una línea entre columnas.


## Trabajo con el panel Propiedades del contenido

El panel Propiedades de contenido permite actualizar fácilmente el aspecto de los elementos en el diseño de página. Las propiedades del panel Propiedades del contenido se dividen en las siguientes secciones:

* **Fuente** : Contiene propiedades relacionadas con el texto. Puede definir Familia de fuentes, Peso, Tamaño, Decoración de texto (como subrayado, subrayado, contorno, interlineado), Estilo de texto (como negrita, cursiva, etc.), Alineación de texto (como izquierda, derecha, centro o justificado), Administrar espacios en blanco (como formato predefinido, sin ajuste, espacio de interrupción, etc.), Altura de línea, Espaciado entre letras y Sangría de texto.

* **Borde** : Contiene propiedades para agregar y dar formato a un borde de un elemento en el diseño de página. Puede definir Borde lateral (como todo, arriba, abajo, derecha o izquierda), Estilo de borde (como Sólido, Discontinuo, Trazado, etc.), Color de borde, Ancho y Radio para tener un borde curvo. En el ejemplo siguiente, se ha añadido un borde curvo en el área de encabezado de la página.

   <img src="./assets/border-properties.png" width="500">

* **Diseño** : Contiene propiedades para configurar el diseño de un elemento en el diseño de página. Puede definir Alto, Ancho, Márgenes y Relleno (para arriba, abajo, izquierda o derecha), Horizontal o Vertical, Flotante (como Izquierda, Derecha o Ninguno), Borrar (como izquierda, derecha, ambos o ninguno), Posición del elemento (como absoluta, fija, relativa o más), Visualización (como bloque, contenido, corrección o más), Índice Z, Transparencia, Transformación (mediante rotación o escalado) y Transformar origen (por X y desplazamiento Y).

* **Contexto** : Contiene propiedades para incluir una imagen de fondo o un tono de color. Puede configurar el tamaño de la imagen (estableciendo Alto o Ancho), Repetir el fondo (como repetición, no repetición, redondo o más) y Posición de fondo (como arriba izquierda, centro derecho, centro inferior o más).
* **Múltiples columnas** : Contiene propiedades para configurar propiedades de varias columnas para la página o cualquier elemento específico, como la tabla de contenido del capítulo. Para obtener más información sobre las propiedades y cómo utilizarlas, consulte _Trabajar con diseño de página de varias columnas_.
