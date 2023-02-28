---
title: Flujo de trabajo de posgeneración
description: Resumen del flujo de trabajo de posgeneración con un ejemplo
source-git-commit: 447cd512d1b6cdce3bd1ddded1575dab87daa04a
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 2%

---


# Publicación de guías de AEM: Flujo de trabajo de posgeneración

AEM guías le proporciona la flexibilidad para especificar un flujo de trabajo de generación posterior a la salida. Puede realizar algunas tareas posteriores al procesamiento en la salida que se genera mediante AEM guías.
Por ejemplo, puede que desee establecer ciertas propiedades en la salida del PDF o enviar un correo electrónico a un conjunto de usuarios una vez que se genere la salida.


## ¿Cuáles son los pasos necesarios para utilizar los flujos de trabajo de generación de anuncios?

### Creación de un proceso de flujo de trabajo

Cree un proceso de flujo de trabajo basado en Java o ECMA que realice la operación en la salida generada. Por ejemplo, copiar algunos metadatos del origen al contenido generado o manipular los metadatos del resultado generado.
- Tomaremos un ejemplo de cómo crear un proceso de este tipo utilizando el script ECMA (puede consultar el paquete adjunto)
- Para ver el proceso de flujo de trabajo basado en Java, consulte la sección &quot;*Personalización del flujo de trabajo de generación posterior a la salida*&quot; de [Guía de instalación y configuración](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_Installation-Configuration-Guide_EN.pdf#page=119)


### Crear un modelo del flujo de trabajo

Con el proceso de flujo de trabajo personalizado que ha creado en el paso anterior, cree un modelo de flujo de trabajo y agréguele ese paso de proceso.
- También debe añadir un paso de proceso obligatorio &quot;*Finalizar generación posterior*&quot; como el último paso del flujo de trabajo.

Consulte el modelo de flujo de trabajo de ejemplo que se muestra a continuación:

![Modelo de flujo de trabajo de posgeneración](../assets/workflows/pgwf-workflow-model.png)


### Usar este flujo de trabajo de posgeneración en un mapa

El flujo de trabajo de generación de publicaciones es una propiedad que se puede configurar en cualquier ajuste preestablecido de salida dentro AEM mecanismo de publicación de las guías. Ejemplo:

![Flujo de trabajo de posgeneración en Ajustes preestablecidos de salida](../assets/workflows/pgwf-preset-settings.png)


Suponiendo que el modelo seleccionado ya se ha creado.


### Pruebas

Ahora puede ejecutar la publicación utilizando este ajuste preestablecido y validar el resultado del paso de proceso


## Muestra

Para su referencia, puede utilizar el paquete siguiente e instalarlo mediante el gestor de paquetes para probar el flujo de trabajo de posgeneración de muestras (*como se menciona en las capturas de pantalla anteriores*)

[Modelo de flujo de trabajo de posgeneración basado en ECMA de muestra](../assets/workflows/sample-pgwf-ecma-test-wfmetadata.zip)
