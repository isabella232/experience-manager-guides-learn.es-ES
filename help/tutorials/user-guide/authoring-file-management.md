---
title: Administrar archivos y carpetas
description: Obtenga información sobre cómo administrar archivos y carpetas
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '2502'
ht-degree: 0%

---


# Administrar archivos y carpetas {#id2116G0L08XA}

En esta sección se explica cómo las guías de AEM gestionan las operaciones básicas de los archivos, como copiar, pegar, arrastrar y soltar archivos y eliminarlos. Los siguientes escenarios son posibles:

## Copiar y pegar archivos

**Si el archivo tiene un nombre de archivo legible en lenguaje natural**

- *Si el archivo con el mismo nombre no existe en la carpeta de destino*: Se crea una copia nueva del archivo y también se le asigna un UUID. En este caso, el nombre del archivo es el mismo que el nombre del archivo original.
- *Si el archivo con el mismo nombre ya existe en la carpeta de destino*: Se crea una nueva copia del archivo con un sufijo \(como filename0.extension\). También se asigna un UUID al archivo recién creado.


**Si el nombre de archivo está basado en un patrón UUID**

- *Si el archivo con el mismo nombre no existe en la carpeta de destino*: Se crea una nueva copia del archivo y también se le asigna un nuevo UUID en la nueva ubicación. En este caso, el nombre del archivo es el mismo que el UUID.
- *Si el archivo con el mismo nombre ya existe en la carpeta de destino*: Se crea una nueva copia del archivo y también se le asigna un nuevo UUID. El nombre del archivo es el mismo que el UUID.


## Copiar y pegar carpetas

**Copiar y pegar una carpeta en la misma ubicación**

- *La carpeta tiene archivos con nombres de archivo legibles por humanos*: Se crea una nueva copia de la carpeta con un sufijo \(como folder name0\). También se asigna un nuevo UUID a los archivos de la carpeta . Sin embargo, no hay ningún cambio en los nombres de archivo.

- *La carpeta tiene archivos con nombres de archivo basados en un patrón UUID*: Se crea una nueva copia de la carpeta con un sufijo \(como folder name0\). También se asigna un nuevo UUID a todos los archivos de la nueva carpeta. También se cambian los nombres de los archivos; los nombres de archivo son los mismos que el nuevo UUID.


**Copiar y pegar una carpeta en una ubicación diferente**

- *La carpeta tiene archivos con nombres de archivo legibles por humanos*: Se crea una nueva copia de la carpeta y también se asigna un nuevo UUID a todos los archivos de la carpeta en la nueva ubicación. En este caso, no hay ningún cambio en los nombres de carpeta o archivo.

- *La carpeta tiene archivos con nombres de archivo basados en un patrón UUID*: Se crea una nueva copia de la carpeta con el mismo nombre que la carpeta original. También se asigna un nuevo UUID a todos los archivos de la nueva carpeta. También se cambian los nombres de los archivos; los nombres de archivo son los mismos que el nuevo UUID.


## Arrastrar y soltar archivos

**Arrastrar y soltar con nombres de archivo legibles por humanos**

- *Arrastrar y soltar en la misma ubicación*: Se le dan las opciones para **Sobrescribir archivo existente\(s\)**, **Mantener ambos archivos\(s\)** y una opción para crear una versión de la copia de trabajo existente.

   ![](images/uuid-human-readable-drag-drop-same-location.PNG){width="650" align="center"}

   Si elige la opción **Sobrescribir archivo existente\(s\)** , el archivo que se está cargando reemplaza la versión de trabajo actual del archivo existente en la ubicación original. El UUID no se crea ni se cambia.

   Si elige la opción **Mantener ambos archivos\(s\)** , se crea una nueva copia del archivo con un sufijo \(como filename0.extension\). También se asigna un nuevo UUID al archivo recién copiado.

   Con la opción Sobrescribir archivo existente\(s\) , si elige la opción de crear una versión a partir de la copia de trabajo existente, también se creará una nueva versión a partir de la copia de trabajo del documento.

   >[!NOTE]
   >
   > **Crear nueva versión para el archivo cargado** debe ser activada por el administrador. Si esta función está habilitada, se crea una nueva versión para el archivo cargado. Si la opción no está seleccionada, no se crea una versión del archivo cargado. Para obtener más información, consulte *Crear nueva versión para el archivo cargado* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.

   Si otro usuario ya ha desprotegido un archivo para editarlo e intenta cargar y sobrescribir el archivo existente, este falla y muestra un error.

   >[!NOTE]
   >
   >La variable **Sobrescribir archivo extraído al cargar** el administrador debe desactivarlo. Si esta función está habilitada, puede sobrescribir los archivos extraídos. Si la función no está activada, se impide que se sobrescriba un archivo extraído. Para obtener más información, consulte *Sobrescribir archivo extraído al cargar* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.


