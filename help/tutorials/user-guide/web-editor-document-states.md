---
title: Estado del documento
description: Aprenda a documentar el estado
source-git-commit: 13106cd1c7f6d38fecb67dd93eef66263eb29bae
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 0%

---


# Estado del documento {#id1821HC00URO}

Para administrar la preparación de los documentos, AEM guías proporciona la propiedad de estado del documento para indicar el estado actual del documento. Los estados de documento ayudan a averiguar rápidamente si un documento es nuevo, está en revisión o si está completado.

## Tipos de estados de documento

Un documento puede tener cualquiera de los estados de documento definidos en el perfil Estado del documento. Por ejemplo, un documento puede tener cualquiera de los siguientes Estados de documento:

- Borrador : indica que el documento se crea y se guarda con cambios nuevos.
- Revisión en curso : indica que se ha iniciado un flujo de trabajo de revisión para el documento.
- Revisado : indica que el documento ha sido revisado por los usuarios deseados.

Estos estados se establecen de forma manual o automática según la configuración de perfil Estados del documento. Por ejemplo, si el perfil de estado del documento está configurado con el estado de inicio como borrador y el estado de revisión está definido para los documentos en revisión. A continuación, al crear un documento, el estado del documento se establece en *Borrador*. Si inicia una tarea de revisión, el estado del documento cambia a En revisión.

También puede cambiar manualmente el estado del documento para uno o varios documentos. Sin embargo, si elige cambiar el estado del documento para varios documentos, el estado permitido viene determinado por los estados comunes permitidos para los documentos seleccionados. Por ejemplo, supongamos que ha definido los estados del documento como Borrador, En revisión, Revisado y Listo para publicar, en el mismo orden. En el documento uno.dita, el estado se establece en *Borrador* y en el documento two.dita, el estado se establece en Revisado. Cuando selecciona ambos (one.dita y two.dita), el estado del documento permitido será *Listo para publicación*. Como two.dita está en *Revisado* state, el siguiente estado posible para two.dita es solamente *Listo para publicación*, que se muestra cuando se seleccionan ambos documentos.

>[!NOTE]
>
> Un documento puede existir en un solo estado a la vez.

## Cambiar el estado del documento

Para cambiar el estado de un documento, realice los siguientes pasos:

1. En la interfaz de usuario de Assets, seleccione uno o varios documentos para los que desea cambiar el estado del documento.
1. En la barra de herramientas principal, haga clic en **Propiedades**.
1. Seleccione el nuevo estado en el **Estado del documento** lista desplegable. Puede seleccionar solo los estados de documento permitidos en la sección Transición de estado del perfil Estado del documento.

   >[!NOTE]
   >
   >Los administradores pueden ver todos los estados de documento y cambiar el documento a cualquier estado posible.

1. Haga clic en **Guardar y cerrar**.

## Ver estado del documento

La vista de tarjeta de la interfaz de usuario de Assets muestra el estado actual junto con la fecha de creación y el tamaño del tema DITA o mapa DITA correspondiente.

![](images/document_state.png){width="800" align="left"}

## Usar estados de documento en DLC

Los estados de documentos desempeñan un papel importante en la administración del ciclo de vida de los documentos en DLC. Si su organización sigue estrictamente el DLC, entonces tener un mecanismo para controlar la edición de documentos basado en su estado se convierte en una característica esencial. Por ejemplo, puede permitir la edición de documentos cuando se encuentren en *Borrador* o *Revisión* estados. Sin embargo, una vez que un documento se revisa y está listo para publicarse, debería haber una manera de evitar una modificación ulterior de los documentos.

AEM guías proporciona un flujo de trabajo de aprobación de documentos que le ayuda a controlar el ciclo de vida del proceso de desarrollo de documentos. Una vez que un documento está listo para publicarse o ha alcanzado el penúltimo estado, puede marcarlo como aprobado. Una vez aprobado un documento, AEM guías crea una nueva versión del documento y lo convierte en solo lectura. A continuación, puede mover el documento para publicarlo o crear una línea de base para un procesamiento posterior.

Para iniciar una nueva versión desde los documentos marcados como aprobados, un autor debe iniciar una nueva versión. Al iniciar una nueva versión, se cambia el estado del documento a *Borrador* de nuevo. Cambiando el estado del documento a *Borrador*, el documento vuelve a ser editable y puede continuar trabajando en la siguiente versión.

Para utilizar la función de aprobación de documentos, realice los pasos siguientes:

>[!NOTE]
>
> El administrador debe activar la función de flujo de trabajo de aprobación. Para obtener más información, consulte *Habilitar flujo de trabajo de aprobación* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.

1. En el Editor web, abra el documento que desea marcar para su aprobación.

1. Haga clic en el **Marca aprobada**![](images/mark_approve_icon.svg) icono.

1. Si el documento se encuentra en el estado que se va a marcar como aprobado, aparecerá el siguiente cuadro de diálogo:

   ![](images/mark-approved-correct-state.png){width="550" align="left"}

   Si el documento no se puede marcar como aprobado, se muestra el siguiente mensaje:

   ![](images/mark-approved-incorrect-state.png){width="550" align="left"}

1. Si el documento está listo para ser marcado como aprobado, seleccione una etiqueta en la lista desplegable y haga clic en **Aprobar**.

   >[!NOTE]
   >
   > Si el administrador no ha configurado una lista predefinida de etiquetas, se le mostrará un campo de texto de forma libre para introducir una etiqueta.

1. Una vez que el documento se ha marcado correctamente como aprobado, se envía una **Vista previa** del documento se muestra en modo de solo lectura.

   ![](images/approved-doc-read-only.png){width="650" align="left"}

   >[!NOTE]
   >
   > En el modo de vista previa, todas las opciones de edición se eliminan de la barra de herramientas. Además, la vista Autor y Origen del documento también se ha eliminado de la barra de navegación superior.


Una vez que un documento está marcado como aprobado, ya no está disponible para edición. Si desea utilizar el documento para la próxima versión, debe volver a colocarlo en la variable *Borrador* estado. Para volver a cambiar el estado del documento de un documento aprobado a *Borrador* realice los siguientes pasos:

1. En un documento aprobado, haga clic en el botón **Iniciar una nueva versión** Icono ![](images/approved-restart-draft-mode-icon.svg).

   Aparece el mensaje Iniciar nueva versión .

1. Haga clic en **Confirmar**.

   El estado del documento se cambia a Borrador y el documento se abre en el Editor web en el modo de edición.


**Tema principal:**[ Trabajar con el Editor web](web-editor.md)

