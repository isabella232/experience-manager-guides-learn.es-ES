---
title: Cargar archivos
description: Obtenga información sobre cómo cargar archivos
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---


# Cargar archivos {#id176FF000JUI}

Lo más probable es que tenga un repositorio de contenido DITA existente que desee utilizar con AEM guías. Para dicho contenido existente, puede utilizar cualquiera de los siguientes enfoques para cargar de forma masiva su contenido en AEM repositorio:

>[!IMPORTANT]
>
> Consulte [Adición de recursos digitales a Adobe Experience Manager as a Cloud Service Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html) para obtener información detallada sobre los métodos de carga de contenido admitidos en AEM.

## Interfaz de usuario de la consola Assets

Puede seleccionar contenido en el escritorio y arrastrar la interfaz de usuario AEM \(explorador web\) a la carpeta de destino. Para obtener más información, consulte [Cargar recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html#upload-assets) en AEM documentación.

## aplicación de escritorio AEM

Utilice AEM aplicación de escritorio si es un profesional creativo y desea administrar los recursos en su escritorio local. Puede abrir y editar estos recursos con las aplicaciones de escritorio. También puede mantener versiones y compartir sus archivos con otros usuarios. Para obtener más información, consulte [aplicación de escritorio AEM](https://experienceleague.adobe.com/docs/experience-manager-desktop-app/using/using.html).

## Ingesta masiva de recursos

Si tiene migraciones a gran escala y entradas masivas ocasionales, utilice el importador masivo de recursos para cargar el contenido. Con esta herramienta, puede cargar contenido masivo desde almacenes de datos compatibles, como Azure o S3. Para obtener más información, consulte [Ingesta masiva de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=en#asset-bulk-ingestor).

## Uso de FrameMaker para la carga masiva

Adobe FrameMaker incluye un potente conector de AEM que le permite cargar fácilmente sus documentos DITA y otros documentos de FrameMaker \(`.book` y `.fm`\) en AEM. Puede utilizar varias funcionalidades de carga de archivos, como cargar un solo archivo o cargar una carpeta completa con o sin dependencias \ (como referencias de contenido, referencias cruzadas y gráficos\).

Para obtener más información sobre el uso de la función de carga masiva en FrameMaker, consulte la sección *Crear una carpeta CRX y cargar archivos* en la Guía del usuario de FrameMaker.

## Error al cargar contenido {#id201MI0I04Y4}

En caso de que no se carguen uno o varios archivos, se mostrará una solicitud al final del proceso de carga con una lista de los archivos que no se han cargado:

![](images/uuid-files-failed-to-upload_cs.png){width="650" align="center"}

Para obtener más información sobre los distintos escenarios de carga de archivos, consulte [Cargar contenido DITA](authoring-file-management.md#).

En caso de que utilice una herramienta como AEM aplicación de escritorio o el ingestor masivo de recursos, la acción que se realizará en un archivo duplicado estará controlada por una configuración en el servidor de AEM. Póngase en contacto con el administrador del sistema para obtener información sobre esta configuración.

**Tema principal:**[ Administrar contenido](authoring.md)

