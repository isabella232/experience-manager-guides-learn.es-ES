---
title: Notas de la versión | Guías de Adobe Experience Manager as a Cloud Service, versión de abril de 2022
description: Versión de abril de las guías de Adobe Experience Manager as a Cloud Service
exl-id: c735ba24-a803-454b-8723-57dacf90061b
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 3%

---

# Versión de abril de las guías de Adobe Experience Manager as a Cloud Service

## Actualización a la versión de abril

Actualice su [!DNL Adobe Experience Manager Guides] as a Cloud Service (posteriormente denominado *[!DNL AEM Guides]as a Cloud Service*) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
1. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2022.4.133.
1. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la versión de abril de [!DNL AEM Guides] as a Cloud Service.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por [!DNL AEM Guides] as a Cloud Service versión de abril de 2022.

### FrameMaker y FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| No compatible | Actualización 4 y posterior de 2020 |
|  |  |


### Conector de oxígeno

| Versión de AEM Guías en la nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac |
| --- | --- | --- |
| 2022.4.0 | 2.5.6 | 2.5.6 |
|  |  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

## Nuevas funciones y mejoras

Se han añadido muchas mejoras y nuevas funciones en el Editor web:

### Resolución de clave mejorada

Una referencia de clave de contenido DITA inserta una parte del contenido de un tema en otro. Utiliza una clave para localizar el contenido. Es necesario resolver las referencias clave asociadas a un tema DITA. El mapa raíz seleccionado tiene la prioridad más alta para resolver las referencias clave.

![cuadro de diálogo preferencias de usuario](assets/user-preferences.png)

Ahora las referencias clave se resuelven sobre la base del mapa raíz configurado en el siguiente orden de prioridad:

1. Preferencias de usuario
1. Panel Vista Mapa
1. Perfil de carpeta

Para obtener más información, consulte *Resolución de referencias clave* en la guía de usuario.

### Agregar un panel personalizado en el panel izquierdo

Ahora puede agregar un panel personalizado en el panel izquierdo del Editor web. Puede utilizar un panel personalizado para varios fines, como proporcionar ayuda o realizar pruebas en un proyecto. Si se ha configurado un panel personalizado, también aparece en la lista de paneles dentro del **Configuración del editor**. Puede alternar el conmutador para mostrar u ocultar el panel personalizado.

### Posibilidad de cambiar el estado del documento de los temas en un mapa DITA

Ahora puede cambiar fácilmente el estado del documento de temas seleccionados dentro de un mapa DITA. También puede abrir y editar las propiedades de los temas seleccionados en un mapa DITA desde el **Más opciones** en la parte inferior del panel Vista de mapa .

![propiedades de tema seleccionadas](assets/map-view-properties.png)

### Información de la versión mostrada en el modo de vista previa

El Editor web le ayuda a administrar sus versiones. Ahora también puede ver la versión del tema activo o del mapa DITA en la esquina superior derecha de la ficha del tema en el modo de vista previa de un tema.

![versión de vista previa](assets/preview-version.png)

## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* Las nuevas etiquetas no se reflejan automáticamente en la lista desplegable Agregar/Quitar etiqueta , sino que es necesario actualizar la línea de base. (9249)
* No se puede editar el título de la línea base si se crea mediante criterios de etiqueta. (9171)
* El trabajo de publicación que utiliza una línea de base se queda atascado en el estado &quot;esperando&quot; si el estado de la línea de base cambia a &quot;fallido&quot;. (9194)
* Al eliminar las etiquetas de las referencias directas también se eliminan las etiquetas de las referencias indirectas. (9257)
* Al buscar mientras escribe, se generan solicitudes de búsqueda no deseadas en la vista Repositorio. (9307)
* Los problemas se producen cuando se utiliza cualquier palabra clave en la ficha Título para . (9318)
* La línea de base falla al añadir una etiqueta con espacios. (9362)
* AEM salida del sitio no muestra correctamente el elemento de glossusage. (8936)
* El error de la consola se produce al abrir el **Salida** en el Editor web. (8715)
* El mensaje de error mostrado al publicar un tipo de registro manual mediante Salesforce no es intuitivo. (8952)
* La validación con la configuración de atributos de condición no se abre inmediatamente, sino que el usuario debe volver a abrir el archivo para ver las validaciones. (9300)
* Los metadatos no se pueden eliminar una vez que se publica un mapa DITA con metadatos.  (9178)
* El panel Traducción está visible incluso al abrir el mapa DITA en el Editor de mapas. (9053)
* El DTD personalizado definido por el usuario no tiene prioridad sobre el DTD DITA estándar incrustado en DITA-OT. (9104)
* En la función PDF nativo, la carga en las plantillas falla para archivos que no sean DITA ni de imagen. (9070)
* El mecanismo de autorización ejecuta dos consultas en lugar de una, en algunos casos especializados. (9221)
* La publicación de la salida del sitio AEM falla al usar DTD personalizado. (9243)
* La nota al pie de página de uso por referencia no se desplaza a la sección de notas al pie de AEM salida del sitio. (9234)

## Problemas conocidos

El Adobe ha identificado el siguiente problema conocido en el [!DNL AEM Guides] Versión as a Cloud Service de abril.

* El Editor web no informa de un error cuando se crean dos o más líneas de base con el mismo nombre pero tienen diferencias de espacio o mayúsculas y minúsculas. Por ejemplo, &quot;adobe&quot; y &quot;Adobe&quot; o &quot;Adobe&quot;.
* El conector de oxígeno se bloquea de forma intermitente mientras se realizan frecuentes inicios de sesión o cierres de sesión o cambios entre diferentes tipos de autenticación.
