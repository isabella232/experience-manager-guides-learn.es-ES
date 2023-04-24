---
title: Sitio AEM
description: Obtenga información sobre cómo AEM el sitio
source-git-commit: 23d6c87b525f0763990166e46f4bd4ac2d6e7cd5
workflow-type: tm+mt
source-wordcount: '2545'
ht-degree: 0%

---


# Sitio AEM {#id205BE3008SW}

Las siguientes opciones están disponibles para la salida AEM Sitio :

Puede crear el ajuste preestablecido AEM sitio de dos maneras:

**Desde el Editor web:** En el panel Repositorio, abra el archivo de asignación DITA en la vista Mapa, luego, en la ficha Salida, seleccione el icono + para crear un ajuste preestablecido de salida y, a continuación, seleccione AEM sitio en la lista desplegable Tipo del cuadro de diálogo Agregar ajuste preestablecido. En el editor Web, las configuraciones se han organizado en las pestañas General y Avanzado :

**General**

La variable **General** contiene las siguientes configuraciones:

- Nombre del sitio
- Ruta de salida
- Páginas de salida existentes
- Eliminar páginas del sitio huérfano
- Aplicar condiciones usando \(Si las condiciones están definidas para un mapa\)
- Usar línea de base \(Si se crea una línea de base para un mapa\)
- Flujo de trabajo de posgeneración

**Avanzado**

La pestaña Advanced contiene las siguientes configuraciones:

- Limpiar archivos temporales DITA-OT
- Generar PDF separado para cada tema
- Usar propiedades de mapa como predeterminadas

