---
title: Preferencias de usuario, Configuración del editor y Barras de herramientas del editor
description: AEM Cambiar las preferencias de usuario y la configuración del editor en las guías de la
exl-id: 8cb099e4-d985-4eeb-b1a5-0e372b04d218
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 2%

---

# Preferencias de usuario, Configuración del editor y Barras de herramientas del editor

El editor tiene una interfaz altamente configurable. La combinación de Preferencias de usuario, Configuración del editor y Perfiles de carpeta permite personalizar casi todos los aspectos según el entorno de trabajo específico.

>[!VIDEO](https://video.tv.adobe.com/v/342769?quality=12&learn=on)

## Mostrar u ocultar etiquetas de elementos

Las etiquetas son indicaciones visuales que indican los límites de un elemento. Un límite de elemento marca el principio y el final de un elemento. A continuación, puede utilizar estos límites como una pista visual para colocar el punto de inserción o seleccionar el texto dentro de un límite.

1. Haga clic en [!UICONTROL **Alternar vista de etiquetas**] en la barra de herramientas secundaria.

   ![Alternar etiquetas](images/lesson-2/tags-on-icon.png)

   Las etiquetas aparecen dentro del tema. Con la Vista de etiquetas puede:

   - Seleccione el contenido de un elemento haciendo clic en la etiqueta de apertura o de cierre.

   - Expanda o contraiga las etiquetas haciendo clic en el signo + o - de la etiqueta.

   - Utilice el menú contextual para cortar, copiar o pegar el elemento seleccionado.

   - Arrastre y suelte los elementos seleccionando la etiqueta y soltando el elemento en una ubicación válida.

1. Haga clic en [!UICONTROL **Alternar vista de etiquetas**] para ocultar las etiquetas.

Las etiquetas desaparecen, lo que le permite centrarse en el texto.

## Bloquear recursos cuando estén en uso

Bloquear (o desproteger) un archivo proporciona al usuario acceso de escritura exclusivo sobre el archivo. Cuando el archivo está Desbloqueado (o protegido), los cambios se guardan en la versión actual del archivo.

1. Haga clic en [!UICONTROL **Bloquear**] en la barra de herramientas secundaria.

   ![Cierre de compra](images/lesson-2/checkout-icon.png)

   El archivo se ha desprotegido y aparece un icono de bloqueo junto al nombre del archivo en el Repositorio.

1. Haga clic en [!UICONTROL **Desbloquear**] icono.

   ![Registrar](images/lesson-2/check-in-icon.png)

El Repositorio se actualiza para mostrar que el archivo se ha protegido.

## Insertar caracteres especiales

1. Haga clic en [!UICONTROL **Insertar caracteres especiales**] en la barra de herramientas secundaria.

   ![Especial](images/lesson-2/special-icon.png)

1. En el cuadro de diálogo Insertar carácter especial, escriba el nombre del carácter en la barra de búsqueda.

   También puede usar la lista desplegable Seleccionar categoría para mostrar todos los caracteres de una categoría específica.

1. Seleccione el carácter que desee.

1. Clic [!UICONTROL **Insertar**].

El carácter especial se inserta en el texto.

## Alternar entre los modos Autor, Origen y Vista previa

La barra de herramientas situada en la parte superior derecha de la pantalla le permite cambiar entre vistas.

![Modos](images/lesson-2/modes.png)

- Seleccionar **Autor** para ver la estructura y el contenido mientras trabaja con un tema.

- Seleccionar **Origen** para mostrar el XML subyacente que conforma el tema.

- Seleccionar **Previsualizar** para mostrar cómo se mostrará un tema cuando lo vea un usuario en el explorador.

## Cambiar la temática con Preferencias de usuario

Puede elegir entre los temas Claro u Oscuro para el editor. Con el tema Claro, las barras de herramientas y los paneles utilizan un fondo gris claro. Con el tema Oscuro, las barras de herramientas y los paneles utilizan un fondo negro. En ambas temáticas, el área de edición de contenido aparece con un fondo blanco.

1. Haga clic en [!UICONTROL **Preferencias de usuario**] en la barra de herramientas superior.

   ![Preferencias de usuario](images/reuse/user-prefs-icon.png)

1. En el cuadro de diálogo Preferencias de usuario, haga clic en [!UICONTROL **Tema**] desplegable.

1. Elija entre las opciones disponibles.

   ![Temáticas](images/lesson-2/themes.png)

1. Haga clic en [!UICONTROL **Guardar**].

El editor se actualiza para mostrar la temática que prefiera.

## Actualizar la ruta base con las preferencias del usuario

Puede actualizar la Ruta base para que la Vista del repositorio muestre el contenido desde una ubicación específica en cuanto inicie el Editor. Esto reduce el tiempo para acceder a los archivos de trabajo.

1. Haga clic en [!UICONTROL **Preferencias de usuario**] en la barra de herramientas superior.

   ![Preferencias de usuario](images/reuse/user-prefs-icon.png)

1. En el cuadro de diálogo Preferencias de usuario, haga clic en [!UICONTROL **Carpeta**] junto a la Ruta básica.

   ![Ruta de carpeta base](images/lesson-2/base-path-folder-icon.png)

1. En el cuadro de diálogo Seleccionar ruta, haga clic en la casilla de verificación situada junto a una carpeta específica.

1. Clic [!UICONTROL **Seleccionar**].

La próxima vez que inicie el Editor, el Repositorio mostrará los archivos especificados en la Ruta base.

## Asignar un nuevo perfil de carpeta

El perfil global es un valor predeterminado del sistema. Los administradores pueden crear perfiles de carpeta adicionales para elegir.

1. Haga clic en [!UICONTROL **Preferencias de usuario**] en la barra de herramientas superior.

   ![Preferencias de usuario](images/reuse/user-prefs-icon.png)

1. En el cuadro de diálogo Preferencias de usuario, haga clic en [!UICONTROL **Perfiles de carpeta**] desplegable.

   ![Lista de perfiles](images/lesson-2/folder-profiles-dropdown.png)

1. Elija un perfil entre las opciones disponibles.

1. Haga clic en [!UICONTROL **Guardar**].

Se ha asignado el nuevo perfil de carpeta. Ha cambiado las opciones de la barra de herramientas, los modos de vista y las Condiciones y los fragmentos de código en el panel izquierdo. También puede cambiar el aspecto visual del contenido en el Editor.

## Cambiar el diccionario con Configuración del editor

La configuración del editor está disponible para los usuarios administrativos. Estas preferencias le permiten configurar una serie de ajustes, uno de los cuales es el diccionario que el editor utiliza para la revisión ortográfica.

1. Haga clic en [!UICONTROL **Configuración del editor**] en la barra de herramientas superior.

   ![Configuración del editor](images/lesson-2/editor-settings-icon.png)

1. En el cuadro de diálogo Configuración del editor, haga clic en [!UICONTROL **General**] pestaña.

1. Seleccione el diccionario con el que desea trabajar.

1. Haga clic en [!UICONTROL **Guardar**].

El diccionario se actualiza. AEM Tenga en cuenta que cambiar a la revisión ortográfica de la le permite utilizar una lista de palabras personalizada.

## Mostrar y ocultar paneles con Configuración del editor

Una de las funciones que se pueden personalizar con Configuración del editor son los paneles. Más específicamente, puede seleccionar qué paneles se muestran o se ocultan en el Editor.

1. Haga clic en [!UICONTROL **Configuración del editor**] en la barra de herramientas superior.

   ![Configuración del editor](images/lesson-2/editor-settings-icon.png)

1. En el cuadro de diálogo Configuración del editor, haga clic en [!UICONTROL **Paneles**] pestaña.

1. Cambie los paneles disponibles para Mostrar u Ocultar según sea necesario.

   ![Alternar panel](images/lesson-2/toggle-panels.png)

1. Haga clic en [!UICONTROL **Guardar**].

El panel izquierdo ahora está configurado para mostrar solo los paneles seleccionados como Mostrar.

## Elementos de nombre y etiqueta en la configuración del editor

La lista de elementos permite asignar un nombre a un elemento específico y asignarle una etiqueta más fácil de usar. El nombre del elemento debe ser uno de los elementos DITA. La etiqueta puede ser cualquier cadena.

1. Haga clic en [!UICONTROL **Configuración del editor**] en la barra de herramientas superior.

   ![Configuración del editor](images/lesson-2/editor-settings-icon.png)

1. En el cuadro de diálogo Configuración del editor, haga clic en [!UICONTROL **Lista de elementos**] pestaña.

1. Escriba un **Nombre del elemento** y una **Etiqueta** en los campos respectivos.

1. Haga clic en [!UICONTROL **Plus**] para añadir más elementos a la lista.

   ![Lista de elementos](images/lesson-2/elements-list.png)

1. Haga clic en [!UICONTROL **Guardar**].

Puede ver inmediatamente el cambio en la Lista de elementos en las etiquetas existentes en el Editor. También puede verlos en las opciones proporcionadas al agregar un elemento nuevo.

## Atributos de nombre y etiqueta en la configuración del editor

La lista de atributos funciona de manera similar a la lista de elementos. Desde Configuración del editor, puede controlar la Lista de atributos y sus nombres para mostrar.

1. Haga clic en [!UICONTROL **Configuración del editor**] en la barra de herramientas superior.

   ![Configuración del editor](images/lesson-2/editor-settings-icon.png)

1. En el cuadro de diálogo Configuración del editor, haga clic en [!UICONTROL **Lista de atributos**] pestaña.

1. Escriba un **Nombre de atributo** y una **Etiqueta** en los campos respectivos.

1. Haga clic en [!UICONTROL **Plus**] para añadir más atributos a la lista.

## Configuración de condiciones en Configuración del editor

La pestaña Condition permite configurar varias propiedades.

1. Haga clic en [!UICONTROL **Configuración del editor**] en la barra de herramientas superior.

   ![Configuración del editor](images/lesson-2/editor-settings-icon.png)

1. En el cuadro de diálogo Configuración del editor, haga clic en [!UICONTROL **Condición**] pestaña.

1. Seleccione las casillas de verificación de las condiciones que desee aplicar.

   ![Pestaña Condición](images/lesson-2/condition.png)

1. Haga clic en [!UICONTROL **Guardar**].

## Crear un perfil de publicación en Configuración del editor

Los perfiles de publicación se pueden utilizar para publicar la base de conocimiento. Por ejemplo, Salesforce utiliza una aplicación configurada con una clave de consumidor y un secreto de consumidor. Esta información se puede utilizar para crear un perfil de publicación de Salesforce.

1. Haga clic en [!UICONTROL **Configuración del editor**] en la barra de herramientas superior.

   ![Configuración del editor](images/lesson-2/editor-settings-icon.png)

1. En el cuadro de diálogo Configuración del editor, haga clic en [!UICONTROL **Perfiles**] pestaña.

1. Haga clic en [!UICONTROL **Plus**] junto a Perfiles.

1. Rellene los campos según sea necesario.

1. Haga clic en [!UICONTROL **Guardar**].

Se ha creado un perfil de publicación.
