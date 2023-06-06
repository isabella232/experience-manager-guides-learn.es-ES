---
title: Notas de versión | Novedades de la versión de junio de 2023 de las guías de Adobe Experience Manager
description: Conozca las funciones nuevas y mejoradas de la versión de junio de 2023 de las guías de Adobe Experience Manager as a Cloud Service
source-git-commit: 5670b4a8f34916c7ff415680c5ddcfab6e9618e6
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 0%

---

# Novedades de la versión de junio de 2023 de Adobe Experience Manager Guides as a Cloud Service

Este artículo cubre las funciones nuevas y mejoradas de la versión de junio de 2023 de las guías de Adobe Experience Manager (más adelante denominadas *AEM Guías de as a Cloud Service*).

Para obtener más información sobre las instrucciones de actualización, la matriz de compatibilidad y los problemas corregidos en esta versión, consulte la [Notas de versión](release-notes-2023.6.0.md) artículo.

## Informe Vínculos rotos en el editor web

AEM Guías de le permite comprobar la integridad general de sus documentos técnicos y generar informes desde el Editor Web. AEM Ahora, en junio de 2023, la versión Guías de le proporciona la función para ver y corregir los vínculos rotos. Este es un informe muy útil que le ayuda a administrar los vínculos rotos. Puede ver fácilmente los vínculos rotos presentes en el mapa DITA y también corregirlos.
![](assets/broken-link-report.png){width="800" align="left"}

Una vez corregido un vínculo, no se muestra en la lista de vínculos rotos.