Para obtener más información, consulte [AEM Configuración del sitio](#id231KIM004X1).

**Desde el panel de mapas**

Para abrir los ajustes preestablecidos de salida para AEM sitio, haga clic en un archivo de asignación DITA desde la interfaz de usuario de Assets y, a continuación, haga clic en Ajustes preestablecidos de salida y, a continuación, haga clic en la opción de salida AEM sitio. En el panel de asignación, haga clic en **Editar** en la parte superior para actualizar las distintas configuraciones y, a continuación, haga clic en **Guardar**.

>[!TIP]
>
> Consulte la *AEM Publicación del sitio* en la guía de prácticas recomendadas para conocer las prácticas recomendadas relacionadas con la creación AEM salida del sitio.

## AEM Configuración del sitio {#id_aem_site_config}

Las siguientes opciones están disponibles para la salida AEM Sitio :

| AEM Opciones de sitio | Descripción |
| --- | --- |
| Tipo de salida | El tipo de salida que desea generar. Para generar resultados AEM sitio adaptables, seleccione la opción AEM sitio . |
| Nombre de la configuración | Asigne un nombre descriptivo a la configuración del sitio AEM que está creando. Por ejemplo, puede especificar *Salida de clientes internos* o *salida de usuarios finales*. |
| Nombre del sitio | Nombre del sitio donde el resultado se almacena en el repositorio de AEM.<br><br>Se crea un nodo en el repositorio de AEM con el nombre especificado aquí. Si no especifica el Nombre del sitio, el nodo del sitio se crea con el nombre del archivo de asignación DITA.<br><br>El nombre del sitio que especifique aquí también se usa como título en la ficha del explorador.<br><br>También puede usar variables al configurar el Nombre del sitio. Para obtener más información sobre el uso de variables, consulte [Utilice variables para configurar las opciones Ruta de destino, Nombre del sitio o Nombre de archivo](generate-output-use-variables.md#id18BUG70K05Z). |
| Diseño | Seleccione la plantilla de diseño que desee utilizar para generar el resultado.<br><br>Para obtener más información sobre cómo utilizar plantillas de diseño personalizadas para generar resultados, póngase en contacto con el administrador de publicación. |
| Ruta de destino | La ruta dentro del repositorio de AEM donde se almacena la salida. Al generar el resultado final, se combinan el Nombre del sitio y la Ruta de destino. Por ejemplo, si especifica el Nombre del sitio como `user-guide` y la ruta de destino como `/content/output/aem-guides`, el resultado final se genera en la sección `/content/output/aem-guides/user-guide` nodo .<br><br>También puede utilizar variables al establecer la ruta de destino. Para obtener más información sobre el uso de variables, consulte [Utilice variables para configurar las opciones Ruta de destino, Nombre del sitio o Nombre de archivo](generate-output-use-variables.md#id18BUG70K05Z). |
| Aplicar condiciones usando | Seleccione una de las siguientes opciones:<br><br>**Ninguno aplicado**: Seleccione esta opción si no desea aplicar ninguna condición en la salida publicada.<br>**Archivo DITAVal**: Seleccione los archivos DITAVal para generar contenido condicional. Puede seleccionar varios archivos DITAVal mediante el cuadro de diálogo Examinar o escribiendo la ruta de acceso del archivo. Utilice el icono cruzado cerca del nombre del archivo para eliminarlo. Los archivos DITAVal se evalúan en el orden especificado, por lo que las condiciones especificadas en el primer archivo tienen prioridad sobre las condiciones coincidentes especificadas en los archivos posteriores. Puede mantener el orden de los archivos añadiendo o eliminando archivos. Si el archivo DITAVal se mueve a otra ubicación o se elimina, no se elimina automáticamente del panel de mapas. Debe actualizar la ubicación en caso de que los archivos se muevan o eliminen. Puede pasar el ratón sobre el nombre del archivo para ver la ruta en el repositorio de AEM donde se almacena el archivo. Sólo puede seleccionar archivos DITAVal y se muestra un error si selecciona cualquier otro tipo de archivo.<br>**Ajuste preestablecido de condición**: Seleccione un ajuste preestablecido de condición en la lista desplegable para aplicar una condición al publicar la salida. Esta opción está visible si ha añadido una condición para el archivo de asignación DITA. Los ajustes condicionales están disponibles en la ficha Ajustes preestablecidos de condición de la consola de asignación DITA. Para obtener más información sobre el ajuste preestablecido de condición, consulte [Usar ajustes preestablecidos de condición](generate-output-use-condition-presets.md#id1825FL004PN). |
| Páginas de salida existentes | Seleccione el **Sobrescribir contenido** para sobrescribir contenido en las páginas existentes. Esta opción solo sobrescribe el contenido presente en los nodos de contenido y encabezado de la página. Esta opción permite la publicación combinada del contenido. Al seleccionar esta opción se proporciona una opción para seleccionar la eliminación de páginas huérfanas de la salida publicada. También es el *default* para crear la salida AEM Sitio.<br><br>Seleccione el **Eliminar y crear** para forzar la eliminación de las páginas existentes durante la publicación. Esta opción elimina el nodo de página junto con su contenido y todas las páginas secundarias debajo de él. Utilice esta opción si ha cambiado la plantilla de diseño del ajuste preestablecido de salida o si desea que se elimine cualquier página adicional ya presente en el destino. |
| Eliminar páginas del sitio huérfano | Al seleccionar la variable **Sobrescribir contenido** en el **Páginas de salida existentes** presenta esta opción. Si selecciona esta opción, todas las páginas huérfanas se eliminarán del sitio AEM publicado. Para que esta función se ejecute correctamente, debe publicar el mapa DITA completo y no utilizar la publicación incremental.<br><br>Digamos que ha publicado un mapa DITA, que contiene los temas a.dita, b.dita y c.dita. Antes de volver a publicar el mapa, eliminó el tema b.dita del mapa. Ahora, si ha seleccionado esta opción, todo el contenido relacionado con b.dita se elimina de la salida AEM Sitio y solo se publican a.dita y c.dita.<br><br>Esta función no elimina ningún mapa secundario publicado. Por ejemplo, si el mapa principal contiene un mapa secundario y se elimina el mapa secundario completo, el contenido del mapa secundario no se elimina de la salida publicada. Sin embargo, si elimina cualquier tema de un mapa secundario y vuelve a publicar, el contenido del tema eliminado se elimina de la salida del sitio.<br><br>Además, si hay contenido al que se hace referencia y ese contenido se elimina antes de volver a publicarse, los datos del contenido al que se hace referencia no se eliminan.<br><br>**Nota**: La información sobre las páginas huérfanas eliminadas también se captura en los registros de generación de salida. Para obtener más información sobre el acceso a los archivos de registro, consulte [Ver y comprobar el archivo de registro](generate-output-basic-troubleshooting.md#id1821I0Y0G0A__id1822G0P0CHS). |
| Limpiar archivos temporales DITA-OT | Seleccione esta opción para limpiar los archivos temporales generados por DITA-OT. La ubicación donde DITA-OT almacena archivos temporales se encuentra en el registro de generación de salida.<br><br>Si está experimentando errores mientras genera resultados a través de DITA-OT, puede anular la selección de esta opción para conservar los archivos temporales. A continuación, puede utilizar esos archivos para solucionar los errores de generación de resultados. |
| Generar PDF separado para cada tema | Si se selecciona, también se crea un PDF para cada tema del mapa DITA. Al elegir esta opción, se muestra una nueva opción Dividir ruta de PDF .<br><br>En el campo Dividir ruta del PDF , especifique la ruta para almacenar los PDF generados para cada tema.<br><br>**Nota**: AEM Guías utiliza el complemento DITA-OT denominado pdfx para generar un PDF para cada tema. Este complemento está integrado con el paquete DITA-OT incluido. Puede personalizar este complemento para que genere un PDF según sus necesidades. Si utiliza un complemento DITA-OT personalizado, asegúrese de integrar el complemento pdfx para que tenga capacidad de generación de PDF a nivel de tema. |
| Ejecutar flujo de trabajo de posgeneración | Al elegir esta opción, se muestra una nueva lista desplegable Flujo de trabajo de posgeneración que contiene todos los flujos de trabajo configurados en AEM. Debe seleccionar un flujo de trabajo que desee ejecutar después de completar el flujo de trabajo de generación de resultados. |
| Usar línea de base | Si ha creado una Línea de base para el mapa DITA seleccionado, seleccione esta opción para especificar la versión que desea publicar.<br><br>**Importante**: Cuando se genera un resultado incremental para el Sitio AEM, el resultado se crea con la versión actual de los archivos y no con la línea de base adjunta.<br><br>Consulte [Trabajo con línea de base](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) para obtener más información. |
| Propiedades | Seleccione las propiedades que desee procesar como metadatos. Estas propiedades se establecen desde la página Propiedades del mapa DITA o del archivo de mapa de libros. Las propiedades que seleccione en la lista desplegable se enumeran debajo del campo Propiedades y se eliminan de la lista desplegable.<br><br>**Nota**: Las propiedades de metadatos distinguen entre mayúsculas y minúsculas.<br><br>*Si ha seleccionado una Línea de base, los valores de las propiedades se basarán en la versión de la Línea de base seleccionada.<br>* Si no ha seleccionado una línea de base, los valores de las propiedades se basan en la última versión.<br><br>También puede pasar los metadatos a la salida mediante la publicación DITA-OT. Para obtener más información, consulte [Pasa los metadatos a la salida utilizando DITA-OT](pass-metadata-dita-ot.md#id21BJ00QD0XA).<br><br>**Nota**: Si no ha definido la variable `cq:tags` en la opción Propiedades , luego los valores de `cq:tags` se seleccionan de la copia de trabajo actual aunque haya seleccionado una línea de base para la publicación. |
| Usar Propiedades De Mapa Si Falta En El Tema | Si se selecciona, las propiedades definidas para el archivo de asignación también se copian en los temas en los que dichas propiedades no están definidas. Tenga en cuenta los siguientes puntos al utilizar esta opción:<br><br>*Solo se pueden pasar propiedades String, Date o Long (solo y de varios valores) a las páginas del sitio AEM.<br>* Los valores de metadatos de una propiedad de tipo String no admiten ningún carácter especial (como `@, #, " "`).<br>* Esta opción debe utilizarse junto con la variable `Properties` . |

## Nota adicional en AEM sitio

### Generar salida basada en artículos desde el Editor web

Puede generar el resultado AEM Sitio para uno o más temas, o el mapa DITA completo desde el Editor web. Debe crear ajustes preestablecidos de salida para su mapa DITA y, a continuación, puede generar fácilmente la salida AEM Sitio para su mapa. Si ha actualizado algunos temas en el mapa, también puede generar el resultado del Sitio AEM solo para esos temas desde el Editor Web. Para obtener más información, consulte [Publicación basada en artículos desde el Editor web](web-editor-article-publishing.md#id218CK0U019I).

### Generación de temas de vinculación de salida de otros mapas

Es muy común tener un gran conjunto de documentación distribuida en varias carpetas y mapas DITA. Resulta extremadamente complejo publicar contenido vinculado desde varios lugares. De forma predeterminada, todos los vínculos `<xref>` se crean con la variable `local` `@scope`. La publicación de estos temas no implica ningún desafío, ya que utiliza un vínculo directo al tema. Si el tema está fuera del mapa DITA actual, el vínculo no muestra el contenido vinculado.

Otra forma de vincular contenido es crear un vínculo mediante la variable `peer` `@scope`. Para dicho contenido, el vínculo se resuelve en tiempo de ejecución seleccionando el contexto configurado para el tema vinculado desde el contexto de publicación del mapa DITA. La siguiente captura de pantalla muestra el panel Propiedades para un vínculo que tiene el valor `peer` `@scope`:

![](images/peer-link-scope-link.png){width="800" align="left"}

Para simplificar la publicación de mapas complejos y temas que se vinculan a otros temas en otros mapas, AEM guías le permite establecer el contexto de publicación para cada ajuste preestablecido de salida.

El contexto de publicación le permite especificar qué tema debe utilizarse desde qué mapa para publicar un resultado específico. Vamos a entender esto con la ayuda de un ejemplo, digamos que tiene cuatro carpetas: muestra a, muestra b, muestra c y muestra d. Cada carpeta contiene un mapa DITA: Mapa DITA A, Mapa DITA B, Mapa DITA C y Mapa DITA D. La vinculación de mapas cruzados se producirá cuando un tema del Mapa DITA A vincule a un tema del Mapa DITA B, C o D. En la siguiente captura de pantalla, un tema de concepto de muestra contiene enlaces \(o referencias\) a archivos que forman parte de otros Mapas DITA.

![](images/sample-concept-link-to-other.png){width="450" align="left"}

Ahora, cuando configure la configuración de publicación del sitio AEM para el archivo de mapa que contiene este tema, puede seleccionar qué contexto de publicación para el contenido vinculado se utilizará al publicar. Un contexto de publicación es una combinación de asignación DITA y su ajuste preestablecido de salida. El ajuste preestablecido de salida, a su vez, contiene una versión específica del contenido y los ajustes preestablecidos condicionales. Esta combinación completa de asignación DITA, ajuste preestablecido de salida, versión \(archivos\) y condiciones definen el contexto de publicación de un mapa vinculado.

Siga estos pasos para especificar el contexto de publicación de los archivos enlazados entre sí:

1. Abra el **Ajustes preestablecidos de salida** del mapa DITA que desea publicar.

1. Seleccione el **Sitio AEM** ajuste preestablecido de salida.

   Se obtienen las fichas Configuración de ajustes preestablecidos de AEM y Publicar contexto .

   ![](images/aem-site-publish-settings.png){width="800" align="left"}

1. Abra el **Publicar contexto** pestaña .

   Se le muestra una lista de temas dependientes. Estos son los temas que están enlazados desde algún tema en el mapa actual, pero están disponibles en otros mapas DITA.

   >[!NOTE]
   >
   > La ficha Publicar contexto muestra los temas que están vinculados mediante el uso de `peer` `@scope` solo. Para vínculos con `local` `@scope`, no es necesario especificar el contexto de publicación.

   De forma predeterminada, todos los temas vinculados tienen seleccionado el último ajuste preestablecido de salida y el mapa.

   ![](images/default-publish-context.png){width="800" align="left"}

1. Para cambiar la selección predeterminada de asignación y ajuste preestablecido de DITA, haga clic en **Editar** \(en la barra de herramientas principal\).

1. Si desea utilizar la salida publicada más recientemente de cada archivo dependiente en el mapa, seleccione **Usar el contexto de publicación generado más recientemente para todos los temas dependientes**.

1. En el **Mapa principal** lista desplegable, seleccione el archivo de asignación con cuya salida desea vincular la salida del mapa actual.

   Al seleccionar un archivo de mapa, el UUID del mapa se muestra en la columna UID del mapa principal. Los ajustes preestablecidos de salida asociados al mapa seleccionado se muestran en la lista Ajustes preestablecidos del mapa principal.

1. En el **Ajuste preestablecido del mapa principal** lista desplegable, seleccione el ajuste preestablecido de salida con el que desea vincular la salida del mapa actual.

1. Seleccione el mapa requerido y su ajuste preestablecido de salida para todos los temas dependientes y haga clic en **Listo**.

   Ya se ha establecido el contexto para los temas dependientes. Puede generar la salida para el mapa actual. Para obtener más información sobre la generación de resultados, consulte [Generar salida para un mapa DITA desde la consola de asignación](generate-output-for-a-dita-map.md#).

### Publicación combinada

AEM guías admite la publicación de contenido DITA en el sitio AEM existente. Por ejemplo, si tiene un sitio existente, puede utilizar la salida AEM Sitio para publicar solamente el contenido DITA en ese sitio. En este proceso, el contenido no DITA existente no se modifica mediante el proceso de publicación. Para obtener más información sobre la configuración del sitio para publicar solo contenido DITA, póngase en contacto con el administrador de publicación.

### Publicación `conref`

Si está utilizando `conref` en el contenido, se publica como contenido normal o incrustado junto con el contenido en el tema de origen \(o referencia\). La variable `conref` el contenido se representa junto con el contenido principal y no se crea ninguna página de sitio independiente para el mismo. Al buscar el contenido al que se hace referencia en la variable `conref`y, a continuación, solo el tema principal o la página que contiene la variable `conref` el contenido se muestra en los resultados de búsqueda.

>[!NOTE]
>
>Si ha generado páginas separadas para la variable `conref` contenido que utilice AEM versión 3.5 o anterior de las guías, se recomienda limpiar o eliminar esas páginas utilizando la variable [Eliminar páginas del sitio huérfano](#delete-orphan-page-aem-site) .


### Buscar una cadena en el contenido

Puede buscar una cadena en la salida AEM Sitio . De forma predeterminada, puede buscar la cadena solo en los títulos. Para buscar la cadena en el contenido o en el cuerpo de la salida del sitio AEM, póngase en contacto con el administrador del sistema para habilitar la propiedad flatening.enabled .


<img src="images/aem-output-search.png" alt="Resultado de la búsqueda AEM sitio" width="800">

Para obtener más información, consulte *Configuración del aplanamiento de AEM estructura de nodos del sitio* en la guía Instalar y configurar guías de Adobe Experience Manager .

**Tema principal:**[ Explicación de los ajustes preestablecidos de salida](generate-output-understand-presets.md)