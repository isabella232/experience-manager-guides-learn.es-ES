---
title: Prácticas recomendadas para la traducción de contenido
description: Conozca las prácticas recomendadas para la traducción de contenido
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 1%

---


# Prácticas recomendadas para la traducción de contenido {#id1678G0S702F}

Considere el siguiente punto para traducir contenido:

- Los nombres de carpeta y archivo deben cumplir con los estándares de nomenclatura de archivos como: no debe haber espacios, apóstrofo, llaves, signo igual, caracteres especiales o no ASCII.

- Si traduce contenido en diferentes idiomas, debe crear carpetas que correspondan a cada idioma. Cada una de estas carpetas de idioma contendrá el contenido correspondiente a ese idioma. Por ejemplo, puede crear carpetas utilizando el indicador de idioma como `de` para alemán, `fr` para francés, etc. O bien, puede crear carpetas utilizando los designadores de idioma y región como `fr-FR` para el francés utilizado en Francia o `fr-CA` para francés como se usa en Canadá.
- El idioma de destino también debe tener seleccionadas las configuraciones regionales reales según las carpetas de idioma de destino en su instancia.
- La configuración de nube debe ser la misma que la de la carpeta de origen y solo debe haber una configuración de nube en una carpeta. Puede crear varias carpetas en /conf, si desea utilizar varios conectores de traducción.
- Una carpeta no debe contener más de 1000 archivos.
- Asegúrese de que el usuario al que se haya encomendado iniciar el proceso de traducción tenga permisos de lectura, modificación, creación y eliminación en las carpetas de idioma de origen y destino.
- Como la traducción de contenido requiere la creación de un proyecto de traducción, el usuario debe tener acceso para crear el proyecto en AEM.
- Si desea utilizar ajustes preestablecidos condicionales con el mapa, debe crearlos antes de iniciar el proceso de traducción. Como los ajustes preestablecidos condicionales también están empaquetados en la versión traducida del mapa, la creación de los ajustes preestablecidos antes de iniciar el proceso de traducción garantiza que estén disponibles en la versión traducida.
- El proceso de traducción de contenido debe iniciarse desde la consola de asignación DITA y no desde la interfaz de usuario de AEM Assets.
- El flujo de trabajo de traducción DITA basada en componentes no se debe utilizar si traduce contenido mediante traducción humana. Sin embargo, esta opción debe utilizarse para la traducción automática.
- El contenido y los medios utilizados de forma global que no requieren localización deben estar fuera de las copias de idioma.
- Todo el contenido común que debe localizarse debe conservarse en una carpeta común en la carpeta de idioma.

La siguiente ilustración muestra un ejemplo de una estructura de carpetas en AEM cuando ha utilizado contenido globalmente y tres copias de idioma.

![](images/aem-directory_structure.png)

## Configurar el servicio de traducción

Siga estos pasos para configurar el servicio de traducción automática o humana que se va a utilizar:

1. En la interfaz de usuario de Assets, seleccione la carpeta de idioma de origen.

1. Abra las propiedades de la carpeta y vaya a **Cloud Services** pestaña .

1. En el **Cloud Services** , configure el servicio de traducción que desea utilizar.

   Puede configurar la traducción automática o humana.

   Asegúrese de que solo haya una configuración para el conector de traducción en una carpeta. Se pueden crear varias carpetas en /conf, si hay varios conectores de traducción. La carpeta del idioma de origen debe tener una configuración de nube seleccionada antes de iniciar el proceso de traducción.

   >[!NOTE]
   >
   > Consulte [Configuración del marco de integración de traducción](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=en) en AEM documentación para obtener detalles sobre la integración con servicios de traducción de terceros.

1. Haga clic en **Guardar y cerrar** para guardar las propiedades de la carpeta actualizada.


>[!TIP]
>
> Consulte la *Traducción* en la guía de prácticas recomendadas para conocer las prácticas recomendadas relacionadas con la traducción de contenido.

## Crear un nuevo proyecto de traducción

Siga estos pasos para crear un proyecto de traducción:

