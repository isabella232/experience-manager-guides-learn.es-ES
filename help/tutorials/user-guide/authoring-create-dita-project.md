---
title: Creación de un proyecto DITA
description: Obtenga información sobre cómo crear un proyecto DITA
source-git-commit: 101766d51d43eb728f0316155acffd19548f83be
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---


# Creación de un proyecto DITA {#id1645HA00NM6}

AEM guías proporciona una plantilla de proyecto DITA que puede utilizar para crear y administrar sus tareas de revisión.

Puede crear un proyecto DITA y luego utilizarlo para iniciar sus revisiones. Un proyecto permite definir una fecha límite y controlar las tareas y el tiempo necesario para completar la tarea de revisión para la que ha creado el proyecto.

Puede agregar integrantes del equipo a un proyecto al que se les puedan asignar varias funciones: Autores, Revisores y Editores.

Una vez creado el proyecto DITA, puede iniciar la revisión desde el Editor web o la interfaz de usuario de Assets. Para obtener más información, consulte [Enviar temas para revisión](review-send-topics-for-review.md#).

Del mismo modo, cada vez que un autor inicia un flujo de trabajo de revisión, los miembros seleccionados del proyecto reciben una notificación por correo electrónico. Para configurar las notificaciones por correo electrónico, consulte *Personalización de las plantillas de correo electrónico* en Instalar y configurar las guías de Adobe Experience Manager as a Cloud Service.

Realice los siguientes pasos para crear un proyecto DITA:

1. Abra la consola Proyectos .

   También puede acceder a la consola Proyectos mediante la siguiente URL:

   ```http
   http://<server name>:<port>/projects.html
   ```

1. Haga clic en **Crear** \> **Proyecto** para iniciar el asistente Crear proyecto .

   ![](images/project-console-63.png)

1. En la página Crear proyecto , seleccione la opción **Proyecto DITA** plantilla y haga clic en **Siguiente**.

1. En la página Propiedades del proyecto , introduzca los siguientes detalles:

   La información de **Básico** pestaña:

   ![](images/create-project.png)

   - Introduzca el **Título**, **Descripción** y **Fecha de vencimiento**.

   - Opcionalmente, puede elegir una miniatura para el proyecto.

   - De forma predeterminada, se le hace propietario del proyecto. Para agregar más usuarios a este proyecto:
   1. Escriba o elija un usuario de la **Usuario** lista desplegable.

   1. Elija un tipo de usuario: autores, revisores o editores.

      >[!NOTE]
      >
      >Verá otros tipos de usuarios en esta lista desplegable, pero para un proyecto DITA solo debe elegir entre el tipo de usuario Autores, Revisores o Editores. Incluso si agrega un usuario de un tipo diferente, ese usuario no podrá acceder a ninguna función específica de DITA disponible en AEM guías.

   1. Haga clic en **Agregar**.

      >[!NOTE]
      >
      >Si utiliza AEM guías de la versión 3.5 o anterior, se le mostrará la opción de seleccionar un archivo de asignación DITA para resolver referencias clave para editar temas, previsualizar y revisar flujos de trabajo. En las versiones 3.6 y posteriores, puede configurar el mapa raíz mediante el Editor web. Para obtener más información, consulte la [Preferencias de usuario](web-editor-features.md#id2087G0P40SB) en el Editor web. Otra forma de configurar el mapa raíz es configurarlo en los perfiles globales o a nivel de carpeta. Para obtener más información, consulte *Configuración de perfiles globales o de nivel de carpeta* en la Guía de instalación y configuración.
   La información de **Avanzadas** pestaña:

   - Introduzca un nombre para el proyecto. Este nombre se utiliza para crear la URL para este proyecto.



1. Haga clic en **Crear**.

   Aparecerá el cuadro de diálogo Proyecto creado.

1. Haga clic en **Apertura** para abrir la página del proyecto.


**Tema principal:**[ Revisión de temas o mapas](review.md)

