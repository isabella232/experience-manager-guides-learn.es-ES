---
title: Utilice variables para configurar las opciones Ruta de destino, Nombre del sitio o Nombre de archivo
description: Obtenga información sobre cómo usar variables para configurar las opciones Ruta de destino, Nombre del sitio o Nombre de archivo
source-git-commit: 8b6294425c6e60d1c5b37d98e99114014a104ee6
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---


# Utilice variables para configurar las opciones Ruta de destino, Nombre del sitio o Nombre de archivo


Al generar resultados en AEM sitio o PDF, puede utilizar variables para definir las opciones Ruta de destino, Nombre AEM sitio o Nombre de archivo del PDF. Puede utilizar una o una combinación de variables para definir estas opciones.

En la tabla siguiente se enumeran las variables que se admiten de forma predeterminada:

| Variable | Ruta de destino final | Ejemplo |
| --- | --- | --- |
| `${map_filename}` | Utiliza el nombre de los archivos de asignación DITA para crear la ruta de destino. | **Nombre del archivo de mapa DITA**:<br>`AEMGuides.ditamap`<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${map_filename}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/aemGuides/AEMGuides.html` |
| `${map_title}` | Utiliza el título del mapa DITA para crear la ruta de destino. | **Nombre del archivo de mapa DITA**:<br>`AEMGuides.ditamap`<br><br>**Título de mapa DITA**:<br>`AEMGuides`<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${map_title}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/AEMGuides/AEMGuides.html` |
| `${preset_name}` | Utiliza el nombre del ajuste preestablecido de salida para crear la ruta de destino. | **Nombre de ajuste preestablecido de salida**:<br>`AEM Guides PDF Output`<br><br>**Nombre del archivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${preset_name}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/AEM Guides PDF Output/SampleDita.html` |
| `${language_code}` | Utiliza el código de idioma donde se encuentra el archivo de asignación para crear la ruta de destino. | **Nombre del archivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Ruta del archivo de asignación DITA**:<br>`/content/dam/projects/AEM-Guides/en/user-guide/`<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${language_code}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/en/SampleDita.html` |
| `${map_parentpath}` | Utiliza la ruta completa del archivo de asignación para crear la ruta de destino.<br><br>**Nota**: Esta variable no se puede usar para especificar el Nombre de sitio AEM o el Nombre de archivo del PDF. | **Nombre del archivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Ruta del archivo de asignación DITA**:<br>`/content/dam/projects/AEM-Guides/en/user-guide`/<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${map_parentpath}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/content/dam/projects/AEM-Guides/en/user-guide/SampleDita.html` |
| `${path_after_langfolder}` | Utiliza la ruta del archivo de asignación después de la carpeta de idioma para crear la ruta de destino.<br><br>**Nota**: Esta variable no se puede usar para especificar el Nombre de sitio AEM o el Nombre de archivo del PDF. | **Nombre del archivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Ruta del archivo de asignación DITA**:<br>`/content/dam/projects/AEM-Guides/en/user-guide/`<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${path\_after\_langfolder}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/user-guide/SampleDita.html` |

Además, también puede utilizar como variables los metadatos definidos para el mapa de DITA o el archivo de mapa de libros. Los metadatos se pueden encontrar en la sección `/jcr:content/metadata` nodo del mapa DITA o del archivo de mapa de libros. Por ejemplo, una de las propiedades de metadatos definidas en la variable `/jcr:content/metadata` el nodo es `dc:title`. Puede especificar `${dc:title}` y el valor title se utiliza en la salida final.
**Tema principal:**[ Generación de resultados](generate-output.md)

