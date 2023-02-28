---
title: Compatibilidad con schematron en webeditor
description: Uso de schematron en webeditor
source-git-commit: 2a036ec628424f0dedfdb69a5e860906ca100cc6
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---


# Control de la calidad del contenido dentro del editor web

Este artículo ofrece información general sobre las posibilidades de validación dentro del editor web de guías de AEM.
Por medio del editor web de diseño, aprovecha la configuración del esquema DITA en el sistema para obligar a los usuarios a crear contenido compatible con DITA. Con esto, todo el contenido almacenado en el sistema es contenido DITA estructurado, reutilizable y válido.

Además de la compatibilidad con las reglas de DITA, el editor web también admite la validación de contenido basado en &quot;*Esquatrón*&quot;.

&quot;*Esquatrón*&quot; hace referencia a un lenguaje de validación basado en reglas utilizado para definir pruebas para un archivo XML. Puede importar los archivos de Esquema y editarlos también en el Editor web. Con un archivo &quot;schematron&quot; puede definir determinadas reglas y después validarlas para un tema DITA o un mapa. Las reglas de esquema pueden garantizar la coherencia de la estructura XML mediante la imposición de restricciones definidas como reglas. Estas restricciones están impulsadas por las PYME que son propietarias de la calidad y la coherencia del contenido.

    NOTA: El editor web admite el esquema ISO.


## Cómo funciona &quot;Schemaatron&quot; en el editor web

### Configuración de reglas de esquema

Consulte la sección &quot;Compatibilidad con archivos de esquema&quot; en la sección [Guía del usuario](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_User-Guide_EN.pdf#page=148)


### Aplicar reglas de validación al guardar archivos

La configuración de Webeditor permite a los usuarios de energía configurar reglas o archivos de esquema que se ejecutan cada vez que un usuario actualiza el contenido. Para obtener más información, consulte la sección &quot;Validación&quot; en [Guía del usuario](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_User-Guide_EN.pdf#page=58)

![Definir reglas a partir de la configuración del editor web](../../../assets/authoring/schematron-editorsettings-validation-tab.png)


### ¿Puede ejecutar la validación manualmente?

Sí, como autor/usuario durante la creación de contenido, puede utilizar el panel Esquatrón de webeditor para cargar un archivo de esquema y ejecutar validaciones en el archivo abierto en editor.

    Para que esto funcione, el administrador de perfiles de carpetas debe permitir que todos los usuarios agreguen archivos de esquema en el panel Validación. Ver configuración del editor (captura de pantalla proporcionada anteriormente)

![Elegir archivo de esquema](../../../assets/authoring/schematron-rightpanel-validation-addsch.png)
![Ejecutar validación](../../../assets/authoring/schematron-rightpanel-validation-runsch.png)


### Reglas compatibles

La versión actual de AEM guías admite la validación utilizando reglas basadas en &quot;aserción&quot; únicamente. (consulte [recurso frente a informe](https://schematron.com/document/205.html)) Todavía no se admiten reglas basadas en &quot;Informes&quot;.


### Ejemplos y más ayuda sobre las reglas de esquema

#### Ejemplos de uso

- Compruebe si un vínculo es externo y si tiene el ámbito &quot;externo&quot;

   ```
   <sch:pattern>
       <sch:rule context="xref[contains(@href, 'http') or contains(@href, 'https')]">
           <sch:assert test="@scope = 'external' and @format = 'html'">
               All external xref links must be with scope='external' and format='html'
           </sch:assert>
       </sch:rule>
   </sch:pattern>
   ```

- Compruebe si hay al menos un &quot;topicref&quot; en un mapa o al menos un &quot;li&quot; debajo de un &quot;ul&quot;

   ```
   <sch:pattern>
       <sch:rule context="map">
           <sch:assert test="count(topicref) > 0">
               There should be atleast one topicref in map
           </sch:assert>
       </sch:rule>
   
       <sch:rule context="ul">
           <sch:assert test="count(li) > 1" >
               A list must have more than one item.
           </sch:assert>
       </sch:rule>
   </sch:pattern>
   ```

- El elemento &quot;indexterm&quot; siempre debe estar presente en un &quot;prolog&quot;

   ```
   <sch:pattern>
       <sch:rule context="*[contains(@class, ' topic/indexterm ')]">
           <sch:assert test="ancestor::node()/local-name() = 'prolog'">
               The indexterm element should be in a prolog.
           </sch:assert>
       </sch:rule>
   </sch:pattern>
   ```

#### Recursos

- Explicación  [Conceptos básicos del esquema](https://da2022.xatapult.com/#what-is-schematron)
- Más información sobre [Reglas de aserción en el esquema](https://www.xml.com/pub/a/2003/11/12/schematron.html#Assertions)
- [Archivo de esquema de muestra](../../../assets/authoring/sample_schematron.sch)