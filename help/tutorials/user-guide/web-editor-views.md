---
title: Vistas del Editor web
description: Obtenga información sobre las vistas del Editor web
source-git-commit: fa6e9f8b32d191f5b6f7136724d2145d81317767
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 0%

---


# Vistas del Editor web {#id204GK0D0V5Z}

El Editor web de las guías de AEM admite la visualización de documentos en tres modos o vistas diferentes:

## Autor

Esta es una vista típica de lo que ve es lo que obtiene \(WYSISYG\) del Editor web. Puede editar temas como lo haría en cualquier editor de texto enriquecido normal. En la vista Autor, tiene las opciones para guardar una revisión del documento, buscar y reemplazar contenido, insertar elemento, insertar hipervínculo, insertar referencia de contenido, etc.

>[!NOTE]
>
> Cuando utiliza la referencia de contenido, el contenido referido también se muestra en la vista Autor en color azul. El contenido referido no es editable.

## Origen

La vista Código fuente muestra el XML subyacente que constituye el tema. Si se siente cómodo trabajando con XML directamente, debe utilizar la vista Código fuente. Además de realizar ediciones de texto normales en esta vista, también puede agregar elementos y atributos utilizando el catálogo inteligente, o buscar y reemplazar texto, elementos o atributos.

- Para invocar el Catálogo inteligente, coloque el cursor al final de cualquier etiqueta de elemento donde desee insertar el nuevo elemento e introduzca &quot;&lt;&quot;. El editor muestra una lista de todos los elementos XML válidos que puede insertar en esa ubicación. Utilice las teclas de flecha para seleccionar el elemento que desea insertar y pulse Intro. Cuando se introduce el corchete de cierre &quot;\>, se agrega automáticamente la etiqueta de cierre del elemento.

   ![](images/smart-catalog-elements.png){width="400" align="left"}

- También puede cambiar un elemento fácilmente desde la vista Origen. Por ejemplo, si cambia la etiqueta de apertura de un `p` elemento a `note`, luego el cierre `p` se cambia automáticamente a `/note`. Si reemplaza un elemento con un elemento incorrecto, se le mostrará inmediatamente el error de validación.

- Si desea añadir un atributo a un elemento, coloque el cursor dentro de la etiqueta element y presione la barra Space. En el Catálogo inteligente se muestra una lista de atributos válidos para ese elemento. Utilice las teclas de flecha para seleccionar el elemento deseado y pulse Intro para insertar el elemento. Para especificar un valor para el atributo, introduzca el signo igual \(=\) y el editor introduce automáticamente las comillas de apertura y cierre &quot;&quot;, donde puede especificar el valor del atributo.

   ![](images/smart-catalog-attribute.png){width="350" align="left"}

- En la vista de origen, existe una opción de sangría automática que reorganiza el código XML en formato presentable y fácil de leer. Además, si selecciona cualquier texto y cambia de Autor a Origen o de Fuente a Autor, el texto seleccionado también se resalta en la otra vista.
- Otra potente función de la vista Origen es la validación XML del documento. Si abre un documento que contiene XML no válido, se abre en la vista Código fuente con la información sobre XML no válido. Por ejemplo, en la siguiente captura de pantalla, la información exacta sobre el XML incorrecto se proporciona en la ventana emergente Error de análisis.

   ![](images/invalid-topic-xml.png){width="650" align="left"}

   En la captura de pantalla anterior, se utiliza un resaltado cruzado para señalar la línea que contiene XML incorrecto.

