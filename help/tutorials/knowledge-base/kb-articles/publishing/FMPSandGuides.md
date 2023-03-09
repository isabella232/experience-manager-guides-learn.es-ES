---
title: AEM Guías de FMPS y
description: AEM Publicación con FMPS mediante guías de usuario de
source-git-commit: e3cef715f635746f7b426cb5de09299715cc354b
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---


# AEM Guías de FrameMaker Publishing Server (FMPS) y

**AEM La integración de guías con FrameMaker Publishing Server podría ser su solución si busca una publicación automatizada de alta calidad.\
AEM El siguiente artículo le ayudará a configurar y ejecutar FMPS con guías de.**

## AEM Compatibilidad de FMPS con Guías de la:

- AEM Compatibilidad con las guías de uso 4.1: [Vínculo](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html?lang=en/#compatibility-matrix)
- AEM Compatibilidad con las guías de 4.0 de la: [Vínculo](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html/#Compatibility%20matrix)
- Versión futura: [Vínculo](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/latest-release-info.html?lang=en)

## Instalación:

### AEM Guías de:

Consulte Instalación y configuración: [Vínculo](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf)

### FMPS:

Para la instalación de FMPS puede consultar [Vínculo de vídeo](https://www.youtube.com/watch?v=2deelyM5VA8&amp;t) o [Documentación](https://help.adobe.com/en_US/framemaker/server/index.html#t=fmps-user-guide%2Finstall_config_fmps.html%23install_config_fmps&amp;rhtocid=_2)

## Configuraciones necesarias:

El contenido DITA se puede generar mediante FrameMaker Publishing Server (FMPS). Puede crear resultados en cualquiera de los muchos formatos que admite FMPS. AEM En la consola web, modifique las siguientes propiedades del paquete com.adobe.fmdita.config.ConfigManager para establecer Guías de la para utilizar FMPS.

Para abrir la consola web, vaya a la URL Acceso http://\&lt;server name=&quot;&quot;>:\&lt;port>/system/console/configMgr.

**Propiedades de configuración y su descripción:** [Vínculo](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf#page=89)

## Ejecución de la prueba:

Con FMPS, puede publicar automáticamente **PDF, HTML interactivo5**, y **Epub** para sus recursos DITA y FM.

En el menú &quot;Generar PDF usando&quot;, seleccione FrameMaker Publishing Server.

El usuario puede proporcionar &quot;settings File(.sts)&quot; y &quot;ditaval. El filtrado se realizará con ditaval en función de las condiciones que proporcione.

- **archivo de configuración**: configuración de FrameMaker /FMPS Publish que contiene todas las configuraciones que desea que FMPS respete al publicar. Por ejemplo: generar resultados con la plantilla personalizada, generar marcas y sangrados (PDF), generar PDF con índice, índice, etc.
- **FMPS presentes:** Combinación predefinida de ditaval y archivo de configuración. En lugar de proporcionar archivos de ditaval y configuración independientes, el usuario puede crear previamente un ajuste preestablecido de FMPS que se puede reutilizar para satisfacer sus necesidades de publicación.

**Nota:** Si no selecciona ninguno de los ajustes o ajustes preestablecidos de FMPS, FMPS publicará con el ajuste predeterminado del sistema.

AEM Si ha seleccionado un ajuste preestablecido de FMPS y también ha proporcionado un archivo de configuración/ditaval desde el archivo, se producirá un conflicto entre este ajuste preestablecido y el de FMPS tendrá prioridad sobre el archivo de configuración/ditaval personalizado.

### Publicación de línea base con FMPS:

Puede Publicar las líneas de base ya creadas con FMPS2020.0.2 o una versión superior.

**Archivo de configuración FMPS de muestra (archivo .sts) para empezar:** [Vínculo](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:ef750752-7a7e-4e51-923e-6b7d9861ed54) (descomprima este archivo)

## Preguntas frecuentes y resolución de problemas:

- La publicación de FMPS falla con &quot;Timeout Exception&quot;.

Compruebe y aumente el valor de &quot;FMPS timeout&quot; (segundos) en /system/console/configMgr/com.adobe.fmdita.config.ConfigManager&quot;

- No se puede obtener el ajuste preestablecido de FMPS en el menú desplegable.

Asegúrese de que ha creado un ajuste preestablecido de FMPS en el servidor y de que la configuración de conexión es correcta.

- Obtengo PDF en blanco al publicar.

AEM Si está utilizando UUID, asegúrese de haber marcado &quot;Usar referencia basada en UUID&quot; en las Preferencias de edición de FrameMaker y viceversa para las guías de usuario que no sean de UUID.

- Mi configuración/ditaval no se aplican en la salida final publicada.

Asegúrese de que no está seleccionando simultáneamente el archivo de configuración/ditaval y el ajuste preestablecido FMPS. Compruebe la salida manualmente con FrameMaker.

- La línea de base no se publica desde FMPS.

La publicación de línea de base es compatible con FMPS2020.0.2 o una versión superior.\
Asegúrese de que la Línea Base se ha creado correctamente, para verificar, vaya a Mapa de descarga de temas del panel de mapas y seleccione &quot;Usar Línea Base&quot;.

- Las tareas de publicación de FMPS tardan más tiempo que otros motores.

Habrá una cabecera fija ideal de aprox. Solo entre 3 y 4 minutos al publicar desde FMPS que con otros motores, si cree que es más que eso, consulte con su administrador de FMPS o póngase en contacto con el servicio de asistencia al Adobe.

## Otros recursos:

[Formación y asistencia para FMPS](https://helpx.adobe.com/support/framemaker-publishing-server.html)

[AEM Aprendizaje y asistencia sobre la](https://helpx.adobe.com/in/support/xml-documentation-for-experience-manager.html)

[Comunidad FrameMaker y FMPS](https://community.adobe.com/t5/framemaker/ct-p/ct-framemaker?page=1&amp;sort=latest_replies&amp;lang=all&amp;tabid=all)

[AEM Comunidad de guías de](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation)
