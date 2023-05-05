---
title: Creación condicional de perfiles de atributos
description: Aprenda a crear perfiles de atributos condicionales
exl-id: 31b0ffe6-44e7-459d-a8df-a64ec868768c
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Creación condicional de perfiles de atributos {#id1843I0HN0Y4}

A nivel empresarial, es extremadamente importante asegurarse de que dispone de un sistema de etiquetado estándar. Las etiquetas o los atributos condicionales se pueden asociar con recursos digitales en el repositorio, lo que ayuda a publicar resultados en función de las condiciones seleccionadas. Por ejemplo, puede crear un atributo condicional para el contenido de Windows y Mac. A continuación, agregue estos atributos al contenido relevante de los temas. En el momento de publicar contenido, puede elegir si desea publicar contenido de solo Windows o Mac.

AEM guías le permite crear y asociar fácilmente atributos condicionales mediante los atributos DITA relevantes. Puede definir atributos condicionales en el nivel global o en el nivel de carpeta. Las condiciones definidas globalmente son visibles en todos los proyectos y las condiciones específicas de las carpetas solo son visibles en los proyectos creados dentro de la carpeta especificada. Los autores de contenido pueden utilizar estos atributos condicionales para condicionar el contenido de sus temas DITA o mapas que crean o utilizan. El editor puede usar estas condiciones para crear ajustes preestablecidos condicionales. Con los ajustes preestablecidos condicionales, el editor puede decidir qué condición incluir y excluir de la salida publicada.

>[!NOTE]
>
> Puede crear o editar los atributos condicionales en un perfil de carpeta al que tenga acceso. Si el administrador del sistema no le ha dado acceso a un perfil de carpeta, no puede crear ni editar los atributos condicionales en el perfil de carpeta.

Para definir atributos condicionales, realice los siguientes pasos:

1. Haga clic en el vínculo Adobe Experience Manager en la parte superior y elija **Herramientas**.

1. Select **Guías** de la lista de herramientas.

1. Haga clic en el **Perfiles de carpeta** y seleccione un perfil de carpeta.

   >[!NOTE]
   >
   > No se puede editar el perfil global.

1. Haga clic en el **Atributos condicionales** y haga clic en **Editar**.

   Se muestra la tabla Atributos condicionales .

1. Haga clic en **Agregar**.

1. Introduzca la variable **Nombre**, **Valor** y **Etiqueta** para el atributo .

   Puede guardar un perfil con solo el nombre del atributo. Sin embargo, un atributo solo se puede utilizar cuando tiene un valor especificado. Si especifica tanto - valor como etiqueta para un atributo, el Editor web seguirá mostrando solo el valor del atributo. La etiqueta se muestra al administrador de publicación en el momento de crear el ajuste preestablecido condicional.

   La siguiente captura de pantalla muestra la definición de `platform` atributo con valor de `unix` y una etiqueta de `Red Hat Linux`.

   ![](images/add-profile.png){width="800" align="left"}

1. Si desea agregar más valores para el mismo atributo, haga clic en el botón **+** e introduzca un valor y una etiqueta adicionales.

1. Si desea agregar más atributos, haga clic en **Agregar**.

1. Haga clic en **Guardar** para guardar los cambios.


La variable `platform` se almacena en el sistema. Cuando un autor decide usar la variable `platform` en un tema DITA de una carpeta, verán los valores en la ficha Propiedades del Editor web.

![](images/properties-tab.png){width="350" align="left"}

**Tema principal:**[ Generación de resultados](generate-output.md)
