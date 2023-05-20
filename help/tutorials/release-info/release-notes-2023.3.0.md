---
title: Notas de versión | Adobe Experience Manager Guides as a Cloud Service, versión de marzo de 2023
description: Lanzamiento de marzo de Adobe Experience Manager Guides as a Cloud Service
exl-id: b3fe7cc8-1654-467a-ab18-6e6912855ecc
source-git-commit: 8073716bccacbe8d6a158b44d5106b083e3a5dcd
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 2%

---

# Lanzamiento de marzo de Adobe Experience Manager Guides as a Cloud Service

## Actualización a la versión de marzo

Actualice las guías de Adobe Experience Manager actuales as a Cloud Service (más adelante denominadas *AEM Guías de as a Cloud Service*) realizando los siguientes pasos:
1. Consulte el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` de su código Git de Cloud Services a 2023.3.242.
3. Confirme los cambios y ejecute la canalización de Cloud Services AEM para actualizar a la versión de marzo de las guías de la aplicación as a Cloud Service de la.

## AEM Pasos para indexar el contenido existente (solo si se encuentra en una versión anterior a la versión de septiembre de Guías de as a Cloud Service)

Realice los siguientes pasos para indexar el contenido existente y utilizar el nuevo texto de buscar y reemplazar en el nivel de asignación:

* Ejecute una solicitud de POST al servidor (con la autenticación correcta): `http://<server:port>/bin/guides/map-find/indexing`.
(Opcional: puede pasar rutas específicas de los mapas para indexarlas, de forma predeterminada se indexarán todas las asignaciones || Ejemplo : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* La API devolverá un jobId. Para comprobar el estado del trabajo, puede enviar una solicitud de GET con el ID del trabajo al mismo punto final: `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por ejemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Una vez completado el trabajo, la solicitud de GET anterior responderá correctamente y mencionará si alguna asignación ha fallado. Los mapas indexados correctamente se pueden confirmar desde los registros del servidor.

## Matriz de compatibilidad

AEM En esta sección se muestra la matriz de compatibilidad para las aplicaciones de software compatibles con las guías de la versión de as a Cloud Service para marzo de 2023.

### FrameMaker y FrameMaker Publishing Server

| AEM Versión de Guides as a Cloud de | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.03.0 | No compatible | 2022 o superior |
|  |  |  |


### Conector de oxígeno

| AEM Versión de Guides as a Cloud de | Ventanas de conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.03.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Nuevas funciones y mejoras

AEM La versión as a Cloud Service de Guías de proporciona mejoras y nuevas funciones en la versión de marzo de 2023:

### Abra y reproduzca archivos de vídeo o audio en el Editor web

AEM Guías de la aplicación ahora proporciona la función para abrir y reproducir los archivos de audio o vídeo en el Editor Web. Puede cambiar el volumen o la vista del vídeo. En el menú contextual, también tiene las opciones para **Descargar**, cambiar **Velocidad de reproducción**, o vista **Imagen en imagen**.

<img src="assets/video-web-editor.png" alt="reproducir vídeo" width="600">


## Problemas solucionados

A continuación se enumeran los errores corregidos en varias áreas:

* El proceso del PDF de descarga no funciona correctamente en el editor web. (11496)
* Salida JSON | Asignar metadatos que tengan el valor de propiedad como `"value in spaces and double quotes"` conduce a un error de publicación. (11438)
* La inserción de archivos multimedia de audio y vídeo falla en el formato YouTube en **Insertar multimedia** icono. (11320)
* El error de validación se produce cuando se crea un mapa con la plantilla que tiene un elemento de título especializado. (11212)
* PDF nativo | la nota al pie presente en el encabezado de la tabla lleva a texto en negrita y alineado al centro en el pie de página correspondiente dentro de la salida del PDF. (10610)
>[!NOTE]
>
>Para reflejar el cambio del PDF nativo, elimine la carpeta del PDF ubicada en /content/dam/dita-templates y luego actualice a la última versión. (10610)

### Problema conocido con la solución

El Adobe AEM de ha identificado el siguiente problema conocido para la versión de Guías de as a Cloud Service para marzo de 2023.

* Los usuarios no pueden guardar ni crear la versión de un recurso duplicado.

**Solución**: Antes de realizar cambios en el recurso duplicado, vuelva a procesarlo desde la interfaz de usuario de Assets.
