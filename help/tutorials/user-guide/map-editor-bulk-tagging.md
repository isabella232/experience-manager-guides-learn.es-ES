---
title: Etiquetado masivo de contenido DITA
description: Aprenda a etiquetar masivamente contenido DITA
exl-id: 0e855575-e62f-4dc7-869c-7fd3ec61ffdb
source-git-commit: 8823669fd29e8a40a41f9ca5d654b38fbea8e2fa
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Etiquetado masivo de contenido DITA {#id179SG0TN05Z}

Las etiquetas permiten agrupar o clasificar contenido dentro del repositorio de contenido y también en la salida publicada. Si ha aplicado etiquetas en el contenido, puede encontrar fácilmente temas relacionados dentro de un mapa DITA que le puedan ayudar a crear contenido. Con la salida publicada, los usuarios finales podrán localizar el contenido correcto más rápido con las etiquetas adecuadas en su lugar.

AEM guías le permite etiquetar contenido DITA en pocos clics. Puede utilizar la función de etiquetado masivo para aplicar varias etiquetas en varios temas, un mapa DITA o en un submapa. O bien, también puede aplicar etiquetas en un tema individual. El etiquetado es la característica nativa de AEM, puede encontrar más información sobre la creación y administración de etiquetas en la sección [Administración de etiquetas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/tags.html?lang=en) en AEM documentación.

De forma predeterminada, AEM guías no concede acceso de lectura a ningún usuario de la carpeta donde se almacenen todas las etiquetas del repositorio de AEM. Para utilizar etiquetas definidas en el repositorio de AEM, debe solicitar al administrador del sistema que conceda acceso a la carpeta en la que se almacenan las etiquetas.

## Aplicar etiquetas masivas

Utilice la función de etiquetado masivo para aplicar varias etiquetas a la vez. Siga estos pasos para aplicar etiquetas a los temas en un mapa DITA:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación DITA y haga clic en él.

   Aparece la consola de asignación DITA que muestra la lista de ajustes preestablecidos de salida disponibles para generar resultados.

1. Haga clic en **Temas**.

   Se muestra una lista de temas disponibles en el mapa DITA. Los UUID de los temas&#39; se muestran debajo del título del tema.

1. Seleccione los temas o el submapa en el que desea aplicar las etiquetas.

   ![](images/apply-tags-uuid.png){width="650" align="left"}


   >[!NOTE]
   >
   > La captura de pantalla anterior muestra un submapa seleccionado y expandido. Al seleccionar el submapa, también se seleccionan todos los temas bajo el submapa.

1. Haga clic en **Aplicar etiquetas**.

   Aparecerá el cuadro de diálogo Seleccionar etiquetas.

1. Seleccione una o varias etiquetas que desee aplicar en los temas seleccionados.

1. Confirme la selección.

   Las etiquetas seleccionadas se aplican a los temas y se muestran junto al título del tema.

   >[!NOTE]
   >
   > Después de agregar etiquetas a los temas, si mueve o elimina un tema, también se eliminan las etiquetas de esos temas. Sin embargo, ese tema permanece en el mapa hasta que lo elimine.


## Aplicación de etiquetas en un tema individual

Siga estos pasos para aplicar etiquetas a un tema individual:

1. En la interfaz de usuario de Assets, vaya al archivo de tema en el que desea aplicar etiquetas y selecciónelo.

1. En la barra de herramientas, haga clic en **Propiedades**.

   Aparece la página de propiedades del tema.

1. En la ficha Básico , haga clic en el icono Examinar situado junto a la **Etiquetas** campo .

1. Seleccione una o varias etiquetas que desee aplicar en el tema seleccionado.

1. Confirme la selección.

1. Haga clic en **Aplicar etiquetas**.

   Las etiquetas seleccionadas se aplican al tema y se muestran en el campo Etiquetas .

1. Haga clic en **Guardar y cerrar**.


## Eliminación de etiquetas

Según sus necesidades comerciales, puede cambiar la información de etiquetado de cualquier tema de DITA. Puede eliminar fácilmente todas las etiquetas a la vez o solo aquellas que no sean válidas en el tema.

Siga estos pasos para eliminar todas las etiquetas de uno o varios temas:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación DITA y haga clic en él.

   Aparece la consola de asignación DITA que muestra la lista de ajustes preestablecidos de salida disponibles para generar resultados.

1. Haga clic en **Temas**.

   Se muestra una lista de temas disponibles en el mapa DITA.

1. Seleccione los temas de los que desea quitar etiquetas.

1. Haga clic en **Eliminar etiquetas**.

   >[!NOTE]
   >
   > Si el icono Eliminar etiquetas no está visible, asegúrese de que no ha habilitado la función Ocultar etiquetas .

1. En el cuadro de diálogo Confirmar eliminación, haga clic en **OK** para quitar etiquetas de los temas seleccionados.


## Mostrar u ocultar etiquetas

Si tiene una larga lista de etiquetas aplicadas a sus temas, es posible que le resulte un poco complicado navegar. Puede ocultar fácilmente las etiquetas en desde la vista de la consola de asignación DITA haciendo clic en el icono Ocultar etiquetas . Del mismo modo, cuando las etiquetas no están visibles, al hacer clic en Mostrar etiquetas se muestran todas las etiquetas.

**Tema principal:**[ Administrar metadatos](manage-metadata.md)
