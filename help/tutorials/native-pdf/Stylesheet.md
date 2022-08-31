---
title: Función de publicación de PDF nativo | Trabajar con estilos de contenido comunes
description: Aprenda a crear hojas de estilo y crear estilos para el contenido.
hide: true
hidefromtoc: true
source-git-commit: fb341dab718b8ae64578748d54a40df7e71af223
workflow-type: tm+mt
source-wordcount: '3500'
ht-degree: 0%

---


# Trabajar con estilos de contenido comunes

Una hoja de estilo contiene las definiciones de estilos para los elementos que se utilizan en la salida del PDF. Puede elegir trabajar con las hojas de estilo de ejemplo o crear otras nuevas. En la mayoría de los casos, la creación de una copia de la hoja de estilo de ejemplo de OOTB le ayudará a empezar rápidamente.

El editor de estilos es un editor WYSIWYG que oculta todas las complejidades de un código CSS detrás de la interfaz de usuario. Con el editor de estilos, puede personalizar fácil y rápidamente los estilos de los elementos que elija. Los estilos se clasifican bajo los siguientes encabezados:

* Estilos de encabezado
* Estilos de párrafo
* Estilos de carácter
* Estilos de hipervínculo
* Estilos de imagen
* Estilos de lista
* Estilos de tabla
* Estilos Div
* Estilos de página
* Otros estilos

Cuando se trabaja con contenido DITA estructurado, la asignación de estilos para la mayoría de los elementos DITA está en su lugar en la hoja de estilo predeterminada. Si está trabajando con elementos DITA estándar, puede cambiar su aspecto directamente realizando cambios en la definición del estilo. Estas definiciones de estilo están disponibles en la categoría Otro estilo . Para obtener más información, consulte *Trabajar con otros estilos* más adelante en este tema.

Las siguientes secciones tratan la configuración de estilo más utilizada en forma de ejemplos.

>[!NOTE]
>
>En los ejemplos siguientes, se da por hecho que está trabajando con la hoja de estilo de ejemplo incluida con el producto.

## Trabajar con estilos de encabezado

Los estilos de encabezado encapsulan todos los estilos básicos para los encabezados utilizados en el contenido. OOTB obtendrá 6 estilos de encabezado base y un estilo de encabezado para el título del tema/capítulo y el apéndice. En un documento estructurado, el H1 representa el título del tema o capítulo y los H2 a H6 se utilizan para subtemas o secciones dentro de un tema o capítulo. Esta jerarquía de encabezados se aplica automáticamente al contenido cada vez que se encuentra el encabezado correspondiente.

>[!NOTE]
>
>Puede crear sus propios estilos de encabezado personalizados y estos se pueden usar en el contenido mediante la clase de salida. Para obtener más información, consulte el paso 4 de *Usar la orientación de la página y la rotación de la vista* ejemplo.

### Crear encabezados de nivel de capítulo personalizados

En un libro (o un mapa de libros), trabajará con los capítulos. Los estilos de encabezado base están diseñados de tal manera que se apliquen en los encabezados de nivel de capítulo sin ninguna personalización. Sin embargo, si desea crear encabezados especializados para el contenido, tendrá que crearlos. Por ejemplo, el valor predeterminado `h1.chapter` se aplica al título del capítulo. Si desea que el título del capítulo aparezca en un estilo diferente, debe personalizar la variable `h1.chapter` estilo. Del mismo modo, puede crear estilos personalizados para los subencabezados del capítulo. Por ejemplo, si desea crear un estilo personalizado para todos los 2<sup>nd</sup> y 3<sup>rd</sup> encabezados de nivel en el capítulo y, a continuación, debe crear un nuevo estilo como `h2.chatper` y `h3.chatper`.

