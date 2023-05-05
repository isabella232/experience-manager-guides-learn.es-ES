---
title: Solución de problemas básicos
description: Obtenga información sobre cómo solucionar problemas básicos
exl-id: b5ab2618-6f11-4aaa-8471-09521f8bb512
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Solución de problemas básicos {#id1821I0Y0G0A}

Mientras trabaja con AEM guías, puede encontrar errores al publicar o abrir el documento. Estos errores podrían estar en el mapa DITA, tema o en AEM propio proceso de guías. Esta sección proporciona información sobre cómo acceder y analizar la información en el archivo de registro de generación de salida. Además, si el tema de DITA es demasiado grande, es posible que vea el error de compilación de JSP. Esta sección también proporciona información sobre cómo resolver el error de compilación de JSP.

## Ver y comprobar el archivo de registro {#id1822G0P0CHS}

Realice los siguientes pasos para ver y comprobar el archivo de registro de generación de salida:

1. Una vez iniciado el proceso de generación de resultados, haga clic en **Salidas** en la consola de asignación DITA.

   La variable **General** de **Productos generados** muestra los iconos para proporcionar una pista visual sobre el éxito o el fracaso de la generación de salida.

   ![](images/output-general-settings.png){width="300" align="left"}

   En la captura de pantalla anterior, los iconos primero y tercero muestran la generación de salida fallida. El segundo icono muestra una generación de salida correcta, pero con mensajes. La última es una generación de salida exitosa sin ningún mensaje.

1. Haga clic en el vínculo en la **Generado en** una vez completado el trabajo.

   El archivo de registro se abre en una nueva pestaña.

   ![](images/log-file.png){width="800" align="left"}

1. Aplique los filtros siguientes para resaltar el texto en el archivo de registro:
   - Mortal: Resalta los errores fatales en el archivo de registro con color rosa.
   - Error: Resalta los errores en el archivo de registro con color naranja.
   - Advertencia: Resalta las advertencias en el archivo de registro con color morado.
   - Información: Resalta los mensajes de información del archivo de registro con color azul.
   - Excepción: Resalta las excepciones en el archivo de registro con color amarillo.
1. Utilice los botones de navegación arriba y abajo para saltar al texto resaltado en el archivo de registro.

   También puede desplazarse por el archivo de registro y comprobar los mensajes.


## Copiar y comprobar el archivo de registro en un editor de texto

Realice los siguientes pasos para copiar y comprobar el archivo de registro de generación de salida en un editor de texto:

1. Una vez iniciado el proceso de generación de resultados, haga clic en **Salidas** en la consola de asignación DITA.

1. Haga clic en el vínculo en la **Generado en** una vez completado el trabajo.

   El archivo de registro se abre en una nueva pestaña.

1. Haga clic en **Copiar registro** botón. El archivo de registro se copia en el portapapeles.
1. Abra un editor de texto y pegue el archivo de registro en el editor.

1. Desplácese por el archivo de registro y compruebe si hay mensajes.

   La siguiente información le ayudará a determinar si hay un error en el archivo DITA o en AEM proceso de guías:

   - *Error relacionado con el archivo de asignación DITA*: En caso de que se encuentre un error en el archivo de asignación DITA o en cualquier otro archivo contenido en el mapa DITA, el archivo de registro contendrá una cadena, &quot;COMPILACIÓN FALLIDA&quot;. Puede comprobar la información proporcionada en el archivo de registro para localizar el archivo erróneo y solucionar el problema.

   En el siguiente fragmento de archivo de registro de muestra, puede ver la variable `BUILD FAILED` junto con el motivo del error.

   ![](images/dita-error-in-log-file.png){width="650" align="left"}

   - *Error relacionado con las guías de AEM*: El otro tipo de error que se puede identificar en el archivo de registro está relacionado con AEM propio proceso de guías. En este caso, el archivo de asignación DITA se analiza correctamente, pero el proceso de generación de salida falla debido a algún error interno en las guías de AEM. Para este tipo de errores, debe solicitar ayuda al equipo de asistencia técnica.

   En el siguiente fragmento de archivo de registro de muestra, puede ver la variable `BUILD SUCCESSFUL` , seguido de otro error técnico.

   ![](images/process-error-in-log-file.png){width="650" align="left"}


## Resolver error de compilación de JSP

Si el tema de DITA es demasiado grande, es posible que vea el error de compilación de JSP \(`org.apache.sling.api.request.TooManyCallsException`\) en el explorador. Este error puede aparecer al abrir un tema para editarlo, revisarlo o publicarlo.

Siga estos pasos para resolver este problema:

1. En Navegación global, seleccione Herramientas y elija Operaciones \> Consola web.

   Aparecerá la página Configuración de la consola web de Adobe Experience Manager.

1. Busque y haga clic en el botón *Servlet principal de Apache Sling* componente.

   Se muestran las opciones configurables para el servlet principal de Apache Sling.

1. Aumente el valor de la variable *Número de llamadas por solicitud* según sus necesidades.


**Tema principal:**[ Generación de resultados](generate-output.md)
