---
title: Configuración de AEM entorno para publicación de PDF nativo
description: Configuración de AEM entorno para publicación de PDF nativo
source-git-commit: f26b8f94e1d7a3c9dd0aaab2eb196a77119e47ac
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 1%

---


# Configuración de AEM entorno para publicación de PDF nativo

AEM guías incluye un motor de publicación nativo para PDF que permite a los usuarios diseñar, desarrollar y publicar el contenido en formato de PDF.

Proporciona la capacidad de crear diferentes diseños de página, plantillas CSS y diseñar las plantillas de PDF junto con los diseños de página y CSS.

Los pasos para configurar este PDF nativo en AEM guías difieren según el sistema operativo. Utilice los pasos de configuración siguientes en función del sistema operativo en el que AEM está instalado.

## Requisitos previos

Requisitos mínimos para configurar el PDF nativo:

- Java Platform instalado, Standard Edition 8 o 11 JDK (Java SE Development Kit) y JRE (Java SE Runtime Environment)
- AEM 6.5 SP13, SP12, SP11 o SP10
- Guías 4.1 y versiones posteriores (no UUID o UUID)

El motor de publicación nativo del PDF necesita Oracle JDK para generar los módulos de nodo en la carpeta crx-quickstart de AEM. De forma predeterminada, admite los siguientes sistemas operativos:

- Windows 10, servidor Windows 2019 y versiones posteriores.
- Linux: (RHEL 8 y versiones posteriores, CentOS 7 y versiones posteriores, Ubuntu 18 y versiones posteriores)
- Sistema operativo Mac (basado en Intel)

## Pasos de configuración para Windows Server (JAVA 11/8)

1. Asegúrese de que AEM servidor esté inactivo.
2. En la barra de tareas de Windows, haga clic con el botón derecho en el icono de Windows y seleccione Sistema.
3. En la ventana Configuración, en Configuración relacionada, haga clic en Configuración avanzada del sistema.
4. En la ficha Avanzadas, haga clic en Variables de entorno.
5. En la sección de variables del sistema, haga clic en &quot;_Nuevo_&quot; para crear una nueva variable de entorno.
6. Escriba el nombre de la variable como JAVA_HOME.
7. En el campo value , proporcione la ruta de instalación de Java y haga clic en Ok.

   Por ejemplo:

   JAVA 11:

   C:\Program Files\JAVA\jdk-11.0.15.1

   JAVA 8:

   C:\Program Files\JAVA\ jdk1.8.0_144

8. Agregue la opción Ruta de acceso de las variables del sistema y haga clic en Editar.

9. Ahora, dentro de las variables Path proporciona el valor de la ruta Server y haga clic en Ok.

   Por ejemplo:

   JAVA 11:

   %JAVA_HOME%\bin\server\

   JAVA 8:

   %JAVA_HOME%\jre\bin\server\

10. Vuelva a hacer clic en &quot;Aceptar&quot; en el cuadro de diálogo Variables de entorno.
11. Vuelva a hacer clic en &quot;Aceptar&quot; en el cuadro de diálogo Propiedades del sistema.
12. Ahora, inicie el servidor AEM.
13. Genere un PDF nativo a partir de ajustes preestablecidos en el editor web.

## Pasos de configuración para Linux Server (RHEL7/centOS 7)

1. Asegúrese de que AEM servidor esté inactivo
2. Verifique la variable JAVA_HOME haciendo echo $JAVA_HOME
3. Si la variable JAVA_HOME no está configurada, siga el paso 4. De lo contrario, vaya directamente al paso 5.
4. Establezca la variable JAVA_HOME utilizando los siguientes comandos basados en la versión de java instalada

   Por ejemplo:

   JAVA 11:

   1. exportar JAVA\_HOME=/usr/lib/jvm/java-11.0.15.1
   2. export PATH=$PATH: $JAVA\_HOME/bin
   3. exportar LD\_LIBRARY\_PATH=/usr/lib/jvm/jdk-11.0.15.1/lib/server:/usr/java/jdk-11.0.15.1/lib/server

   JAVA 8:

   1. exportar JAVA\_HOME=/usr/lib/jvm/java-11.0.15.1
   2. export PATH=$PATH: $JAVA\_HOME/bin


5. Reiniciar servidor AEM
6. Copie el &quot;_node_module.zip_&quot; se adjunta en la parte inferior de este artículo al directorio crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166/ .
7. Abra el terminal en la ubicación crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166/.
8. Eliminar el directorio node_module usando el siguiente comando

   **rm -rf node_module**

9. Descomprimir node_modules.zip mediante el comando siguiente

   **unzip node_module.zip**

10. Si el comando unzip no está instalado/reconocido, puede instalarse usando el siguiente comando

   **yum install unzip**

11. Instale el paquete fontconfig.
Comando: yum install fontconfig
12. Genere un PDF nativo a partir de ajustes preestablecidos en el editor web.

**NOTA** : el paquete node_module.zip se puede descargar [here](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:295d8f03-41e1-429b-8465-2761ce3c2fb3).

La importación manual de módulos de nodos descargados para el sistema operativo Linux es una solución para los usuarios que están en Guías 4.1 o versiones anteriores.

## Pasos de configuración para el equipo Mac (JAVA 11/8)

1. Instale el Oracle JAVA 11 o el Oracle JAVA 8.
2. Establezca la variable de entorno JAVA_HOME en el directorio JAVA instalado.
3. Abra un shell de Unix.
(Bash se utiliza aquí para configurar la configuración)

   Comando: nano ~/.bashrc

4. Establezca la variable JAVA_HOME utilizando los siguientes comandos basados en la versión de java instalada

   Por ejemplo:

   JAVA 11:

   exportar JAVA\_HOME= /Library/Java/JavaVirtualMachines/jdk-11.0.15.1.jdk/Contents/Home

5. Volver a cargar bashrc

   Comando: fuente ~/.bashrc.

6. Verifique que JAVA_HOME esté configurado mediante el comando echo $JAVA_HOME

7. Ejecute los tres comandos siguientes desde AEM ruta de instalación

   C:/{aem-installation-folder}/crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166

   i) buscar . -type d -exec chmod 0755 {} \; ii) encontrar . -type f -exec chmod 0755 {} \; iii) ./node-darwin/bin/node node-darwin/lib/node_modules/npm/bin/npm-cli.js —prefix . install —unsafe-perm —scripts-prepend-node-path

8. Compruebe si Java está instalado con el comando siguiente

   i) Ejecutar **./node-darwin/bin/node** comando de la carpeta /crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166

   ![mac](../assets/publishing/mac.png)

   ii) a = required(&#39;java&#39;)

9. Instale el paquete fontconfig.
Comando: instalación de apt fontconfig

10. Genere un PDF nativo a partir de ajustes preestablecidos en el editor web.

## Solución de problemas

A continuación se muestran los errores comunes que pueden producirse durante la generación de PDF cuando las variables de entorno no están configuradas correctamente.

### Excepción de puntero nulo en Windows/Mac OS

![excepción de puntero nulo](../assets/publishing/null-pointer-exception.png)

### Bibliotecas que faltan en el sistema operativo Linux RHEL 7

![bibliotecas que faltan](../assets/publishing/missing-libraries.png)

Si tiene algún problema al realizar cualquiera de los pasos anteriores, publique su pregunta en la Comunidad de guías de AEM [foro](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation) para obtener ayuda.