Como la característica Publicación de PDF nativos contiene las definiciones de estilo base para los estilos más comunes, aunque elimine accidentalmente un estilo, el estilo predeterminado se aplica al contenido. Por ejemplo, si no hay definición de estilo para el estilo h2 en la hoja de estilo, la función Publicación de PDF nativos aplicará algún estilo base al contenido h2.

En este ejemplo, crearemos un estilo de encabezado de capítulo de segundo nivel:

1. Abra la hoja de estilo necesaria para editarla.
   >[!NOTE]
   >
   >Consulte *Personalización de un estilo nuevo o predefinido* para abrir una hoja de estilo para personalizarla o editarla.

1. En el **Estilos** , expanda la **Estilos de encabezado**.
1. Haga clic con el botón derecho en **Estilos de encabezado** estilo y elija **Nuevo estilo**.
1. En el *Agregar estilo* mantenga la variable **Etiqueta** name como `h2` y escriba `chapter` en el **Clase** campo name .
1. Haga clic en **Listo**.

Un nuevo estilo de encabezado con el nombre `h2.chapter` se crea y se agrega en la lista Estilos de encabezado.

Una vez que haya creado un estilo, puede personalizar las propiedades del estilo con el editor de estilos.

### Crear encabezados de número automático

Uno de los estilos de salida más utilizados son los encabezados numerados automáticamente. Estos encabezados representan los números de capítulo, tema y subtema. Los encabezados de número automático son diferentes de los estilos de lista en los que a una lista de elementos de un tema se les asignan números automáticos.

En este ejemplo, personalizaremos los encabezados de nivel 1 a nivel 3 para usar números automáticos en diferentes formatos.

1. Abra la hoja de estilo necesaria para editarla.

   >[!NOTE]
   >
   >Consulte *Personalización de un estilo nuevo o predefinido* para abrir una hoja de estilo para personalizarla o editarla.

1. En el **Estilos** , expanda la **Estilos de encabezado**.

1. Seleccione el **h1** de la lista.
Las propiedades del estilo h1 se muestran en el panel Propiedades junto con su Vista previa.

   >[!NOTE]
   >
   >El panel Vista previa le proporciona una vista en tiempo real de cualquier actualización de estilo que aplique en cualquier elemento.

1. Seleccione el **Autonumber** propiedad.

   Los estilos que se pueden aplicar en la lista de números automáticos se muestran debajo de la propiedad Autonumber .

