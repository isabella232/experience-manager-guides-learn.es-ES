---
title: Iniciar el editor web
description: Obtenga información sobre cómo iniciar el editor web
exl-id: f02f9612-7aaa-42ea-bad3-c44d23b5d034
source-git-commit: 8073716bccacbe8d6a158b44d5106b083e3a5dcd
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# Iniciar el editor web {#id2056B0140HS}

Puede iniciar el Editor Web desde las ubicaciones siguientes:

- [AEM Página de navegación de](#id2056BG00RZJ)
- [IU de AEM Assets](#id2056BG0307U)
- [Consola de mapa DITA](#id2056BG090BF)

En las secciones siguientes se describen los detalles de cómo puede tener acceso al Editor Web y cómo puede iniciarlo desde varias ubicaciones.

## AEM Página de navegación de {#id2056BG00RZJ}

AEM Al iniciar sesión en la sesión de, se le mostrará la página Navegación:

![](images/web-editor-from-navigation-page_cs.png){width="800" align="left"}

Haciendo clic en **Editor XML** Este vínculo le lleva directamente al Editor web.

![](images/web-editor-launch-page.png){width="800" align="left"}

Cuando haya iniciado el Editor Web sin seleccionar ningún archivo, aparecerá una pantalla en blanco. AEM Puede abrir un archivo para editarlo desde el repositorio o desde la colección de Favoritos de la aplicación.

## IU de AEM Assets {#id2056BG0307U}

Otra ubicación desde la que puede iniciar el Editor web es desde la interfaz de usuario de AEM Assets. Puede seleccionar uno o varios temas y abrirlos directamente en el Editor web. Para abrir un tema en el Editor Web, siga estos pasos:

1. En la interfaz de usuario de Assets, vaya al tema que desee editar.

   >[!NOTE]
   >
   > También puede ver el UUID del tema.

   .

   ![](images/assets_ui_with_uuid_cs.png){width="800" align="left"}

   >[!IMPORTANT]
   >
   > Asegúrese de tener los permisos de lectura y escritura en la carpeta que contiene el tema que desea editar.

1. Para obtener un bloqueo exclusivo sobre el tema, seleccione el tema y haga clic en **Desproteger**.

   >[!IMPORTANT]
   >
   > Si el administrador ha configurado la variable **Desactivar la edición sin cierre de compra** , debe retirar el archivo antes de editar. Si no desprotege el archivo, no podrá ver la opción de edición.

1. Cierre el modo de selección de recursos y haga clic en el tema que desee editar.

   Se muestra la vista previa del tema.

   Puede abrir el editor web desde la vista de lista, la vista de tarjeta y el modo de vista previa.

   >[!IMPORTANT]
   >
   > Si desea abrir varios temas para editarlos, seleccione los temas que desee en la interfaz de usuario de recursos y haga clic en Editar. Asegúrese de que el explorador no tenga habilitado el bloqueador de ventanas emergentes; de lo contrario, solo se abrirá el primer tema de la lista seleccionada para editarlo.

   ![](images/edit-from-preview_cs.png){width="800" align="left"}

   Si no desea obtener una vista previa de un tema y desea abrirlo directamente en el Editor Web, haga clic en el icono Editar del menú de acción rápida desde la vista de tarjeta:

   ![](images/edit-topic-from-quick-action_cs.png){width="800" align="left"}

1. Clic **Editar** para abrir el tema en el Editor Web.

   ![](images/edit-mode.png){width="800" align="left"}


## Consola de mapa DITA {#id2056BG090BF}

Para abrir el Editor Web desde la consola de mapas DITA, siga estos pasos:

1. En la interfaz de usuario de Assets, vaya al fichero de mapa DITA que contiene el tema que se debe editar y haga clic en él.

   Se muestra la consola de mapas DITA.

1. Clic **Temas**.

   Se muestra una lista de temas en el fichero de asignación. El UUID de los temas se muestra debajo del título del tema.

1. Seleccione el archivo de tema que desee editar.

1. Clic **Editar tema**.

   ![](images/edit-topics-map-console_cs.png){width="800" align="left"}

1. El tema se abre en el Editor Web.

   >[!IMPORTANT]
   >
   > Si el administrador ha configurado la variable **Desactivar la edición sin cierre de compra** , debe retirar el archivo antes de editar. Si no desprotege el archivo, el documento se abrirá en el editor en modo de solo lectura.


**Tema principal:**[ Trabajar con el editor web](web-editor.md)
