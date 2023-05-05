---
title: Creación de un mapa
description: Obtenga información sobre cómo crear un mapa
exl-id: d35ee09f-f951-4866-a2b1-e4b19f76e7a1
source-git-commit: 3bca42f0954afc2362ab24f369e698113324dbc3
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Creación de un mapa {#id176FEN0D05Z}

AEM guías proporciona dos plantillas de asignación predeterminadas: Mapa DITA y Bookmap. También puede crear sus propias plantillas de asignación y compartirlas con sus autores para crear archivos de asignación.

Siga estos pasos para crear un archivo de asignación:

1. En la interfaz de usuario de Assets, vaya a la ubicación en la que desea crear el archivo de asignación.

1. Haga clic en **Crear** \> **Mapa DITA**.

1. En la página Modelo, seleccione el tipo de plantillas de mapa que desee utilizar y haga clic en **Siguiente**.

   >[!NOTE]
   >
   > La forma en que se hace referencia a los temas en un archivo de mapa depende de la plantilla de mapa. Por ejemplo, si selecciona la plantilla Mapa, el tema hace referencia a \(`topicref`\) se utilizan para hacer referencia a temas. En el caso de un Bookmap, las referencias de temas se crean utilizando la variable `chapter` en DITA.

   ![](images/map-template.png){width="650" align="left"}

1. En la página Propiedades, especifique el mapa **Título**.

1. \(Opcional\) Especifique el archivo **Nombre**.

   Si el administrador ha configurado el nombre de archivo automático en función de la configuración de UUID, no verá la opción para especificar el nombre de archivo. Se asigna automáticamente al archivo un nombre de archivo basado en UUID.

   Si la opción de asignación de nombres de archivos está disponible, también se sugiere automáticamente el nombre en función del Título del mapa. Si desea especificar manualmente el nombre del archivo de asignación, asegúrese de que el nombre del archivo no contenga espacios, apóstrofo o llaves y termine con `.ditamap`.

1. Haga clic en **Crear**.

   Aparecerá el mensaje Mapa creado.

   Cada nuevo archivo de asignación que cree desde la interfaz de usuario de Assets **Crear** \> **Mapa DITA** o al Editor web se le asigna un ID de asignación único. Además, el nuevo mapa se guarda como la última copia de trabajo en DAM. Hasta que no guarde una revisión de un mapa recién creado, no verá ningún número de versión en el Historial de versiones. Si abre el mapa para editarlo, la información de la versión se muestra en la esquina superior derecha de la pestaña del archivo de mapa:

   ![](images/first-version-map-none.png){width="650" align="left"}

   La información de la versión de un mapa recién creado se muestra como *ninguno*. Cuando guarda una nueva versión, se le asigna un número de versión 1.0. Para obtener más información sobre cómo guardar una nueva versión, consulte [Guardar como nueva versión](web-editor-features.md#save-as-new-version-id209ME400GXA).

   Puede elegir abrir el mapa para editarlo en el editor de mapas configurado o guardar el archivo de mapa en el repositorio de AEM.

   >[!NOTE]
   >
   > Para usar el Editor de mapas avanzado, acceda al archivo de mapa en el Editor web. Si el administrador ha configurado el Editor de mapas avanzado como editor predeterminado en los archivos de mapa, el archivo de mapa se abre directamente en el Editor de mapas avanzado para su edición. Consulte *Establecer el Editor de mapas avanzado como predeterminado* en Instalar y configurar las guías de Adobe Experience Manager as a Cloud Service.


**Tema principal:**[ Trabajar con el Editor de mapas](map-editor.md)
