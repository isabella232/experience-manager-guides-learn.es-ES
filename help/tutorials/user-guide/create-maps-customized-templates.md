---
title: Crear mapas basados en plantillas personalizadas
description: Obtenga información sobre cómo crear mapas basados en plantillas personalizadas
exl-id: 02513148-3876-4549-962a-9984f619030f
source-git-commit: 3bca42f0954afc2362ab24f369e698113324dbc3
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Crear mapas basados en plantillas personalizadas {#id225VF0808MP}

Puede crear plantillas de asignación personalizadas y utilizarlas para crear mapas DITA junto con las plantillas de tema y las plantillas de asignación a las que se hace referencia en la plantilla de asignación

Puede consultar otras plantillas de asignación y plantillas de tema desde la plantilla de asignación personalizada. Las plantillas de mapa a las que se hace referencia pueden hacer referencia a varias plantillas de mapa, plantillas de temas, temas, mapas, imágenes, vídeos y otros recursos. La plantilla de mapa personalizada puede ayudarle a replicar fácilmente las plantillas de mapa y toda la estructura de carpetas referida. Estas plantillas personalizadas son especialmente útiles para crear y recrear múltiples mapas que tienen estructuras y referencias recursivas.

>[!NOTE]
>
> Las plantillas de temas no se crean de forma recursiva. Solo se generan las plantillas de tema que están directamente dentro de la plantilla de asignación y cualquier plantilla de tema dentro de una plantilla de tema simplemente se hace referencia en el tema principal directamente.

## Crear plantillas personalizadas

AEM guías le permite crear mapas y temas personalizados a partir de la carpeta dita-templates . Puede utilizar estas plantillas personalizadas para crear su mapa y tema. También puede compartir estas plantillas con los autores, que pueden utilizar para crear sus archivos. Con estas plantillas, puede permitir a los autores mantener copias independientes de ciertos recursos que se encuentran dentro de la carpeta de plantillas.

>[!NOTE]
>
> Todos los recursos a los que solo se hace referencia y se mantienen en la carpeta deben mantenerse fuera de la carpeta de plantillas.

**Plantilla de tema**

Siga estos pasos para crear una plantilla de tema:

1. En el **IU de recursos**, vaya a la carpeta dita-templates .

   ![](images/dita-templates.png){width="800" align="left"}

1. Haga clic en **temas** carpeta para abrirla. Haga clic en **Crear \> Plantilla DITA**.
1. En la página Modelo, seleccione **Tema** y haga clic en **Siguiente.**
1. En la página Propiedades, especifique la plantilla de tema **Título**.
1. Especifique el archivo **Nombre**

   >[!NOTE]
   >
   > El nombre del archivo debe tener la extensión .dita.

1. \(Opcional\) Añada una descripción.
1. Haga clic en **Crear**. Aparece el mensaje de plantilla de tema creada. A continuación, puede abrir la plantilla del tema y editarla.

**Plantilla de mapa**

Siga estos pasos para crear una plantilla de asignación:

1. En el **IU de recursos**, vaya a la carpeta dita-templates .
1. Haga clic en **mapas** para abrirla.
1. Haga clic en **Crear \> Plantilla DITA.**

   ![](images/create-dita-template.png){width="300" align="left"}

1. En la página Modelo, seleccione **Mapa** y haga clic en **Siguiente**.
1. En la página Propiedades, especifique la plantilla de asignación **Título**.
1. Especifique el archivo **Nombre**.

   >[!NOTE]
   >
   > El nombre del archivo debe tener la extensión .ditamap.

1. (Opcional\) Añada una descripción. Haga clic en **Crear**. Aparece el mensaje de plantilla de asignación creada. A continuación, puede abrir la plantilla de asignación y editarla. Puede agregar las referencias para las plantillas de tema, las plantillas de asignación y también otros recursos en la plantilla de asignación.

## Pasa el título definido en las plantillas

Si desea pasar el título del tema o el mapa utilizado dentro de la plantilla a los mapas DITA creados con esa plantilla, utilice llaves alrededor del título.

Ejemplo

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
> Solo la primera aparición de corchetes se reemplazará por title.

Si no utiliza llaves alrededor del título, el mapa DITA resultante solo seleccionará el primer elemento y el anidado del título no se seleccionará de la plantilla y tendrá el siguiente aspecto:

```XML
<pubtitle> Rootmap1 </pubtitle>
```

>[!NOTE]
> También puede utilizar las llaves alrededor del texto para pasar su estructura anidada desde las plantillas personalizadas a los mapas DITA.

Ejemplo

```XML
<title>    
    <sub>        
        <b>{title}</b>    
    </sub>
</title>
```

## Utilice la plantilla de asignación para crear nuevos mapas

>[!NOTE]
>
> El administrador debe configurar la plantilla de asignación y facilitar su creación. Para obtener más información, consulte *Configuración de plantillas de creación* en la sección Instalar y configurar guías de Adobe Experience Manager as a Cloud Service.

Siga estos pasos para crear un mapa con la plantilla de asignación personalizada:

1. En el **IU de recursos,** vaya a la carpeta en la que desea crear el mapa.
1. Haga clic en **Crear \> Mapa DITA**.
1. En la página Modelo, seleccione la plantilla de asignación que desee utilizar y haga clic en **Siguiente**. Por ejemplo, si ha creado una plantilla de asignación &#39;test-template&#39;, selecciónela.
1. En la página Propiedades, especifique el mapa **Título**.
1. Especifique el archivo **Nombre**.

   >[!NOTE]
   >
   > El nombre del archivo debe tener la extensión .ditamap.

1. Haga clic en **Crear**. Aparecerá el mensaje creado por el mapa.


El mapa genera todos los recursos a los que se hace referencia dentro de la carpeta de plantillas. Algunos tipos de recursos a los que se hace referencia en un mapa pueden ser los siguientes:

- Si el mapa contiene la referencia a una plantilla de tema, se crea una copia dentro de la carpeta, en la misma jerarquía que en la carpeta de temas de la `dita-templates` carpeta.
- Si el mapa contiene la referencia a una plantilla de asignación, se crea una copia de ella dentro de la carpeta, en la misma jerarquía que en la carpeta de mapas de la `dita-templates` carpeta.
- Si el mapa contiene la referencia genérica a un tema o mapa fuera del `dita-templates/topics` o `dita-templates/maps` carpeta, solo se hace referencia a la misma y no se crea ninguna copia.

   >[!NOTE]
   >
   > `dita-templates/topics` y `dita-templates/maps` son las rutas predeterminadas de las guías y se pueden configurar.


   Si hay una definición de clave de plantilla de tema dentro de la plantilla de asignación, se crea una nueva clave \(por lo tanto, se hace referencia a un nuevo tema\) en el mapa.

- Si se crea otro mapa o tema en el mismo nivel de la carpeta, los nombres de los recursos recién creados se añaden a 0, 1, 2, etc. Puede elegir abrir el mapa para editarlo o guardar el archivo de mapa en el repositorio.

**Tema principal:**[ Trabajar con el Editor de mapas](map-editor.md)