- *Arrastrar y soltar archivos en una ubicación diferente*: Se crea una nueva copia del archivo y también se le asigna un nuevo UUID en la nueva ubicación. En este caso, el nombre del archivo es el mismo que el nombre del archivo original.


**Arrastrar y soltar con nombres de archivo basados en un patrón UUID**

*Arrastrar y soltar archivo en la misma ubicación*: Se le dan las opciones para **Sobrescribir archivo existente\(s\)** junto con la opción para crear una versión de la copia de trabajo existente.

![](images/uuid-drag-drop-same-location.PNG){width="650" align="center"}

Cuando se sobrescribe el archivo, no se produce ningún cambio en el nombre del archivo o en su UUID.

Si selecciona la opción **Crear versión para la copia de trabajo existente** , se crea una nueva versión de la copia de trabajo del documento; el nuevo archivo se carga, también se crea una nueva versión del archivo y se hace como la copia de trabajo del documento.

**Crear nueva versión para el archivo cargado** debe ser activada por el administrador. Si esta función está habilitada, se crea una nueva versión para el archivo cargado. Si la opción no está seleccionada, no se crea una versión del archivo cargado. Para obtener más información, consulte *Crear nueva versión para el archivo cargado* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.


*Arrastrar y soltar archivo en una ubicación diferente*: Se le dan las opciones para **Sobrescribir archivo existente\(s\)**, **Mover archivo\(s\) a nueva ubicación** y una opción para crear una versión de la copia de trabajo existente.

![](images/uuid-drag-drop-different-location.PNG){width="650" align="center"}

Si elige la opción **Sobrescribir archivo existente\(s\)** , el archivo que se está cargando reemplaza al archivo existente en la ubicación original. El UUID no se crea ni se cambia.

Si elige la opción **Mover archivo\(s\) a nueva ubicación** , el archivo existente se mueve a la ubicación actual y, a continuación, se sobrescribe con el archivo que se está cargando. Mover un archivo a la nueva ubicación no rompe ninguna referencia existente desde o hacia el archivo.

Al reemplazar o mover los archivos, si elige la opción de crear una versión a partir de la copia existente, se crea una nueva versión a partir de la copia de trabajo del documento; el nuevo archivo se reemplaza en la ubicación existente o se mueve a la nueva ubicación.


## Mover archivos de forma masiva

AEM guías viene con la herramienta de movimiento masivo que ayuda a un administrador a mover una carpeta que tiene un gran número de archivos de una ubicación a otra. Esta herramienta puede mover fácilmente archivos dentro de una o más carpetas a una carpeta diferente del repositorio de AEM. Una de las características principales de esta herramienta es que no solo mueve un gran número de archivos, sino que también mantiene las referencias a y desde los archivos que se mueven. Puede modificar el número de archivos que puede mover por lotes sin obstaculizar las tareas de creación y publicación.

>[!NOTE]
>
> La herramienta Mover masivamente solo funciona en el nivel de carpeta. Si desea mover archivos de tema o asignación individuales, utilice la herramienta de desplazamiento normal desde AEM interfaz de usuario de Assets.

Estas son algunas de las funciones que proporciona la herramienta de desplazamiento masivo:

- Puede modificar el número de archivos que desea procesar en cada lote. Esto puede requerir que ejecute algunas pruebas antes de llegar a un número óptimo que su sistema pueda manejar fácilmente.
- Los servicios de creación y publicación se ejecutan sin problemas sin interrupciones en la operación de traslado.
- Tener control completo sobre el intervalo de tiempo entre los procesos por lotes \(ejecución de\) subsiguientes. Este intervalo de tiempo garantiza que la operación de posprocesamiento se complete antes de iniciar el siguiente lote de archivos.

- Administración automática de carpetas con el mismo nombre. Esta función garantiza que, incluso si hay carpetas con el mismo nombre moviéndose, no se sobrescriban.

