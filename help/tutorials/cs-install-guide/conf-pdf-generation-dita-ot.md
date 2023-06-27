---
title: Configuración de la generación de PDF de tema único
description: Obtenga información sobre cómo configurar la generación de PDF de un solo tema
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---


# Configuración de la generación de PDF de tema único {#id22ADC70M0XA}

AEM Con las Guías de, puede generar el PDF de temas individuales o un archivo de mapa completo. Los temas se pueden publicar en formato de PDF utilizando el PDF nativo o el método DITA-OT. Utilice el método de PDF nativo para generar una salida de PDF con numerosas funciones basada en los estándares de medios paginados CSS3 y CSS del W3C. Se puede utilizar el método DITA-OT para generar una salida de PDF para un mapa desde el tablero de mapas.

>[!NOTE]
>
> El PDF nativo es el método predeterminado para generar un PDF AEM en la versión actual de las guías de la aplicación.

Para activar la generación del PDF antiguo mediante DITA-OT desde el modo de vista previa del tema, realice los pasos siguientes:

1. Inicie sesión en Adobe Experience Manager como administrador y descargue el archivo de configuración de la interfaz de usuario.

1. Para ello, haga clic en el vínculo Adobe Experience Manager en la parte superior y seleccione **Herramientas**.
1. Seleccionar **Guías** en la lista de herramientas y haga clic en **Perfiles de carpeta**.
1. Haga clic en **Perfil global** mosaico.
1. Seleccione el **Configuración del editor XML** y haga clic en **Editar** en la parte superior
1. Haga clic en **Descargar** para descargar el archivo ui\_config.json en su sistema local. A continuación, puede realizar cambios en el archivo y luego cargarlo.
1. En el `ui_config.json` , busque la siguiente configuración:

   ```
   {
                           "component": "button",
                           "variant": "action",
                           "quiet": true,
                           "icon": "filePDF",
                           "title": "Download as PDF",
                           "on-click": "EDITOR_SAVE_AS_PDF"
                           }
   ```

   y reemplácelo por

   ```
   {
                           "component": "button",
                           "icon": "filePDF",
                           "variant": "action",
                           "quiet": true, "title": "Export as PDF",
                           "on-click": "DOWNLOAD_TOPIC_PDF",
                           "show" : ["@isPreviewMode", "@isXmlMode"]
                           }
   ```

1. Guarde el archivo y cárguelo.

Después de realizar los pasos dados anteriormente, si elige el mismo perfil de carpeta de Preferencias de usuario en el Editor Web, verá la opción de generación de PDF en el modo de vista previa de un tema.

**Tema principal:**[ Personalizar editor web](conf-web-editor.md)

