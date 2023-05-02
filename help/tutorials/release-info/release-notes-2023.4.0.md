---
title: Notas de la versión | Guías de Adobe Experience Manager as a Cloud Service, versión de abril de 2023
description: Última versión de las guías de Adobe Experience Manager as a Cloud Service
exl-id: 3b09f0b3-cfa4-422d-91b7-733ab1c1896c
source-git-commit: cf612da41f79b0bf9da4c4d7454a0e3c86af7a4c
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 2%

---

# Versión de abril de las guías de Adobe Experience Manager as a Cloud Service

## Actualice a la última versión

Actualice las guías actuales de Adobe Experience Manager as a Cloud Service (más adelante, *Guías AEM as a Cloud Service*) realizando los siguientes pasos:

1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2023.4.249.
3. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la última versión de AEM guías as a Cloud Service.

## Pasos para indexar el contenido existente (solo si está en una versión anterior a la versión de septiembre de AEM Guías as a Cloud Service)

Realice los siguientes pasos para indexar el contenido existente y utilizar el nuevo texto de buscar y reemplazar en el nivel del mapa:

* Ejecute una solicitud de POST al servidor (con autenticación correcta): `http://<server:port>/bin/guides/map-find/indexing`.
(Opcional: Puede pasar rutas específicas de los mapas para indexarlos, de forma predeterminada todos los mapas se indexarán || Ejemplo: `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* La API devolverá un jobId. Para comprobar el estado del trabajo, puede enviar una solicitud de GET con id de trabajo al mismo punto final: `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por ejemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Una vez completado el trabajo, la solicitud de GET anterior responderá con éxito y mencionará si se han producido errores en los mapas. Los mapas indexados correctamente se pueden confirmar desde los registros del servidor.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por AEM Guías as a Cloud Service de la versión de abril de 2023.

### FrameMaker y FrameMaker Publishing Server

| AEM guías como una versión en la nube | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.04.0 | No compatible | 2022 o posterior |
|  |  |  |


### Conector de oxígeno

| AEM guías como una versión en la nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.04.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Nuevas funciones y mejoras

AEM guías as a Cloud Service proporciona mejoras y nuevas funciones en la última versión:

### Compatibilidad avanzada con metadatos en la publicación de PDF

AEM guías ahora proporciona compatibilidad avanzada con los metadatos asignados a los metadatos en la salida del PDF. Las opciones de metadatos incluyen información sobre el documento y su contenido, como el nombre del autor, el título del documento, las palabras clave, la información de copyright y otros campos de datos.

<img src="assets/pdf-metadata.png" alt=" metadatos pdf nativos">

Puede importar un archivo XMP y AEM guías pueden seleccionar la información del archivo. También tiene la opción de proporcionar los nombres y valores de los metadatos mediante la lista desplegable. También puede agregar metadatos personalizados escribiendo directamente en el campo de nombre.


### Panel de vista de esquema mejorado

AEM guías proporciona un panel de vista de esquema mejorado en el que se obtiene la vista jerárquica de los elementos utilizados en el documento.

<img src="assets/select-element-content-outline-view_cs.png" alt=" metadatos pdf nativos">

La Vista de esquema proporciona las siguientes mejoras:

* La lista desplegable Opciones de vista se muestra en la parte superior del panel Vista de esquema. Si un elemento tiene un ID, un atributo y un texto, puede seleccionarlos en la lista desplegable para mostrarlos junto con el elemento . Los atributos que se pueden mostrar en el panel Vista de esquema están determinados por la configuración de Atributos de visualización que ha configurado el administrador en el **Configuración del editor**.

* Con la función de búsqueda, puede buscar un elemento por su nombre, id, texto o valor de atributo.


### Publicación basada en microservicios para guías AEM as a Cloud Service

AEM guías as a Cloud Service proporciona la función para ejecutar grandes cargas de trabajo de publicación simultáneamente con la publicación basada en microservicios y aprovechar la plataforma sin servidor Adobe I/O Runtime líder en el sector.

Ahora, en la versión de abril, puede ejecutar varias solicitudes de publicación simultáneamente y generar salidas de PDF masivo de forma muy eficaz mediante la publicación de PDF nativos basada en microservicios.
Para obtener más información, consulte [Configuración de la nueva publicación basada en microservicios para AEM guías as a Cloud Service](../knowledge-base/publishing/configure-microservices.md).


## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* PDF nativo | La publicación de contenido que tiene una clase de salida con paréntesis() produce un bloqueo de publicación. (11596)
* El problema se produce al mover (arrastrar y soltar) en lugar de un elemento de lista existente con Seguimiento de cambios activado. (11570)
* El problema se produce al mover (arrastrar y soltar) como un nuevo elemento de lista con Seguimiento de cambios activado. (11569)
* La sangría o la anulación de sangría de elementos de lista no funcionan como se espera con Seguimiento de cambios en . (11568)
* Añadir contenido en una línea con el control de cambios activado y desactivar el control de cambios no lo desactiva. (11567)
* Dificultad al arrastrar y soltar un elemento de lista, el texto se mueve en lugar del elemento de lista. (11566)
* La revisión finalizada no se abre en modo de solo lectura. (11387)
* El problema se produce en AEM búsqueda del sitio (no funciona más allá de los nodos de 2 a 3 niveles). (11352)
* En la creación del elemento que se muestra en verde (Seguimiento de cambios), el nuevo contenido se muestra como cambio de seguimiento aunque el cambio de seguimiento esté desactivado. (7021)

### Problema conocido con la solución alternativa

Adobe ha identificado el siguiente problema conocido para AEM versión as a Cloud Service de abril de 2023 de las Guías.

* PDF nativo | Los metadatos antiguos no se rellenan hasta que se abre explícitamente el ajuste preestablecido de salida.