>[!NOTE]
>
> Antes de realizar los pasos de este procedimiento, asegúrese de que ha creado las carpetas de destino y raíz de idioma necesarias, tal como se describe en la sección [Prácticas recomendadas para la traducción de contenido](#id1678G0S702F).

1. En la interfaz de usuario de Assets, haga clic en el archivo de asignación DITA.

1. Haga clic en el **Traducción** pestaña .

1. En el **Idiomas de destino** , seleccione la configuración regional a la que desea traducir el proyecto y haga clic en **Listo**.

   Se muestra un Resumen y Detalles de los temas y los recursos asociados.

   >[!IMPORTANT]
   >
   > La variable **Idiomas de destino** mostrar solo aquellos idiomas para los que se crea una carpeta de idioma en paralelo al idioma de origen. Tampoco se muestra una carpeta de idioma creada en otro nivel, como un nivel inferior desde la carpeta del idioma de origen. Asegúrese de crear todas las carpetas de idioma de destino en el mismo nivel que la carpeta de idioma de origen.

1. Seleccione los temas que desea enviar para su traducción.

   También puede utilizar las siguientes opciones de filtrado de temas:

   >[!NOTE]
   >
   > Después de aplicar el filtro requerido, haga clic en **Listo** en el panel Filtro para filtrar temas según su selección.

   - **Estado de traducción**: Elija filtrar los temas según su estado de traducción. Las opciones disponibles son: Sin sincronización, sin copia, en curso y en sincronización.
   - **Buscar**: Escriba uno o varios términos para buscar en los títulos de los temas.
   - **Tipo de origen**: Elija filtrar los temas según sus tipos de archivo. Las opciones disponibles son: Todos, DITA, Mapa DITA, Recurso.
   - **Versión de origen modificada después de**: Elija filtrar el tema en función de su fecha y hora de modificación. Todos los temas modificados después de la fecha y hora especificadas se muestran en la lista.
   - **Línea de base**: Haga clic en Usar línea de base y seleccione una línea de base creada en el mapa. Todos los archivos que forman parte de la Línea de base seleccionada se muestran en la página Traducción . Puede elegir los archivos deseados desde la línea de base y continuar con el proceso de traducción. Una vez traducido el contenido, puede exportar la línea de base traducida. Para obtener más información sobre la exportación de la línea de base traducida, consulte [Exportar línea de base traducida](generate-output-use-baseline-for-publishing.md#id196SE600GHS).
1. Haga clic en **Crear/actualizar copias de idioma** en la parte inferior del panel Filtro.

1. En el **Proyecto** lista, seleccionar **Crear un nuevo proyecto de traducción**.

   >[!NOTE]
   >
   > Si ya tiene un proyecto de traducción, puede agregar temas a ese proyecto. Select **Agregar a proyecto de traducción existente** de la **Proyecto** y elija un proyecto de la lista **Proyecto de traducción existente** lista.

1. En el campo **Título del proyecto**, introduzca un título.

1. Seleccione el **Incluir mapa DITA** para enviar el mapa para su traducción.
1. Haga clic en **Inicio** para crear un nuevo proyecto de traducción.

   Se crea un nuevo proyecto de traducción con la versión seleccionada de los temas. En este momento, se muestra un mensaje emergente que confirma la creación del proyecto de traducción. Una vez que todas las copias de idioma de destino estén disponibles en el proyecto de traducción, se obtiene una notificación en la Bandeja de entrada. Una vez que el área de copia del idioma de destino está disponible en el proyecto de traducción, puede continuar e iniciar el trabajo de traducción.


## Iniciar el trabajo de traducción {#id225IK030OE8}

Realice los siguientes pasos para iniciar el trabajo de traducción:

1. En el **Proyectos** , vaya a la carpeta del proyecto que ha creado para la localización.

1. Haga clic en el proyecto de localización para abrir la página de detalles.

1. Haga clic en la flecha de la **Trabajo de traducción** mosaico y seleccione **Inicio** de la lista para iniciar el flujo de trabajo de traducción.

   >[!NOTE]
   >
   > Si utiliza el servicio de traducción humana, debe exportar el contenido para su traducción. Una vez que tenga el contenido traducido, debe importarlo de nuevo en el proyecto de traducción.

1. Para ver el estado del trabajo de traducción, haga clic en los puntos suspensivos en la parte inferior del **Trabajo de traducción** mosaico.


Una vez finalizada la traducción, el estado del trabajo de traducción cambia a *Listo para revisión*. Para completar el proceso de traducción, debe aceptar la copia traducida y los metadatos de recurso del mosaico Trabajo de traducción en la consola Proyecto .

>[!NOTE]
>
> Si rechaza la traducción para uno o más temas de un trabajo de traducción, la variable **En curso** el estado de traducción de todos los temas rechazados vuelve a su estado original. El estado de los temas referidos se comprueba y se revierte según el estado de traducción más reciente. Además, los archivos de traducción creados en el proyecto de destino no se eliminan aunque la traducción se rechace para ellos.

**Tema principal:**[ Traducir contenido](translation.md)