- Gestión automática de referencias a los archivos que se van a mover y desde ellos.


Debe tener en cuenta los siguientes puntos antes de ejecutar el proceso por lotes:

- Si planea mover temas que están actualmente en revisión, debe cerrar el proceso de revisión de todos esos temas antes de moverlos. No cerrar la tarea de revisión romperá el proceso de revisión.
- Debe ejecutar una única operación de movimiento masivo en el sistema en cualquier momento. Esto garantiza un tratamiento adecuado de las referencias a y desde los temas que se van a mover.


Para mover archivos de forma masiva, realice los siguientes pasos:

1. Haga clic en el vínculo Adobe Experience Manager en la parte superior y elija **Herramientas**.
1. Select **Guías** de la lista de herramientas.
1. Haga clic en el **Herramienta Mover masivamente** mosaico.

   Se muestra la página Herramienta de traslado masivo .

   ![](images/bulk-move-tool_cs.PNG){width="550" align="center"}

1. Proporcione los siguientes detalles en la página Herramienta de desplazamiento masivo :

   - **Agregar sufijo a archivos duplicados**: Si va a mover carpetas con el mismo nombre, debe seleccionar esta opción. Por ejemplo, en la captura de pantalla anterior, la variable **Ruta de origen** contiene el nombre de las carpetas que se van a mover. La carpeta denominada topic existe en dos ubicaciones diferentes: test-A y test-B. Cuando seleccione esta opción, las carpetas se moverán correctamente. La primera carpeta movida tendrá el nombre de tema, mientras que la segunda carpeta se llamará tema0. La operación de movimiento agrega un sufijo de la serie secuencial \(0, 1, 2, etc.) a las carpetas con el mismo nombre.

      Si está moviendo carpetas con el mismo nombre sin seleccionar esta opción, la operación se interrumpirá con un mensaje.

   - **Ruta de origen\(s\)**: Especifique la ubicación de las carpetas que desea mover. Normalmente, tendrá que copiar y pegar la ubicación de origen desde la barra de direcciones del explorador. Para especificar varias ubicaciones de carpetas, haga clic en el botón **Agregar** botón.

   - **Ruta de destino**: Especifique la ubicación a la que desea mover las carpetas de origen.

1. Haga clic en **Movimiento masivo**.

   El sistema empieza a mover archivos del origen a la ubicación de destino. Una vez completado el proceso, se muestra un resumen del proceso de movimiento en la parte inferior de la página.

   ![](images/bulk-move-summary.PNG){width="650" align="center"}


## Buscar contenido DITA

De forma predeterminada, AEM no reconoce el contenido DITA, por lo que no proporciona ningún mecanismo para buscar contenido DITA en su repositorio. AEM guías añade una capa sobre AEM, lo que permite a AEM comprender y procesar el contenido DITA. La función Buscar contenido DITA en AEM guías le permite buscar contenido DITA en AEM repositorio.

>[!NOTE]
>
>El administrador del sistema puede configurar la variable **Elemento DITA** componente de búsqueda y, a continuación, puede utilizar la función desde la interfaz de usuario de AEM Assets. Para obtener más información, consulte *Añadir componente de búsqueda de elementos DITA en la interfaz de usuario de Assets* en Instalar y configurar las guías de Adobe Experience Manager as a Cloud Service.

Con la función de búsqueda, puede:

- Busque contenido DITA basado en un valor de elemento; por ejemplo, `author`= xml
- Busque contenido DITA basado en un valor de atributo; por ejemplo, `@platform`= windows
- Utilice una combinación de elemento DITA y valor de atributo; por ejemplo, `author`= xml `AND` `@platform`= windows

Realice los siguientes pasos para buscar contenido DITA en AEM repositorio:

1. Abra la interfaz de usuario de Assets.

1. En el carril izquierdo, seleccione **Filtros**.

   ![](images/left-rail-filter.png){width="450" align="center"}

   Las opciones de filtrado de contenido se muestran en el carril izquierdo. También encontrará la opción de filtrado: Elemento DITA, que se utiliza para filtrar el contenido DITA.

   ![](images/dita-element-search.png){width="450" align="center"}

1. *\(Opcional\)* En el **Seleccionar directorio de búsqueda** , busque la ubicación en la que desea buscar.

