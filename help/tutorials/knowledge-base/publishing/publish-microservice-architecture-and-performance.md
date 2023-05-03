---
title: Arquitectura y rendimiento del microservicio de Cloud Publishing
description: Comprenda cómo el nuevo microservicio permite la publicación escalable en AEMaaCS.
source-git-commit: 2e45f132ced5ac29118a7301f104bedc03c93253
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---


# Arquitectura y análisis de rendimiento del microservicio de Cloud Publishing

Este artículo comparte la información sobre la arquitectura y los números de rendimiento del nuevo microservicio de publicación en la nube.

>[!NOTE]
>
> Actualmente, la publicación basada en microservicios en AEM guías solo admite la salida de PDF mediante la publicación de PDF nativos o a través de DITA-OT. AEM guías agregarán compatibilidad con la publicación basada en microservicios para más tipos de salida en futuras versiones.

## Problemas con flujos de trabajo de publicación existentes en la nube

DITA Publishing es un proceso intensivo en recursos que depende principalmente de la memoria del sistema y la CPU disponibles. La necesidad de estos recursos aumenta aún más si los editores publican mapas de gran tamaño con muchos temas o si se activan varias solicitudes de publicación paralelas.

Si no utiliza el nuevo servicio, todas las publicaciones se realizan en el mismo pod de Kubernetes(k8) que también ejecuta el servidor de nube AEM. Un pod típico k8 tiene un límite en la cantidad de memoria y CPU que puede usar. Si los usuarios de AEM guías publican cargas de trabajo grandes o paralelas, este límite puede infringirse rápidamente. K8 reinicia los pods que intentan utilizar más recursos que el límite configurado, lo que puede tener un impacto grave en la propia instancia de nube de AEM.

Esta restricción de recursos fue la principal motivación para crear un servicio dedicado que nos permita ejecutar varias cargas de trabajo de publicación simultáneas y grandes en la nube.

## Introducción a la nueva arquitectura

El servicio utiliza las soluciones de nube de vanguardia de Adobe, como App Builder, IO Eventing e IMS, para crear una oferta sin servidor. Estos servicios se basan en sí mismos en los estándares del sector ampliamente aceptados, como Kubernetes y docker.

Cada solicitud al nuevo microservicio de publicación se ejecuta en un contenedor de docker aislado que ejecuta solo una solicitud de publicación a la vez. Si se reciben nuevas solicitudes de publicación, se crean automáticamente varios contenedores nuevos. Esta configuración de contenedor único por solicitud permite que el microservicio ofrezca el mejor rendimiento a los clientes sin introducir riesgos de seguridad. Estos contenedores se descartan una vez finalizada la publicación, lo que libera los recursos no utilizados.

Todas estas comunicaciones están garantizadas por Adobe IMS mediante autenticación y autorización basadas en JWT y se ejecutan mediante HTTPS.

<img src="assets/architecture.png" alt="ficha proyectos" width="600">

>[!NOTE]
>
> El proceso de publicación ejecuta algunas partes de la solicitud que dependen del contenido en el propio servidor de AEM, como la generación de listas de dependencias. Sin embargo, las partes más exhaustivas del proceso de publicación, como la ejecución de DITA-OT o el motor nativo, se han descargado al nuevo servicio.


## Análisis de rendimiento

Esta sección muestra los números de rendimiento del microservicio. Compara el rendimiento del microservicio con la oferta in situ de AEM guías, ya que la arquitectura de la nube antigua tenía problemas al publicar simultáneamente o mapas muy grandes.

Si está publicando un mapa grande en el local, es posible que tenga que modificar los parámetros de la pila de Java o que encuentre errores de memoria insuficiente. En la nube, el microservicio ya está perfilado y tiene una pila de Java óptima y otras configuraciones listas para usar.

### Ejecución de una publicación en la nube o en la instalación

* Nube

   Si está ejecutando una sola publicación en la nube mediante el nuevo servicio, la publicación puede tardar un poco más en comparación con la publicación local única. Este tiempo ligeramente elevado se debe a la naturaleza distribuida de la nueva arquitectura de la nube.

   <img src="assets/cloud_single_publish.png" alt="ficha proyectos" width="600">

* local

   Los resultados de una sola publicación son mejores en la arquitectura antigua de la nube o en la propia instalación, ya que la publicación completa se está realizando en el mismo pod/equipo en el que se está ejecutando AEM.

   <img src="assets/onprem_single_publish.png" alt="ficha proyectos" width="600">

### Ejecución de varias publicaciones en la nube o en la instalación

* Nube

   El nuevo microservicio de publicación aparece en esta situación. Como puede ver en la imagen siguiente, con el aumento de los varios trabajos de publicación simultáneos, la nube puede publicarlos sin ningún aumento significativo en el tiempo de publicación.

   <img src="assets/cloud_bulk_publish.png" alt="ficha proyectos" width="600">

* local

   La ejecución de una publicación simultánea en un servidor local provoca una grave degradación del rendimiento. Esta caída del rendimiento es más grave si los editores publican incluso más mapas simultáneamente.

   <img src="assets/onprem_bulk_publish.png" alt="ficha proyectos" width="600">

## Ventajas adicionales

Parte de cada solicitud de publicación debe ejecutarse en la instancia de AEM para recuperar el contenido de publicación correcto que se enviará al microservicio. La nueva arquitectura de nube utiliza AEM trabajos en lugar de flujos de trabajo AEM, como ocurría en la arquitectura antigua. Este cambio permite a los administradores de las guías de AEM configurar de forma individual la cola de publicación en la nube sin afectar a otros trabajos AEM o configuraciones de flujo de trabajo.

Puede encontrar más información sobre cómo configurar el nuevo microservicio de publicación aquí: [Configurar Microservice](configure-microservices.md)