---
title: Notas de versión | Adobe Experience Manager Guides as a Cloud Service, versión de abril de 2023
description: Última versión de Adobe Experience Manager Guides as a Cloud Service
exl-id: 3b09f0b3-cfa4-422d-91b7-733ab1c1896c
source-git-commit: cf612da41f79b0bf9da4c4d7454a0e3c86af7a4c
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 2%

---

# Lanzamiento en abril de las guías de Adobe Experience Manager as a Cloud Service

## Actualice a la última versión

Actualice las guías de Adobe Experience Manager actuales as a Cloud Service (más adelante denominadas *AEM Guías de as a Cloud Service*) realizando los siguientes pasos:

1. Consulte el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` de su código Git de Cloud Services a 2023.4.249.
3. Confirme los cambios y ejecute la canalización de Cloud Services AEM para actualizar a la última versión de las guías de la aplicación de la versión de la versión de las guías de la versión as a Cloud Service.

## AEM Pasos para indexar el contenido existente (solo si se encuentra en una versión anterior a la versión de septiembre de Guías de as a Cloud Service)

Realice los siguientes pasos para indexar el contenido existente y utilizar el nuevo texto de buscar y reemplazar en el nivel de asignación:

* Ejecute una solicitud de POST al servidor (con la autenticación correcta): `http://<server:port>/bin/guides/map-find/indexing`.
(Opcional: puede pasar rutas específicas de los mapas para indexarlas, de forma predeterminada se indexarán todas las asignaciones || Ejemplo : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* La API devolverá un jobId. Para comprobar el estado del trabajo, puede enviar una solicitud de GET con el ID del trabajo al mismo punto final: `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por ejemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Una vez completado el trabajo, la solicitud de GET anterior responderá correctamente y mencionará si alguna asignación ha fallado. Los mapas indexados correctamente se pueden confirmar desde los registros del servidor.

## Matriz de compatibilidad

AEM En esta sección se enumera la matriz de compatibilidad para las aplicaciones de software compatibles con las guías de la aplicación as a Cloud Service para la versión de abril de 2023 de las Guías de la.

### FrameMaker y FrameMaker Publishing Server

| AEM Versión de Guides as a Cloud de | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.04.0 | No compatible | 2022 o superior |
|  |  |  |


### Conector de oxígeno

| AEM Versión de Guides as a Cloud de | Ventanas de conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.04.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Nuevas funciones y mejoras

AEM Guías as a Cloud Service de proporciona mejoras y nuevas funciones en la última versión:

### Compatibilidad de metadatos avanzada en la publicación de PDF

AEM Guías de ahora proporciona soporte avanzado para los metadatos asignados a los metadatos en la salida del PDF. Las opciones de metadatos incluyen información sobre el documento y su contenido, como el nombre del autor, el título del documento, las palabras clave, la información de copyright y otros campos de datos.

<img src="assets/pdf-metadata.png" alt=" metadatos pdf nativos">

XMP AEM Puede importar un archivo de y las guías de usuario pueden seleccionar la información del archivo. También tiene la opción de proporcionar los nombres y valores de los metadatos mediante la lista desplegable. También puede agregar metadatos personalizados escribiendo directamente en el campo de nombre.


### Panel de vista de esquema mejorada

AEM Guías proporciona un panel de vista de esquema mejorado en el que se obtiene la vista jerárquica de los elementos utilizados en el documento.

<img src="assets/select-element-content-outline-view_cs.png" alt=" metadatos pdf nativos">

La vista Esquema proporciona las siguientes mejoras:

* El menú desplegable Opciones de vista se muestra en la parte superior del panel Vista de esquema. Si un elemento tiene un ID, un atributo y un texto, puede seleccionarlos en la lista desplegable para mostrarlos junto con el elemento. Los atributos que se pueden mostrar en el panel Vista de esquema están determinados por la configuración de Atributos de visualización que ha configurado el administrador en el **Configuración del editor**.

* Con la función de búsqueda, puede buscar un elemento por su nombre, ID, texto o valor de atributo.


### AEM Publicación basada en microservicios para Guías de as a Cloud Service

AEM Guides as a Cloud Service de proporciona la función para ejecutar grandes cargas de trabajo de publicación simultáneamente con publicaciones basadas en microservicios y aprovechar la plataforma sin servidor de Adobe I/O Runtime líder en el sector.

Ahora, en la versión de abril, puede ejecutar varias solicitudes de publicación simultáneamente y generar salidas de PDF masivas de forma muy eficaz mediante la publicación de PDF nativos basada en microservicios.
Para obtener más información, consulte [AEM Configuración de una nueva publicación basada en microservicios para guías de la aplicación de la as a Cloud Service](../knowledge-base/publishing/configure-microservices.md).


## Problemas solucionados

A continuación se enumeran los errores corregidos en varias áreas:

* PDF nativo | La publicación de contenido que tiene una clase de salida con paréntesis() provoca la congelación de la publicación. (11596)
* El problema se produce al mover (arrastrar y soltar) un elemento de lista existente con el control de cambios activado. (11570)
* El problema se produce al mover (arrastrar y soltar) un nuevo elemento de lista con el control de cambios activado. (11569)
* La aplicación o anulación de sangría de elementos de lista no funciona según lo esperado con Control de cambios activado. (11568)
* Agregar contenido en una línea con Control de cambios activado y, a continuación, desactivar Control de cambios no lo desactiva. (11567)
* Dificultad para arrastrar y soltar un elemento de lista; el texto se mueve en lugar del elemento de lista. (11566)
* La revisión completada no se abre en modo de solo lectura. (11387)
* AEM El problema se produce en la búsqueda del sitio de la (no funciona más allá de 2-3 nodos de nivel). (11352)
* Al crear el elemento mostrado en verde (Control de cambios), el nuevo contenido se muestra como control de cambios aunque el control de cambios esté desactivado. (7021)

### Problema conocido con la solución

El Adobe AEM de ha identificado el siguiente problema conocido para la versión de Guías de as a Cloud Service para abril de 2023.

* PDF nativo | Los metadatos antiguos no se rellenan hasta que se abre explícitamente el ajuste preestablecido de salida.