Para obtener más información, consulte [Ver y corregir vínculos rotos](../user-guide/reports-web-editor.md#report-broken-links).

## Cambiar nombre y mover archivos en la vista Repositorio

Ahora también puede cambiar el nombre de un archivo o moverlo desde el panel del repositorio. Esta función es muy práctica y ayuda a administrar sus archivos fácilmente desde el panel Repositorio. Puede seleccionar un archivo y cambiarle el nombre o moverlo mediante el **Opciones** para el archivo seleccionado. AEM Guías del usuario muestra un mensaje de éxito al mover o cambiar el nombre de un archivo.

![](assets/rename-move-assets.png){width="650" align="left"}

Para obtener más información sobre el menú Opciones de un archivo, consulte la **Vista de repositorio** descripción de la función en [Panel izquierdo](../user-guide/web-editor-features.md#id2051EA0M0HS) sección.

## Mejoras del PDF nativo

### Agregar una marca de agua a la salida del PDF para borradores de documentos

Ahora puede agregar una marca de agua a la salida del PDF del documento que aún no está aprobado. Esta marca de agua no aparece si genera el PDF para el documento en el estado de documento &quot;Aprobado&quot;. Por ejemplo, puede agregar una marca de agua Borrador para la salida del PDF.

Para obtener más información, consulte [Agregar una marca de agua a la salida del PDF para los borradores de documentos](../native-pdf/use-javascript-content-style.md#watermark-draft-document).

### Compatibilidad con variables de idioma en elementos DITA

AEM Guías de proporciona compatibilidad con las variables de idioma. Estas variables son muy útiles para generar cadenas localizadas para elementos como nota, sugerencia, advertencia y precaución. Por ejemplo, puede tener las siguientes formas de presentar la NOTA en la salida del PDF: Alemán: Notiz Español: Nota

### Compatibilidad con variables de idioma en el pie de página

Puede agregar una variable de idioma a un encabezado o pie de página en ejecución en la página maestra de un documento. La variable se muestra en todas las páginas del cuerpo del documento que tienen aplicada esta página maestra. Por ejemplo, 1 de 1 página.
También puede utilizarlo para presentar los números en varios idiomas.

### Prefijos localizados para el índice

También tiene la función de mostrar términos localizados que se utilizarán para presentar los prefijos en los encabezados.
Por ejemplo, puede tener las siguientes formas de presentar el prefijo &quot;Chapter&quot; en la salida del PDF: German: Kapitel Spanish: Capítulo

### AEM Posibilidad de utilizar metadatos de en diseños de PDF


Los metadatos son la descripción o definición del contenido. Estos metadatos se almacenan en el contenido del mapa DITA de origen.

AEM Ahora, en las guías de los recursos también puede seleccionar las propiedades de metadatos de los recursos y agregarlas al diseño de página. AEM A continuación, Guías de recursos selecciona estas propiedades de metadatos de los recursos y las publica en la salida del PDF.


![](assets/native-pdf-metadata-asset.png){width="550" align="left"}

>[!NOTE]
>
> AEM Las guías también son compatibles con las propiedades de metadatos de los mapas DITA.

Para obtener más información, consulte [Añadir campos y metadatos](../native-pdf/design-page-layout.md#add-fields-metadata).


## Mejoras de Schematron

### Usar instrucciones de informe para comprobar reglas en Schematron

AEM Guías de informes ahora también admite las instrucciones de informe con Schematron. Una instrucción de informe genera un mensaje cuando una instrucción de prueba se evalúa como verdadera. Por ejemplo, si desea que la descripción breve tenga menos de 150 caracteres o menos, puede definir una instrucción de informe para comprobar los temas en los que la descripción breve tenga más de 150 caracteres.

Para obtener más información, consulte [Usar instrucciones Assert y Report para comprobar las reglas](../user-guide/support-schematron-file.md#schematron-assert-report).

### Uso de expresiones Regex

También puede utilizar expresiones Regex para definir una regla con la función matches() y luego realizar la validación mediante el archivo Schematron.

Para obtener más información, consulte [Usar expresiones Regex](../user-guide/support-schematron-file.md#schematron-assert-report).


### Definir patrones abstractos

AEM Guías de también admite patrones abstractos en Schematron. Puede definir patrones abstractos genéricos y reutilizarlos. Los patrones abstractos pueden simplificar el esquema de Schematron y también ayudarle a administrar y actualizar la lógica de validación.


Para obtener más información, consulte [Definir patrones abstractos](../user-guide/support-schematron-file.md#schematron-abstract-patterns).

## AEM Navegue desde el Editor Web hasta la página principal de la

AEM Ahora puede navegar fácilmente desde el Editor Web a la página de inicio de la página de la página de inicio de la.

![](assets/web-editor-launch-page.png){width="800" align="left"}

* Haga clic en **Guías** icono (![](assets/aem-guides-icon.png) AEM ), para volver a la página Navegación de la.


Para obtener más información, consulte [AEM Página de navegación de](../user-guide/web-editor-launch-editor.md#id2056BG00RZJ).

## Gestión de definiciones jerárquicas de definiciones de temas y enumeraciones

AEM Las guías incluyen la potente función de crear mapas de esquema de asunto, que son una forma especializada de mapas DITA que se utilizan para definir sujetos taxonómicos y valores controlados. AEM Ahora, Guías de también le permite definir la definición del asunto en un mapa y las definiciones de enumeración en otro mapa. A continuación, puede añadir la referencia de mapa y utilizar el esquema de asunto.
Las referencias de asunto y enumeración se resuelven en el mismo mapa o en el mapa al que se hace referencia.

Para obtener más información sobre la administración de definiciones jerárquicas de definiciones de temas y enumeraciones, consulte la **Régimen del sujeto** descripción de la función en [Panel izquierdo](../user-guide/web-editor-features.md#id2051EA0M0HS) sección.

## Compatibilidad con el formato XLIFF en la traducción

AEM Las guías de datos también proporcionan compatibilidad con el formato de archivo de intercambio de localización XML (XLIFF) en la traducción. Ahora también puede elegir lo siguiente **Crear un nuevo proyecto de traducción XLIFF** para convertir el contenido XML al formato XLIFF.
Con este formato, puede exportar el contenido al formato XLIFF estándar del sector y, a continuación, proporcionar lo mismo a los proveedores de traducción. Para obtener más información, consulte [Creación de un proyecto de traducción](../user-guide/translate-documents-web-editor.md#create-translation-project).

![](assets/translation-project-types.png){width="350" align="left"}



## Panel Favoritos mejorado

AEM Guías de ayuda a crear una colección o lista de favoritos de sus archivos y carpetas y utilizarlos fácilmente. Ahora **Opciones** El menú también está disponible en **Favoritos** panel. Puede cambiar el nombre de la colección seleccionada o eliminarla del **Opciones** menú. Puede seleccionar el **Actualizar** para obtener una nueva lista de archivos o carpetas del repositorio. También puede ver el contenido de la carpeta en la interfaz de usuario de Assets.

![](assets/favorites-options.png){width="650" align="left"}

>[!NOTE]
>
> También puede actualizar la lista utilizando el **Actualizar** en la parte superior.

Para obtener más información sobre **Opciones** menú de una colección Favoritos, vea el **Favoritos** descripción de la función en [Panel izquierdo](../user-guide/web-editor-features.md#id2051EA0M0HS) sección.

## Cambiar al tema del sistema

Ahora también puede utilizar el tema del dispositivo. Uso del **Preferencias de usuario** AEM , puede configurar las guías de usuario para que cambien automáticamente entre los temas claro y oscuro en función del tema del dispositivo.

![](assets/device-theme-user-preferences.png){width="550" align="left"}

Para obtener más información, consulte la **Preferencias de usuario** descripción de la función en [Barra de herramientas principal](../user-guide/web-editor-features.md#id2051EA0G05Z) sección.
