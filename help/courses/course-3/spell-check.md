---
title: Corrección ortográfica y buscar/reemplazar
description: AEM Uso de la revisión ortográfica y de buscar/reemplazar en las guías de la
exl-id: 5f39618d-a919-4d3c-a4de-2896f2d1bf20
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 1%

---

# Corrección ortográfica y Buscar/reemplazar

AEM El Editor de guías de la tiene potentes funciones de revisión ortográfica y Buscar y reemplazar.

>[!VIDEO](https://video.tv.adobe.com/v/342768?quality=12&learn=on)

Corregir un error ortográfico

1. Busque un error en un tema abierto, que se muestra con un subrayado rojo.

1. Mantenga pulsado Ctrl + clic en el botón secundario del ratón dentro de la palabra.

1. Elija la ortografía correcta entre las sugerencias.

Si no se sugiere la ortografía correcta, siempre puede editar la palabra manualmente.

## AEM Cambiar a comprobación de ortografía de

Es posible que desee utilizar una herramienta de revisión ortográfica que no sea el diccionario predeterminado del explorador.

1. Vaya a **Configuración del editor**.

1. Seleccione el **General** pestaña configuración.

   ![Configuración de revisión ortográfica](images/lesson-11/configure-dictionary.png)

1. Hay dos opciones:

   - **Corrección ortográfica del explorador** — la configuración predeterminada en la que la revisión ortográfica utiliza el diccionario integrado del explorador.

   - **AEM Corrección ortográfica de** AEM — utilice esta opción para crear una lista de palabras personalizada utilizando el diccionario personalizado de la aplicación de la aplicación de la aplicación.

1. Elegir **AEM Corrección ortográfica de**.

1. Haga clic en [!UICONTROL **Guardar**].

Configurar un diccionario personalizado

AEM El administrador puede cambiar la configuración para que el diccionario de la aplicación reconozca palabras personalizadas, como nombres de empresas.

1. Vaya a **Herramientas** panel.

1. Iniciar sesión en **CRXDE Lite**.

   ![AEM Icono de CRXDE Lite de IU](images/lesson-11/crxde-lite.png)

1. Vaya a **_nodo /apps/fmdita/config_**.

   ![Nodo de configuración del CRXDE Lite](images/lesson-11/config-node.png)

1. Cree un nuevo archivo.

   a. Haga clic con el botón derecho en la carpeta de configuración.

   b. Elegir **Crear > Crear archivo**.

   ![Creación de nuevo archivo de diccionario](images/lesson-11/new-dictionary-file.png)

   c. Asigne un nombre al archivo _**user_dictionary.txt**_.

   ![Texto del diccionario del usuario](images/lesson-11/user-dictionary.png)

   d. Haga clic [!UICONTROL **OK**].

1. Abra el archivo.

1. Agregue una lista de palabras que desee incluir en el diccionario personalizado.

1. Haga clic en [!UICONTROL **Guardar todo**].

1. Cierre el archivo.

AEM Es posible que los autores tengan que reiniciar su sesión del Editor Web para obtener la lista de palabras personalizada actualizada en el Diccionario de palabras de la aplicación de la aplicación de la aplicación de la aplicación de código de la aplicación de la aplicación de.

## Buscar y reemplazar en un solo archivo

1. Haga clic en el icono Buscar y reemplazar de la barra de herramientas superior.

   ![Icono Buscar y reemplazar](images/lesson-11/find-replace-icon.png)

1. En la barra de herramientas inferior, escriba una palabra o frase.

1. Clic [!UICONTROL **Buscar**].

1. Si es necesario, escriba una palabra para reemplazar la palabra encontrada.

1. Clic [!UICONTROL **Reemplazar**].

## Buscar y reemplazar en todo el repositorio

1. Vaya a **Repositorio**.

1. Haga clic en [!UICONTROL **Buscar y reemplazar**] en la parte inferior izquierda de la pantalla.

1. Haga clic en [!UICONTROL **Mostrar configuración**] icono.

1. Elija una de estas opciones

   - **Archivo de retirada antes de reemplazar** — si lo activa un administrador, el fichero se extraerá automáticamente antes de sustituir los términos de búsqueda.

   - **Solo palabra completa** — restringe la búsqueda para que sólo devuelva la palabra o frase exacta introducida.

   ![Buscar y reemplazar en el repositorio](images/lesson-11/repository-find-replace.png)

1. Haga clic en [!UICONTROL **Aplicar filtro**] para seleccionar la ruta del repositorio en la que desea realizar la búsqueda.

1. Introduzca los términos que desea buscar y reemplazar.

1. Si es necesario, seleccione **Crear nueva versión tras reemplazar**.

1. Clic [!UICONTROL **Buscar**].

1. Abra el archivo deseado y utilice las flechas para desplazarse de un resultado encontrado al siguiente.

   ![Buscar IU de navegación de reemplazo](images/lesson-11/find-replace-navigation.png)
