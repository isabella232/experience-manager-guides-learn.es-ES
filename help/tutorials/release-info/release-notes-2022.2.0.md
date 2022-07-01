---
title: Notas de la versión para [!DNL AEM Guides], versión de febrero de 2022
description: Versión de febrero de [!DNL Adobe Experience Manager Guides] as a Cloud Service
exl-id: eb7ff475-bb5b-4d32-b291-024147fbfed1
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 3%

---

# Versión de febrero de [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Actualización a la versión de febrero

Actualice su [!DNL Adobe Experience Manager Guides] as a Cloud Service (posteriormente denominado [!DNL AEM Guides] as a Cloud Service) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2022.2.114.
3. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la versión de febrero de [!DNL AEM Guides] as a Cloud Service.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por [!DNL AEM Guides] Versión as a Cloud Service de febrero de 2022.

### FrameMaker y FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| No compatible | Actualización 4 y posterior de 2020 |
|  |  |


### Conector de oxígeno

| [!DNL AEM Guides] Versión en nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac |
| --- | --- | --- |
| 2022.2.0 | 2.4.0 | 2.4.0 |
|  |  |  |


## Nuevas funciones y mejoras

### Publicación del PDF nativo

También se agregó compatibilidad con la creación de un PDF nativo en la versión de febrero de [!DNL AEM Guides] as a Cloud Service. Se ha introducido un nuevo motor de publicación con las siguientes funciones:
* Creación de una plantilla CSS
* Crear distintas plantillas de página
* Plantillas de PDF de diseño que incluyen plantillas de página y CSS
* Publicar contenido de mapas y temas en formato de PDF

### Compatibilidad con la ruta del sitio de la base de conocimientos en la publicación basada en artículos

[!DNL AEM Guides] as a Cloud Service proporciona la función de publicación basada en artículos para generar de manera incremental un resultado de uno o más temas o publicar el contenido en una plataforma de base de conocimiento. Con la versión de febrero, tiene una opción adicional para elegir la ruta del sitio de la Base de conocimiento a la que se debe publicar el tema o el mapa. Una vez seleccionada la ruta, la salida se genera en la ruta especificada.

### Mejoras en el Editor web

Se han añadido muchas mejoras y nuevas funciones en el Editor web:

* **Cuadro de diálogo mejorado en el cierre de archivos**

[!DNL AEM Guides] as a Cloud Service le solicita que guarde los cambios y desbloquee los archivos bloqueados cuando intente cerrar un archivo abierto en el Editor web. Los mensajes se muestran en función de la variable **Solicitar el registro de entrada al cerrar** y **Solicitar una nueva versión al cerrar** configuración del administrador.

Según la configuración, tiene la opción de guardar los cambios y crear una nueva versión del documento. O bien, también puede proteger el archivo y guardar los cambios en la versión actual.

![Cierre de archivos](assets/file-close-save-changes-unlock.png)

Para obtener más información, consulte *Situaciones de cierre y guardado de archivos* en la Guía del usuario.

* Se ha añadido un espacio de no separación al pallet de caracteres.  A **no separación** El espacio evita un salto de línea automático en un punto concreto de un documento de HTML. El Editor web admite un espacio de no separación tanto para AEM salida de Sitio como para HTML5.

* Cuando se carga una imagen desde el Editor web, se muestra un cuadro de diálogo de confirmación si ya existe una imagen con el mismo nombre. Puede mantener ambos archivos, el existente y el nuevo, o sobrescribir el archivo existente y guardar solo el nuevo.

* Si algún usuario ha bloqueado cualquier archivo para editarlo, un administrador puede liberar el bloqueo y proteger el archivo. Esta función será útil cuando se necesiten editar algunos archivos, pero los usuarios que no estén disponibles para proteger el archivo los hayan bloqueado

### Mapa del tablero

Cuando selecciona descargar el mapa DITA, la solicitud se pone en cola y recibe una notificación una vez que el mapa está listo para descargarse. Puede elegir descargar el archivo de mapa inmediatamente o descargarlo más tarde desde el vínculo proporcionado en la bandeja de entrada de notificaciones de AEM.

![Descarga de mapas](assets/download-map-prompt.png)

### Crítica

Puede mencionar los detalles en el campo de descripción de la tarea de revisión y se muestra en el mensaje de correo electrónico enviado al revisor.

## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

### Publicación basada en artículos

* La publicación basada en artículos no publica artículos basados en la línea de base seleccionada. (8771)
* Los archivos DITAVAL no se respetan en la publicación basada en artículos. (8770)
* No se puede realizar la publicación basada en artículos para el perfil de Salesforce cuando el tipo de registro es preguntas más frecuentes y el contenido del campo del artículo es Pregunta. (8448)
* No se puede realizar la publicación basada en artículos para el perfil de Salesforce cuando el tipo de registro es manual. (8447)

### Editor web

* Arrastrar y soltar una condición no funciona en los temas de DITA. (8761)
* Faltan atributos al añadir un capítulo a un mapa de marcadores mediante Arrastrar y soltar desde la vista Favoritos. (8746)
* La edición de las propiedades de una imagen (altura, anchura) provoca un error de aplicación. (8722)
* Los vínculos rotos no aparecen en el panel Esquema de la vista de origen. (8590)
* El Editor XML elimina la etiqueta de nueva línea en el bloque de código. (8522)
* Glossusage se muestra como una Nota cuando se crea un Glossentry. (8384)
* xref no se puede insertar ni siquiera en ubicaciones válidas. (8354)
* La lista de elementos (Alt+Intro) aparece atenuada en el tema oscuro/más oscuro. (7913)
* La lista de plantillas de asignación de **Crear** opción (menú elipsis) del panel Repositorio no es según el **Perfil de carpeta** en Preferencias de usuario. (5918)
* Los ID de elemento no se generan automáticamente para los elementos añadidos desde la función Reutilizar contenido de la barra de herramientas principal. (5826)

### IU de recursos

* La edición de imágenes no funciona como se espera en el servidor de nube. (8768)
* En el panel del historial de versiones, la sección de la versión actual muestra una marca de tiempo incorrecta y la información la modifica. (8765)
* La carga de archivos DITAVAL en el servidor en la nube falla cuando se utiliza AEM herramienta de escritorio. (8707)
* El segundo usuario administrador no se puede agregar como el primer usuario administrador a una carpeta. (8430)
* Las propiedades no únicas de un recurso no se copian al copiarlo y pegarlo. (8241)

### Cambios en el uso

* En el panel Revisión del Editor web, si un nombre de usuario es largo, los iconos para aceptar/rechazar no se muestran claramente. (8793)
* En el **Buscar y reemplazar** , aparece un icono no deseado al pasar el ratón por encima de la sección de resultados. (8775)
* El icono Personalizado no se selecciona en la propiedad y, en su lugar, se muestra el icono predeterminado para los informes generados mediante el botón Generar informe . (8573)
