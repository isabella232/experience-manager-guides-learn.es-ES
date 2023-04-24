---
title: Usar ajustes preestablecidos de condición
description: Aprenda a utilizar ajustes preestablecidos de condición
source-git-commit: 6eb8d29e71301581e8dbb5b6a4252194c5a89f96
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 2%

---


# Usar ajustes preestablecidos de condición {#id1825FL004PN}

Puede definir atributos en los temas de DITA y utilizar el ajuste preestablecido de condición para especificar lo que sucede con el atributo en la salida final. Por ejemplo, puede añadir atributos como versión 1.0 y 2.0 en el contenido y utilizar un ajuste preestablecido de condición para incluir la versión 1.0 para la versión 1.0 y excluir la versión 2.0. Del mismo modo, puede agregar atributos como SO Windows y OS Linux al contenido y luego incluir o excluir el contenido relevante para la salida final según el sistema operativo.

## Crear un ajuste preestablecido de condición

Realice los siguientes pasos para crear un ajuste preestablecido de condición:

1. Haga clic en **Ajustes preestablecidos de condición** en la consola de asignación DITA.
1. Haga clic en **Crear** botón.
1. Introduzca un nombre para el ajuste preestablecido en **Condición de nombre**.
1. Seleccione una de las siguientes acciones predeterminadas de **Establezca la acción predeterminada como** lista desplegable:

   - Incluir
   - Excluir
   - Pasaje
   - Marca La acción se establece como acción predeterminada para todos los atributos, independientemente de si se añaden o no al ajuste preestablecido de condición.

   Por ejemplo, tiene 15 atributos de condición en el documento y ha incluido cuatro de ellos en el ajuste preestablecido de condición. Si selecciona **excluir** como acción predeterminada, se aplica a los 15 atributos.

1. Realice una de las siguientes acciones para agregar los atributos:
   - Haga clic en **Agregar** a un atributo del ajuste preestablecido de condición. Puede repetir este paso para agregar más atributos.
   - Haga clic en **Agregar todo** para añadir todos los atributos al ajuste preestablecido de condición.
1. \(Opcional\) Si es necesario, puede anular la acción predeterminada aplicada a los atributos en el paso 4. Realice una de las siguientes acciones:
   - Seleccionar varios atributos, elegir una acción **Establezca la acción para las condiciones seleccionadas en** y haga clic en **Aplicar**.
   - Seleccione una acción para un atributo en el **Acción** lista desplegable.
1. Haga clic en **Guardar**.

## Editar un ajuste preestablecido de condición

Puede realizar cambios en un ajuste preestablecido de condición existente para cambiar las acciones aplicadas a los atributos en el ajuste preestablecido de condición. Realice los siguientes pasos para editar un ajuste preestablecido de condición:

1. Haga clic en **Ajustes preestablecidos de condición** en la consola de asignación DITA.
1. Haga clic en **Editar** botón.
1. Realice los cambios necesarios para todos los atributos en el ajuste preestablecido de condición.
1. Haga clic en **Guardar**.

## Creación de una copia de un ajuste preestablecido de condición

Puede crear una copia de un ajuste preestablecido de condición y luego modificarlo según sus necesidades. Realice los siguientes pasos para crear una copia de un ajuste preestablecido de condición:

1. Haga clic en **Ajustes preestablecidos de condición** en la consola de asignación DITA.
1. Haga clic en **Duplicar** botón.

   >[!NOTE]
   >
   > El nombre predeterminado del ajuste preestablecido es `<selected condition preset name>_Duplicate`

   Puede cambiar el nombre según sus necesidades.

1. \(Opcional\) Realice los cambios necesarios para todos los atributos del ajuste preestablecido de condición.
1. Haga clic en **Guardar**.

## Ajuste preestablecido de condición de eliminación

Puede eliminar uno o varios ajustes preestablecidos de condición de la variable **Ajuste preestablecido de condición** de la consola de asignación DITA. Siga estos pasos para eliminar los ajustes preestablecidos de condición:

1. Haga clic en **Ajustes preestablecidos de condición** en la consola de asignación DITA.
1. Seleccione los\(s\) preestablecidos de condición que desee eliminar.
1. Haga clic en **Eliminar** botón.
1. Haga clic en **Eliminar** para confirmar la acción.

**Tema principal:**[ Generación de resultados](generate-output.md)