1. Establezca las siguientes propiedades:
   * **Estilo**: Seleccione entre una amplia gama de estilos de numeración genéricos o específicos de la configuración regional. Puede elegir estilos como árabe-hindi, devanagari, georgiano, decimal, alfa inferior, etc. Para el ejemplo actual, seleccione `upper-alpha`.

   * **Formato**: El formato predeterminado es `<x>`, donde el `x` se reemplaza por el estilo de numeración que haya seleccionado en la propiedad Estilo. Por ejemplo, si ha seleccionado `decimal` (1) estilo y, a continuación, el valor de `x` incrementos automáticos para cada instancia de la variable `h1` y va como 2, 3, etc. También puede agregar texto personalizado en el campo para dar formato al estilo del encabezado. Por ejemplo, si desea que todos los encabezados h1 tengan un prefijo de `Chapter`, debe definir este campo como `Chapter <x>`.

   * **Insertar carácter**: Si desea agregar cualquier carácter especial en el Formato, haga clic en Insertar carácter (<img src="./assets/insert-chars.png" width="25">) icono. Seleccione el carácter que desee agregar en el formato de estilo y haga clic en Insertar. Existen diferentes tipos de caracteres especiales que puede elegir en la lista desplegable Seleccionar categoría . Para nuestro ejemplo, seleccione la Comilla de ángulo doble puntal derecha en la categoría Puntuación .

      <img src="./assets/insert-special-chars.png" width="400">


   * **Iniciar numeración desde**: Si desea que la numeración comience desde un número específico, proporcione ese valor. Para nuestro ejemplo, mantenga el valor predeterminado de 1.

   * **Sangría**: Si desea sangrar el encabezado, debe definir el valor de sangría. Para nuestro ejemplo, establézcalo en 0 px.

      >[!NOTE]
      >
      >Puede introducir el valor en px (píxeles), pt (puntos), rem, em, % (porcentaje) o en unidades (pulgadas).

   * **Anchura de prefijo**: Este es el área ocupada por el formato de número automático. Se establece automáticamente en un tamaño que puede acomodar fácilmente el formato de estilo seleccionado. Si desea aumentar el tamaño, puede reemplazar el valor predeterminado.

      Al configurar este valor manualmente, intente cambiar las demás propiedades que afectarán a la anchura. Por ejemplo, cambie el tamaño de fuente, el formato con prefijo (capítulo) o un sufijo (:), establezca el valor máximo en la variable *Iniciar numeración desde* y las distintas propiedades de fuente para obtener un tamaño óptimo.

      Para nuestro ejemplo, mantenga el valor predeterminado.

   * **Espaciado**: Especifique el espaciado horizontal y vertical. Para nuestro ejemplo, mantenga los valores predeterminados.

      Con las personalizaciones anteriores, el estilo se personaliza como se muestra a continuación:

      <img src="./assets/h1-style-custmization.png" width="500">

   * **Aplicar formato a**: Las propiedades de la categoría Autonumber le ayudarán a definir el estilo de numeración. Para aplicar más personalizaciones al estilo de numeración o al contenido del formato de encabezado, puede elegir Numeración o Párrafo en este campo. Si elige Numeración, cualquier cambio realizado en Fuente, Borde, Diseño y otras categorías se aplicará únicamente al estilo de numeración del encabezado. Sin embargo, si elige Párrafo, los cambios se aplicarán al contenido del encabezado y no al estilo de numeración.

   Utilice la siguiente configuración para generar un resultado mostrado en la siguiente captura de pantalla:

   |**Estilo de encabezado**|**Propiedad**|**Valor**|**Comentarios adicionales**| | :- | :- | :- | :- | |h1|Estilo|Decimal|Estas propiedades se encuentran en la categoría Autónomo | ||Formato|`Capter <x>:`|| ||Ancho del prefijo|160 px|| ||Fuente > Alineación de texto|Izquierda|Asegúrese de que Aplicar formato a está establecido en Numeración| |h2|Estilo|Decimal|Estas propiedades se encuentran en la categoría Autónomo | ||Formato|`Section <x>:`|| ||Ancho del prefijo|125 px|| ||Fuente > Alineación de texto|Izquierda|Asegúrese de que Aplicar formato a está establecido en Numeración| |h3|Estilo|Decimal|Estas propiedades se encuentran en la categoría Autónomo | ||Insertar nivel|2|| ||Formato|`Section <2>.<x>:`|| ||Ancho del prefijo|125 px|| ||Fuente > Alineación de texto|Izquierda|Asegúrese de que Aplicar formato a está establecido en Numeración| ||

   <img src="./assets/auto-number-output.png" width="500">

## Trabajar con estilos de párrafo

Se puede crear un estilo de párrafo para aplicar un formato especial a todo un párrafo. Sin embargo, con la seudoclase, puede aplicar un estilo solo a una parte específica del texto. En el siguiente ejemplo, se creará un estilo de párrafo para usar el estilo de la tapa de colocación.

### Crear el estilo de la tapa desplegable

En las revistas se utiliza un estilo de capuchón (o capital perdido) y en los documentos literarios donde el primer carácter de un párrafo o sección tiene un estilo especial. Puede lograr el mismo efecto utilizando la función Publicación de PDF nativo.

En el siguiente ejemplo, se creará un estilo de límite de colocación:

1. Abra la hoja de estilo necesaria para editarla.

   >[!NOTE]
   Consulte *Personalización de un estilo nuevo o predefinido* para abrir una hoja de estilo para personalizarla o editarla.

