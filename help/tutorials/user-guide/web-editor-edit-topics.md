---
title: Editar temas en el Editor web
description: Obtenga información sobre cómo editar temas en el Editor web
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---


# Editar temas en el Editor web {#id2056B040VUI}

El Editor web incluye una serie de funciones de edición que permiten crear o modificar fácilmente los archivos de temas. En general, realizaría los siguientes pasos para editar un tema en el Editor web.

>[!IMPORTANT]
>
> Si se produce un error de aplicación al trabajar en el Editor web, actualice la página para continuar trabajando.

1. Para realizar cambios en el tema, haga clic dentro del límite de texto del elemento requerido y comience a realizar ediciones.

1. Para insertar un elemento específico, haga clic en al final del elemento tras el cual desea insertar el nuevo elemento y haga clic en el icono del elemento requerido en la barra de herramientas. También puede utilizar la combinación de teclas `Alt+Enter` para invocar la variable **Insertar elemento** ventana emergente.

   Aparece una lista de elementos que se pueden utilizar en el tema. AEM guías realiza una colocación inteligente de los elementos según su ubicación válida en el tema.

   >[!NOTE]
   >
   > También puede elegir qué icono mostrar en la barra de herramientas configurando la variable `ui_config.json` archivo ubicado en - `/etc/designs/fmdita/clientlibs/xmleditor/`. Para obtener más información sobre la personalización de funciones, póngase en contacto con el administrador del sistema.

1. Una vez que haya terminado de editar el documento, haga clic en **Guardar**.

   >[!NOTE]
   >
   > Si no desea confirmar los cambios en AEM repositorio, haga clic en **Cerrar** y, a continuación, haga clic en **Cerrar sin guardar** en el cuadro de diálogo Cambios no guardados .

   **Actualizar el explorador al editar los archivos**
AEM guías permite actualizar el navegador mientras edita el contenido en el Editor web. Esta función le ayuda a seguir editando contenido en caso de que encuentre un error de aplicación mientras trabaja. Si pulsa en la actualización del explorador mientras se abren para la edición uno o más archivos con cambios sin guardar, se le advertirá de que se pueden perder los cambios sin guardar. Se le da la opción de cancelar la operación de actualización y guardar los archivos para conservar los cambios.

   Incluso al actualizar el navegador, las vistas del panel izquierdo y derecho se conservan en el Editor web. Por ejemplo, el tema activo en el panel Repositorio se vuelve a abrir. El panel de mapa se conserva junto con el mapa abierto anteriormente.

   El tema activo o el mapa DITA se vuelve a abrir en el área de edición de contenido.

   El panel derecho también se vuelve a abrir y muestra la misma vista que antes de la actualización.

   **Indicador de copia de trabajo**
AEM guías proporciona el indicador de copia de trabajo que muestra si el \(copia de trabajo\) actual del archivo está sincronizado con la versión guardada o no. Si ha realizado cambios en la copia actual y no ha guardado el archivo, aparece una marca \* junto con el título en la ficha archivo del tema. Este indicador actúa como recordatorio para guardar los cambios y desaparece al guardar el archivo.

   ![](images/working-copy-text-update-indicator.png){width="550" align="left"}

   AEM guías también indica si la última copia guardada de \(working\) del archivo está sincronizada con la versión guardada o no. Si tiene algunos cambios sin guardar entre la copia de trabajo y la última versión guardada, aparece una marca \* junto con la información de la versión que se muestra en la esquina superior derecha de la pestaña del archivo del tema. Este indicador actúa como recordatorio para guardar y crear una versión a partir de la copia \(de trabajo\) actual del archivo.

   ![](images/version-update-indicator.png){width="550" align="left"}


**Tema principal:**[ Trabajar con el Editor web](web-editor.md)

