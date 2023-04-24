---
title: Notas de la versión | Guías de Adobe Experience Manager as a Cloud Service, versión de marzo de 2023
description: Versión de marzo de las guías de Adobe Experience Manager as a Cloud Service
source-git-commit: d762cccc4a8f89eb91a1a8eb2c1410a7e0358b85
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 2%

---

# Versión de marzo de las guías de Adobe Experience Manager as a Cloud Service

## Actualización a la versión de marzo

Actualice las guías actuales de Adobe Experience Manager as a Cloud Service (más adelante, *Guías AEM as a Cloud Service*) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2023.3.242.
3. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la versión de marzo de AEM Guías as a Cloud Service.

## Pasos para indexar el contenido existente (solo si está en una versión anterior a la versión de septiembre de AEM Guías as a Cloud Service)

Realice los siguientes pasos para indexar el contenido existente y utilizar el nuevo texto de buscar y reemplazar en el nivel del mapa:

* Ejecute una solicitud de POST al servidor (con autenticación correcta): `http://<server:port>/bin/guides/map-find/indexing`.
(Opcional: Puede pasar rutas específicas de los mapas para indexarlos, de forma predeterminada todos los mapas se indexarán || Ejemplo: `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* La API devolverá un jobId. Para comprobar el estado del trabajo, puede enviar una solicitud de GET con id de trabajo al mismo punto final: `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por ejemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Una vez completado el trabajo, la solicitud de GET anterior responderá con éxito y mencionará si se han producido errores en los mapas. Los mapas indexados correctamente se pueden confirmar desde los registros del servidor.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por AEM Guías as a Cloud Service de la versión de marzo de 2023.

### FrameMaker y FrameMaker Publishing Server

| AEM guías como una versión en la nube | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.03.0 | No compatible | 2022 o posterior |
|  |  |  |


### Conector de oxígeno

| AEM guías como una versión en la nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.03.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Nuevas funciones y mejoras

AEM Guías as a Cloud Service proporciona mejoras y nuevas funciones en la versión de marzo de 2023:

### Abra y reproduzca archivos de vídeo o audio en el Editor web

AEM guías ahora proporciona la función de abrir y reproducir archivos de audio o vídeo en el Editor web. Puede cambiar el volumen o la vista del vídeo. En el menú contextual, también tiene las opciones para **Descargar**, cambiar **Reproducir velocidad** o ver **Imagen en imagen**.

<img src="assets/video-web-editor.png" alt="reproducir vídeo" width="600">


## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* El proceso de descarga del PDF no funciona correctamente en el Editor web. (11496)
* Salida JSON | Asignación de metadatos con valor de propiedad como `"value in spaces and double quotes"` genera un error de publicación. (11438)
* La inserción para archivos multimedia de audio y vídeo falla en el formato YouTube en el **Insertar multimedia** icono. (11320)
* El error de validación se produce cuando se crea un mapa con la plantilla que tiene un elemento de título especializado. (11212)
* PDF nativo | la nota al pie presente en el encabezado de tabla lleva al texto en negrita y centrado alineado en el pie de página correspondiente dentro de la salida del PDF. (10610)
>[!NOTE]
>
>Para reflejar el cambio del PDF nativo, elimine la carpeta del PDF ubicada en /content/dam/dita-templates y luego actualice a la última versión. (10610)

### Problema conocido con la solución alternativa

Adobe ha identificado el siguiente problema conocido para AEM versión as a Cloud Service de marzo de 2023 de las Guías.

* Los usuarios no pueden guardar ni crear versiones de un recurso duplicado.

**Solución alternativa**: Antes de realizar cambios en el recurso duplicado, vuelva a procesarlo desde la interfaz de usuario de Assets.

