---
title: Comentarios de revisión de direcciones
description: Obtenga información sobre cómo dirigir comentarios de revisión
exl-id: 04f6114d-601f-4e92-a303-18a6dd309a49
source-git-commit: 8823669fd29e8a40a41f9ca5d654b38fbea8e2fa
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 0%

---

# Comentarios de revisión de direcciones {#id2056B0X0KBI}

Como autor, puede enviar comentarios en un tema mediante el Editor web. Las secciones siguientes describen formas de editar comentarios en el Editor web.

Un autor puede enviar comentarios en un documento desde el Editor web. Se proporcionan indicadores visuales que indican si se insertaron comentarios \(texto\), se eliminaron o se resaltaron. Además, el tipo de comentario se menciona en la parte superior de cada entrada de comentario.

>[!NOTE]
>
> Al tratar los comentarios de revisión \(para un documento de revisión activo\), asegúrese de no abrir el tema de revisión en varias pestañas con la vista de etiquetas completa habilitada, no cambie entre los modos de vista Autor y Origen.

![](images/comments-page-web-editor_cs.png){width="650" align="left"}

En el modo Editor web , el panel derecho contiene los iconos Revisar y Rastrear cambios . El panel Revisión muestra todos los comentarios realizados en el documento por los revisores. El panel Cambios rastreados muestra el estado de todos los comentarios insertados y eliminados del documento.

- **A**: Seleccione un proyecto de revisión para ver los comentarios de revisión. Si el tema se ha compartido para su revisión en varias tareas de revisión, verá esas tareas en esta lista desplegable.

   Cuando selecciona una tarea de revisión de la lista, puede ver los comentarios realizados por los revisores en esa tarea. Puede dirigir los comentarios de revisión de forma independiente en las tareas, lo que significa que cualquier actualización de un comentario solo es visible para los revisores de esa tarea respectiva.

- **B:** Cada **Revisar proyecto** se crea en una versión específica del documento. La variable **Revisar versión** muestra la versión asociada al proyecto de revisión seleccionado. Esto le ayuda a realizar un seguimiento de la versión que había compartido para su revisión.

- **C**: Si ha actualizado el tema después de iniciar la revisión, al hacer clic en el icono Revertir tema a versión de revisión se revierte la copia de trabajo a la versión que se compartió para su revisión. Esto facilita la incorporación de los comentarios de revisión directamente en la versión que se compartió para su revisión. Después de incorporar los comentarios, puede guardar los cambios en la versión revertida o crear una nueva revisión del tema. Si decide crear una nueva revisión del tema, se creará una nueva rama a partir de la versión del tema que se compartió para su revisión. Por ejemplo, si ha compartido la versión `1.2` de un tema para revisión mientras que la versión actual de creación es `1.3`, puede utilizar este icono para volver a la versión `1.2` para incorporar las observaciones de revisión. Si elige crear una nueva revisión después de incorporar cambios a la versión `1.2`, luego una rama nueva con versión `1.2.0` se crea para el tema.

   Normalmente, después de incorporar los comentarios de revisión, le gustaría combinar los cambios de la última versión del tema. Para ello, utilice el [Combinar](web-editor-features.md#id205DF04E0HS) para obtener todas las actualizaciones realizadas después de compartir el tema para su revisión.

- **D**: Abra la vista contigua para mostrar la versión comentada del tema. Como se ve en la captura de pantalla anterior, la sección situada más a la izquierda es la última versión del tema en la que puede realizar cambios. La siguiente sección es la versión comentada del tema. A medida que navega entre los comentarios del tema, la vista lateral cambia y muestra la versión del tema en la que se realizó el comentario. Cada comentario del panel de comentarios está vinculado al texto correspondiente de esta sección. Ayuda a identificar el texto comentado. Los comentarios se muestran en el orden del texto comentado en el documento.

   Puede ver el número de versión en la parte superior de la vista lateral. Al hacer clic en este icono de nuevo se oculta la versión comentada del tema.

- E: Importe directamente los comentarios \(o tachado\) insertados y eliminados en el tema. Después de hacer clic en el icono Importar, todas las inserciones y eliminaciones de texto se muestran en la copia de trabajo del tema. Ahora, hay dos maneras de aceptar o rechazar comentarios.

   Si desea incorporar el cambio sugerido \(inserción o eliminación\) de una en una, simplemente haga clic con el botón derecho en el comentario del contenido y seleccione Aceptar cambio o Rechazar cambio. Según la selección, el comentario se acepta o rechaza. En caso de comentarios aceptados, el contenido se añade en el contenido; y en caso de rechazo, se elimina del contenido. Además, el estado del comentario cambia en el panel Revisión.

   ![](images/import-comment-accept-web-editor_cs.png){width="800" align="left"}

   También puede utilizar la función de revisión del panel derecho para aceptar o rechazar comentarios. Al hacer clic en cualquier comentario se resalta el comentario del documento.

   ![](images/changes-tab_cs.png){width="800" align="left"}

   >[!IMPORTANT]
   >
   > La función de importación de comentarios solo funciona en los documentos que no han cambiado desde que se compartieron para su revisión. Si ha realizado algún cambio después de enviar el documento para su revisión, recibirá una alerta para **Forzar importación** comentarios en el documento. Sin embargo, si lo hace, se perderán todas las actualizaciones que haya realizado en el documento. La variable **Forzar importación** también se muestra una alerta si el documento se crea fuera y luego se comparte para su revisión. Puede seguir importando los comentarios.

   A medida que acepta o rechaza un comentario, se elimina de la lista Cambios rastreados. Esto también sirve de indicador del número de observaciones que deben abordarse en el documento.

- **F**: En el menú Más opciones , descargue todos los archivos adjuntos disponibles en el tema de revisión.
- **G**: Busque un texto dentro de los comentarios.
- **H**: Acepte o rechace un comentario.

- **I**: Aplique un filtro a los comentarios. Puede filtrar para ver los comentarios según el tipo de revisión \(todos, resaltados, eliminados, insertados o nota adhesiva\), Estado de revisión \(todos, aceptados, rechazados o ninguno\), Revisores \(todos o algunos revisores\(s\)\) o Versiones del tema.


**Tema principal:**[ Revisión de temas o mapas](review.md)
