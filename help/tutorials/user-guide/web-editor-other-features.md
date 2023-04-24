---
title: Otras funciones del Editor web
description: Obtenga información sobre otras funciones del Editor web
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '2131'
ht-degree: 0%

---


# Otras funciones del Editor web {#id2056B0B0YPF}

Hay otras funciones útiles en el Editor web que puede utilizar:

**Funciones del menú contextual en la ficha de un archivo**

Cuando abra un archivo en el Editor web, puede realizar varias acciones desde el menú contextual. Puede que vea diferentes opciones en función de si abre un archivo multimedia, un solo archivo DITA o varios archivos.

**Archivo multimedia**

Las siguientes funciones se obtienen en el menú contextual de la ficha de un archivo multimedia abierto:

![](images/media-file-context-menu.png){width="300" align="left"}

**Archivo DITA único**

Las siguientes funciones se obtienen en el menú contextual de la ficha de un archivo abierto:

:   ![](images/single-file-context-menu.png){width="300" align="left"}

**Varios archivos**

Cuando tiene varios archivos abiertos, obtiene más opciones en el menú contextual:

![](images/multiple-files-context-menu.png){width="550" align="left"}

A continuación se explican las distintas opciones del menú contextual:

***Guardar***: Puede elegir entre las siguientes opciones:

- **Guardar**: Para guardar un archivo sin crear una nueva versión, seleccione **Guardar**. Siempre que cree un tema nuevo, se creará en DAM una copia de trabajo del tema sin versión. Al guardar el documento, se actualiza la copia de trabajo del documento en DAM. Al realizar un simple guardado en esta versión, no se crea una nueva versión de un tema. Si el tema se está revisando, guardar un tema no da acceso a los revisores al contenido del tema cambiado.

- **Guardar todo**: Si hay varios documentos abiertos en el Editor web, también tiene la opción de **Guardar todo** abrir documentos.


***Guardar como nueva versión***

