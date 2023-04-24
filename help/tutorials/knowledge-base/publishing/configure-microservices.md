---
title: Configuración de la nueva publicación basada en microservicios para AEM guías as a Cloud Service
description: Obtenga información sobre cómo configurar la nueva publicación basada en microservicios para AEM guías.
exl-id: 92e3091d-6337-4dc6-9609-12b1503684cd
source-git-commit: 95c89acd02b798d42c817b52f6f8e0710a0abb76
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 0%

---

# Configuración de la nueva publicación basada en microservicios para AEM guías as a Cloud Service

El nuevo microservicio de publicación permite a los usuarios ejecutar grandes cargas de trabajo de publicación simultáneamente en AEM guías as a Cloud Service y aprovechar la plataforma sin servidor líder en el sector de Adobe I/O Runtime.

Para cada solicitud de publicación, AEM guías as a Cloud Service ejecuta un contenedor independiente que se escala horizontalmente según las solicitudes del usuario. Esto proporciona a los usuarios las capacidades para ejecutar varias solicitudes de publicación y obtener un mejor rendimiento que sus grandes servidores de AEM locales.

>[!NOTE]
>
> Actualmente, la publicación basada en microservicios en AEM guías solo admite la salida de PDF mediante la publicación de PDF nativos o a través de DITA-OT. En las próximas versiones añadiremos compatibilidad con la publicación basada en microservicios para más tipos de salida.

Como el nuevo servicio de publicación en la nube está protegido por la autenticación basada en JWT de Adobe IMS, los clientes deben seguir los pasos que se indican a continuación para integrar sus entornos con los flujos de trabajo de autenticación seguros basados en token de Adobe y empezar a utilizar la nueva solución de publicación escalable basada en la nube.


## Crear configuraciones de IMS en la consola de Adobe Developer

**Función necesaria para crear las confusiones**: Administrador del sistema

Siga estos pasos para crear configuraciones de IMS en la consola de Adobe Developer:

1. Abra Developer Console: `https://developer.adobe.com/console`.

1. Cambie a **Proyectos** de la parte superior.

   <img src="assets/projects-tab.png" alt="ficha proyectos" width="500">

1. Para crear un nuevo proyecto vacío, seleccione **Proyecto vacío** de la variable **Crear nuevo proyecto** lista desplegable.

   <img src="assets/create-new-project.png" alt="crear nuevo proyecto" width="500">

1. Select **API** de la variable **Agregar a proyecto** para agregar la API de administración de E/S al proyecto.

   <img src="assets/add-project.png" alt="agregar proyecto" width="300">

   <img src="assets/io-management-api.png" alt="io management" width="500">

1. Cree un nuevo par de claves privada y pública al añadir la API. Esto descargará automáticamente la clave privada en su sistema.

   <img src="assets/generate-key-pair.png" alt="generar par de claves" width="500">

1. Guarde la API configurada.

   <img src="assets/save-api.png" alt="guardar api" width="600">

1. Vuelva a **Proyectos** y haga clic en **Información general del proyecto** a la izquierda.

   <img src="assets/project-overview.png" alt="información general del proyecto" width="500">

1. Haga clic en **Descargar** en la parte superior para descargar el servicio JSON.

   <img src="assets/download-json.png" alt="descargar json" width="500">

Ahora ha configurado los detalles de autenticación JWT y también ha descargado la clave privada y los detalles del servicio JSON. Mantenga estos dos archivos a mano, ya que estos archivos son necesarios en la siguiente sección.

### Añadir la configuración de IMS al entorno

Siga estos pasos para agregar la configuración de IMS al entorno:

1. Abra experience manager y, a continuación, seleccione el programa que contiene el entorno que desea configurar.
1. Cambie a **Entornos** pestaña .
1. Haga clic en el nombre del entorno que desea configurar. Esto le llevará a la página Información del entorno .
1. Cambie a **Configuración** pestaña .
1. Cargue la clave privada y el JSON del proyecto como se muestra en la captura de pantalla siguiente. Asegúrese de que está utilizando los mismos nombres y configuraciones que se indican a continuación.

   <img src="assets/ims-config-environment.png" alt="configuraciones de ims" width="500">

>[!NOTE]
>
> Debe abrir, copiar y pegar el contenido del archivo JSON de clave privada y detalles del servicio en la columna de valor del panel Configuración como se muestra en la captura de pantalla anterior.

Una vez añadida la configuración de IMS al entorno, realice los siguientes pasos para vincular estas propiedades con AEM guías mediante OSGi:

1. En el código del proyecto Git de Cloud Manager, agregue los dos archivos siguientes (Para el contenido del archivo, consulte [Apéndice](#appendix)).

   * `com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`
   * `com.adobe.fmdita.publishworkflow.PublishWorkflowConfigurationService.xml`
1. Asegúrese de que el `filter.xml`.
1. Confirme y presione los cambios de Git.
1. Ejecute la canalización para aplicar los cambios en el entorno.

Una vez hecho esto, debería poder usar la nueva publicación en la nube basada en microservicios.

## Apéndice {#appendix}

**Archivo**:
`com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

**Contenido**:

```
{
  "service.account.details": "$[secret:SERVICE_ACCOUNT_DETAILS]",
  "private.key": "$[secret:PRIVATE_KEY]"
}
```

**Archivo**: `com.adobe.fmdita.publishworkflow.PublishWorkflowConfigurationService.xml`

**Contenido**:
* `dxml.use.publish.microservice`: Cambie para habilitar la publicación de PDF basada en microservicios mediante DITA-OT
* `dxml.use.publish.microservice.native.pdf`: Cambie para habilitar la publicación de PDF nativos basada en microservicios

```
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:jcr="http://www.jcp.org/jcr/1.0" xmlns:sling="http://sling.apache.org/jcr/sling/1.0"
          jcr:primaryType="sling:OsgiConfig"
          dxml.publish.microservice.url="https://adobeioruntime.net/api/v1/web/543112-guidespublisher/default/publishercaller.json"
          dxml.use.publish.microservice="{Boolean}true"
          dxml.use.publish.microservice.native.pdf="{Boolean}true"
/>
```
