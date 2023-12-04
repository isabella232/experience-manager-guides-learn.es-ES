---
title: PDF nativo | Configuración de indicadores JVM para la publicación de PDF nativos
description: Configuración de indicadores JVM para la publicación de PDF nativos
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# Configuración de indicadores JVM para la publicación de PDF nativos

La publicación de PDF nativos inicia un proceso de JVM independiente para generar un PDF. Es posible que tenga que modificar las configuraciones de esta JVM para que admitan diferentes escenarios. Por ejemplo, para ejecutar cargas de trabajo más grandes debe aumentar el tamaño máximo de pila disponible para el proceso de JVM generado.

AEM Realice los siguientes pasos para configurar los indicadores de JVM de publicación de PDF nativo de las guías de:

1. Abra la página Configuración de la consola web de Adobe Experience Manager.

   La URL predeterminada para acceder a la página de configuración es:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Busque y seleccione el *com.adobe.fmdita.config.ConfigManager* paquete.

1. Actualizar la propiedad **Opciones de línea de comandos de Java para el pdf nativo** (*native.pdf.java.opts*) para pasar cualquier indicador JVM estándar.



1. Haga clic en **Guardar**.
