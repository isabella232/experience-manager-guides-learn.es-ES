---
title: Complemento Oxygen para las guías de Adobe Experience Manager
description: Aprenda a utilizar el complemento de Oxygen para las guías de Adobe Experience Manager para crear y administrar su contenido.
hide: true
hidefromtoc: true
source-git-commit: 96347fed96979eb735dc55c32fcda90cc70ddcb4
workflow-type: tm+mt
source-wordcount: '5762'
ht-degree: 1%

---


# Complemento Oxygen para las guías de Adobe Experience Manager {#id1645H6010Q5}

El complemento Oxygen para las guías de Adobe Experience Manager \ (denominado posteriormente complemento de oxígeno para guías AEM en la guía\) le permite conectar el Autor XML de Oxygen con el repositorio de Adobe Experience Manager \(AEM\) para la creación y administración de contenido. Puede utilizar el complemento para examinar, buscar y abrir archivos; archivos de registro y registro; cargar carpetas y archivos en AEM repositorio. El panel AEM guías de la aplicación de escritorio le permite marcar las carpetas deseadas \(desde AEM repositorio\) a la lista de carpetas favoritas para un acceso rápido. Además, puede instalar un paquete en AEM interfaz web y abrir sus archivos DITA en Oxygen XML Author directamente desde la interfaz web de AEM.

## Descargar e instalar {#id1826M0L0PUI}

