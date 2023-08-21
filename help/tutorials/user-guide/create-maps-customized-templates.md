---
title: Creación de mapas basados en plantillas personalizadas
description: Aprenda a crear mapas basados en plantillas personalizadas
exl-id: 02513148-3876-4549-962a-9984f619030f
source-git-commit: be1a61d9475185da594b382c1daf361d3fe60b08
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Creación de mapas basados en plantillas personalizadas {#id225VF0808MP}

Se pueden crear plantillas de mapa personalizadas y utilizarlas para crear mapas DITA junto con las plantillas de tema y las plantillas de mapa a las que se hace referencia en la plantilla de mapa

Puede hacer referencia a otras plantillas de mapas y plantillas de temas desde la plantilla de mapas personalizada. Las plantillas de mapas a las que se hace referencia pueden hacer referencia a varias plantillas de mapas, plantillas de temas, temas, mapas, imágenes, vídeos y otros recursos. La plantilla de mapa personalizada puede ayudarle a replicar muy fácilmente las plantillas de mapa y toda la estructura de carpetas de referencia. Estas plantillas personalizadas son especialmente útiles para crear y recrear varios mapas con estructuras y referencias recursivas.

>[!NOTE]
>
> Las plantillas de temas no se crean de forma recursiva. Solo se generan las plantillas de tema que están directamente dentro de la plantilla de mapa y cualquier plantilla de tema dentro de una plantilla de tema simplemente se hace referencia en el elemento principal directamente.

## Creación de plantillas personalizadas

AEM Guías de le permite crear mapas y temas personalizados a partir de la carpeta dita-templates. Puede utilizar estas plantillas personalizadas para crear el mapa y el tema. También puede compartir estas plantillas con los autores para que puedan utilizarlas en la creación de sus archivos. Con estas plantillas, puede permitir a los autores mantener copias independientes de ciertos recursos que están dentro de la carpeta de plantillas.

>[!NOTE]
>
> Todos los recursos a los que solo se haga referencia y que se mantengan deben mantenerse fuera de la carpeta de plantillas.

**Plantilla de tema**

Siga estos pasos para crear una plantilla de tema:

1. En el **IU de Assets**, vaya a la carpeta dita-templates.

   ![](images/dita-templates.png){width="800" align="left"}

1. Clic **temas** carpeta para abrirla.Haga clic en **Crear \> plantilla DITA**.
1. En la página Modelo, seleccione **Tema** y luego haga clic en **Siguiente.**
1. En la página Propiedades, especifique la plantilla de tema **Título**.
1. Especifique el archivo **Nombre**

   >[!NOTE]
   >
   > El nombre del archivo debe tener la extensión .dita.

1. \(Opcional\) Agregue una descripción.
1. Haga clic en **Crear**. Aparecerá el mensaje de plantilla de tema creada. A continuación, puede abrir la plantilla de tema y editarla.

**Plantilla de mapa**

Realice los siguientes pasos para crear una plantilla de asignación:

1. En el **IU de Assets**, vaya a la carpeta dita-templates.
1. Clic **mapas** para abrirla.
1. Clic **Crear** > **Plantilla DITA.**

   ![](images/create-dita-template.png){width="300" align="left"}

1. En la página Modelo, seleccione **Mapa** y haga clic en **Siguiente**.
1. En la página Propiedades, especifique la plantilla de asignación **Título**.
1. Especifique el archivo **Nombre**.

   >[!NOTE]
   >
   > El nombre del archivo debe tener la extensión .ditamap.

1. (Opcional\) Agregue una descripción.Haga clic en **Crear**. Aparecerá el mensaje creado para la plantilla de mapa. A continuación, puede abrir la plantilla de asignación y editarla. Puede agregar las referencias para las plantillas de tema, las plantillas de mapa y también otros recursos en la plantilla de mapa.

## Pasar el título definido en las plantillas

Si desea pasar el título del tema o el mapa utilizado dentro de la plantilla a los mapas DITA creados con esa plantilla, utilice llaves alrededor del título.

Ejemplos

```XML
<pubtitle>
   <mainpubtitle outputclass="booktitle">
   {title}
   </mainpubtitle>
   <subtitle>Subtitle</subtitle>
</pubtitle>

The resultant DITA map with title "Rootmap1" will look like as follows:
<pubtitle>
   <mainpubtitle outputclass="booktitle">Rootmap1
   </mainpubtitle>
   <subtitle>Subtitle</subtitle>
</pubtitle>
```

>[!NOTE]
> Solo la primera aparición de llaves se sustituirá por el título.

Si no utiliza llaves alrededor del título, el mapa DITA resultante solo seleccionará el primer elemento y el anidamiento del título no se seleccionará de la plantilla y tendrá el siguiente aspecto:

```XML
<pubtitle> Rootmap1 </pubtitle>
```

>[!NOTE]
> También se pueden utilizar llaves alrededor del texto para pasar su estructura anidada desde las plantillas personalizadas a los mapas DITA.

Ejemplos

```XML
<title>    
    <sub>        
        <b>{title}</b>    
    </sub>
</title>
```

## Utilice la plantilla de asignación para crear nuevas asignaciones

>[!NOTE]
>
> El administrador debe configurar y poner a disposición de la creación la plantilla de mapa. Para obtener más información, consulte *Configuración de plantillas de creación* de la sección Instalar y configurar las guías de Adobe Experience Manager as a Cloud Service.

Realice los siguientes pasos para crear un mapa con la plantilla de mapa personalizada:

1. En el **IU de Assets,** vaya a la carpeta en la que desea crear el mapa.
1. Clic **Crear \> mapa DITA**.
1. En la página Modelo, seleccione la plantilla de mapa que desee utilizar y haga clic en **Siguiente**. Por ejemplo, si ha creado una plantilla de mapa &quot;plantilla de prueba&quot;, selecciónela.
1. En la página Propiedades, especifique el mapa **Título**.
1. Especifique el archivo **Nombre**.

   >[!NOTE]
   >
   > El nombre del archivo debe tener la extensión .ditamap.

1. Haga clic en **Crear**. Aparecerá el mensaje de asignación creada.


El mapa genera todos los recursos a los que se hace referencia dentro de la carpeta de plantillas. Algunos tipos de recursos a los que se hace referencia en un mapa pueden ser los siguientes:

- Si el mapa contiene la referencia a una plantilla de tema, se crea una copia de ella dentro de la carpeta, en la misma jerarquía que en la carpeta de temas de `dita-templates` carpeta.
- Si el mapa contiene la referencia a una plantilla de mapa, se crea una copia de ella dentro de la carpeta, en la misma jerarquía que en la carpeta de mapas de `dita-templates` carpeta.
- Si el mapa contiene la referencia genérica a un tema o mapa fuera de `dita-templates/topics` o `dita-templates/maps` carpeta, solo se hace referencia a la misma y no se crea ninguna copia.

  >[!NOTE]
  >
  > `dita-templates/topics` y `dita-templates/maps` son las rutas predeterminadas en las guías y se pueden configurar.


  Si hay una definición de clave de plantilla de tema dentro de la plantilla de asignación, se crea una nueva clave \(por lo tanto, nuevo tema\) y se hace referencia a ella en el mapa.

- Si se crea otro mapa o tema en el mismo nivel de la carpeta, los nombres de los recursos recién creados se anexan con 0,1,2, etc. Puede elegir abrir la asignación para editarla o guardar el archivo de asignación en el repositorio.

**Tema principal:**[ Trabajo con el editor de mapas](map-editor.md)
