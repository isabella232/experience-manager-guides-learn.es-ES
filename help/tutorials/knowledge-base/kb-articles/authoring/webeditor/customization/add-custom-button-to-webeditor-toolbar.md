---
title: Añadir nuevo botón de acción personalizado en la barra de herramientas de webeditor
description: Aprenda a añadir un nuevo botón personalizado en la barra de herramientas de webeditor e invocar javascript para que lo gestione de forma personalizada.
source-git-commit: 26a6acde54953eab1d751f165d0f7769c7e790fe
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# Añadir nuevo botón de acción personalizado en la barra de herramientas de webeditor

En este artículo aprenderemos a añadir un nuevo botón personalizado en la barra de herramientas de webeditor e invocar javascript para realizar la operación personalizada deseada.

Añadir un botón procesable a webeditor implica los siguientes pasos:
- Adición del botón en la variable *ui_config.json* en la posición en la que sea necesario
- Registro del evento en el que se hace clic del botón en el editor web para que el usuario realice una acción cuando haga clic en él


## Implementación tomando un ejemplo

Comprendamos esto con un ejemplo en el que un autor quiere añadir una referencia de jira a una sección de prólogo de temas. La sección prolog con el id de referencia de jira integrado puede tener el siguiente aspecto:

![Sección Prolog con referencia de ID de JIRA](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-sample.png)

El elemento &quot;change-request-id&quot; que contiene el ID de JIRA debe recuperarse de la API (digamos, en función de una consulta JIRA específica que la aplicación representa). Cuando el usuario está creando la sección de prólogos, debe poder hacer clic en un botón e insertar un id de referencia de jira desde la barra de herramientas del editor web, algo así como:

![Sección Prolog - añadir referencia JIRA](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-insertjirareference.png)

Y cuando el usuario hace clic en el botón, debería mostrar un cuadro de diálogo que debería extraer las opciones posibles y permitir al usuario seleccionar el ID de JIRA deseado, algo así como:

![Sección de Prolog añadir cuadro de diálogo de JIRA ID](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-insertjirareference-dialog.png)

que luego debe agregar el &quot;change-request-id&quot; al prolog:

![Sección Prolog con referencia de ID de JIRA](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-sample.png)



## Implementación de


### Agregue el botón en webeditor configurándolo en *ui_config.json*

Utilice los perfiles de carpeta para comprobar la variable *ui_config.json* en la pestaña &quot;Configuración del editor XML&quot; y añada la configuración del botón JSON a la sección deseada del grupo &quot;barra de herramientas&quot;

```
{
    "on-click":"insertJIRARef",
    "icon":"linkCheck",
    "variant":"quiet",
    "type":"button",
    "title":"Insert JIRA Reference"
}
```

[utilice este vínculo para obtener más información sobre el perfil de carpeta y la configuración de ui_config.json](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/videos/advanced-user-guide/editor-configuration.html?lang=en)


### Gestión del evento en el que se hace clic para el nuevo botón

    NOTA: Los pasos mencionados a continuación están disponibles como paquete adjunto en esta publicación


- Después de guardar el perfil de carpeta, cree un &quot;cq:ClientLibraryFolder&quot; en un directorio de proyecto (podría estar en */apps*) y añada propiedades como se muestra en la captura de pantalla siguiente:
   ![Configuración de la biblioteca de cliente para webeditor](../../../assets/authoring/webeditor-add-customtoolbarbutton-clientlibrarysettings.png)

```
This example uses "coralui3" library to show a dialog as it is used in the Javascript sample we presented.
You may use different library of your choice.
```

- En esta carpeta de biblioteca de cliente, cree dos archivos como se indica a continuación:
   - *overrides.js*: que tendrá el código javascript para gestionar el evento en el que se hace clic para &quot;insertJIRARef&quot; (utilice el paquete adjunto para obtener el contenido de este javascript)
   - *js.txt*: que incluirá &quot;overrides.js&quot; para habilitar este javascript

- Guarde los cambios y debe estar listo para probarlos.


### Pruebas

- Abrir editor web
- En las preferencias del usuario, elija el perfil de carpeta en el que ha añadido la variable *ui_config.json*. Si lo agregó al perfil Global , probablemente ya esté usando eso.
- Abra un tema, verá que la barra de herramientas tiene un nuevo botón &quot;Insertar referencia de Jira&quot;
- A continuación, puede agregar la sección de prólogos como se indica a continuación al tema e intentar hacer clic en el botón &quot;Insertar referencia de Jira&quot; dentro del elemento de prolog &quot;change-request-reference&quot;

```
<prolog>
    <change-historylist>
        <change-item>
            <change-request-reference>
            </change-request-reference>
            <change-completed></change-completed>
            <change-summary></change-summary>
        </change-item>
    </change-historylist>
</prolog>
```

Consulte la captura de pantalla siguiente para saber cómo se verá:

![Botón Probar nuevo](../../../assets/authoring/webeditor-add-customtoolbarbutton-testing.png)


### Archivos adjuntos

- Paquete clientlibs de muestra que instalará la biblioteca cliente de webeditor con código javascript para la acción del botón de barra de herramientas: [descargar con este vínculo](../../../assets/authoring/webeditor-addbuttonontoolbar-insertjira-clientlib.zip)
- Ejemplo *ui_config.json* que puede cargar en un perfil de carpeta: [descargar ejemplo ui_config.json](../../../assets/authoring/sample_ui_config_Guides4.2-InsertJiraReference.json)

```
Please note this is compatible to AEM 6.5 and AEM Guides version 4.2.
If you are using a different version please add the toolbar button to the ui_config.json manually.
```