1. En el **Estilos** , expanda la **Estilos de párrafo**.

1. Haga clic con el botón derecho en el **Estilo de párrafo** y elija **Nuevo estilo**.

1. En el *Agregar estilo* mantenga la variable **Etiqueta** nombre como p y en la variable **Pseudo** **Clase** campo, seleccione `::first-letter`.

1. Haga clic en **Listo**.

   Un nuevo estilo de párrafo llamado `::first-letter`  se crea y se agrega en la variable **Estilos de párrafo** lista.

1. Select `::first-letter` en el estilo p y defina las siguientes propiedades:

   * **Fuente**: Defina la fuente que desee para la primera letra del párrafo. Para nuestro ejemplo, defina la Familia de fuentes como cursiva, el peso de fuente como 500, el tamaño de fuente como 30 pt y elija un color de fuente.

   * **Diseño**: Establezca la alineación vertical del texto alrededor del estilo de la tapa de colocación. Para nuestro ejemplo, estableceremos la Alineación vertical en Abajo.

Como `p` se asigna con la variable `<p>` en DITA, no es necesario añadir explícitamente este estilo utilizando el atributo outputclass . Donde sea que esté en el contenido a `<p>` se utiliza, el estilo de límite de colocación se aplica automáticamente. En la siguiente captura de pantalla, el título del capítulo, la descripción breve y los elementos de la lista de definición no tienen formato con el estilo de la tapa de colocación. Solo se da formato al estilo de párrafo con el estilo de la tapa de colocación:

<img src="./assets/char-style-drop-cap.png" width="500">

## Trabajar con estilos de carácter

Con los estilos de carácter, puede crear estilos para dar formato a caracteres o palabras dentro del contenido. Por ejemplo, puede crear un estilo de carácter para el código en línea o el nombre de archivo, o bien crear un estilo que utilice varios formatos de estilo en el contenido seleccionado.

### Crear un estilo de carácter en línea

El formato de caracteres en línea o de palabras en un párrafo es un estilo muy común. El proceso de creación de un estilo en línea implica dos tareas: primero, crear un nuevo estilo en la hoja de estilo y, segundo, aplicar el estilo en el contenido utilizando la variable `outputclass` atributo.

En el siguiente ejemplo, se creará un estilo de carácter en línea:

1. Abra la hoja de estilo necesaria para editarla.

   >[!NOTE]
   Consulte *Personalización de un estilo nuevo o predefinido* para abrir una hoja de estilo para personalizarla o editarla.

1. En el **Estilos** , expanda la **Estilos de carácter**.

1. Haga clic con el botón derecho en el **Estilo de carácter** y elija **Nuevo estilo**.

1. En el cuadro de diálogo Agregar estilo, mantenga la variable **Etiqueta** nombre como intervalo e introduzca `BoldItalic` en el **Clase** campo name .

   <img src="./assets/create-char-style.png" width="400">

1. Haga clic en **Listo**.

   Se crea y se agrega un nuevo estilo de carácter denominado código en la lista Estilos de carácter.

1. Select `span.BoldItalic` de la variable **Estilo de carácter** y establezca las siguientes propiedades:

   * **Fuente**: Todas las propiedades relacionadas con fuentes se pueden personalizar desde esta sección. De forma predeterminada, hay algunas fuentes empaquetadas con el producto. Puede elegir la fuente que desee para el estilo de carácter. Para nuestro ejemplo, establezca la Familia de fuentes en *Serif,* y seleccione *Negrita* y *Cursiva* en la propiedad Estilo de fuente . También puede personalizar otras propiedades de fuente, como Grosor de fuente (como negrita, más claro), Decoración de texto (como subrayado, subrayado), Tamaño de fuente, Color de fuente, Alineación de texto, etc.

      >[!NOTE]
      También puede agregar fuentes a la plantilla, que se almacenan en la sección Recursos de la plantilla. Para obtener más información sobre cómo agregar fuentes y trabajar con Recursos, consulte **Agregar un vínculo a la sección Recursos**.

   * **Diseño**: Puede establecer las propiedades relacionadas con el diseño, como Alto y Ancho, Margen, Relleno, Alineación, etc.

   * **Contexto**: Las propiedades Fondo permiten dar formato al color de fondo de un estilo concreto. Puede definir el color de fondo o la imagen para cualquier estilo.

