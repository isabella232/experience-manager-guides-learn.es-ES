---
title: Crear ajustes preestablecidos de salida desde el Editor web
description: Obtenga información sobre cómo crear ajustes preestablecidos de salida desde el Editor web
exl-id: 7fde0057-06a5-428e-a91b-9e9386a56270
source-git-commit: 3bca42f0954afc2362ab24f369e698113324dbc3
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Crear ajustes preestablecidos de salida desde el Editor web {#id218CL400JW3}

Realice los siguientes pasos para crear ajustes preestablecidos de salida para su mapa DITA:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación que desea editar.

1. Para obtener un bloqueo exclusivo en el archivo de mapa, seleccione el archivo de mapa y haga clic en **Comprobar**.

1. Seleccione el **Editar temas** en el menú de acción del archivo de asignación.

   El archivo de mapa se abre para su edición en el Editor web.

   >[!NOTE]
   >
   > Puede agregar o eliminar cualquier tema del mapa con el Editor de mapas avanzado. Para obtener más información, consulte [Trabajar con el editor de mapas avanzado](map-editor-advanced-map-editor.md#).

1. En el **Salida** , seleccione el icono + para crear un ajuste preestablecido de salida para su mapa DITA.

   ![](images/output-tab-preset_cs.png){width="350" align="left"}

1. Introduzca el nombre del ajuste preestablecido en el cuadro de diálogo Agregar ajuste preestablecido y haga clic en **Agregar**.

1. Introduzca los siguientes detalles de configuración.

   1. Seleccione las opciones necesarias en la **General** pestaña . Puede elegir crear un ajuste preestablecido de salida con o sin condiciones. También puede utilizar un archivo DITVAL. AEM guías también le permite seleccionar una línea de base para publicar una versión específica del mapa DITA.
   1. Introduzca los detalles del sitio AEM en la **AEM** pestaña . **Sitio** muestra la lista de AEM Sites disponible en el repositorio de AEM. **Categoría**, **Plantilla de sección** y **Plantilla de artículo** son los componentes estructurales utilizados para organizar el aspecto de su salida. Se predefinen en la plantilla Sitio AEM.

      >[!NOTE]
      >
      > Actualice cada menú desplegable para obtener más clasificación en la siguiente lista desplegable.

   1. En el **Artículos** , seleccione los temas para los que desea generar el resultado.
1. Seleccione el **Generar ajuste preestablecido** en la parte superior para generar la salida.

   ![](images/add-preset-articles-tab_cs.png){width="800" align="left"}

1. Verá el estado del proceso de generación de salida. La variable **Temas** lista los temas para los que se genera el resultado mientras se usa la variable **Estado** muestra el estado de publicación de cada tema.

   Para ver el resultado, pase el puntero del ratón sobre el tema y haga clic en Ver salida.

   ![](images/add-preset-output-generated_cs.png){width="800" align="left"}


>[!NOTE]
>
> También puede editar, cambiar el nombre, duplicar o eliminar un ajuste preestablecido de salida existente desde el menú Opciones.

![](images/edit-preset_cs.png){width="550" align="left"}

**Tema principal:**[ Publicación basada en artículos desde el Editor web](web-editor-article-publishing.md)