1. En el **Elemento DITA** , proporcione la variable **Nombre del elemento**, **Atributo** y un valor que desee buscar. Por ejemplo, para buscar documentos que tengan `author` elemento que es de `@type` creador, debe proporcionar la información como se muestra en la siguiente captura de pantalla:

   ![](images/search-params.png){width="650" align="center"}

   Los criterios de búsqueda introducidos en la variable **Elemento DITA** se muestra en la parte superior de la barra de búsqueda. Los archivos que coinciden con los criterios de búsqueda se muestran en la **Resultados de la búsqueda** .

   Tenga en cuenta los siguientes puntos al especificar los criterios de búsqueda:

   - Para buscar una frase exacta, escriba la frase en el campo Valor entre comillas `"`búsqueda de frases`"`.
   - Puede agregar hasta 3 criterios de búsqueda de elementos DITA.
   - Si especifica varios criterios de búsqueda, todos se combinarán con la lógica AND.
   - No puede usar caracteres comodín en los criterios de búsqueda. Por ejemplo, para buscar la plataforma \(attribute\) con valor de Windows, no se puede especificar \*form ni Windo?s.

**Filtro de estado de cierre de compra en la búsqueda**

Además del filtro Elemento DITA, AEM guías también le permite buscar contenido en función de su estado de cierre de compra. Esto es útil cuando desea filtrar rápidamente los archivos que está desprotegido por usted y desea volver a protegerlos.

Realice los siguientes pasos para buscar archivos en función de su estado de cierre de compra:

1. Abra la interfaz de usuario de Assets.

1. Haga clic en **Filtro** en el carril izquierdo.
1. Escriba la palabra clave de búsqueda en la barra de búsqueda.
1. Aplique los filtros necesarios desde el carril izquierdo.

   Por ejemplo, puede aplicar **Estado de cierre de compra** para mostrar los temas desprotegidos o desprotegidos. Puede refinar aún más esta lista eligiendo el usuario o grupo de la lista Protegido por .

   Se muestra el resultado de la búsqueda.


## Eliminar archivos

La eliminación de archivos de AEM repositorio es una función restringida que controla el administrador del sistema. En función de las configuraciones, la eliminación de archivos podría restringirse si:

- Desprotegido
- Tener referencias entrantes o salientes

También puede eliminar archivos únicamente si pertenece a un grupo de usuarios específico que tenga privilegios para eliminar archivos.

>[!NOTE]
>
> Para obtener más información sobre las configuraciones de administración de archivos, consulte *Impedir la eliminación de archivos desprotegidos* y *Impedir la eliminación de archivos a los que se hace referencia* secciones de la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.

Si el administrador ha concedido el permiso de eliminación de archivos a todos los usuarios, se mostrará el siguiente mensaje cuando elimine archivos que contengan referencias:

![](images/allow_unsafe_delete-force-delete.PNG){width="650" align="center"}

En esta situación, puede eliminar archivos sin eliminar las referencias entrantes o salientes de los archivos.

Si los permisos de eliminación se otorgan a un grupo de usuarios específico, también aparecerá el mensaje anterior para los usuarios que pertenecen a ese grupo. Sin embargo, para otros usuarios, se muestra el siguiente mensaje:

![](images/allow_unsafe_delete_for_delete_assets_group.PNG){width="650" align="center"}

En esta situación, los usuarios no podrán eliminar archivos hasta que se hayan eliminado todas las referencias entrantes y salientes.

## Trabajar con archivos multimedia

Los archivos multimedia como imágenes y vídeos son una parte integral del contenido. Mientras carga y administra el contenido, también puede trabajar con archivos multimedia.

Si el archivo multimedia ha sufrido algún cambio, puede encontrar y previsualizar los archivos en la **Historial de versiones**.Para conocer los cambios en las distintas versiones de un archivo multimedia:

1. Acceda al archivo en **IU de recursos**.
1. Seleccione el archivo para el que desea ver el historial de versiones.
1. En el carril izquierdo, haga clic en **Historial de versiones** y seleccione una versión.
1. También puede ver las miniaturas de las diferentes versiones en el Historial de versiones.

   ![](images/media-version-history-icon.png){width="800" align="center"}

1. En las versiones de la lista, seleccione la que desee utilizar como versión base y haga clic en **Vista previa de la versión**. La vista previa de la versión seleccionada se muestra en la ventana Vista previa de la versión .

   ![](images/media-version-preview.png){width="650" align="center"}


**Tema principal:**[ Administrar contenido](authoring.md)

