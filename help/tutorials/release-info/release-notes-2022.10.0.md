---
title: Notas de la versión | Guías de Adobe Experience Manager as a Cloud Service, versión de octubre de 2022
description: Versión de octubre de las guías de Adobe Experience Manager as a Cloud Service
exl-id: 38638080-625c-49c3-9e54-56cc23831546
source-git-commit: 4183162142f5f6291fdb6e832e10b46a3c0da73a
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 4%

---

# Versión de octubre de las guías de Adobe Experience Manager as a Cloud Service

## Actualización a la versión de octubre

Actualice las guías actuales de Adobe Experience Manager as a Cloud Service (más adelante, *Guías AEM as a Cloud Service*) realizando los siguientes pasos:
1. Compruebe el código Git de los Cloud Services y cambie a la rama configurada en la canalización de Cloud Services correspondiente al entorno que desea actualizar.
2. Actualizar `<dox.version>` propiedad en `/dox/dox.installer/pom.xml` del código Git de sus Cloud Services a 2022.10.183.
3. Confirme los cambios y ejecute la canalización de Cloud Services para actualizar a la versión de octubre de AEM guías as a Cloud Service.

## Matriz de compatibilidad

Esta sección enumera la matriz de compatibilidad para las aplicaciones de software admitidas por AEM Guías as a Cloud Service para la versión de octubre de 2022.

### FrameMaker y FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| No compatible | Actualización 4 y posterior de 2020 |
|  |  |

*La línea de base y las condiciones creadas en AEM son compatibles con las versiones de FMPS a partir de 2020.2.

### Conector de oxígeno

| AEM guías como una versión en la nube | Ventanas del conector de oxígeno | Conector de oxígeno Mac | Editar en ventanas de oxígeno | Editar en Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022.10.0 | 2,7,13 | 2,7,13 | 2.3 | 2,3 |
|  |  |  |  |


## Nuevas funciones y mejoras

AEM guías as a Cloud Service proporciona mejoras y nuevas funciones en la versión de octubre:


### Panel de generación rápida

Ahora AEM guías proporciona la variable **Generación rápida** que le ayuda a generar y ver rápidamente los resultados de los ajustes preestablecidos creados para su mapa DITA.

![Icono de Generación rápida](assets/quick-generate-icon.png)

En el **Generación rápida** , puede ver la lista de todos los ajustes preestablecidos de salida creados para su mapa DITA.

![Panel de generación rápida](assets/quick-generate-panel.png)

Seleccione uno o varios ajustes preestablecidos y genere rápidamente el resultado. También puede ver rápidamente el resultado generado para los ajustes preestablecidos. Se muestra un mensaje de éxito en la generación de la salida. Se muestra un mensaje de error si falla la generación de salida. También puede ver el registro de errores para ver los detalles del error que se produjo en el proceso de generación.


## Problemas solucionados

Los errores corregidos en varias áreas se enumeran a continuación:

* PDF nativo | El error se produce al eliminar los temas solo de recursos de la salida del PDF. (10554)
* PDF nativo | Las claves vacías aparecen en la salida del PDF. (10553)
* PDF nativo | `navtitle` para `topichead` no se respeta. (10509)
* PDF nativo | Soporte necesario para los sabores amd64 JDK. (10465)
* PDF nativo | No se pueden ocultar los temas principales de la tabla de contenido. (10355)
* PDF nativo | Al reiniciar el número de página en el diseño del capítulo, se empieza a numerar aleatoriamente desde el final del capítulo anterior. (10154)
* Explorador Chrome | La pantalla se está quedando en blanco al arrastrar y soltar cualquier elemento de la interfaz de usuario. Por ejemplo, al arrastrar una condición desde el panel Condiciones . (10524)
* Las propiedades de nodo se eliminan tras la operación de copiar y pegar de un recurso. (10053)
* Al hacer clic en  **Cerrar** se redirigía a los usuarios a los recursos. la experiencia se ha corregido para que los usuarios se dirijan a la página principal de AEM. (9654)
