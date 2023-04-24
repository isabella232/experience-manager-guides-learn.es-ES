---
title: Administrar contenido
description: Obtenga información sobre cómo administrar contenido
source-git-commit: bad2f5cea2c00ca6c9758da27f0dba89a8579eb7
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 10%

---


# Administrar contenido {#id164JBG0M0T1}

Antes de comenzar con la creación real de contenido, debe familiarizarse con algunos conceptos básicos de la administración de contenido en AEM guías. A continuación, comience creando diferentes grupos de usuarios y organizando los recursos.

## Conceptos clave

Algunos conceptos clave de la administración de contenido en AEM son los siguientes:

**Administración de activos**

AEM guías utiliza AEM administración de recursos digitales \(DAM\) para administrar los archivos DITA. Los archivos que cargue o proteja en DAM se almacenan como recursos digitales. Puede administrar y editar los recursos en AEM Assets. Para obtener más información sobre la administración de recursos, consulte [Administrar recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html?lang=en).

**Administración de vínculos**

Mueva o cambie el nombre de los archivos o la estructura de carpetas en el repositorio de contenido, sin tener que preocuparse por las referencias rotas. Todas las referencias al contenido afectado y procedentes de él se actualizan automáticamente. Obtenga advertencias al eliminar contenido al que se hace referencia desde cualquier otra parte para evitar interrupciones no intencionales.

**Administración de versiones**

AEM guías proporciona administración de versiones para los recursos digitales. Puede activar fácilmente esta funcionalidad desde la aplicación de creación DITA que elija. Permitiendo que sus escritores realicen las funciones de control de versiones estándar, como el check-in y check-out.

Para obtener más información sobre cómo crear versiones o revertir a una versión específica, consulte [Rama, revertir y versiones posteriores](web-editor-preview-topics.md#id193PG0Y051X).

**Administración de DITA nativa**

Aunque AEM guías mantiene la estructura de sus archivos DITA, también permite AEM gestionar de forma nativa DITA mediante asignación de elementos para asignar los elementos DITA a AEM componentes. La gestión DITA nativa se utiliza en funciones como la vista previa del tema, la publicación en AEM Sites y los flujos de trabajo de revisión.

## Identificación de su función y permisos {#id181TF0K0MHT}

AEM guías proporciona tres grupos predeterminados. Estos grupos son: *Autores*, *Revisores* y *Editores*. Según el grupo al que esté asociado, tiene permisos para realizar tareas específicas, como se menciona en la tabla siguiente. Por ejemplo, la tarea de publicación solo puede realizarla un editor, pero no un autor o un revisor. Del mismo modo, un autor puede crear un tema nuevo y un revisor solo puede revisar un tema.

>[!TIP]
>
> Consulte la *Permisos* en la guía de prácticas recomendadas para conocer las prácticas recomendadas relacionadas con la configuración de los permisos de usuario.

En la tabla siguiente se enumeran varias tareas y los grupos que pueden realizar dichas tareas:

| Tarea | Autores | Revisores | Editores |
|----|-------|---------|----------|
| Crear tema DITA | Sí |   | Sí |
| Crear mapa DITA | Sí |   | Sí |
| Asignar colecciones | Sí |   | Sí |
| Crear tarea de revisión | Sí |   | Sí |
| Revisar tema[1](#fntarg_1) | Sí | Sí | Sí |
| Resolución clave | Sí |   | Sí |
| Extracción y registro | Sí |   | Sí |
| Editar tema | Sí |   | Sí |
| Mover tema | Sí |   | Sí |
| Editar propiedades del tema | Sí |   | Sí |
| Copiar | Sí |   | Sí |
| Eliminar | Sí |   | Sí |
| Compartir | Sí |   | Sí |
| **Estado del documento** |
| Crear/editar perfil de estado del documento |   |   | Sí |
| Cambiar el estado del documento[2](#fntarg_2) | Sí | Sí | Sí |
| **Funciones disponibles en la consola de asignación DITA \(ficha Ajustes preestablecidos de salida\)** |
| Generar |   |   | Sí |
| Editar |   |   | Sí |
| Duplicar |   |   | Sí |
| Crear |   |   | Sí |
| Eliminar ajuste preestablecido |   |   | Sí |
| **Funciones disponibles en la consola de asignación DITA \(pestaña Salidas\)** |
| Ver el resultado generado | Sí |   | Sí |
| **Funciones disponibles en la consola de asignación DITA \(pestaña Temas\)** |
| Crear tarea de revisión | Sí |   | Sí |
| Editar | Sí |   | Sí |
| **Funciones disponibles en la consola de asignación DITA \(pestaña Líneas de base\)** |
| Crear |   |   | Sí |
| Editar |   |   | Sí |
| Duplicar |   |   | Sí |
| Quitar |   |   | Sí |
| Consola de asignación DITA \(ficha Informes\) | Sí |   | Sí |
| **Funciones disponibles en la consola de asignación DITA \(Ajustes preestablecidos de condición\)** |
| Crear/editar condición preestablecida |   |   | Sí |

[1](#fnsrc_1) If *Autores* y *Editores* están invitados a un examen.

[2](#fnsrc_2) Según los derechos otorgados al usuario en el perfil de estado del documento.

## Requisitos previos para la creación de contenido

**Trabajar con perfiles globales o de nivel de carpeta**

En una empresa, diferentes grupos o productos pueden utilizar distintas plantillas de creación, plantillas de salida, perfiles de atributos condicionales \(o esquemas de asunto\) y configuraciones del Editor web. La configuración de estas opciones solo en el nivel de empresa \(o global\) puede dificultar la experiencia de los autores, ya que verán plantillas o perfiles que no les son relevantes.

AEM guías le permite configurar las plantillas de creación \(tema o asignación\), las plantillas de salida, los atributos condicionales y las configuraciones del Editor web en un nivel de empresa \(global\), así como en un nivel de carpeta. De este modo, puede separar las configuraciones de diferentes departamentos o productos de su empresa.

Además, puede delegar las configuraciones específicas de carpeta a un departamento o a administradores de productos para descentralizar la administración.

Para obtener más información sobre la configuración de perfiles globales y de nivel de carpeta, consulte *Configuración de perfiles globales o de nivel de carpeta* en Instalar y configurar las guías de Adobe Experience Manager as a Cloud Service.





