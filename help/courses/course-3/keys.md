---
title: Claves
description: Las claves permiten incluir información de variables en al trabajar con DITA en AEM guías
exl-id: cb64e094-fe6d-4a5e-8f0e-25ae58aaa2c6
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---

# Claves

Diferentes conjuntos de materiales pueden contener información similar que debe personalizarse en determinados lugares. Las claves permiten incluir información de variables a al trabajar con DITA.

Los archivos de muestra que puede utilizar para esta lección se proporcionan en el archivo . [keys.zip](assets/keys.zip).

>[!VIDEO](https://video.tv.adobe.com/v/342756?quality=12&learn=on)

## Habilitar claves

1. Cargue el conjunto de archivos de ejemplo proporcionados.

   a. Cargue el archivo zip.

   b. Actualice el entorno de AEM.

   c. Seleccione el archivo que desea extraer.

   ![Seleccionar código postal](images/lesson-9/select-zip.png)

   d. Haga clic en [!UICONTROL **Extraer archivo**] en la barra de herramientas superior.

   ![Barra de herramientas](images/lesson-9/extract-archive.png)

   e. En el cuadro de diálogo, elija la ubicación específica para los archivos que se extraerán, como una carpeta denominada Keys.

   f. Haga clic en [!UICONTROL **Siguiente**].

   g. Omita los conflictos, ya que no existirán para contenido que nunca se haya cargado antes.

   h. Select [!UICONTROL **Extraer**] en la parte superior derecha de la pantalla.

1. Cuando finalice la extracción, haga clic en [!UICONTROL **Vaya a la carpeta de destino**].

   ![Confirmación](images/lesson-9/go-to-target.png)

## Resolver claves en valores de referencia

Para utilizar correctamente las claves, las preferencias de usuario deben hacer referencia a un mapa específico como el mapa raíz. Dentro de este mapa hay una colección de claves, agrupadas dentro de un grupo de temas. Al abrir el mapa y los temas, se resuelven las claves en los valores a los que hace referencia este mapa.

1. Especifique un mapa raíz.

   a. En la pantalla Claves , abra un mapa.

   b. Configure las preferencias de usuario.

   c. Haga clic en el [!UICONTROL **Preferencias de usuario**] en la barra de herramientas superior.

   ![Barra de herramientas superior](images/lesson-9/author-view.png)

   d. Haga clic en el icono de clave para especificar un **Mapa raíz** que se utilizará para resolver claves.

   e. Seleccione las casillas de verificación de los recursos que desee.

   ![Menú desplegable Recursos](images/lesson-9/select-assets.png)

   f. Haga clic en [!UICONTROL **Select**].

   g. **Guardar** las Preferencias de usuario.

1. Vaya a la **Vista Mapa**.

1. Abra el mapa especificado.

Las claves se han resuelto.

## Añadir una nueva clave manualmente

1. Abra un mapa con un mapa raíz especificado.

1. Seleccione una Clave.

   ![Menú desplegable Clave](images/lesson-9/hybrid-key.png)

1. Inserte una nueva clave.

   a. Haga clic en una ubicación válida en el mapa.

   b. Seleccione el **Keydef** en la barra de herramientas superior.

   ![Barra de herramientas Keydef](images/lesson-9/key-icon.png)

   c. En el cuadro de diálogo Insertar clave, introduzca un valor único para las claves que tenga sentido para la definición que está creando.

   d. Haga clic en [!UICONTROL **Insertar**].

1. Agregue topicmeta dentro de la clave.

   a. Haga clic en el [!UICONTROL **Insertar elemento**] en la barra de herramientas superior.

   ![Barra de herramientas Keydef](images/lesson-9/add-icon.png)

   b. En el cuadro de diálogo Insertar elemento, busque y seleccione &quot;topicmeta&quot;.

1. Agregue palabras clave dentro del tema.

   a. Haga clic en el [!UICONTROL **Insertar elemento**] en la barra de herramientas superior.

   ![Barra de herramientas Keydef](images/lesson-9/add-icon.png)

   b. En el cuadro de diálogo Insertar elemento, busque y seleccione &quot;palabras clave&quot;.

1. Agregue una palabra clave dentro de la meta de tema.

   a. Haga clic en el [!UICONTROL **Insertar elemento**] en la barra de herramientas superior.

   ![Barra de herramientas Keydef](images/lesson-9/add-icon.png)

   b. En el **Insertar elemento** diálogo, buscar y seleccionar &quot;palabra clave&quot;

1. Escriba el valor de la clave en la palabra clave.

En el mapa, la clave debería tener este aspecto:

![Keydef Finalizado](images/lesson-9/keydef.png)

## Configuración de una clave como un fragmento

Los fragmentos de código son fragmentos de contenido pequeños que se pueden reutilizar en varios temas del proyecto de documentación. En lugar de generar manualmente cada clave, puede configurar una sola clave como un fragmento.

1. Seleccione un elemento keydef en el mapa.

1. En el menú contextual, haga clic en [!UICONTROL **Crear fragmento**].

1. En el cuadro de diálogo Nuevo fragmento, añada un Título y una Descripción.
También es posible que desee eliminar las claves o definiciones de palabras clave existentes del Contenido.

1. Haga clic en [!UICONTROL **Crear**].

1. En el panel izquierdo, seleccione **Fragmentos**.

1. Arrastre y suelte el fragmento que acaba de crear desde el panel Fragmentos hasta el mapa.

1. Actualice la clave según sea necesario mediante Propiedades de contenido.
Cuando se guarde y actualice, este conjunto de claves estará disponible para cualquier usuario que haya definido un mapa que contenga el mismo mapa raíz.