El plug-in de oxígeno para guías AEM está disponible a través de su portal de distribución de software de Adobe. Busque &quot;oxígeno&quot; en la pestaña del Experience Manager y, a continuación, descargue el instalador del complemento de su [Portal de distribución de software de Adobe](https://experience.adobe.com/#/downloads/content/software-distribution/en/general.html).

>[!NOTE]
>
>Compruebe la compatibilidad de la versión del conector de oxígeno en las notas de la versión de las guías específicas de Adobe Experience Manager.

Una vez que tenga el instalador, instálelo en su equipo local donde está instalado Oxygen XML Author . Antes de comenzar el proceso de instalación, debe asegurarse de que su sistema cumpla los requisitos técnicos para instalar el plugin de oxígeno para AEM guías.

### Requisitos técnicos

- Oxygen XML Author versión 24.1

- Guías de Adobe Experience Manager versión 3.4 o superior

- Adobe Experience Manager versión 6.5 con Service Pack 10, 11, 12 y 13

- Sistema operativo compatible con Oxygen XML Author versión 24.1

- Kit de desarrollo de Java
   - Oracle SE 8 JRE 1.8

### Instalar el complemento en Windows

>[!IMPORTANT]
>
>Si tiene instalada una versión anterior del complemento en su sistema, asegúrese de desinstalarlo antes de iniciar el proceso de instalación. Consulte la **Desinstalación de paquetes** en la sección [Cómo trabajar con paquetes](https://helpx.adobe.com/es/experience-manager/6-4/sites/administering/using/package-manager.html) para instrucciones de desinstalación.

Realice los siguientes pasos en el sistema en el que está instalado Oxygen XML Author:

1. Inicie el `.exe` archivo.

   Aparecerá la pantalla de bienvenida del asistente de instalación.

1. Haga clic en **Siguiente** y busque la ubicación en la que está disponible el archivo .exe de Oxygen XML Author.

1. Seleccione el archivo y haga clic en **Apertura**.

   La ubicación del archivo seleccionado se agrega en el asistente de instalación.

1. Haga clic en **Siguiente**.

1. Haga clic en **Instalar**.

1. Haga clic en **Finalizar** para cerrar el asistente de instalación.
1. Inicie Oxygen XML Author.

   El panel Guías de AEM se muestra en el Autor XML de Oxygen.

   ![](images/oxygen-aem-connector.png)

   >[!NOTE]
   >
   >Si no ve el panel Guías de AEM, consulte las soluciones alternativas en la sección Solución de problemas:[Falta el panel Guías AEM](#id192BH200ZAX).


### Instalación del complemento en Mac

>[!IMPORTANT]
>
>Si tiene instalada una versión anterior del complemento en su sistema, asegúrese de desinstalarlo antes de iniciar el proceso de instalación. Consulte la **Desinstalación de paquetes** en la sección [Cómo trabajar con paquetes](https://helpx.adobe.com/es/experience-manager/6-4/sites/administering/using/package-manager.html) instrucciones de desinstalación del artículo.

Realice los siguientes pasos en el sistema en el que está instalado Oxygen XML Author:

1. Localice el archivo .dmg del complemento en su sistema.

1. Haga doble clic en el archivo .dmg para abrir el contenido del archivo.

   El archivo .dmg contiene una carpeta aem-connector-x.x y un archivo aem-connector-x.x-setup.

   >[!NOTE]
   >
   >x.x en los nombres de archivo es el número de versión del complemento.

1. Copie la carpeta aem-connector-x.x en la carpeta plugins de Oxygen XML Author.
1. Haga doble clic en el archivo de configuración aem-connector-x.x-setup para iniciar el instalador.

1. Inicie Oxygen XML Author.

   El panel Guías de AEM se muestra en el Autor XML de Oxygen.

   ![](images/oxygen-aem-connector-mac.png)

   >[!NOTE]
   >
   >Si no ve el panel Guías de AEM, consulte las soluciones alternativas en la sección Solución de problemas:[Falta el panel Guías AEM](#id192BH200ZAX).


### Instale el paquete para activar la función de edición de documentos desde AEM interfaz web {#id182CE0Q0TY4}

Como autor, puede abrir y editar sus mapas o temas DITA en Oxygen XML Author directamente desde la interfaz web AEM. Para habilitar esta función en AEM interfaz web, el administrador de AEM debe instalar un paquete en la instancia de creación de AEM.

Como administrador de AEM, realice los siguientes pasos para instalar el paquete:

1. Obtenga el archivo .zip del paquete de su equipo de TI.
1. Inicie sesión en la instancia de AEM *\(como administrador\)* y vaya al Administrador de paquetes CRX. La dirección URL predeterminada para acceder al administrador de paquetes es

   `http://<server name>:<port>/crx/packmgr/index.jsp`

   El Administrador de paquetes administra los paquetes en la instalación AEM local. Para obtener más información sobre cómo trabajar con el Administrador de paquetes, consulte [Cómo trabajar con paquetes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developer-tools/package-manager.html?lang=en) en AEM documentación.

   ![](images/package-manager.png)

1. Para cargar el paquete Oxygen, haga clic en **Cargar paquete**.
1. En el cuadro de diálogo Cargar paquete , vaya al archivo del paquete de Oxygen que descargó en el paso 1 y haga clic en Aceptar.

   El paquete se carga en la instancia de AEM.

1. Para iniciar el proceso de instalación, haga clic en **Instalar**.

   ![](images/oxygen-package.png)

1. En el cuadro de diálogo Instalar paquete , haga clic en **Instalar**.
1. Una vez finalizada la instalación, haga clic en el botón Home en la esquina superior izquierda del Administrador de paquetes CRX.
1. Seleccione un archivo DITA en la carpeta de recursos.

   **Editar en oxígeno** está disponible en la barra de herramientas. Para obtener más información sobre el uso de esta opción, consulte [Abrir tema DITA en Oxygen XML Author desde AEM interfaz web](#id182CE0I905Z).

   >[!NOTE]
   >
   >La variable **Editar en oxígeno** está visible al seleccionar un tema DITA. Si selecciona varios temas, la opción no estará visible.


## Configuración del complemento de oxígeno para las guías de AEM {#id1826KF00AHS}

Después de descargar e instalar el complemento, debe configurar lo siguiente para que funcione con el complemento:

- **Configuración de autenticación web**: Configuración de la autenticación SSO en el complemento para AEM guías.
- **Configuración general**: Configuración de conexión para el complemento, como AEM URL del servidor, detalles de inicio de sesión, etc.
- **Preferencia para la personalización de atributos de creación de perfiles**: Esta configuración es necesaria para los esquemas de atributos de creación de perfiles de los conjuntos de documentación.

### Configuración de autenticación web

JxBrowser se utiliza para la autenticación SSO mediante el complemento conector Oxygen. Es un navegador basado en cromo. Para java 9+, se requiere acceso a API no públicas y el usuario debe conceder explícitamente este acceso a JxBrowser. Para obtener más información, consulte [Solución de problemas del explorador Jx](https://jxbrowser-support.teamdev.com/docs/guides/troubleshooting/issues.html).

Actualice los archivos dados para configurar la configuración de autenticación web en el complemento de oxígeno para las guías de AEM:

>[!NOTE]
>
>Haga una copia de seguridad del archivo antes de actualizarlo.

**Para Mac y oxígeno 24.1**

Añada las siguientes líneas en env.sh

```java
--illegal-access=permit\
--add-opens=java.desktop/javax.swing.plaf.basic=ALL-UNNAMED\
--add-exports=javafx.controls/com.sun.javafx.scene.control=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.stage=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.scene=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.scene.traversal=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.tk=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED\
--add-opens=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED\
--add-opens=javafx.graphics/javafx.stage=ALL-UNNAMED\
--add-opens=javafx.graphics/com.sun.javafx.tk.quantum=ALL-UNNAMED\
--add-exports=java.desktop/sun.awt=ALL-UNNAMED\
--add-opens javafx.swing/javafx.embed.swing=ALL-UNNAMED
```

Añada las siguientes líneas en el archivo oxigenAuthor.sh

```java
-Djdk.module.illegalAccess=permit\-Djava.ipc.external=true\
```

**Para Windows y Oxígeno 24.1**

Añada las siguientes líneas en env.bat

```java
--illegal-access=permit --add-opens=java.desktop/javax.swing.plaf.basic=ALL-UNNAMED --add-exports=javafx.controls/com.sun.javafx.scene.control=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.stage=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.scene=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.scene.traversal=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.tk=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED --add-opens=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED --add-opens=javafx.graphics/javafx.stage=ALL-UNNAMED --add-opens=javafx.graphics/com.sun.javafx.tk.quantum=ALL-UNNAMED --add-exports=java.desktop/sun.awt=ALL-UNNAMED --add-opens javafx.swing/javafx.embed.swing=ALL-UNNAMED
```

Añada las siguientes líneas en el archivo oxigenAuthor.bat

```java
-Djdk.module.illegalAccess=permit -Djava.ipc.external=true
```

>[!NOTE]
>
>Se debe ejecutar oxígeno desde oxigenAuthor.sh para Mac y oxigenAuthor.bat para Windows como administrador.

### Configuración general

Realice los siguientes pasos para configurar la configuración de conexión en el complemento de oxígeno para las guías de Adobe Experience Manager:

1. En el panel AEM guías, haga clic en el icono de configuración y, a continuación, seleccione **Configuración**.

   ![](images/settings.png)

1. Especifique los siguientes detalles:
   - **URL del servidor**: URL del servidor de AEM, por ejemplo:

      ```http
      http[s]://<host>:<port>
      ```

      En la URL anterior, especifique el nombre de host y el puerto del servidor donde se implementa AEM servidor.

      >[!IMPORTANT]
      >
      >Si el servidor de AEM está implementado en el puerto 80 o 443, no es necesario especificarlo en la dirección URL.

   - **Autenticación:** Elija entre **\(Nombre de usuario/contraseña\) básico** o **Autenticación web**. En caso de que seleccione **Básico** autenticación que debe introducir la variable **Nombre de usuario** y **Contraseña** en el cuadro de diálogo Preferencias.

      Si selecciona Autenticación web, se mostrará la pantalla Inicio de sesión AEM. Introduzca sus credenciales de inicio de sesión y haga clic en el botón **Iniciar sesión** botón. Cuando el inicio de sesión se realiza correctamente, se cierra la pantalla Inicio de sesión de AEM y el panel Guías de AEM muestra la lista de archivos del servidor de AEM.

   - **Tiempo de espera de conexión**: Especifique el tiempo en segundos que el cliente esperará para recibir una respuesta del servidor de AEM. En caso de que no se reciba ninguna respuesta del servidor dentro del tiempo especificado, la solicitud se finaliza. El valor predeterminado es 20 segundos.

   - **Carpeta local**: Ubicación en el equipo local donde los archivos de AEM repositorio se almacenan después de la cierre de compra. Si especifica una ubicación que no existe en la unidad, el complemento crea esa ubicación.
   - **Abrir archivo cuando esté desprotegido**: Si está seleccionado, abre los archivos al cerrar la compra.
   - **Cerrar archivo al proteger**: Si está seleccionado, cierra los archivos al registrarse. Antes de cerrar el archivo, se muestra una ventana emergente en la que puede especificar los comentarios de la versión.
   - **Mostrar cuadro de diálogo de activación al cerrar archivo**: Si está seleccionado, aparece una ventana emergente al cerrar un archivo. Desde la ventana emergente, puede elegir entre proteger el archivo o cerrarlo sin proteger.
   - **Archivo de cierre de compra automático al abrirlo**: Si se selecciona, al hacer doble clic en un archivo, se cierra la compra automáticamente y se abre para su edición. Si el archivo ya está desprotegido, simplemente se abre para editarlo. Si esta opción no está seleccionada, al abrir un archivo en el que no tiene un bloqueo se abre en modo de solo lectura.
1. Haga clic en **Aceptar**.

### Preferencia para la personalización de atributos de creación de perfiles {#id1827K0D0OHT}

Debe configurar las preferencias en Oxygen XML Author para utilizar el atributo de perfil asociado con los temas de DITA en el repositorio de AEM.

Siga estos pasos para configurar los atributos de perfil:

1. En Oxygen XML Author, haga clic en **Opciones** \> **Preferencias**.
1. En el **Asociación de tipo de documento** , seleccione **DITA** y, a continuación, haga clic en **Ampliar**.

   ![](images/document_type_association.png)

1. En el **Classpath** seleccione com.adobe.o2.connector en la pestaña **Usar el cargador de clase principal desde el complemento con ID** lista desplegable.

   ![](images/dita-extension.png)

1. En el **Extensiones** , realice los siguientes cambios:
1. 
   - Haga clic en **Choose** junto a la variable **Receptor de estado de extensión de autor** under **Extensiones individuales** y seleccione CustomAuthorExtensionStateListener - com.adobe.o2.framework.extn en la **Clase** lista. Haga clic en **Aceptar**.
- Haga clic en **Choose** junto a la variable **Editor de valores de atributos personalizados de autor** under **Extensiones individuales** y seleccione CustomValueEditor - com.adobe.o2.framework.extn en la **Clase** lista. Haga clic en **Aceptar**.
La siguiente captura de pantalla muestra la configuración de **Extensión** para temas DITA:

   ![](images/dita-topic-extension-tab.png)

1. Haga clic en **OK** en todos los cuadros de diálogo para guardar los cambios.

### Configurar la extensión de mapa DITA

La configuración de la extensión de mapa DITA es necesaria para permitir la apertura de archivos de mapa en Oxygen XML Author directamente desde la interfaz web AEM. Estas configuraciones son similares a las configuraciones para perfiles realizadas en el procedimiento anterior.

Realice los siguientes pasos para configurar la extensión de mapa DITA:

1. En Oxygen XML Author, haga clic en **Opciones** \> **Preferencias**.
1. En el **Asociación de tipo de documento** , seleccione **Mapa DITA** y, a continuación, haga clic en **Ampliar**.
1. En el **Classpath** seleccione com.adobe.o2.connector en la pestaña **Usar el cargador de clase principal desde el complemento con ID** lista desplegable.
1. En el **Extensiones** , realice los siguientes cambios:
1. 
   - Haga clic en **Choose** junto a la variable **Receptor de estado de extensión de autor** under **Extensiones individuales** y seleccione CustomDITAMapAuthorExtensionStateListener - com.adobe.o2.framework.extn en la **Clase** lista. Haga clic en **Aceptar**.
- Haga clic en **Choose** junto a la variable **Editor de valores de atributos personalizados de autor** under **Extensiones individuales** y seleccione CustomValueEditor - com.adobe.o2.framework.extn en la **Clase** lista. Haga clic en **Aceptar**.
- *\(Opcional\)* Si no desea resolver referencias al abrir un archivo de mapa, debe realizar la siguiente configuración adicional:

   Haga clic en **Choose** junto a la variable **Resolución de referencias** under **Extensiones individuales** y seleccione CustomDITAMapReferenceResolver - com.adobe.o2.framework.extn en la **Clase** lista. Haga clic en **Aceptar**.

   La siguiente captura de pantalla muestra la configuración de **Extensión** pestaña:

   ![](images/dita-map-extension-tab.png)

1. Haga clic en **OK** en todos los cuadros de diálogo para guardar los cambios.

## Trabajar con el plugin de oxígeno para AEM guías {#id1826JG00WY4}

### Panel de guías de AEM

La siguiente pantalla muestra el panel Guías de AEM.

![](images/connector-panel.png)

**A**\) Muestra la barra de búsqueda.

**B**\) Muestra la carpeta Favoritos. De forma predeterminada, está vacío. Puede agregar carpetas desde el repositorio de AEM como favorita, las carpetas favoritas se muestran aquí.

**C**\) La carpeta DAM muestra el repositorio AEM. Puede expandir y contraer la vista de carpetas.

**D**\) El icono Configuración \(engranaje\) con las siguientes opciones:

- **Connect**: Seleccione esta opción para conectarse al servidor de AEM. La opción está desactivada cuando Oxygen XML Author está conectado al servidor de AEM.
- **Actualizar**: Seleccione esta opción para obtener el estado más reciente de los archivos y la carpeta desde el repositorio de AEM.

   >[!NOTE]
   >
   >Asegúrese de guardar los archivos antes de actualizarlos. Al seleccionar **Actualizar** , recibe una advertencia para guardar los archivos antes de actualizarlos. Si no ha guardado los archivos, puede hacer clic en **Cancelar** y guárdelos.

- **Configuración**: Puede utilizar esta opción para abrir el cuadro de diálogo Preferencias generales del complemento.
- **Cerrar sesión**: Seleccione esta opción para cerrar la conexión AEM servidor. Esta opción solo está disponible si utiliza el modo de autenticación web.

### Funciones del menú contextual

Las funciones del complemento Oxygen para guías AEM están disponibles al hacer clic con el botón derecho en una carpeta o archivo del repositorio de AEM. Las funciones disponibles para las carpetas son diferentes de los archivos. A continuación se muestra una lista completa de las funciones del complemento de oxígeno para AEM menú contextual de guías:

- **Apertura**: Abre el archivo seleccionado o expande la carpeta seleccionada.
- **Abrir en**: Puede elegir abrir el archivo seleccionado en el Editor web de guías de AEM o en el tablero de mapas o en el Editor de mapas. Para obtener más información sobre estas opciones, consulte [Abrir archivo en el editor de guías de AEM](#id195GH0V30KX).
- **Extracción**: Extrae un archivo de AEM repositorio. Para obtener más información, consulte [Archivos de desprotección](#id195HC020TS4).
- **Extracción con dependientes**: Extrae un archivo con sus referencias directas. Para obtener más información, consulte [Archivos de desprotección](#id195HC020TS4).
- **Extracción con dependientes de solo lectura**: Extrae el archivo seleccionado junto con sus archivos dependientes. No puede realizar ningún cambio en los archivos dependientes. Para obtener más información, consulte [Archivos de desprotección](#id195HC020TS4).
- **Cancelar desprotección**: Cancela el archivo extraído, cierra el archivo desde el editor y revierte los cambios a la última versión del archivo guardado en el servidor.
- **Actualizar**: En el caso de un archivo, obtiene la última copia del archivo desde el repositorio de AEM. Para una carpeta, se obtiene la estructura de carpetas y el estado del archivo. Esto significa que se agrega un archivo y se muestra en la vista de guías AEM. Además, si un archivo está desprotegido en AEM servidor, al realizar una actualización en Oxygen Author, se mostrará el archivo como desprotegido. Sin embargo, esto no actualiza la lista de archivos en la variable *Archivos extraídos en AEM guías* Ver.
- **Actualizar archivos extraídos**: Actualiza la lista de archivos extraídos en el *Archivos extraídos en AEM guías* Ver. Si un archivo está desprotegido en AEM servidor, al realizar una actualización se actualizará la lista de archivos desprotegidos en la *Archivos extraídos en AEM guías* Ver. Sin embargo, si se ha agregado un nuevo archivo o el estado de un archivo ha cambiado, no se actualiza en la vista de árbol de las guías de AEM. Para actualizar el estado de los archivos en AEM, debe realizar una actualización.
- **Registro**: Protege los archivos que ha desprotegido. Para obtener más información, consulte [Insertar un archivo](#id182CF0J0FHS).
- **Registro con dependientes**: Si ha extraído archivos con dependientes, esta opción comprueba el archivo principal junto con sus dependientes. Para obtener más información, consulte [Insertar un archivo](#id182CF0J0FHS).
- **Crear carpeta**: Crea una carpeta en el repositorio de AEM. Esta opción solo está disponible en el nivel de carpeta.
- **Cargar archivo\(s\)**: Carga uno o varios archivos. Para obtener más información, consulte [Cargar archivos y carpetas](#id195HC03F03J).
- **Cargar con dependientes**: Carga archivos DITA \(XML, DITA, Book map o DITA map\) con sus dependientes. Para obtener más información, consulte [Cargar archivos y carpetas](#id195HC03F03J).
- **Cargar carpeta**: Carga una carpeta en el repositorio de AEM. Para obtener más información, consulte [Cargar archivos y carpetas](#id195HC03F03J).
- **Agregar a favoritos**: Agrega una carpeta a la *Favoritos* en el panel Guías de AEM. Se recomienda añadir la carpeta de trabajo aquí, lo que facilita la sincronización de archivos y el estado del archivo desde AEM.
- **Eliminar de Favoritos**: Quita una carpeta de *Favoritos*. Para obtener más información, consulte [Agregar o quitar favoritos](#id195HC04405P).
- **Ver metadatos**: Muestra los metadatos, como la clase DITA, el título, el tipo, el UUID y otra información asociada a un archivo. Para obtener más información, consulte [Ver los metadatos de un archivo](#id195GHN0H05C).
- **Ver versiones**: Muestra el historial de versiones de un archivo. Para obtener más información, consulte [Ver el historial de versiones de un archivo](#id195GI000D5Q).

### Abrir un archivo en Oxygen XML Author {#id195GHJ0A0UB}

Una vez que se haya conectado al repositorio de AEM, puede abrir archivos para editarlos en el Autor XML de Oxygen. Realice los siguientes pasos para abrir un archivo para editarlo en el Autor XML de Oxygen:

1. Haga clic con el botón derecho en un archivo del panel Guías de AEM que desee abrir para editarlo.

1. Select **Apertura** en el menú contextual.

   El archivo se abre en el editor de Oxygen XML Author.

   ![](images/guid-in-file-tab.png)

   Cuando pasa el puntero del ratón sobre la ficha de un archivo, se muestra la ruta del servidor junto con su UUID. En la captura de pantalla anterior, se resalta el UUID del documento.


Si ha seleccionado la variable **Archivo de cierre de compra automático al abrirlo** opción \(en el cuadro de diálogo Preferencias\), al abrir un archivo, éste se extrae automáticamente y está disponible para edición. Para abrir un archivo, puede hacer doble clic en el nombre de un archivo o hacer clic con el botón derecho en el nombre del archivo y seleccionar **Apertura** en el menú contextual. Si esta opción no está seleccionada, el archivo se abre en modo de solo lectura.

>[!NOTE]
>
>También puede hacer doble clic en un archivo para abrirlo.

### Abrir archivo en el editor de guías de AEM {#id195GH0V30KX}

Si desea utilizar los editores disponibles en AEM guías, puede hacerlo seleccionando la opción requerida en el menú contextual. Realice los siguientes pasos para utilizar AEM editor de guías en lugar del editor de Oxygen XML Author:

1. Haga clic con el botón derecho en un archivo del panel Guías de AEM que desee abrir para editarlo.

1. Select **Abrir en** en el menú contextual y elija entre las siguientes opciones:

   - **Editor de temas web**: Si el archivo que está abriendo es un archivo .xml o .dita, puede abrirlo para editarlo en el Editor web. Elija la **Editor de temas web** para abrir el archivo seleccionado y editarlo en el Editor web.

   - **Asignar tablero**: Puede elegir editar un archivo .ditamap en el panel de mapas, donde puede realizar diversas operaciones en el archivo de mapa. Estas operaciones dependen del rol o grupo al que pertenezca.

   - **Editor de mapas DITA web**: Si desea abrir el archivo .ditamap para editarlo en el Editor de mapas, elija esta opción. Con la opción Editor de mapas DITA, puede agregar o quitar temas, agregar tablas de relación y realizar otras operaciones en el mapa.


### Archivos de desprotección {#id195HC020TS4}

Cuando cierra la compra de un archivo, se almacena localmente en el sistema y se bloquea para editarlo en el repositorio de AEM. Realice los siguientes pasos para extraer un archivo:

1. Haga clic con el botón derecho en un archivo del panel Guías de AEM.
1. Seleccione una de las siguientes opciones:
   - **Extracción:** Extrae un archivo de AEM repositorio y lo pone a disposición para su edición.
   - **Extracción con dependientes**: Extrae un archivo con sus referencias directas. Puede realizar cambios en las páginas principales y secundarias mediante esta opción. El plugin de oxígeno para AEM guías permite extraer un nivel de dependientes. Por ejemplo, Asignación A hace referencia al Tema A y el Tema A hace referencia al Tema B. Si se desconecta Mapa A, se retirará el Tema A independientemente de su nivel en la jerarquía de TDC. Sin embargo, no retirará el Tema B porque no está directamente vinculado desde el Mapa A.
   - **Extracción con dependientes de solo lectura**: Extrae un archivo y descarga sus archivos dependientes a su equipo local como copias de solo lectura. No puede realizar ningún cambio en los archivos dependientes.

Si ha seleccionado la variable **Abrir archivos al cierre de compra** opción \(en el cuadro de diálogo Preferencias\) y, al retirar un archivo, el archivo se abre automáticamente para su edición.

Si ha seleccionado la variable **Archivo de cierre de compra automático al abrirlo** opción \(en el cuadro de diálogo Preferencias\), al abrir el archivo, éste se desprotege automáticamente y está disponible para edición. Para abrir un archivo, puede hacer doble clic en el nombre de un archivo o hacer clic con el botón derecho en el nombre del archivo y seleccionar **Apertura** en el menú contextual.

Cuando se extrae un archivo, el icono del archivo cambia para mostrar su estado de bloqueo.

![](images/check-out-file.png)

En la captura de pantalla anterior, un archivo extraído por otro usuario se muestra con un icono de candado de color negro \(A\). El archivo extraído por el usuario actual se muestra con un bloqueo de color verde \(B\).

>[!NOTE]
>
>Si el archivo extraído se elimina o se mueve a cualquier otra carpeta de AEM, aparecerá un mensaje de error al proteger el archivo. Asegúrese de que el archivo extraído no se mueva ni elimine mediante la interfaz web de AEM.

### Insertar un archivo {#id182CF0J0FHS}

Al registrar un archivo, la copia local del sistema se almacena en el repositorio de AEM y se elimina el bloqueo del archivo. Realice los siguientes pasos para proteger un archivo:

1. Guarde el archivo haciendo clic en **Archivo** \> **Guardar**.

1. Haga clic con el botón derecho en un archivo extraído y elija entre las dos opciones siguientes:

   - **Registro**: Registra el archivo seleccionado del sistema local en AEM repositorio.
   - **Registro con dependientes:** Si ha extraído un archivo junto con sus archivos dependientes, utilice esta opción para proteger todos los archivos dependientes en una sola operación. Al seleccionar esta opción, se muestra el cuadro de diálogo Registro con todos los archivos dependientes. Haga clic en Aceptar para registrar todos los archivos a la vez.

   Si no ha extraído los archivos dependientes y luego elige esta opción, solo se registrarán los archivos dependientes que haya extraído \(separadamente\). Se mostrará una lista de archivos que no se pudieron registrar:

   ![](images/check-in-error.png)

   Se recomienda no mover un archivo que esté desprotegido. Sin embargo, si un archivo extraído se mueve a una ubicación diferente, debe cancelar la compra de ese archivo. Si desea realizar actualizaciones en ese archivo, vuelva a desproteger el archivo, realice cambios y vuelva a comprobarlo. Si intenta registrar un archivo que se ha movido de su ubicación original, obtendrá un error.

   Si se extrae un archivo dependiente en AEM, el registro con dependientes no mostrará el archivo dependiente en el cuadro de diálogo Registro. Para obtener una lista de los archivos dependientes que están desprotegidos en AEM, debe actualizar la carpeta.

   Del mismo modo, si ha registrado un archivo dependiente a través de AEM, la lista de archivos no se actualiza en Oxygen Author hasta que realice una actualización y actualización de los archivos extraídos. Si realiza un registro con Dependentes con algunos archivos registrados a través de AEM, obtendrá un error enumerando los archivos que no se pudieron registrar.

1. \(Opcional\) En el cuadro de diálogo Registro, agregue un comentario en **Comentarios de la versión** cuadro de texto.

   >[!NOTE]
   >
   >Este comentario se muestra en el historial AEM versión del archivo.

1. Haga clic en **Aceptar**.

>[!NOTE]
>
>Si el archivo extraído se elimina o se mueve a cualquier otra carpeta de AEM, aparecerá un mensaje de error al proteger el archivo. Asegúrese de que el archivo extraído no se mueva ni elimine mediante la interfaz web de AEM.

### Archivos extraídos en AEM vista de guías

Cuando se tiene en varias carpetas, no es fácil averiguar cuántos archivos se extraen en una vista. AEM guías proporciona archivos extraídos en AEM vista de guías, que proporciona una instantánea completa de los archivos retirados actualmente. Con esta vista, puede averiguar fácilmente qué archivos ha comprobado en AEM repositorio utilizando las guías de AEM. Realice los siguientes pasos para acceder a esta vista y trabajar con ella:

1. Haga clic en **Ventana** \> **Mostrar vista** \> **Archivos extraídos en AEM guías**.

   Se muestra la vista Archivos extraídos en AEM guías.

   ![](images/files-checkedout-view.png)

1. Haga clic con el botón derecho en un archivo de esta vista para obtener las siguientes opciones:

   - [Abrir](#id195GH0V30KX)
   - [Abrir en](#id195GH0V30KX)
   - Cancelar desprotección
   - [Registro](#id182CF0J0FHS)
   - [Registro con dependientes](#id182CF0J0FHS)
   - [Ver metadatos](#id195GHN0H05C)
   - [Ver versiones](#id195GI000D5Q)

**Notas sobre los archivos extraídos en AEM vista de guías:**

- La variable *Archivos extraídos en AEM guías* Ver mantiene las sesiones del usuario. Esto significa que los archivos extraídos por el usuario actual se almacenan y mantienen en la vista en las mismas sesiones \(o caché\) del usuario.

- Si el usuario cambia las credenciales de inicio de sesión o el servidor de AEM, se restablecen los datos \(o la caché\) del archivo extraído en la vista. El usuario debe ejecutar manualmente un *Actualizar archivos extraídos* en cada carpeta desde la que se desprotegieron los archivos anteriormente. Para simplificar esto, se recomienda añadir las carpetas de trabajo a *Favoritos* desde donde puede actualizar rápidamente la carpeta.

- Puede ordenar la lista de archivos en función de sus nombres de archivo, título o ruta. Si se extrae un nuevo archivo, éste aparece en orden ordenado en la vista.


### Carga de archivos y carpetas {#id195HC03F03J}

Siga estos pasos para cargar archivos o carpetas:

1. Haga clic con el botón derecho en una carpeta del panel Guías de AEM.
1. Seleccione una de las siguientes opciones:
   - **Cargar archivo\(s\)**: Seleccione esta opción para cargar uno o varios archivos en la carpeta seleccionada del repositorio de AEM. En el cuadro de diálogo Seleccionar archivos \(s\) para cargar, seleccione los archivos y haga clic en **Apertura**.
   - **Cargar con dependientes**: Seleccione esta opción para cargar un archivo DITA con sus dependientes. En el cuadro de diálogo Seleccionar archivo para cargar, seleccione los archivos y haga clic en **Apertura**.
   - **Cargar carpeta**: Seleccione esta opción para cargar una carpeta en el repositorio de AEM. En el cuadro de diálogo Elegir, seleccione la carpeta y haga clic en **Choose**.

**Notas adicionales sobre el trabajo con archivos basados en UUID**:

Se deben tener en cuenta los siguientes puntos al mover o copiar contenido desde el sistema local al repositorio de AEM:

- Al cargar uno o varios archivos, se genera un nuevo UUID para los archivos que no tengan ningún UUID. Este UUID se agrega en la variable `topic id` de un archivo DITA.

- Al copiar una carpeta, las referencias a los archivos \(dentro de la carpeta\) se actualizan automáticamente en todas las asignaciones DITA que hacen referencia a los archivos de esa carpeta.

- Al copiar un archivo de asignación DITA, las referencias UUID dentro del archivo de asignación no se cambian.

- Si un archivo o una carpeta tiene un conflicto o un duplicado, se genera un nombre de archivo único para el nuevo archivo que se está copiando o moviendo.

- Dos archivos no pueden tener el mismo UUID. Se asigna un UUID único a todos los archivos nuevos.

- Si en caso de que dos usuarios diferentes estén cargando un archivo al mismo tiempo, el archivo que se procesa posteriormente sobrescribe el archivo anterior. Sin embargo, debe evitarse esa práctica.

- Cuando cierre la compra de contenido desde AEM repositorio y realice cambios en el sistema local, asegúrese de que el nombre del archivo no cambie en el momento de cargarlo.


### Agregar o quitar favoritos {#id195HC04405P}

Siga los siguientes pasos para agregar o quitar una carpeta de la carpeta Favoritos del panel Guías de AEM:

- Haga clic con el botón derecho en una carpeta y seleccione **Agregar a favoritos**. Puede agregar una carpeta a favoritos si no está en Favoritos.
- Puede quitar una carpeta de favoritos de las siguientes maneras:
   - Haga clic con el botón derecho en una carpeta de la **Favoritos** carpeta y seleccione **Eliminar de Favoritos**.
   - Haga clic con el botón derecho en una carpeta del repositorio de AEM en **DAM** carpeta que ya se ha agregado como favorita y seleccione **Eliminar de Favoritos**.

### Ver el historial de versiones de un archivo {#id195GI000D5Q}

Realice los siguientes pasos para ver el historial de versiones de un archivo:

1. Haga clic con el botón derecho en un archivo del panel Guías de AEM.

1. Select **Ver versiones** en el menú contextual.

   El historial de versiones del archivo se muestra en el cuadro de diálogo Versiones.

   ![](images/version-history.png)


### Ver los metadatos de un archivo {#id195GHN0H05C}

Siga estos pasos para ver los metadatos de un archivo:

1. Haga clic con el botón derecho en un archivo del panel Guías de AEM.

1. Select **Ver metadatos** en el menú contextual.

   Los metadatos del archivo, como la clase DITA, el estado del documento, la fecha de modificación, el tamaño, el título y el UUID, se muestran en el cuadro de diálogo Metadatos.

   ![](images/metadata.png)


## Buscar un tema en el repositorio de AEM {#id1826J20405Z}

Puede buscar temas en el repositorio de AEM utilizando la barra de búsqueda del panel AEM guías . Puede buscar en toda la carpeta DAM o seleccionar una carpeta y, a continuación, buscar un tema en esa carpeta. El resultado de la búsqueda muestra los temas que tienen texto coincidente con la consulta de búsqueda.

Siga estos pasos para buscar temas:

1. Seleccione una carpeta en el repositorio de AEM donde desee buscar un tema.
1. Introduzca la consulta de búsqueda \(por ejemplo, `introduction`\) en la barra de búsqueda del complemento Oxygen para guías AEM.
1. Haga clic en el botón de búsqueda o pulse Intro.

   El resultado se muestra en la ficha Resultados de la búsqueda como una lista con la ruta del archivo. Si no hay ningún resultado coincidente para la consulta de búsqueda, no se encontraron resultados en &lt;path of=&quot;&quot; the=&quot;&quot; selected=&quot;&quot; folder=&quot;&quot;> se muestra.

   ![](images/search.png)

1. \(Opcional\) Haga doble clic en un archivo del resultado de la búsqueda para abrirlo en Oxygen XML Author.
1. Para volver a la vista Repositorio AEM, realice una de las siguientes acciones:
   - Para ver la vista Repositorio AEM sin borrar los resultados de la búsqueda, haga clic en **Examinar** pestaña .
   - Para borrar los resultados de búsqueda y ver el Repositorio AEM, haga clic en Eliminar icono de búsqueda.

## Abrir tema DITA en Oxygen XML Author desde AEM interfaz web {#id182CE0I905Z}

Puede abrir y editar el tema DITA en Oxygen XML Author desde la interfaz web AEM. Debe instalar un paquete en AEM para activar esta opción. Para obtener más información sobre la instalación de paquetes, consulte [Instale el paquete para activar la función de edición de documentos desde AEM interfaz web](#id182CE0Q0TY4).

>[!NOTE]
>
>La variable **Editar en oxígeno** es accesible desde varios lugares de AEM: cuando se selecciona un tema, cuando se previsualiza un tema o desde la ficha Temas e informes de la consola de asignación DITA. Si selecciona varios temas, la opción no estará visible en la barra de herramientas.

**Apertura de un tema DITA**

Realice los siguientes pasos para abrir un tema DITA en Oxygen XML Author:

1. Seleccione un tema en los recursos y haga clic en **Editar en oxígeno** en la barra de herramientas.

   >[!NOTE]
   >
   >Si el tema no está desprotegido, primero se desprotege y después se abre en Oxygen en el modo de edición.

1. Seleccionar autor XML de oxígeno *&lt;version>* en el **Iniciar aplicación** en el Navegador. Puede seleccionar **Recordar mi elección para AEM vínculos** para guardar sus preferencias.

**Editar un tema de DITA**

Realice los siguientes pasos para editar un tema DITA en Oxygen XML Author:

1. Seleccione y extraiga un tema de sus recursos.
1. Haga clic en **Editar en oxígeno** en la barra de herramientas.

   >[!NOTE]
   >
   >Si el tema no está desprotegido, primero se desprotege y después se abre en Oxygen en el modo de edición.

1. Seleccionar autor XML de oxígeno *&lt;version>* en el **Iniciar aplicación** en el Navegador. Puede seleccionar **Recordar mi elección para AEM vínculos** para guardar sus preferencias.
1. Edite el tema en Oxygen XML Author.
1. Consulte el tema desde el complemento Oxygen para obtener AEM guías.

   Para obtener más información sobre cómo registrar un tema utilizando el complemento de oxígeno para AEM guías, consulte [Insertar un archivo](#id182CF0J0FHS).

   >[!NOTE]
   >
   >Asegúrese de registrar el tema utilizando el plugin de oxígeno para guías de AEM, si se registra desde la interfaz web de AEM, los cambios que realice en Oxygen XML Author no se guardarán en la versión marcada del tema.


## Trabajo con perfiles de atributo {#id1827JA002YK}

AEM guías le permite crear y asociar fácilmente atributos condicionales mediante los atributos DITA relevantes. Puede definir atributos condicionales en el nivel global o en el nivel de carpeta. Las condiciones definidas globalmente son visibles en todos los proyectos y las condiciones de nivel de carpeta solo son visibles en los proyectos creados dentro de la carpeta especificada. Los autores de contenido pueden utilizar estos atributos condicionales para condicionar el contenido de sus temas DITA o mapas que crean o utilizan. Para obtener más información sobre cómo crear atributos condicionales en AEM con las guías de AEM, consulte *Configuración de atributos condicionales para perfiles globales o de nivel de carpeta* en Instalar y configurar las guías de Adobe Experience Manager.

>[!NOTE]
>
>Asegúrese de haber añadido los atributos condicionales en AEM y de haber configurado [Preferencia para la personalización de atributos de creación de perfiles](#id1827K0D0OHT) antes de añadir atributos condicionales al contenido.

Realice los siguientes pasos para añadir atributos condicionales al contenido en Oxygen XML Author:

1. Consulte y abra un tema en la *Complemento Oxygen para guías AEM*.
1. Seleccione la parte del contenido en la que desea aplicar los atributos condicionales.
1. Haga doble clic en el atributo condicional en el panel Atributos del Autor XML de Oxygen.

   ![](images/attribute-panel.png)

1. En el **Disponible** en el cuadro de diálogo Editar atributo, seleccione el atributo\(s\) y haga clic en **Agregar**.

   Se muestra la siguiente pantalla `audience` atributos.

   ![](images/edit-attributes.png)

1. Haga clic en **Aceptar**.

   Los atributos se añaden al contenido.


## Solución de problemas comunes {#id188ABC00RY4}

Este tema cubre algunos de los problemas más comunes que podría enfrentar al trabajar con el complemento, junto con sus soluciones.

### Falta el panel Guías AEM {#id192BH200ZAX}

**Problema** - Si no ve el panel Guías de AEM en Oxygen XML Author, pruebe las siguientes soluciones:

Solución 1:

1. En Oxygen XML Author, habilite el complemento.

   Haga clic en **Opciones** \> **Preferencias** \> **Complementos** y seleccione **Complemento Oxygen para las guías de Adobe Experience Manager.**

1. Vuelva a iniciar Oxygen XML Author.


Solución 2:

1. Si todavía no ve el panel Guías de AEM, habilite AEM ventana Guías.

   En Oxygen XML Author, haga clic en **Ventana** \> **Mostrar vista** \> **Guías AEM**.

Solución 3:

1. Desinstale y vuelva a instalar el complemento Oxygen para las guías de Adobe Experience Manager.

   - En Windows, desinstale el complemento de **Agregar o quitar programas** lista. A continuación, vuelva a instalar el complemento.

   - En Mac, acceda a la carpeta aem-connector-x.x de la carpeta plugins de Oxygen XML Author y muévala a **Papelera**. A continuación, vacíe la variable **Papelera** carpeta.


### Configuración del puerto para la transformación DITA-OT

**Problema** - Cuando se ejecuta cualquier transformación DITA-OT en archivos procesados por el complemento, la transformación falla con el siguiente error:

![](images/proxy-server-path-error-new.png)

**Solución** - Este problema se ha solucionado añadiendo un servidor proxy entre DITA-OT y el complemento. Este servidor proxy procesa y comparte todos los archivos solicitados por DITA-OT para transformaciones. El puerto predeterminado en el que se ha configurado este servidor es: `5972`. Si utiliza este puerto para otro servidor, puede especificar un puerto diferente para el servidor proxy.

Realice los siguientes pasos para cambiar el puerto predeterminado del servidor proxy:

1. Vaya al directorio principal \(del usuario\).
1. Cree un archivo llamado aem\_connector\_proxy.
1. Abra el archivo en cualquier editor de texto y añada un número de puerto disponible en la primera línea del archivo.
1. Guarde y cierre el archivo.
1. Reinicie Oxygen XML Author y ejecute la transformación DITA-OT.


### AEM panel Guías no busca la ubicación del archivo abierto

Problema: Cuando elige abrir un archivo para editarlo en Oxygen XML Author desde AEM servidor, el archivo se abre para editarlo en Oxygen XML Author. Sin embargo, AEM panel Guías no muestra la ubicación del archivo en el árbol de navegación.

Solución: Este problema se ha observado en escenarios donde la ruta del archivo contiene /content/dam dos veces. De forma predeterminada, todos los recursos de AEM se almacenan en la carpeta /content/dam. Si carga o crea una estructura de carpetas que también contiene /content/dam, se observa este problema. Puede realizar todas las operaciones normales en estos archivos, pero su ubicación dentro del árbol de navegación no se muestra de forma predeterminada. Para acceder a dicho archivo en el árbol de navegación, debe buscar manualmente la ubicación del archivo. Tenga en cuenta que en el árbol de navegación, la ruta duplicada /content/dam se reemplaza por /content/assets.

### Configuración del registro

Problema: De forma predeterminada, el complemento Oxygen para las guías de AEM no genera ningún &quot;log&quot;, lo que dificulta la depuración de cualquier escenario de error.

Solución: Realice los siguientes pasos para habilitar la función de generación de registros en el complemento:

1. Vaya a la ubicación de instalación de Oxygen XML Author.

1. Abra el archivo oxigenAuthor19.1.vmoptions en un editor de texto.

   >[!NOTE]
   >
   >El número de versión del archivo puede variar en función del número de versión de la aplicación instalada en el sistema.

1. Añada la línea siguiente al archivo :

   ```java
   -Djava.util.logging.config.file=./log.properties
   ```

1. Guarde y cierre el archivo.

1. En la misma ubicación, cree un archivo llamado log.properties con el siguiente contenido:

   ```java
   handlers=java.util.logging.FileHandler
   java.util.logging.FileHandler.level = DEBUG
   java.util.logging.FileHandler.limit = 1048576
   java.util.logging.FileHandler.count = 5
   java.util.logging.FileHandler.pattern = %h/aem-plugin%g.log
   java.util.logging.FileHandler.formatter = java.util.logging.SimpleFormatter
   java.util.logging.FileHandler.format=[%1$tF %1$tT] [%4$s] %5$s %n
   ```

1. Guarde y cierre el archivo.
1. Inicie Oxygen XML Author.


El complemento ahora crea registros en el directorio raíz del usuario con el nombre de archivo aem-pluginX.log \(*donde X indica el número de rotación*\).