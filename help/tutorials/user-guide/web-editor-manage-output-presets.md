---
title: Administrar ajustes preestablecidos de salida de Perfil de carpetas y global
description: Obtenga información sobre cómo administrar los ajustes preestablecidos de salida de Perfil de carpetas y global
source-git-commit: 3b33b27e4acb8d0b185427725e23b8beac0c2a46
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---


# Administrar ajustes preestablecidos de salida de Perfil de carpetas y global {#id22BLJ0D0V1U}

Los ajustes preestablecidos Perfil global y Perfil de carpeta solo están disponibles para usuarios administrativos de nivel de carpeta.

Como administrador, AEM guías le permite crear y administrar ajustes preestablecidos de salida para los Perfiles globales y de carpeta. A continuación, puede utilizar fácilmente estos ajustes preestablecidos de salida para generar resultados para todos los mapas relacionados con ese perfil global o de carpeta.

Realice los siguientes pasos para crear un ajuste preestablecido de salida para los perfiles global y de carpeta:

1. Seleccione el mapa DITA para el que desea crear un ajuste preestablecido de salida.
1. Seleccione el **Editar temas** de la **Opciones** del archivo de mapa. El archivo de mapa se abre para su edición en el Editor web.
1. En el **Salida** , seleccione el icono + para crear un ajuste preestablecido de salida para su mapa DITA.

   ![](images/add-global-output-preset.png){width="350" align="left"}

1. Introduzca los siguientes detalles en la **Agregar ajuste preestablecido** diálogo:
   - Tipo
   - Nombre
   - Target \(para preajuste de base de conocimiento\)
1. Seleccione el **Añadir a perfil de carpeta** para crear un ajuste preestablecido de salida para el perfil de carpeta relacionado y, a continuación, haga clic en **Agregar**. El ajuste preestablecido se crea y aparece en la sección **Salida** de todos los mapas relacionados. \( ![](images/global-preset-icon.svg)\) indica un ajuste preestablecido de nivel de perfil de carpeta.
1. Introduzca los detalles de configuración.

   >[!NOTE]
   >
   > Estos ajustes preestablecidos agregados al perfil de carpetas son independientes de los mapas, por lo que las configuraciones específicas del mapa no están presentes para estos ajustes preestablecidos.

1. Puede seleccionar el **Generar ajuste preestablecido** en la parte superior para generar el resultado de los mapas relacionados con el ajuste preestablecido de salida creado. Verá el estado del proceso de generación de salida. Para ver el resultado, pase el puntero del ratón sobre el tema y haga clic en **Ver salida**.

>[!NOTE]
>
> AEM guías también proporciona un ajuste preestablecido de salida de PDF listo para usar para generar el resultado de los mapas DITA.

**Otras operaciones del menú Opciones**

También puede realizar las siguientes operaciones en el ajuste preestablecido desde el menú Opciones:

- Seleccione el ajuste preestablecido como ajuste preestablecido de pdf predeterminado. A continuación, el ajuste preestablecido seleccionado se utilizará como ajuste preestablecido predeterminado para generar la salida del PDF mediante la variable **Descargar como PDF** para un mapa.
- **Editar**, **Cambiar nombre**, **Duplicar** o **Eliminar** un ajuste preestablecido de salida existente de la variable **Opciones** para abrir el Navegador.

>[!NOTE]
>
> Cuando se elimina un ajuste preestablecido de salida en Perfiles globales y de carpeta, se reflejará en todos los mapas relacionados y no aparecerá en el **Salida** pestaña .

**Tema principal:**[ Trabajar con el Editor web](web-editor.md)