Una vez que haya creado el estilo de carácter en línea, debe aplicarlo en el contenido. Para aplicar el estilo de código en línea, vaya a la vista de origen y añada la variable `outputclass` en el contenido deseado:

`outputclass="BoldItalic"`

En el siguiente ejemplo se muestra el formato de negrita cursiva que se está aplicando en diferentes lugares del texto en ejecución:

<img src="./assets/char-format-applied.png" width="500">

## Personalizar estilo de lista

Los estilos de lista contienen la configuración de estilo predeterminada para las listas ordenadas y sin ordenar. Puede personalizar fácilmente estos estilos de lista para satisfacer los requisitos de documentación.

En el siguiente ejemplo, personalizaremos el estilo de lista numerada u ordenada:

1. Abra la hoja de estilo necesaria para editarla.

   >[!NOTE]
   Consulte *Personalización de un estilo nuevo o predefinido* para abrir una hoja de estilo para personalizarla o editarla.

1. En el **Estilos** , expanda la **Estilos de lista**.

1. Seleccione el **ol** de la lista.

   Las propiedades del estilo antiguo se muestran en el panel Propiedades junto con su Vista previa.

   <img src="./assets/list-style-default.png" width="500">

1. Seleccione el **Formato avanzado** .

   Se muestra un mensaje de confirmación.

1. Haga clic en **Sí** en el *Confirmación* para abrir el **Formato avanzado** propiedades.

   Las siguientes propiedades están disponibles de forma predeterminada:

   * **Nivel**: De forma predeterminada, hay 6 niveles de listas numeradas. El nivel que seleccione en esta lista desplegable controla los cambios de estilo en el nivel seleccionado y en todos los niveles subsiguientes. Por ejemplo, si selecciona el nivel 4, todos los cambios de estilo que aplique se establecerán en los niveles 4, 5 y 6.

   * **Tipo de estilo de lista**: Hay varios estilos de numeración de listas entre los que puede elegir. La lista contiene estilos de numeración genéricos y específicos de la configuración regional que se utilizan para crear una lista numerada. Algunos de los tipos de estilos de lista son árabe, camboyano, devanagari, etíope, hangul, hebreo, japonés, coreano, chino simple, urdu y más.

   Además, puede trabajar con las siguientes propiedades de formato avanzado:

   * **Formato de número**: El formato predeterminado es `<x>`, donde el `x` se reemplaza con el estilo de numeración que se seleccionó en la propiedad Tipo de estilo de lista . Por ejemplo, si ha seleccionado `decimal` (1) estilo y, a continuación, el valor de `x` aumenta automáticamente para cada instancia del elemento de lista y va como 2, 3, etc. También puede agregar texto personalizado en el campo para dar formato al estilo de la lista. Por ejemplo, si desea que todos los estilos de lista de primer nivel tengan un sufijo &quot;`)`&quot;, debe definir este campo para el estilo de lista de primer nivel como &quot;`<x>)`&quot;.

   * **Insertar carácter**: Si desea agregar cualquier carácter especial en el Formato de número, haga clic en Insertar carácter (<img src="./assets/insert-chars.png" width="25">) icono. Seleccione el carácter que desee agregar en el formato de estilo y haga clic en Insertar. Existen diferentes tipos de caracteres especiales que puede elegir en la lista desplegable Seleccionar categoría .

   * **Insertar nivel**: Puede incluir el número de cualquiera de los niveles anteriores en el formato numérico. Por ejemplo, si desea incluir el formato de número del quinto nivel en el formato de número del sexto nivel, elija 5 en la lista desplegable Insertar nivel. Tenga en cuenta que la lista desplegable Insertar nivel muestra los números solo de los niveles anteriores y no del nivel siguiente. Por ejemplo, mientras esté en el Nivel 3, la lista Insertar nivel solo mostrará los niveles 1 y 2.

      <img src="./assets/list-insert-level.png" width="400">

      También puede cambiar el Formato de número para presentar los valores de lista según sea necesario. Por ejemplo, cuando se utiliza un estilo de numeración anidado para el nivel 3, se puede formatear como &quot;`<2>.<x>))`&quot;. Se mostrará la lista número 2, seguida de un punto, luego la lista número 3 y luego dos corchetes, como `2.3))`.

   * **Sangría**: Si desea sangrar la lista, debe establecer el valor de sangría. Cualquier cambio en la sangría se puede revisar en el panel Vista previa y ajustar.

      >[!NOTE]
      Puede introducir el valor en px (píxeles), pt (puntos), rem, em, % (porcentaje) o en unidades (pulgadas).

   * **Anchura de prefijo**: Este es el área ocupada por el Formato de número. Se establece automáticamente en un tamaño que puede acomodar fácilmente el formato seleccionado. Si desea aumentar el tamaño, puede reemplazar el valor predeterminado.

      Al configurar este valor manualmente, intente cambiar las demás propiedades que afectarán a la anchura. Por ejemplo, cambie el tamaño de fuente, el formato con prefijo o sufijo y las distintas propiedades de fuente para obtener el tamaño óptimo.

   * **Espaciado**: Especifique el espaciado horizontal entre el formato de número de lista y el contenido. El espaciado vertical controla el espacio entre los dos elementos de la lista.

      La siguiente captura de pantalla muestra la lista ordenada personalizada para cada nivel:

      <img src="./assets/list-number-format-final.png" width="500">


