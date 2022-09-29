---
title: Notas de la versión | Guías de Adobe Experience Manager as a Cloud Service, versión de septiembre de 2022
description: Última versión de las guías de Adobe Experience Manager as a Cloud Service
source-git-commit: f2ad6e920c47fff61dd85e3aeafb558c7fd6cfea
workflow-type: tm+mt
source-wordcount: '1284'
ht-degree: 3%

---

# Última versión de las guías de Adobe Experience Manager as a Cloud Service

## Actualice a la última versión

Actualice las guías actuales de Adobe Experience Manager as a Cloud Service (más adelante, *Guías AEM as a Cloud Service*) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2022.9.178.
3. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la última versión de AEM guías as a Cloud Service.

## Pasos para indexar el contenido existente

Realice los siguientes pasos para indexar el contenido existente y utilice el nuevo texto de buscar y reemplazar en el nivel del mapa:
* Ejecute una solicitud de POST al servidor (con autenticación correcta): `http://<server:port>/bin/guides/map-find/indexin`.
(Opcional: Puede pasar rutas específicas de los mapas para indexarlos, de forma predeterminada todos los mapas se indexarán || Ejemplo:   `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)
* La API devolverá un jobId. Para comprobar el estado del trabajo, puede enviar una solicitud de GET con id de trabajo al mismo punto final: `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por ejemplo: `http://<_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)`
* Una vez completado el trabajo, la solicitud de GET anterior responderá con éxito y mencionará si se han producido errores en los mapas. Los mapas indexados correctamente se pueden confirmar desde los registros del servidor.


## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por AEM Guías as a Cloud Service para la versión de septiembre de 2022.

### FrameMaker y FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| No compatible | Actualización 4 y posterior de 2020 |
|  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

### Conector de oxígeno

| AEM guías como una versión en la nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022.9.0 | 2,7,13 | 2,7,13 | 2.3 | 2,3 |
|  |  |  |  |


## Nuevas funciones y mejoras

AEM guías as a Cloud Service proporciona muchas mejoras y nuevas funciones en la última versión:


### Crear una línea de base dinámica basada en etiquetas

Ahora, AEM guías le proporciona la función de crear líneas de base dinámicas basadas en etiquetas. Si genera una línea de base, descarga una línea de base o crea un proyecto de traducción con una línea de base, los archivos se seleccionan dinámicamente en función de las etiquetas actualizadas. Esta función es útil, ya que no es necesario modificar la línea de base al actualizar las etiquetas.
También puede exportar la instantánea de la línea base como CSV.

![Crear líneas de base](assets/preset-metadata.png)

### Buscar y reemplazar el texto en el nivel del mapa

Ahora puede buscar archivos dentro de un mapa que contengan texto específico. El texto buscado se resalta en los archivos. También puede reemplazar la palabra o frase buscada con otra palabra o frase dentro de los archivos.
Seleccione el **Reemplazar** para reemplazar la incidencia actual y la variable **Reemplazar todo en el archivo** para reemplazar todas las ocurrencias del archivo seleccionado.

![Buscar Reemplazar en el mapa](assets/map-find-replace.png)

De forma predeterminada, las opciones **Archivo de cierre de compra antes de reemplazar** y **Crear nueva versión después de reemplazar** están seleccionadas, por lo que se desprotege un archivo antes de reemplazar el texto y se crea una nueva versión después de reemplazar el texto.

### Ver la diferencia de versión de los archivos fuera de sincronización desde el panel de traducción

Ahora puede elegir traducir la variable **Sin sincronización** archivos basados en los cambios realizados entre las dos versiones de un tema.\
![Panel de traducción](assets/translation-version-diff.png)
Desde el panel de traducción, puede ver fácilmente las diferencias entre la última versión traducida y la versión actual del archivo seleccionado.

![cuadro de diálogo diferencia de versión](assets/version-diff.png)

En función de las diferencias, puede decidir si desea traducir un tema o no.

### IU de metadatos disponible para ajustes preestablecidos de PDF

Puede establecer los metadatos desde el ajuste preestablecido de salida de un mapa DITA. Puede definir los metadatos Título, Autor, Asunto y Palabras clave. Estos metadatos se asignan a los metadatos en las Propiedades del archivo del PDF de salida.
Estos metadatos anulan los metadatos definidos a nivel de libro. Puede definir los metadatos específicamente en cada ajuste preestablecido de salida y pasarlos al PDF de salida.

![Metadatos del ajuste preestablecido](assets/preset-metadata.png)


## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* Editor web | Al mover elementos dentro de un tema, las ID asignadas a elementos se sobrescriben con las ID asignadas automáticamente. (7895)
* Seguimiento de cambios | El contenido se pierde cuando se introduce un nuevo elemento mediante la tecla Intro. (10246)
* El submapa que se refiere al mapa principal en plantillas de datos no se está creando. (10231)
* Editor XML | La función de copiar y pegar no funciona en el modo de creación. (10309)
* Una vez seleccionadas, no se desactivan las etiquetas de varias versiones. (9561)
* La navegación automática a la ruta en el cuadro de diálogo del explorador del sitio no funciona como la exploración de archivos. (9920)
* El panel Esquema no muestra el contenido cuando se cambia de **Autor** a **Fuente** en el menú contextual. (10319)
* La conref en un nuevo tema creado con un contenido en la plantilla de tema no funciona. El ID de hash copiado no se actualiza en la copia de contenido. (9890)
* Editor web | No existe ningún cargador al crear un mapa a partir de la plantilla de mapa. (9891)
* Nuevo editor de mapas | Si se cambia de **Autor** a **Diseño** vista. (10218)
* Nuevo editor de mapas | Las condiciones aplicadas a cualquier referencia no se pueden eliminar de la vista Presentación. (10213)
* Nuevo editor de mapas | La aplicación de referencias de condiciones no funciona en la vista Presentación como la vista Autor. (10198)
* Nuevo editor de mapas | Mover a la izquierda desde el menú contextual elimina la referencia si no se puede mover a la izquierda. (10219)
* Nuevo editor de mapas |El icono se muestra incorrectamente para las referencias de un mapa creado con la vista Diseño. (10197)
* Panel de repositorio | El clic con el botón derecho en el panel del repositorio da un error de aplicación. (10123)
* Buscar y reemplazar | El modo oscuro no es legible para los resultados de búsqueda en el Editor web. (9978)
* Traducción | Los metadatos y las etiquetas no se propagan a las copias traducidas. (4696)
* Copiar el contenido pegado (ctrl+c/ctrl+v) genera un error en modo de autor. (10304)
* Plantilla de PDF | Al agregar imágenes de fondo a cualquier diseño de página, se muestra la ruta de la imagen en absoluto y las imágenes no se muestran en el PDF de salida. (10297)
* PDF nativo | El título del capítulo y el encabezado del capítulo no funcionan en la publicación del PDF. (9947)
* PDF nativo | `xref` para un concepto no se resuelve correctamente para un tema DITA específico. (10229)
* PDF nativo | No se puede ver el texto del rótulo de una tabla en la salida del PDF generado. (9827)
* PDF nativo | Las referencias de los apéndices no se muestran como apéndices en la salida del PDF. (10182)
* PDF nativo | El atributo Frame de una tabla no se propaga al HTML temporal (como clase). (10353)
* PDF nativo | los archivos de HTML temporal añaden las clases de colección y fila a td y a aunque su valor sea 0 en la DITA de origen. (10352)
* PDF nativo | No se aceptan los metadatos para los criterios agregados en el diseño de página. (10377)
* PDF nativo | La generación de PDF falla para contenido específico. (9927)
* PDF nativo | El contenido a través de conkeyref no se muestra en la salida del PDF. (9836)
* PDF nativo | Las referencias clave para Keydefs con imágenes o vínculos externos no se resuelven. (10063)
* La vista Autor de un mapa no muestra texto de marcador de posición para la lista de tablas y la lista de figuras. (10330)
* Cuando creamos una nueva línea de base, no se aplica el filtro de línea de base seleccionado. (9954)
* Falta el archivo de vídeo en la línea de base si el nombre de la carpeta principal tiene un carácter de espacio. 10031)
* La creación de la línea de base no elige la versión más reciente cuando la zona horaria del usuario es diferente de la del servidor. (10190)
* El método abreviado Control + F no abre el modo de búsqueda del explorador en la consola Recursos después de instalar AEM Guías 4.1 en la AEM 6.5.12. (10189)


## Problemas conocidos

Adobe ha identificado los siguientes problemas conocidos de AEM Guías as a Cloud Service para la versión de septiembre de 2022.


* La línea de base dinámica no está integrada con la publicación de la base de conocimientos.

* Traducción | El icono de diferencia de versión aparece para el contenido de origen debido a cualquier cambio en el contenido de destino.
