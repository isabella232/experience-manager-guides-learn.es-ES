---
title: Crear temas
description: Descubra cómo crear temas
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---


# Crear temas {#id2056AL00O5Z}

AEM guías le permite crear temas DITA de tipo: tema, tarea, concepto, referencia, glosario, DITAVAL, etc. Además de crear temas basados en las plantillas integradas, también puede definir las plantillas personalizadas. Para obtener más información sobre el uso de las plantillas DITA personalizadas, consulte *Configuración de plantillas y etiquetas para la creación* en Instalar y configurar las guías de Adobe Experience Manager as a Cloud Service.

Siga estos pasos para crear un tema:

1. En la interfaz de usuario de Assets, vaya a la ubicación en la que desee crear el tema.

1. Para crear un tema nuevo, haga clic en **Crear** \> **Tema DITA**.

1. En la página Modelo, seleccione el tipo de documento DITA que desea crear y haga clic en **Siguiente**.

   ![](images/create_dita_topic.png){width="800" align="left"}

   De forma predeterminada, AEM guías proporciona las plantillas de temas DITA más utilizadas. Puede configurar más plantillas de temas según sus necesidades organizativas; consulte *Configuración de plantillas y etiquetas para la creación* en Instalar y configurar las guías de Adobe Experience Manager as a Cloud Service.

   >[!NOTE]
   >
   > En la vista de lista de la interfaz de usuario de Assets, el tipo de tema DITA se muestra en la columna Tipo como Tema, Tarea, Concepto, Referencia, Glossentry o DITAVAL. El mapa DITA se muestra como Mapa.

1. En la página Propiedades, especifique el documento **Título**.

1. \(Opcional\) Especifique el archivo **Nombre**.

   Si el administrador ha configurado el nombre de archivo automático en función de la configuración de UUID, no verá la opción para especificar el nombre de archivo. Se asigna automáticamente al archivo un nombre de archivo basado en UUID.

   Si la opción de nomenclatura del archivo está disponible, también se sugiere automáticamente el nombre en función de la variable **Título** del documento. Si desea especificar manualmente el nombre del documento, asegúrese de que la variable **Nombre** no contiene espacios, apóstrofo o llaves y termina con .xml o .dita. De forma predeterminada, las guías de AEM reemplazan todos los caracteres especiales por guiones. Consulte la sección Nombres de archivo en la guía Prácticas recomendadas para conocer las prácticas recomendadas relacionadas con la asignación de nombres a archivos DITA.

1. Haga clic en **Crear**. Aparecerá el mensaje Tema creado.

   Puede elegir abrir el tema para editarlo en el Editor web o guardar el archivo de tema en el repositorio de AEM.

   Cada tema nuevo que cree desde la interfaz de usuario de Assets **Crear** \> **Tema DITA** o al Editor web se le asigna un ID de tema único. El valor de este ID es el nombre de archivo en sí. Además, se guarda un nuevo documento como la última copia de trabajo del tema en DAM. Hasta que no guarde una revisión de un tema recién creado, no verá ningún número de versión en el Historial de versiones. Si abre el tema para editarlo, la información de la versión se muestra en la esquina superior derecha de la pestaña del archivo del tema:

   ![](images/topic-version-none_cs.png){width="550" align="left"}

   La información de la versión de un tema recién creado se muestra como *ninguno*. Cuando guarda una nueva versión, se le asigna un número de versión 1.0. Para obtener más información sobre cómo guardar una nueva versión, consulte [Guardar como nueva versión](web-editor-features.md#save-as-new-version-id209ME400GXA).


>[!NOTE]
>
> Si el administrador ha configurado el Editor web para extraer archivos antes de editarlos, no podrá editar un archivo hasta que lo desproteja. Del mismo modo, si está configurado, se le pedirá que proteja cualquier archivo desprotegido antes de cerrarlo.

>[!IMPORTANT]
>
> Una vez creado el tema DITA, guarde los cambios en su copia de trabajo y cree una nueva versión una vez que haya completado las actualizaciones del tema.

**Tema principal:**[ Crear y previsualizar temas](create-preview-topics.md)

