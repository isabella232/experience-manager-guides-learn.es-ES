---
title: Usar ajustes preestablecidos de condición
description: Aprenda a utilizar ajustes preestablecidos de condición
exl-id: cd8f8196-ba03-4a4b-9ce8-2651de4e5cc2
source-git-commit: 8073716bccacbe8d6a158b44d5106b083e3a5dcd
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 2%

---

# Usar ajustes preestablecidos de condición {#id1825FL004PN}

Se pueden definir atributos en los temas DITA y utilizar el ajuste preestablecido de condición para especificar lo que sucede con el atributo en la salida final. Por ejemplo, puede agregar atributos como la versión 1.0 y la versión 2.0 en el contenido y utilizar un ajuste preestablecido de condición para incluir la versión 1.0 para la versión 1.0 y excluir la versión 2.0. Del mismo modo, puede añadir atributos como SO Windows y OS Linux al contenido y, a continuación, incluir o excluir el contenido relevante para la salida final según el sistema operativo.

## Crear un ajuste preestablecido de condición

Siga estos pasos para crear un ajuste preestablecido de condición:

1. Clic **Ajustes preestablecidos** de la consola de mapas DITA.
1. Clic **Crear** botón.
1. Introduzca un nombre para el ajuste preestablecido en **Condición de nombre**.
1. Seleccione una de las siguientes acciones predeterminadas de **Establecer acción predeterminada en** lista desplegable:

   - Incluir
   - Excluir
   - Passthrough
   - Indicador La acción se establece como acción predeterminada para todos los atributos, independientemente de si se añaden o no al ajuste preestablecido de condición.

   Por ejemplo, tiene 15 atributos de condición en el documento y ha incluido cuatro de ellos en el ajuste preestablecido de condición. Si selecciona **excluir** como acción predeterminada, se aplica a los 15 atributos.

1. Siga uno de estos procedimientos para agregar los atributos:
   - Clic **Añadir** a un atributo del ajuste preestablecido de condición. Puede repetir este paso para agregar más atributos.
   - Clic **Añadir todo** para añadir todos los atributos al ajuste preestablecido de condición.
1. \(Opcional\) Si es necesario, puede anular la acción predeterminada aplicada a los atributos en el paso 4. Realice una de las siguientes acciones:
   - Seleccionar varios atributos, elegir una acción de **Definir la acción para las condiciones seleccionadas como** y haga clic en **Aplicar**.
   - Seleccione una acción para un atributo de la **Acción** menú desplegable.
1. Haga clic en **Guardar**.

## Edición de un ajuste preestablecido de condición

Puede realizar cambios en un ajuste preestablecido de condición existente para cambiar las acciones aplicadas a los atributos en el ajuste preestablecido de condición. Siga estos pasos para editar un ajuste preestablecido de condición:

1. Clic **Ajustes preestablecidos** de la consola de mapas DITA.
1. Clic **Editar** botón.
1. Realice los cambios necesarios para todos los atributos en el ajuste preestablecido de condición.
1. Haga clic en **Guardar**.

## Crear una copia de un ajuste preestablecido de condición

Puede crear una copia de un ajuste preestablecido de condición y, a continuación, modificarlo según sus necesidades. Realice los siguientes pasos para crear una copia de un ajuste preestablecido de condición:

1. Clic **Ajustes preestablecidos** de la consola de mapas DITA.
1. Clic **Duplicar** botón.

   >[!NOTE]
   >
   > El nombre predeterminado del ajuste preestablecido es `<selected condition preset name>_Duplicate`

   Puede cambiar el nombre según sus necesidades.

1. \(Opcional\) Realice los cambios necesarios para todos los atributos del ajuste preestablecido de condición.
1. Haga clic en **Guardar**.

## Eliminar ajuste preestablecido de condición

Puede eliminar uno o más ajustes preestablecidos de condición del **Ajuste preestablecido de condición** de la consola de mapas DITA. Siga estos pasos para eliminar los ajustes preestablecidos de condición:

1. Clic **Ajustes preestablecidos** de la consola de mapas DITA.
1. Seleccione los ajustes preestablecidos\(s\) de condición que desee eliminar.
1. Clic **Eliminar** botón.
1. Clic **Eliminar** para confirmar la acción.

**Tema principal:**[ Generación de salida](generate-output.md)