## Trabajo con estilo de tabla

Con las hojas de estilo, puede diseñar *n* número de estilos de tabla. Con los estilos de tabla, puede diseñar cómo se completa la tabla, una fila o columna en particular. Con el control en el estilo de nivel de celda, puede crear estilos de tabla muy presentables.

En el siguiente ejemplo, vemos cómo crear un estilo de tabla y las distintas opciones de estilo de tabla que puede personalizar:

1. Abra la hoja de estilo necesaria para editarla.

   >[!NOTE]
   Consulte *Personalización de un estilo nuevo o predefinido* para abrir una hoja de estilo para personalizarla o editarla.

1. En el **Estilos** , haga clic con el botón derecho en la **Estilo de tabla** y elija **Nuevo estilo**.

1. En el *Agregar estilo* mantenga la variable **Etiqueta** name como `table` y escriba `double-border` en el **Clase** campo name .

1. Haga clic en **Listo**.

   Un nuevo estilo de tabla con el nombre `table.double-border` se crea y agrega en la lista Estilos de tabla .

1. Select `table.double-border` de la variable **Estilos de tabla** y establezca las siguientes propiedades:

   * **Aplicar formato a**: Puede aplicar el formato de estilo a toda la tabla, filas o columnas impares o primera/última fila o columna.

      >[!NOTE]
      Las siguientes opciones de configuración están disponibles en la sección **General** sección cuando **Aplicar formato a** está configurado como **Tabla completa**.

   * **Ajuste de texto**: Seleccione cómo ajustar texto alrededor de la tabla. Esto resulta útil cuando la tabla está dentro de otro elemento de nivel de bloque y la tabla debe procesarse junto con otro contenido en el elemento de bloque. Las opciones de ajuste son *left* o *right* alineado, o *ninguno*.

   * **Contraer borde**: Seleccione el aspecto del borde de la tabla. Si selecciona contraer, solo se dibuja una línea de borde entre las celdas de la tabla. Sin embargo, para un estilo independiente, el borde es visible alrededor de cada celda con relleno adicional.

      <img src="./assets/table-style-collapse-separate.png" width="500">

   * **Espaciado del borde**: Esta configuración solo está disponible cuando Contraer borde está definido como Separar. Con esta configuración, puede especificar el espaciado vertical y horizontal entre los bordes de las celdas.

      <img src="./assets/table-border-spacing.png" width="500">

      >[!NOTE]
      Las siguientes opciones de configuración están disponibles en la sección **Celda** sección cuando **Aplicar formato a** está configurado como **Tabla completa**.

   * **Relleno**: Especifique el relleno entre celdas de tabla. Puede especificar diferentes valores de relleno para los lados superior, inferior, izquierdo y derecho.

   * **Alineación vertical**: Especifique la alineación vertical del contenido de la celda. Las opciones disponibles son: Superior, Centro y Abajo.

   * **Borde lateral, Estilo, Color, Ancho, Radio:** Especifique las propiedades relacionadas con el borde. Puede elegir tener bordes solo en lados específicos como Izquierda o Derecha. El estilo de borde muestra los estilos de borde disponibles, como Sólido, Discontinuo, Línea doble, etc. Especifique el color del borde mediante la paleta de colores. Puede especificar el ancho del borde en px, pt, rem, em, % y en unidades. El radio define la curva para hacer esquinas circulares.

   Las demás propiedades de Fuente, Borde, Presentación, Paginación y Fondo se explican en otros ejemplos de este tema. Según la selección en la variable **Aplicar formato a** , puede aplicar estos valores a toda la tabla o a las filas o columnas seleccionadas.

   A continuación se muestra una vista previa de una tabla de muestra con filas diferentes con formato diferente:

   <img src="./assets/table-final-design.png" width="500">

