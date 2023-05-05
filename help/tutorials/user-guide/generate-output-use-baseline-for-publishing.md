---
title: Trabajo con línea de base
description: Aprenda a trabajar con la línea de base
exl-id: dcafab53-c388-48c3-9455-e4251cdda17d
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '1917'
ht-degree: 0%

---

# Trabajo con línea de base {#id1825FI0J0PF}

La función de línea de base le permite crear una versión de sus temas y recursos que luego se puede usar para publicar o traducir. Por ejemplo, si el mapa de DITA tiene `topicA` y `imageA`, puede crear una línea de base para utilizar la tercera versión de `topicA`, pero la cuarta versión de `ImageA`. Una vez que haya configurado una línea de base, puede publicar o traducir temas de distintas versiones con un solo clic.

La selección de una línea de base es opcional para los ajustes preestablecidos de salida y un mapa DITA puede tener más de una línea de base. Sin embargo, cada ajuste preestablecido de salida dentro de un mapa DITA puede asociarse con una única línea de base. Si no se especifica ninguna línea de base en el momento de la publicación, el resultado se publica con la última versión del contenido.

Del mismo modo, la selección de una línea de base para traducir contenido es opcional. Sin embargo, si elige traducir contenido mediante una línea de base, el contenido de la línea de base también se guarda junto con las copias traducidas. A continuación, puede utilizar la línea de base traducida para realizar más operaciones, como compartirla con editores externos o archivarla. Para obtener más información sobre cómo exportar una línea de base traducida, consulte [Exportar línea de base traducida](#id196SE600GHS).

>[!TIP]
>
> Consulte la *Línea de base* en la Guía de prácticas recomendadas para conocer las prácticas recomendadas relacionadas con el trabajo con líneas de base.

El administrador puede configurar la pestaña Línea de base en el panel de asignación. Para obtener más información, consulte *Configuración de la pestaña Línea de base en el tablero de mapas DITA* en la Guía de instalación y configuración.

Puede acceder a la función Línea de base siguiendo estos pasos:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación DITA y haga clic en él.
1. Vaya a la **Líneas de base** pestaña .

En la pestaña Líneas de base, puede realizar las siguientes acciones:

- [Crear una línea de base](#id195FI0I0MUQ)
- [Ver el contenido de una línea de base](#id195FI0I0TLN)
- [Editar, duplicar o eliminar líneas de base](#id195FI0I0YJL)
- [Agregar etiquetas a una línea de base](#id184KD0T305Z)

## Crear una línea de base {#id195FI0I0MUQ}

Puede crear una línea de base con una versión específica de los temas y el contenido al que se hace referencia disponible en una fecha y hora específicas, o con una etiqueta definida para una versión de los temas. Puede especificar individualmente las versiones de los temas seleccionados en una Línea de base para que cada vez que aplique la Línea de base en el flujo de trabajo de publicación o traducción, los temas seleccionados y sus versiones correspondientes se incluyan en la generación de salida o la traducción.

Siga estos pasos para crear una línea de base:

1. En la página Líneas Base, haga clic en **Crear**.
1. Escriba un nombre para la línea de base en **Nombre de línea de base**.
1. En **Configurar la versión en función de**, seleccione una de las siguientes opciones:

   - **Etiqueta**: Seleccione esta opción para elegir los temas según la etiqueta que se les haya aplicado. Introduzca una etiqueta para filtrar la lista en función de la cadena introducida. En la lista filtrada, puede elegir una etiqueta para seleccionar temas y otros recursos que tengan la etiqueta especificada.
   Al seleccionar **Etiqueta**, también se le ofrece una opción adicional para utilizar la versión más reciente de los temas a los que no se les ha aplicado la etiqueta especificada. Si no selecciona esta opción y hay algún tema o archivo multimedia que no tenga la etiqueta especificada en ella, el proceso de creación de la línea de base fallará. Para obtener más información sobre cómo agregar etiquetas, consulte [Usar etiquetas](web-editor-use-label.md#).

   - **Versión en** &lt;*marca de tiempo*\>: Selecciona la versión de los temas en la fecha y hora especificadas. Tenga en cuenta que la hora especificada aquí corresponde a la zona horaria del servidor de AEM. Si el servidor se encuentra en una zona horaria diferente, los temas se recogerán según la zona horaria del servidor y no la zona horaria local.

   Una vez que haya seleccionado una etiqueta o versión como fecha, todos los temas a los que se hace referencia y los archivos multimedia del mapa se seleccionan según corresponda. Esta selección de temas no se muestra en la interfaz de usuario, pero se guarda en el servidor.

1. Si desea utilizar una versión diferente para uno o más temas, puede hacerlo seleccionando manualmente esos temas. Haga clic en **Examinar tema**, seleccione el tema para el que desea utilizar una versión diferente. En la lista desplegable Seleccionar una versión para el tema seleccionado, seleccione una versión del tema que desee utilizar en la línea base y haga clic en **OK**.

   ![](images/baseline-select-version-drop-down.png){width="800" align="left"}

   La información sobre el tema y su versión seleccionada se almacena en el servidor. Puede repetir este paso para cambiar la versión seleccionada para varios temas.

1. Haga clic en el **Examinar todos los temas** enlace para cargar todos los temas y archivos multimedia referidos desde el mapa DITA.El UUID de temas y archivos multimedia también se muestra debajo del título del tema o del nombre del archivo \(media\).

   >[!NOTE]
   >
   > Si tiene un conjunto muy grande de archivos en su mapa DITA, con mapas anidados y temas, entonces hacer clic en Examinar todos los temas puede tardar un tiempo en cargar todos los archivos.

   El contenido de su mapa se presenta en las tres secciones: el archivo de asignación, Contenido \(referencias de tema\) y Contenido referido \(temas anidados, mapas y otros recursos\). Una vez que haya disponible todo el contenido al que se hace referencia, puede seleccionar individualmente la versión del tema que desea utilizar en la línea de base.

   La variable **Versión** la lista desplegable muestra las versiones disponibles de los temas o el contenido al que se hace referencia. Para el contenido al que se hace referencia, tiene la opción de elegir una versión automáticamente.

   Si elige **Seleccionar automáticamente** para el contenido al que se hace referencia, el sistema selecciona automáticamente la versión del contenido al que se hace referencia correspondiente a la versión del contenido en la que se hace referencia. Por ejemplo, supongamos que un tema A tiene una referencia a una imagen B. Cuando se creó la versión 1.5 del tema A, la versión de la imagen B era 1.2 en el repositorio. Ahora, cuando se crea una línea de base con la versión 1.5 del tema A con la imagen B definida como **Seleccionar automáticamente**, el sistema seleccionará automáticamente la versión 1.2 de la imagen B.

   Si crea una línea de base con las etiquetas , **Seleccionar automáticamente** se aplica a la versión de todo el contenido al que se hace referencia.

   Si el contenido o los recursos a los que se hace referencia \(tema, submapas, imágenes o vídeos\) no tienen versiones \ (como el contenido recién cargado\), la creación de una línea de base creará una versión para dichos archivos. Sin embargo, si los archivos tienen versiones, no se crea ninguna versión incremental para esos archivos. Este comportamiento se controla mediante la configuración de la versión de creación automática, que está habilitada de forma predeterminada. Esto también es necesario para traducir contenido donde el proceso de traducción espera que todos los archivos tengan una versión.

   >[!NOTE]
   >
   > Si desea especificar una versión diferente para cualquier recurso en particular, puede hacerlo eligiendo la versión deseada del **Versión** lista desplegable.

1. Haga clic en **Guardar**.

## Ver el contenido de una línea de base {#id195FI0I0TLN}

Para ver el contenido de una línea de base existente, haga clic en la ficha Líneas de base y seleccione la versión de línea de base que desee en la lista. La página Líneas de base se divide en tres partes: archivo de mapa DITA, contenido o temas del mapa y el contenido al que se hace referencia. Si el mapa contiene submapas, los temas a los que se hace referencia desde el submapa también se muestran en la sección Contenido . A continuación se describen las distintas columnas de la página Línea de base:

- **Nombre**: Muestra el título del tema o mapa DITA o el nombre del recurso, como el nombre de archivo de una imagen.

- **Tipo**: Muestra el tipo o tipo de recurso en el mapa, como mapa DITA, tema DITA o formato de imagen.

- **Versión**: Muestra la versión del recurso disponible en la línea de base.

- **Fecha y hora de la versión**: Muestra la fecha y hora de creación del recurso para la versión seleccionada.

- **Última**: Indica si la última versión del recurso se utiliza en la línea de base.

- **Mapa principal**: Si el archivo de mapa contiene submapas, esta columna contiene el nombre del mapa en el que se hace referencia a un tema.

- **Etiqueta**: Enumera la etiqueta\(s\) aplicada a la versión del tema.

- **Referenciado por**: Esta columna solo está disponible para el contenido al que se hace referencia. Indica el tema principal del recurso al que se hace referencia. Si un recurso es referido por varios temas, entonces los temas están separados por comas.

## Editar, duplicar o eliminar líneas de base {#id195FI0I0YJL}

**Editar líneas de base**

Siga estos pasos para editar una línea de base existente:

1. Seleccione Línea de base y haga clic en **Editar**.
1. Realizar los cambios necesarios en la línea base. Puede cambiar el nombre y la versión del tema o el contenido al que se hace referencia.
1. Haga clic en **Guardar**.

**Duplicar líneas base**

Seleccione Línea de base y haga clic en **Duplicar** para crear una copia de una línea de base existente. Especifique un nombre diferente para la línea de base, elija el número de versión para los temas y el contenido al que se hace referencia y haga clic en **Guardar**.

**Quitar líneas de base**

Seleccione la versión de las líneas de base y haga clic en **Eliminar** para eliminar una línea de base.

## Agregar etiquetas a una línea de base {#id184KD0T305Z}

Añadir etiquetas a cada tema puede llevar mucho tiempo. AEM guías proporciona un mecanismo de un solo clic para añadir etiquetas a varios temas y contenido de referencia en un mapa DITA.

Realice los siguientes pasos para agregar una etiqueta a varios temas y contenido de referencia en un mapa DITA:

1. En la página Líneas de base, seleccione una línea de base que contenga los temas y el contenido al que se hace referencia en el que desea agregar una etiqueta.

   >[!NOTE]
   >
   > Asegúrese de que la línea de base no tiene la versión más reciente de ningún tema o recurso. Una etiqueta solo se puede agregar a un tema o recurso con versiones.

1. Haga clic en **Agregar etiquetas**.

   ![](images/add-label-baseline-uuid.png){width="800" align="left"}

1. En el **Agregar etiqueta** , especifique una etiqueta única para asociarla a esta línea de base.

   Si el administrador ha configurado etiquetas predefinidas, se le mostrarán dichas etiquetas en una lista desplegable. Debe elegir una etiqueta de la lista.

1. Si desea aplicar la etiqueta a temas a los que se hace referencia desde los submapas, seleccione **Aplicar etiqueta a mapas secundarios y dependientes** .

   - Haga clic en **Agregar**.
La etiqueta especificada se agrega al mapa DITA y a los temas y el contenido a los que se hace referencia.

      ![](images/label-added-baseline-uuid.png){width="650" align="left"}


## Exportar línea de base traducida {#id196SE600GHS}

Puede utilizar Línea de base para traducir contenido. Por ejemplo, puede crear una línea de base para la versión 1.1 que esté lista para su traducción en francés. En la pestaña Translation , debe utilizar Baseline para filtrar el contenido y, a continuación, seleccionar el Baseline para la versión 1.1 del contenido. El uso de la línea de base para traducir contenido facilita la administración del contenido.

Una vez traducido el contenido, puede exportar la línea de base traducida para archivarla o compartirla con diferentes equipos de su organización. Debe tener en cuenta los siguientes puntos antes de exportar una línea de base traducida:

- La exportación de una línea de base solo es posible después de traducir el contenido de la línea de base. Si intenta exportar una línea de base para la que la traducción no se ha iniciado o no se ha completado, se producirá un error.
- Solo puede transferir la línea de base para una versión que ya esté traducida. Por ejemplo, si ha creado una línea de base para la versión 1.1 del contenido y lo mismo se ha traducido, puede exportar esta línea de base. Sin embargo, si ha creado una línea de base para la versión 1.2, que no está traducida, no puede exportar esta línea de base.
- Si ya se ha exportado una línea de base, puede sobrescribir la línea de base existente seleccionando la *Sobrescribir Línea Base Existente* al exportar.

Siga estos pasos para exportar una línea de base traducida:

1. Abra el mapa DITA que contiene la línea de base traducida.

1. En el **Traducción** expanda la pestaña **Línea de base** disponible en el carril izquierdo.

   ![](images/export-baseline.png){width="800" align="left"}

1. Seleccione el **Usar línea de base** y seleccione la línea de base que desea exportar.

1. Haga clic en **Exportar línea de base**.

   Se muestra el estado de exportación. Si el proceso se realiza correctamente, se mostrará un mensaje que menciona el idioma para el que se exporta la línea de base. En caso de error, se muestra la causa del error.

   Si intenta exportar la línea de base que ya se ha exportado, también se mostrará el mensaje de error de creación de línea de base .

1. \(Opcional\) Para exportar una línea de base que ya se ha exportado, seleccione **Sobrescribir Línea Base Existente** y haga clic en **Exportar línea de base**.


**Tema principal:**[ Generación de resultados](generate-output.md)