- La función Buscar y reemplazar permite buscar texto, elemento o atributo en la vista de origen.
Para obtener más información, consulte la **Buscar y reemplazar** descripción de la función en el [Barra de herramientas principal](web-editor-features.md#id#id2051EA0G05Z) para obtener más información.

- La vista de origen proporciona muchos métodos abreviados para ayudarle a desplazarse rápidamente y trabajar en un documento. En la tabla siguiente se enumeran las acciones admitidas y sus teclas de método abreviado:

   | Para ello, haga lo siguiente | Usar este acceso directo |
   |----------|-----------------|
   | Añadir varios cursores | **Ctrl**+ Clic izquierdo |
   | Varias selecciones de texto no consecutivas | **Ctrl**+ Haga clic izquierdo para arrastrar y seleccionar texto |
   | Seleccionar texto entre líneas | **Alt**+ Haga clic izquierdo para arrastrar y seleccionar texto |
   | Deshacer varias selecciones o salir del modo de pantalla completa | **Esc** |
   | Mostrar autocompletado | **Ctrl**+**Espacio** |
   | Vaya a la etiqueta de apertura o cierre de la etiqueta actual | **Ctrl**+**J** |
   | Expandir o contraer la etiqueta actual y su contenido | **Ctrl**+**Q** |
   | Seleccione el elemento actual y su contenido | **Ctrl**+**L** |
   | Anular sangría del elemento actual | **Mayús**+**Tabulación** |
   | Eliminar el elemento actual y su contenido | **Mayús**+**Ctrl**+**K** |
   | Mover el cursor una palabra a la izquierda | **Alt**+**Flecha izquierda** |
   | Mover el cursor una palabra a la derecha | **Alt**+**Flecha derecha** |
   | Desplácese una línea hacia arriba sin cambiar la ubicación del cursor | **Ctrl**+**Flecha arriba** |
   | Desplácese una línea hacia abajo sin cambiar la ubicación del cursor | **Ctrl**+**Flecha abajo** |
   | Alternar pantalla completa | **F11** |
   | Insertar una línea nueva después del elemento actual | **Ctrl**+**Entrar** |
   | Insertar una línea nueva antes del elemento actual | **Mayús**+**Ctrl**+**Entrar** |
   | Buscar y seleccionar la siguiente incidencia de la palabra actual | **Ctrl**+**D** |
   | Mover el elemento actual y su contenido un elemento hacia arriba | **Mayús**+**Ctrl**+**Flecha arriba** |
   | Mover el elemento actual y su contenido un elemento hacia abajo | **Mayús**+**Ctrl**+**Flecha abajo** |
   | Ajustar el elemento actual en la etiqueta de comentario | **Ctrl**+**/** |
   | Duplicar el elemento actual y su contenido | **Mayús**+**Ctrl**+**D** |
   | Elimine el texto que sigue al cursor. Si el cursor está antes de un elemento de apertura, se elimina todo el elemento. | **Ctrl**+**K**+**K** |
   | Se elimina el texto a la izquierda del cursor en la línea actual. Si el cursor está después de la etiqueta de cierre de un elemento, se elimina todo el elemento. | **Ctrl**+**K**+**Retroceso** |
   | Convertir el texto actual a mayúsculas | **Ctrl**+**K**+**U** |
   | Convertir el texto actual a minúsculas | **Ctrl**+**K**+**L** |
   | Desplácese el elemento actual al centro del editor | **Ctrl**+**K**+**C** |
   | Añada un cursor sobre la posición actual | **Ctrl**+**Alt**+**Flecha arriba** |
   | Añadir un cursor debajo de la posición actual | **Ctrl**+**Alt**+**Flecha abajo** |
   | Buscar de forma recursiva la palabra actual \(en dirección hacia adelante\) | **Ctrl**+**F3** |
   | Buscar de forma recursiva la palabra actual \ (en dirección atrás\) | **Mayús**+**Ctrl**+**F3** |


## Vista previa

Al abrir un tema en el modo de vista previa, se muestra cómo se mostrará un tema cuando lo vea un usuario en su explorador. En el caso de un mapa DITA, se muestra una previsualización del mapa donde se muestra un solo documento compuesto de todos los temas dentro del mapa.

El modo Vista previa le ofrece las siguientes funcionalidades:

- [Ver contenido basado en filtros condicionales](#id2114BI00VXA)
- [Ver las marcas de seguimiento de cambios](#id2114BJ00CE8)
- [Exportación de un tema como PDF](#id2114BL00B5U)

### Ver contenido basado en filtros condicionales {#id2114BI00VXA}

Si ha utilizado condiciones en su tema o mapa, esas condiciones se muestran en el panel Filtros . De forma predeterminada, se seleccionan todas las condiciones y se muestra todo el contenido. Si anula la selección de una condición, el contenido que tenga esa condición se elimina de la vista. También puede elegir resaltar el contenido condicional.

La siguiente imagen muestra un tema que usa dos condiciones: `Audience` y `Product`. El contenido condicional se resalta con fondo amarillo.

![](images/preview-filters.png){width="800" align="left"}

### Ver las marcas de seguimiento de cambios {#id2114BJ00CE8}

Si un documento contiene marcas de seguimiento de cambios \(o señales visuales\), también puede obtener una vista previa del documento con o sin esas marcas. Al obtener una vista previa de un documento, el panel derecho contiene las opciones Filtros y Seguimiento.

![](images/preview-tracking_cs.png){width="400" align="left"}

Hay tres **Seguimiento** opciones entre las que puede elegir:

- **Sin marcado**: En esta vista, se aceptan todas las inserciones y eliminaciones, y se presenta una vista simple del documento. En esta vista, no ve ninguna marca de seguimiento de cambios.
- **Original**: En esta vista, todas las inserciones se rechazan y todas las eliminaciones se restauran de nuevo y, a continuación, se muestra una vista previa. Simplemente, obtiene el formulario original del documento antes de activar el modo de seguimiento de cambios.
- **Mostrar marcado**: En esta vista, se obtienen todas las marcas para el contenido insertado y eliminado.

   La siguiente imagen muestra la vista previa de un archivo de mapa con marcas:

   ![](images/preview-map-with-track-changes.PNG){width="800" align="left"}


### Exportación de un tema como PDF {#id2114BL00B5U}

PDF es uno de los formatos de salida más comunes que se utiliza en todas las etapas posibles del ciclo de desarrollo de documentos. AEM guías le proporciona la flexibilidad para generar el PDF de un tema individual o de un archivo de asignación completo. La función Exportar como PDF permite al autor, al editor o a un administrador generar fácilmente la salida del PDF para un tema individual. Utiliza las configuraciones de DITA-OT guardadas en el perfil de nivel de carpeta para generar el PDF.

Esta función es compatible con las siguientes funcionalidades:

- Genere el PDF de la copia de trabajo activa de un tema.
- Acepte el nombre de transformación DITA-OT y los argumentos de línea de comandos para generar el PDF.
- Guarde la salida generada en el sistema local.
- Resuelva las referencias de contenido y clave utilizadas en el tema antes de generar el resultado.

Para exportar un tema como PDF, siga estos pasos:

1. Abra el tema en modo Vista previa.

1. Haga clic en el **Exportar como PDF** \(![](images/export-as-pdf-icon.svg)\).

   Se muestra el cuadro de diálogo Exportar como PDF .

   ![](images/export-as-pdf-dialog.png){width="350" align="left"}

1. *\(Opcional\)* Especifique el nombre de transformación DITA-OT y cualquier argumento de línea de comandos que desee utilizar.

1. Haga clic en **Descargar**.

   >[!NOTE]
   >
   > Asegúrese de haber habilitado la ventana emergente en la configuración del explorador; de lo contrario, el PDF no se descargará.

   El PDF se genera y abre en una nueva pestaña o se muestra un cuadro de diálogo para guardar el PDF en el sistema local.


**Tema principal:**[ Trabajar con el Editor web](web-editor.md)