## Trabajar con otros estilos

Si está trabajando con contenido estructurado (DITA), observará que casi todos los elementos DITA tienen una asignación de estilos en la hoja de estilo predeterminada. Por ejemplo, una `<shortdesc>` el estilo del elemento se define en **Otro estilo** > **.short desc** definición de estilo. Puede personalizar fácilmente cualquiera de estos estilos y se aplican automáticamente en la salida de PDF generada a partir del contenido estructurado. Esto significa que, a diferencia de otros estilos personalizados, no es necesario agregar un `outputclass` en el contenido para estos estilos.

Si desea crear una definición de estilo para cualquier elemento que no esté disponible de forma predeterminada o que tenga un elemento personalizado, puede crearlo fácilmente en la hoja de estilo. El único punto que debe tener en cuenta es crear el estilo con el mismo nombre que el nombre del elemento estructurado.

En el siguiente ejemplo, se crea el título de una nueva ventana (`wintitle`).

1. Abra la hoja de estilo necesaria para editarla.

   >[!NOTE]
   Consulte *Personalización de un estilo nuevo o predefinido* para abrir una hoja de estilo para personalizarla o editarla.

1. En el **Estilos** lista, expandir **Otros estilos**.

1. Haga clic con el botón derecho en el **Otro estilo** y elija **Nuevo estilo**.

1. En el *Agregar estilo* mantenga la variable **Etiqueta** name como *blank* y escriba `wintitle` en el **Clase** campo name .

   Como `wintitle` es un nombre de elemento DITA reconocido, su definición de estilo se asigna automáticamente al `<wintitle>` en el origen.

1. Haga clic en **Listo**.

   Un nuevo estilo llamado `.wintitle` se crea y se agrega en la variable **Otros estilos** lista.

1. Seleccione .wintitle en la **Otros estilos** y establezca las propiedades según sea necesario.

La siguiente captura de pantalla muestra el estilo wintitle que se aplica al texto &quot;Control principal&quot;.

<img src="./assets/other-style-wintitle.png" width="500">