---
title: Configuración del número de LimitReads de una consulta
description: Obtenga información sobre cómo configurar el número de LimitReads para una consulta
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# Configuración del número de LimitReads de una consulta {#id231RC0HL0ID}

Para aumentar el número de nodos que una consulta puede leer a la vez, realice los siguientes pasos:

1. Abra la página Adobe Experience Manager Web Console JMX.

   La URL predeterminada para acceder a la página de configuración es:

   ```http
   http://<server name>:<port>/system/console/jmx
   ```

1. Busque y haga clic en **QueryEngineSettings**.

1. Cambiar el valor del atributo para **LimitReads** atributo.

1. Haga clic en **Guardar**.


Cuando se aumenta este valor de atributo, se ayuda a generar el informe para mapas DITA más grandes.

**Tema principal:**[ Personalizar editor web](conf-web-editor.md)