Para crear una nueva versión del archivo, seleccione **Guardar como nueva versión**. Para obtener más información, consulte **Guardar** y **Guardar como nueva versión**, consulte [Conozca las funciones del Editor web](web-editor-features.md#).

***Copiar***: Puede elegir entre las siguientes opciones:

- **Copiar UUID**: Para copiar el UUID del archivo activo actualmente en el Portapapeles, seleccione **Copiar \> Copiar UUID**.
- **Copiar ruta**: Para copiar la ruta completa del archivo activo actualmente en el Portapapeles, seleccione **Copiar \> Copiar ruta**.


***Localizar en***: Puede elegir entre las siguientes opciones:

- **Mapa**: Si ha abierto un mapa DITA grande y desea encontrar la ubicación exacta de un archivo en el mapa, seleccione **Localizar en \> Mapa**. Cuando selecciona la opción Localizar en mapa , el archivo \(desde donde se invoca la opción\) se encuentra y se resalta en la jerarquía del mapa. Para poder utilizar esta función, debe abrir el archivo de asignación en el Editor web. Si la vista Mapa está oculta, invocar esta función mostrará la vista Mapa y el archivo se resaltará en la jerarquía del mapa.

- **Repositorio**: Similar a Localizar en el mapa, la variable **Localizar En \> Repositorio** muestra la ubicación del archivo en el repositorio \(o DAM\). Se abre la vista del repositorio y el archivo seleccionado se resalta en el repositorio. Si el archivo se encuentra dentro de una carpeta, esta se expande para mostrar la ubicación del archivo seleccionado en el repositorio.


***Agregar a***: Puede elegir entre las siguientes opciones:

- **Favoritos**: Para añadir el archivo seleccionado a la colección favorita, seleccione **Agregar A \> Favoritos**. Para obtener más información, consulte la **Favoritos** descripción de la función en el [Panel izquierdo](web-editor-features.md#id2051EA0M0HS) para obtener más información.



- **Contenido reutilizable**: Para copiar el archivo seleccionado en la lista de contenido reutilizable, seleccione **Agregar A \> Contenido Reutilizable**. Para obtener más información, consulte la **Contenido reutilizable** descripción de la función en el [Panel izquierdo](web-editor-features.md#id2051EA0M0HS) para obtener más información.




***Propiedades***

Para ver la página AEM propiedades del archivo seleccionado, seleccione **Propiedades**.

***Split***: Puede elegir entre las siguientes opciones:

**Arriba, Abajo, Izquierda o Derecha**

De forma predeterminada, el Editor web permite ver un tema a la vez. Puede haber casos en los que desee ver dos o más temas al mismo tiempo. Dividir la pantalla del editor le permite ver varios temas al mismo tiempo. Por ejemplo, si tiene dos temas: A y B se abren en el editor. Hacer clic con el botón derecho en el tema B y elegir **Dividir \> Arriba** divide la ventana del editor en dos partes. El tema B se muestra en la mitad superior y el tema A se muestra en la mitad inferior. Del mismo modo, también puede dividir la pantalla horizontalmente seleccionando **Dividir \> Izquierda** o **Dividir \> Derecha**. La siguiente captura de pantalla del Editor web muestra los temas divididos horizontal y verticalmente. En cada división, puede tener una vista diferente. Por ejemplo, en la siguiente captura de pantalla, la pantalla 1 está en el modo de vista Código fuente, la pantalla 2 tiene dos documentos abiertos en el modo Autor y la pantalla 3 en el modo de Vista previa. Puede mover los documentos de una pantalla a otra arrastrando la ficha del archivo y soltándola en la pantalla en la que desea colocarla. Del mismo modo, también puede reordenar las fichas de archivo arrastrándolas y moviéndolas según sus preferencias.

![](images/split-editor.png){width="800" align="left"}

***Generación rápida***

Genere el resultado del archivo seleccionado. La salida solo se puede generar para archivos que formen parte de un ajuste preestablecido de salida. Para obtener más información, consulte [Publicación basada en artículos desde el Editor web](web-editor-article-publishing.md#id218CK0U019I).

***Cerrar***: Puede elegir entre las siguientes opciones:

**Cerrar**, **Cerrar otros** o **Cerrar todo**

Si desea cerrar el archivo desde el que invocó el menú contextual, seleccione **Cerrar \> Cerrar**. Uso **Cerrar \> Cerrar otros** para cerrar todos los demás archivos abiertos excepto el archivo activo actualmente. Para cerrar todos los archivos abiertos, seleccione la opción **Cerrar \> Cerrar todo** en el menú contextual o también puede cerrar el Editor web. Si hay archivos sin guardar en la sesión, se le pedirá que los guarde.

**Situaciones de cierre y guardado de archivos**

Cuando intenta cerrar un archivo abierto en el Editor web utilizando la variable **Cerrar** en la pestaña del archivo o en la pestaña **Cerrar** en el menú Opciones , AEM guías le pedirá que guarde las ediciones y desbloquee un archivo bloqueado.

Las indicaciones se basan en las siguientes configuraciones seleccionadas por el administrador:

- **Solicite el check-in al cerrar:** Tiene la opción de proteger el archivo \(que ha desprotegido\) al cerrar el editor.
- **Solicitar una nueva versión al cerrar**: Se le da la opción de guardar el archivo \(que ha editado\) como una nueva versión cuando cierre el editor.

La experiencia de guardado de archivos dependerá de las tres situaciones siguientes, en las que tenga:

- No se ha realizado ningún cambio en el contenido.
- Se editó el contenido y se guardaron los cambios.
- Se editó el contenido pero no se guardaron los cambios.

Puede ver las siguientes opciones en función de si el archivo está bloqueado/desbloqueado y tiene cambios guardados o no guardados:

- **Desbloquear y cerrar**: El bloqueo del archivo se libera y el archivo se cierra.

   ![](images/file-close-unlock-file.png){width="400" align="left"}

- **Guardar como nueva versión**: Esto guardará los cambios realizados en el contenido y creará una nueva versión del archivo. También puede agregar etiquetas y comentarios para la versión guardada recientemente. Para obtener más información sobre cómo guardar una nueva versión, consulte [Guardar como nueva versión](web-editor-features.md#save-as-new-version-id209ME400GXA).

- **Desbloquear el archivo**: Si elige desbloquear un archivo, se liberará el bloqueo del archivo y los cambios se guardarán en la versión actual del archivo.

>[!NOTE]
>
> Si anula la selección de la opción para desbloquear el archivo, también puede cerrar el archivo sin guardar los cambios.

Por ejemplo, una de las indicaciones se muestra en la siguiente captura de pantalla:

![](images/file-close-save-changes-unlock.png){width="400" align="left"}

**Indicaciones visuales para referencias rotas**

- Si el tema contiene referencias cruzadas rotas o referencias de contenido, se muestran en texto rojo.

**Copia inteligente y pegado**

- Puede copiar y pegar fácilmente contenido dentro de y entre los temas. La estructura del elemento de origen se mantiene en el destino. Además, si el contenido copiado contiene referencias de contenido, también se copian.

**Recordar la última ubicación explorada**

- El Editor web proporciona un cuadro de diálogo de exploración de archivos inteligente. El editor recuerda la última ubicación usada al insertar una referencia o contenido. La primera vez que invoque el cuadro de diálogo Examinar archivo \(mediante Insertar referencia o Insertar contenido reutilizar\), se le dirigirá a la ubicación donde se guarda el documento actual. En la misma sesión, si intenta insertar otra referencia, el cuadro de diálogo de exploración de archivos navegará automáticamente a la ubicación desde la que insertó la última referencia.

>[!NOTE]
>
> En el caso de un archivo de imagen, audio o vídeo, el cuadro de diálogo de exploración de archivos toma como valor predeterminado la ubicación del archivo y no la última ubicación usada.

**Compatibilidad con la publicación basada en artículos**

- Desde el Editor web, puede generar el resultado para uno o más temas o el mapa DITA completo. Debe crear ajustes preestablecidos de salida para su mapa DITA y, a continuación, puede generar fácilmente el resultado para uno o más temas. Si ha actualizado algunos temas en el mapa, también puede generar el resultado solo para esos temas desde el Editor web. Para obtener más información, consulte [Publicación basada en artículos desde el Editor web](web-editor-article-publishing.md#id218CK0U019I).

**Compatibilidad con documentos Markdown**

- El Editor web permite utilizar documentos Markdown \(.md\) junto con documentos DITA. Puede crear y previsualizar fácilmente un documento Markdown en el Editor web y también agregarlo en el archivo de mapa a través del editor de mapas DITA. Para obtener más información, consulte [Creación de documentos Markdown desde el Editor web](web-editor-markdown-topic.md#).

**Compatibilidad con el tema del término del glosario de DITA**

- El Editor web admite los términos de glosario DITA que puede insertar añadiendo `term` o `abbreviated-form` elementos.

**Insertar ecuaciones de MathML**

- AEM guías le ofrece una compatibilidad predeterminada para insertar ecuaciones MathML mediante la integración con [MathType Web](https://docs.wiris.com/en/mathtype/mathtype_web/intro) aplicación. Para insertar una ecuación MathML, haga clic en la **Insertar elemento** y escriba mathml. Al seleccionar un elemento matemático de la lista, se muestra el cuadro de diálogo Insertar MathML:

![](images/insert-mathml-equation.png){width="550" align="left"}

Con las herramientas de ecuación MathML, cree la ecuación y haga clic en Insert para añadirla al documento. La ecuación se inserta con fondo gris claro, como se muestra a continuación:

![](images/sample-mathml-equation.PNG){width="400" align="left"}

Puede actualizar una ecuación haciendo clic con el botón derecho en una ecuación existente y seleccionando **Editar MathML** en el menú contextual.

**Insertar notas al pie**

- Inserte una nota al pie en el contenido utilizando la variable `fn` elemento. En el modo de creación, el valor de la nota al pie se muestra en línea con el contenido. Sin embargo, cuando cambia al modo de vista previa o publica el documento, la nota al pie aparece al final del tema.

**Cambiar el nombre o reemplazar un elemento**

- El Editor web muestra la ruta de exploración del elemento en la parte superior del tema. Si desea intercambiar o reemplazar un elemento por otro elemento, puede hacerlo desde el menú contextual de la ruta de exploración. Por ejemplo, puede intercambiar `p` elemento con `note` o cualquier otro elemento válido en el contexto.

![](images/rename-element.png){width="400" align="left"}

En la ruta de exploración, haga clic con el botón derecho en el nombre de un elemento que desea reemplazar y, a continuación, seleccione Cambiar nombre de elemento en el menú contextual. El cuadro de diálogo Cambiar nombre de elemento muestra todos los elementos válidos permitidos en la ubicación actual. En el cuadro de diálogo Cambiar nombre de elemento, seleccione el elemento que desee utilizar. El elemento original se reemplaza por el nuevo elemento.

Además del menú contextual de la ruta de exploración, también se puede acceder al cuadro de diálogo Cambiar nombre de elemento desde otras ubicaciones:

- Haga clic en el nombre del elemento en la ruta de exploración para seleccionar el contenido del elemento y haga clic con el botón derecho en el contenido seleccionado para que aparezca el menú contextual.

- Habilite la vista Etiquetas , haga clic en la etiqueta de apertura de cualquier elemento y, a continuación, haga clic con el botón derecho en el contenido seleccionado para que aparezca el menú contextual.

- Puede acceder al cuadro de diálogo Cambiar nombre de elemento invocando el menú Opciones de un elemento en el panel Esquema.


**Desajustar un elemento**

- Desajustar un elemento le permite quitar la etiqueta de elemento del texto seleccionado y combinarlo con su elemento principal. Por ejemplo, si tiene un `p` dentro de un `note` , puede desajustar el `p` para combinar el texto directamente dentro del `note` elemento. La opción Desajustar elemento está disponible en el menú contextual de la ruta de exploración del tema. Para desajustar un elemento, selecciónelo en la ruta de exploración del tema, haga clic con el botón derecho en el elemento para abrir el menú contextual y, por último, seleccione Desajustar elemento para eliminar el elemento y combine el texto del elemento con su elemento principal.

**Conservación de saltos de línea y sangría**

- Los elementos DITA que contienen salto de línea y espacios se admiten y procesan según su definición en los modos Autor, Origen o Vista previa, y también en la salida publicada final. La siguiente captura de pantalla muestra el contenido dentro del `msgblock` elemento en el que se han conservado los saltos de línea y los espacios \(sangría\):

![](images/new-line-support_cs.png){width="500" align="left"}

**Generar automáticamente ID de elemento**

- Puede generar automáticamente ID para los elementos de su tema DITA. Estos ID son únicos dentro de un tema de DITA. Por ejemplo, si genera ID para un elemento de párrafo, los ID serán p\_1, p2, p\_3, etc. Puede seleccionar varios elementos y generar ID para cada elemento seleccionado.

Para generar ID automáticamente para uno o varios elementos, haga lo siguiente:

1. Abra el tema en el editor web.
1. Seleccione el contenido al que desea asignar las ID.
1. Haga clic con el botón derecho y seleccione **Genere ID desde el menú contextual.**

   También puede hacer clic con el botón derecho en la ruta de exploración y seleccionar **Generar ID**.


**Tema principal:**[ Trabajar con el Editor web](web-editor.md)

