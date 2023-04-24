---
title: Inicio del Editor web
description: Obtenga información sobre cómo iniciar el Editor web
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---


# Inicio del Editor web {#id2056B0140HS}

Puede iniciar el Editor web desde las siguientes ubicaciones:

- [Página AEM navegación](#id2056BG00RZJ)
- [Interfaz de usuario de AEM Assets](#id2056BG0307U)
- [Consola de asignación DITA](#id2056BG090BF)

Las secciones siguientes tratan los detalles de cómo puede acceder e iniciar el Editor web desde distintas ubicaciones.

## Página AEM navegación {#id2056BG00RZJ}

Cuando inicia sesión en AEM, se muestra la página Navegación :

![](images/web-editor-from-navigation-page_cs.png){width="800" align="left"}

Al hacer clic en el botón **Editor XML** le lleva directamente al Editor web.

![](images/web-editor-launch-page.png){width="800" align="left"}

Como ha iniciado el Editor web sin seleccionar ningún archivo, se muestra una pantalla de Editor web en blanco. Puede abrir un archivo para editarlo desde AEM repositorio o desde la colección Favoritos.

## Interfaz de usuario de AEM Assets {#id2056BG0307U}

Otra ubicación desde la que puede iniciar el Editor web es desde la interfaz de usuario de AEM Assets. Puede seleccionar uno o más temas y abrirlos directamente en el Editor web. Para abrir un tema en el Editor web, siga estos pasos:

1. En la interfaz de usuario de Assets, vaya al tema que desee editar.

   >[!NOTE]
   >
   > También puede ver el UUID del tema.

   .

   ![](images/assets_ui_with_uuid_cs.png){width="800" align="left"}

   >[!IMPORTANT]
   >
   > Asegúrese de que tiene los permisos de lectura y escritura en la carpeta que contiene el tema que desea editar.

1. Para obtener un bloqueo exclusivo sobre el tema, seleccione el tema y haga clic en **Comprobar**.

   >[!IMPORTANT]
   >
   > Si el administrador ha configurado la variable **Deshabilitar edición sin cierre de compra** , debe desproteger el archivo antes de editarlo. Si no cierra la compra del archivo, no podrá ver la opción de edición.

1. Cierre el modo de selección de recursos y haga clic en el tema que desee editar.

   Se muestra la vista previa del tema.

   Puede abrir el Editor web desde la vista de lista, la vista de tarjeta y el modo de vista previa.

   >[!IMPORTANT]
   >
   > Si desea abrir varios temas para editarlos, seleccione los temas deseados en la interfaz de usuario de Asset y haga clic en Editar. Asegúrese de que el explorador no tenga el bloqueador de ventanas emergentes habilitado, de lo contrario solo se abrirá el primer tema de la lista seleccionada para su edición.

   ![](images/edit-from-preview_cs.png){width="800" align="left"}

   Si no desea obtener una vista previa de un tema y desea abrirlo directamente en el Editor web, haga clic en el icono Editar del menú de acción rápida desde la vista de tarjeta:

   ![](images/edit-topic-from-quick-action_cs.png){width="800" align="left"}

1. Haga clic en **Editar** para abrir el tema en el Editor web.

   ![](images/edit-mode.png){width="800" align="left"}


## Consola de asignación DITA {#id2056BG090BF}

Para abrir el Editor web desde la consola de asignación DITA, siga estos pasos:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación DITA que contiene el tema que desea editar y haga clic en él.

   Se muestra la consola de asignación DITA.

1. Haga clic en **Temas**.

   Se muestra una lista de temas en el archivo de asignación. El UUID de los temas se muestra debajo del título del tema.

1. Seleccione el archivo de tema que desea editar.

1. Haga clic en **Editar tema**.

   ![](images/edit-topics-map-console_cs.png){width="800" align="left"}

1. El tema se abre en el Editor web.

   >[!IMPORTANT]
   >
   > Si el administrador ha configurado la variable **Deshabilitar edición sin cierre de compra** , debe desproteger el archivo antes de editarlo. Si no extrae el archivo, el documento se abrirá en el editor en modo de solo lectura.


**Tema principal:**[ Trabajar con el Editor web](web-editor.md)

