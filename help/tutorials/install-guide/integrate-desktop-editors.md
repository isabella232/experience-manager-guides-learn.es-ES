---
title: Integración de editores XML basados en escritorio
description: Aprenda a integrar editores XML basados en escritorio
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# Integración de editores XML basados en escritorio {#id181GB01G0HS}

Hay muchos editores XML disponibles en el mercado, y es posible que ya esté utilizando uno. Adobe FrameMaker AEM es uno de los editores XML más poderosos, que viene con conector de la. AEM AEM Con el conector de la en FrameMaker, puede conectarse fácilmente con el repositorio de la, retirar y registrar archivos, y editar archivos directamente en FrameMaker. AEM También puede configurar guías de usuario para que inicien FrameMaker desde el Editor Web. AEM Una vez abierto el archivo en FrameMaker, puede editarlo y volver a registrarlo en el repositorio de la biblioteca de archivos de la biblioteca de archivos de la biblioteca de la biblioteca de archivos de la biblioteca de archivos de la biblioteca de archivos de la biblioteca de carpetas.

## Habilitar la edición de archivos en FrameMaker desde el Editor Web

Puede utilizar FrameMaker o cualquier otro editor DITA para crear y actualizar contenido DITA. AEM Sin embargo, si su organización utiliza FrameMaker como editor DITA, puede proporcionar a los usuarios una opción para abrir documentos DITA directamente en FrameMaker desde el propio servidor de correo electrónico de.

De forma predeterminada, los usuarios no ven el **Abrir en FrameMaker** AEM en la barra de herramientas de la. AEM Siga estos pasos para agregar este botón en la barra de herramientas de la barra de herramientas de la:

1. Abra la página Configuración de la consola web de Adobe Experience Manager.

   La URL predeterminada para acceder a la página de configuración es:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Busque y haga clic en **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** paquete.

   ![](assets/open-in-fm-toolbar.png){width="550" align="left"}

1. Seleccione el **Mostrar el botón Abrir en FrameMaker** opción.

1. Haga clic en **Guardar**.


Al activar la variable **Mostrar el botón Abrir en FrameMaker** y luego la opción **Abrir en FrameMaker** AEM se muestra al seleccionar cualquier fichero DITA en el repositorio de. Cuando esta opción es *sin activar*, el **Abrir en FrameMaker** El botón solo se muestra al seleccionar un archivo .fm o .book en el repositorio.

